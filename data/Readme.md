# Data sheet
In this doc, we cover the basics of what the data columns stands for.

## Nasa-tlx
This data contains the nasa-tlx participants self-reported.

SID,Ver,Ratings,Mental,Physical,Temporal,Performance,Effort,Frustration,Ranking,Mental,Physical,Temporal,Performance,Effort,Fustration,Total Count,Adjusted Rating,Mental,Physical,Temporal,Performance,Effort,Fustration,Sum,Weighted Rate

- SID: Subject ID
- Ver: Version
- Weighted Rate: The final score of the NASA-TLX

The first set of Mental, Physical, Temporal, Performance, Effort, Frustration are the raw scores, the second set are the sets, the third set are the weighted subscale scores

## vx_cleaned_public
These files are extracted user behavior data with the specific options masked.

- type: The type of the event recorded by the system
    - initializing system: The user began the study
    - options/updateOptionVotes: The user voted on an option
    - options/updateOptionGroup: The user assigned an option to a group
    - options/updateOptionPosition: The user moved an option (drag-and-drop)
    - begin voting: The user began voting (in the two-phase interface)
- timestamp: The time the event was recorded
- time_diff: The time difference between the current event and the previous event
- totalCursorDistance: The total distance the cursor moved during the event
- totalMouseClicks: The total number of mouse clicks during the event
- user_id: Subject ID
- version_id: Version
    - v1: short-text
    - v2: short-two-phase
    - v3: long-text
    - v4: long-two-phase
- option_id: The option ID
- old_vote: The previous vote of the option
- new_vote: The new vote of the option
- vote_diff: The difference between the new and old vote
- option_position: The position of the option (counted fromthe top)
- option_position_view: The position of the option (counted from the bottom)
- old_group: The previous group of the option
- new_group: The new group of the option
- card_order: The nth card that appeared during the organization phase
- filled_page_action: The page that the user is at
    - grouping: The user is on the organization page
    - voting: The user is on the voting page
- new_position: The new position of the option (counted from the top)
- old_position: The old position of the option (counted from the top)

## voting combined data
This data contains filtered data from the four cleaned data files. This data is mainly used for distance analysis. We explain additional columns

- diff_square: The difference in credit spent
- distance_diff: The difference between the current and previous distance
- abs_distance: The absolute distance
- cumulative_distance: The cumulative distance
- cumulative_voting_time: The cumulative voting time
- cumulative_cursor_distance: The cumulative cursor distance
- cumsum_diff_square: The cumulative sum of the square of the difference, which corresponds to the total credit spent
- step: The nth step the user took