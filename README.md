Product Engineering Review – Campus Stores

1. What works well

The inventory and loan register work well together. Each physical unit has its own asset ID, and the system distinguishes between equipment on the shelf, on loan, and in repair.

During the Film Society pickup, this helps the desk staff issue only approved and available equipment. It also prevents issuing the same equipment type twice for the same request.

2. What I would change

I would improve the partial-return and shift-handover experience.

In the current workflow, Kabir returns the projector and speaker on Friday evening, while Leela promises to return the adapter on Saturday morning. The next shift must read the desk book, identify the outstanding equipment, and manually work out which record needs to be closed.

This creates unnecessary mental effort and leaves room for mistakes.

3. Proposed improvement: Smart Handover Checklist

I propose adding an automatic handover checklist linked to the original request and loan records.

The checklist would show:

- Request ID and club name.
- Equipment originally issued.
- Equipment already returned.
- Equipment still outstanding.
- Expected return time.
- Person expected to return it.

Prototype – Smart Handover Screen

┌──────────────────────────────────────────────┐
│           CAMPUS STORES                      │
│           SHIFT HANDOVER                     │
├──────────────────────────────────────────────┤
│ Club: Film Society                           │
│ Request: Film Screening                      │
│ Issued to: Kabir                              │
│ Handover to: Leela                            │
│                                              │
│ EQUIPMENT STATUS                             │
│                                              │
│ 1. HDMI Projector                             │
│    Status: RETURNED                           │
│    Action: Closed                             │
│                                              │
│ 2. Portable Speaker                           │
│    Status: RETURNED                           │
│    Action: Closed                             │
│                                              │
│ 3. USB-C to HDMI Adapter                      │
│    Status: OUTSTANDING                        │
│    Expected: Saturday, 9:00 AM                │
│    Action: Awaiting return                    │
│                                              │
├──────────────────────────────────────────────┤
│ NEXT SHIFT ACTION                             │
│                                              │
│ [ ] Verify adapter asset ID                   │
│ [ ] Confirm physical return                   │
│ [ ] Update inventory status                   │
│ [ ] Close outstanding loan                    │
└──────────────────────────────────────────────┘

Design principle: The next shift should immediately identify what has been returned, what is pending, and what action is required without searching through handwritten notes.

Next shift action: Confirm the adapter's asset ID, record its return, and close the correct outstanding record.

4. Walkthrough using the improved design

Friday – 3:45 PM: Kabir collects the Film Society equipment. The system checks the approved request and available physical units.

Friday – 7:30 PM: Kabir returns the projector and speaker. The system updates their status and automatically keeps the adapter outstanding.

Saturday – 9:00 AM: Leela brings the adapter. The morning staff can see the pending return immediately, verify its asset ID, and close the correct record.

5. What I would keep

I would retain the existing individual asset IDs, inventory status tracking, approved-request validation, and simple loan register. These provide a good foundation for reliable equipment tracking.

6. How I would measure success

At a real equipment counter, I would observe the time taken by the next shift to identify and complete pending returns.

I would compare the average handover completion time and the number of missed or incorrectly closed returns before and after introducing the checklist.

The goal is to reduce manual searching, improve accountability, and make shift changes easier.# Campus Stores

Campus Stores is a Product Engineer work sample set at a fictional campus media equipment desk. Work through a club’s screening, from equipment pickup to a partial return and the next morning’s handover. Open **Candidate brief** in the app for the assignment.

## Run the app

Open `index.html` in a modern browser. The app includes its scripts, styles, and icons and can run offline.

To serve it over local HTTP, run this from the repository folder and visit `http://localhost:8000`.

```sh
python3 -m http.server 8000 --bind 127.0.0.1
```

Each browser stores its own sample shift locally when browser storage is available. **Restart sample shift** restores the fictional starting records.

## Source

- `index.html` contains the desk layout, candidate brief, and bundled icons.
- `app.js` contains the sample records and interactions.
- `styles.css` defines the desktop and mobile layouts.

Icon license notices are in [third-party/lucide-LICENSE.txt](third-party/lucide-LICENSE.txt).


## Submit your work

1. [Fork Campus Stores](https://github.com/virinchi-healthcare/campus-stores/fork) into your GitHub account. Complete the candidate brief and push your changes to your public fork. In your README, point reviewers to your work and explain the decision you made.
2. In your fork, open **Commits**, select the final commit you want reviewed, and copy the page URL. It should look like `https://github.com/YOUR-USERNAME/campus-stores/commit/COMMIT-SHA`.
3. [Submit your work through the Google Form](https://docs.google.com/forms/d/e/1FAIpQLScvzoh1R4WS-SkiwAVBQbMvniieJYSoOEfLMyVo5CyjOvYUgQ/viewform). Your **roll number**, **email ID**, and **final commit link from your public fork** are required. Enter your roll number and email ID in the form only.
