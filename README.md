## Product Engineering Practical — My Changes

### What works well
The loan register provides a simple way to record equipment returns. When a return is recorded, the item is marked as returned to stock and the loan slip is closed, reducing manual tracking.

### Problem identified
The shift handover information is spread across messages. Staff taking over a shift need to read multiple notes to understand which equipment has been returned, what is outstanding, and whether the correct loan record is being updated.

### My solution
I added a **Shift Handover Summary** to the Desk Book for the Film Society screening (RQ-214).

The summary highlights:
- Projector — returned
- Speaker — returned
- Adapter — received from Leela
- A warning to verify the loan record
- A clear next action before closing a return

### Why I made this change
I wanted to reduce the mental effort required during shift handovers and make important information visible at a glance. The summary also helps staff notice a possible mismatch between the screening's equipment and the outstanding loan record before taking action.

### How I would measure success
My primary metric would be **incorrect loan closures**. I would also track handover completion time and missed-item incidents to understand whether the summary improves accuracy and efficiency.

### Prototype
The prototype is implemented in `app.js`. Open the deployed Campus Stores application, advance to the morning shift, and select **Desk book** to view the Shift Handover Summary.
