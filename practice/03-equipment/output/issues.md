# Equipment data cleaning issues

## Row counts

- Input records: 10
- Valid records retained: 9
- Removed: 1 (source row 6 was an empty object: all fields were absent/empty)

## Normalization applied

- Trimmed surrounding whitespace in `item_id`, `name`, and `status`; `qty` values were preserved as supplied.
- Mapped `available`, `可借`, and `可出借` to `available`.
- Mapped `borrowed` and `借出` to `borrowed`.
- Mapped `待盤點` and other unrecognized statuses to `unknown`.
- Kept every valid row with its `source_row`; rows sharing an ID were not merged or removed.

## Quantity issues

- Source row 7 (`EQ04`): quantity is an empty string and is uncertain. It remains `""`; no value was inferred.
- Source row 8 (`EQ05`): quantity is `-1`, which is outside the accepted nonnegative integer range. It remains `-1` and is flagged; it was not changed to a positive value or zero.
- Source row 10 (`EQ07`): quantity `0` is valid and was preserved.

## Repeated IDs

- `EQ01`, source rows 1 and 4: after trimming and status normalization, `name`, `qty`, and `status` match. Both records remain.
- `EQ02`, source rows 2 and 5: `name` and normalized `status` match, but `qty` conflicts (2 versus 3). Both records remain; a person must resolve the discrepancy.

Identical names do not establish that records refer to the same physical item. No item records were merged or deleted on that basis.
