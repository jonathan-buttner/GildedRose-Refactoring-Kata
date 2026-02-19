# Requirements Specification

We have a system in place that updates our inventory for us. Your task is to add the new feature to our system so that
we can begin selling a new category of items.

## Intro

- All `items` have a `SellIn` value which denotes the number of days we have to sell the `items`
- All `items` have a `Quality` value which denotes how valuable the item is
- At the end of each day our system lowers both values for every item

## Requirements

- Once the sell by date has passed, `Quality` degrades twice as fast
- The `Quality` of an item is never negative
- __"Aged Brie"__ actually increases in `Quality` the older it gets
- The `Quality` of an item is never more than `50`
  - **Exception:** __"Sulfuras"__ is a legendary item and as such its `Quality` is `80` and it never changes
- __"Sulfuras"__, being a legendary item, never has to be sold and never decreases in `Quality`
- __"Backstage passes"__, like aged brie, increases in `Quality` as its `SellIn` value approaches;
  - `Quality` increases by `2` when there are `10` days or less and by `3` when there are `5` days or less
  - `Quality` drops to `0` after the concert

## New feature

- __"Conjured Mana Cake"__ items degrade in `Quality` twice as fast as normal items

## Instructions

Make any changes and add any new code as long as everything still works correctly. There should be no changes to the
[TexttestFixture](Java/src/test/java/com/gildedrose/TexttestFixture.java) file.

The text [stdout.gr](texttests/ThirtyDays/stdout.gr) contains most of expected output. This file should only
change when the `Conjured Mana Cake` item is implemented and the text related to the other items should not change.
