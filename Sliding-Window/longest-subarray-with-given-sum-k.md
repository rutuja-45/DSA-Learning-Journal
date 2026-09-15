# Longest Subarray with Given Sum K — Positives

## 1. Core Pattern

Sliding Window / Two Pointers

## 2. Missing Trick

When removing an element from the left of the window, I forgot to subtract that element from `sum`.

```java
sum -= arr[left];
left++;
```

## 3. Flawed Approach

My original approach was correct, but while shrinking the window, I only moved `left` without updating `sum`.

This caused the window sum to become incorrect.
