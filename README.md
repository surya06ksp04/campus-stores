Campus Stores – Product Engineering Review

Product: Campus Stores – Media Equipment Desk
Role: Product Engineer
Focus: Equipment pickup, partial returns and shift handover

---

1. Understanding the Product

Campus Stores is an equipment management application for a fictional campus media equipment desk.

The application allows staff to manage equipment requests, check inventory, record equipment loans and maintain handover information between shifts.

My focus was to understand the complete Film Society screening workflow, from equipment pickup on Friday afternoon to the partial return on Friday evening and the next morning's handover.

2. What Works Well

Individual Equipment Identification

One thing I liked about the product is that each physical equipment unit has its own asset ID.

For example, the inventory contains two USB-C to HDMI adapters:

- AD-12 – Belkin AVC002
- AD-15 – Anker A8312

This is useful because staff need to identify the exact physical item rather than simply knowing the equipment type.

During the Film Society pickup, this level of identification helps the staff select and track the correct equipment.

Why I would keep it: Individual asset identification makes inventory tracking more reliable and helps avoid confusion when multiple units belong to the same equipment category.

3. What I Would Change

Improving Partial Returns and Shift Handover

I would improve the way the application communicates outstanding equipment during a shift change.

Consider the Film Society scenario:

- Friday, 3:45 PM: Kabir collects equipment for the screening.
- Friday, 7:30 PM: Kabir returns the projector and speaker.
- The adapter is still with Leela, who promises to return it on Saturday at 9:00 AM.
- Saturday, 9:00 AM: The morning staff must identify the outstanding equipment and close the correct loan.

The challenge is that the next shift needs to understand the previous shift's activity before taking action.

I would make this information more visible and actionable instead of depending on staff to manually interpret handover notes.

4. Proposed Improvement – Smart Handover Checklist

My proposed improvement is a dedicated handover summary linked to the original request and individual asset records.

It should clearly communicate:

- Original request and club name.
- Equipment issued.
- Equipment already returned.
- Equipment still outstanding.
- Expected return time.
- Person responsible for the pending return.
- Next action required by the staff.

Prototype – Smart Handover Screen

CAMPUS STORES | SHIFT HANDOVER

Club: Film Society
Request: RQ-214 – Courtyard Screening
Issued to: Kabir Sen
Pending return contact: Leela Das

Equipment Status

Equipment| Asset ID| Status| Action
HDMI Projector| PR-04| Returned| Closed
Portable Speaker| SP-02| Returned| Closed
USB-C Adapter| AD-12| Outstanding| Awaiting return

Expected return: Saturday, 9:00 AM

Next Shift Action

- [ ] Verify the adapter's physical asset ID.
- [ ] Match it with the outstanding loan.
- [ ] Confirm the physical return.
- [ ] Update inventory status.
- [ ] Close the outstanding loan.

Important: The asset ID must be verified before closing the loan because the inventory contains multiple adapters.

Design Principle

The next shift should immediately understand what has been returned, what is pending and what action needs to be taken without searching through previous records.

5. Walkthrough Using the Proposed Improvement

Friday – 3:45 PM | Equipment Pickup

Kabir arrives to collect the Film Society equipment.

The staff checks the request, verifies available equipment and records the physical asset IDs issued.

Friday – 7:30 PM | Partial Return

Kabir returns the projector and speaker.

The staff records these returns individually. The adapter remains outstanding.

The handover summary automatically displays the pending adapter and its expected return time.

Saturday – 9:00 AM | Morning Shift

The morning staff opens the handover summary.

Leela arrives with an adapter. The staff verifies its asset ID against the outstanding loan, confirms the physical return and closes the correct record.

This reduces the need to reconstruct the previous evening's events manually.

6. What I Would Keep

I would retain the following existing features:

- Individual asset identification.
- Inventory management.
- Equipment request records.
- Loan register.
- Desk book and handover information.
- Simple navigation between different records.

These features already provide a useful foundation for managing equipment at a campus desk.

My improvement focuses on connecting the existing information more clearly rather than making the application unnecessarily complicated.

7. How I Would Measure Success

I would evaluate the improvement through observation at a real equipment counter.

The main observation would be:

How long does the next shift take to identify and correctly close an outstanding equipment return?

I would compare the average handover completion time before and after introducing the checklist.

I would also observe whether staff make fewer mistakes while identifying equipment and closing outstanding loans.

The expected outcome is faster handovers, fewer missed returns and better accountability between shifts.

8. Final Thoughts

I would keep the existing simplicity of Campus Stores while improving the visibility of information during shift changes.

A good product should not only help staff complete individual tasks but also make it easier for the next person to continue the work without confusion.

My proposed Smart Handover Checklist focuses on making that transition clearer, faster and more reliable.

---

Project Information

Campus Stores is a standalone application containing its own scripts, styles and icons.

Source Files

- "index.html" – Application layout, candidate brief and bundled icons.
- "app.js" – Sample records and application interactions.
- "styles.css" – Desktop and mobile layouts.

Running the Application

Open "index.html" in a modern browser.

Alternatively, run the following command from the repository folder:

python3 -m http.server 8000 --bind 127.0.0.1

Then visit "http://localhost:8000".

The application stores sample shift data locally in the browser when browser storage is available.

Original Repository

https://github.com/virinchi-healthcare/campus-stores