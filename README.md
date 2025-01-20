# Unexpected Behavior in Async/Await Tasks without Priority Specification
This repository demonstrates a subtle issue in Swift's async/await functionality. When creating a Task without explicitly setting its priority, the behavior might become unpredictable, particularly in scenarios involving long-running operations or UI updates.  The provided example showcases the problem and its solution.

## Problem
The `fetchData()` function performs a network request.  If this task is created without priority specification it could lead to unexpected delays in the UI or interference with other tasks.

## Solution
Setting the priority of the Task ensures that it is handled appropriately by the system.  Using `.userInitiated` priority is generally appropriate for user-triggered actions.  The corrected code explicitly sets the priority, making the task's execution more predictable and manageable.