# React Native FlatList Performance Bug

This repository demonstrates a common performance issue in React Native's `FlatList` component when dealing with large datasets.  The bug arises from an improper or missing `keyExtractor` prop, leading to slow rendering, performance bottlenecks, and potential crashes.  The solution involves correctly implementing the `keyExtractor` prop to provide unique keys for each item in the dataset.

## Bug Description

When rendering a `FlatList` with a large number of items and without a properly functioning `keyExtractor`, React Native struggles to efficiently update the list. This results in slow scrolling, lag, and potentially application crashes. The root cause is React Native's reliance on unique keys to identify and recycle list items.

## Solution

The solution is straightforward: implement the `keyExtractor` prop and ensure each item in your dataset has a unique identifier. The `keyExtractor` should return a unique string for each item. This allows React Native to efficiently track and update the list items, dramatically improving performance.

## How to reproduce

1. Clone the repository.
2. Run `npm install` or `yarn install`.
3. Run the app on an emulator or device using `react-native run-android` or `react-native run-ios`.
4. Observe the slow rendering and performance issues.