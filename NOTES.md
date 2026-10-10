# Notes

## Bugs I Fixed

1. Search filter issue

In `TaskRepository.java`, I found that the search conditions were not grouped properly. Because of this, the status filter and archived task condition might not work correctly for all search results. I added brackets around the title and description search conditions to fix this.

2. Loading and error handling

In `useTasks.js`, loading was set to false only when the API request was successful. If the request failed, the loading state could remain active. I added a `finally` block so loading stops in both cases. I also cleared the previous error before making a new request.

## What I Did Not Change

I did not change the database structure or API response format. I wanted to keep the changes small and avoid affecting other parts of the application.

## Biggest Remaining Risk

Page number and page size validation still need improvement. Invalid values could cause problems with pagination.

## Tools Used

I used VS Code to make the changes and tested the application locally. I also used AI assistance to understand the code and help with debugging.