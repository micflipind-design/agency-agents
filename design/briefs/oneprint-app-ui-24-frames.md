# OnePrint App UI Design Brief — 24 Mobile Frames

## Project Goal
Create a clean, easy-to-understand, premium mobile UI system for the **OnePrint** app. The app helps users connect thermal/label printers, import files, select templates, configure print jobs, and print PDFs, images, Excel/CSV files, receipts, KOTs, and external print jobs.

The design must feel modern, trustworthy, and operationally clear for small businesses, ecommerce sellers, restaurants, warehouses, and office users.

## Required Output
Design **24 total mobile app frames**:

- **18 core screens**
- **6 supporting states/modals**

Design one frame at a time, but keep every frame visually consistent with the same design system.

Recommended canvas: **390 × 844 px** or **393 × 852 px** mobile frame.

## Brand Direction

### Brand Personality
- Premium but friendly
- Fast, practical, and business-ready
- Clean interface with strong clarity
- Rounded, chunky, confident visual style
- Avoid clutter, cheap gradients, excessive shadows, or random icons

### Logo Direction
Create/use a **OnePrint** wordmark style:
- Typography: bold rounded chunky style, close to **Montserrat Bold / Montserrat ExtraBold**
- Wordmark: `OnePrint` or `oneprint`
- Embed a small printer icon inside the **“i”** of **print** where possible
- Use a thick black drop shadow/extrude style only on brand/hero moments, not everywhere
- Keep app UI itself cleaner and more premium than the logo style

## Color System

### Primary Palette
```css
--oneprint-orange-deep: #F5421E;
--oneprint-orange-bright: #F5A623;
--oneprint-orange-gradient: linear-gradient(135deg, #F5421E 0%, #F5A623 100%);
--oneprint-coral: #EE8A60;
--oneprint-charcoal: #282828;
--oneprint-cream: #F5F3ED;
```

### Recommended Supporting Colors
Use these if needed for clarity and premium finish:
```css
--oneprint-white: #FFFFFF;
--oneprint-black: #111111;
--oneprint-ink: #1E1E1E;
--oneprint-muted: #77736B;
--oneprint-border: #E7E1D8;
--oneprint-card: #FFFDF8;
--oneprint-success: #22A06B;
--oneprint-warning: #F59E0B;
--oneprint-error: #E5484D;
--oneprint-info: #3B82F6;
```

### Usage Rules
- Use **Pale Cream** as the main background for warmth.
- Use **Charcoal** for text and structural UI.
- Use the orange gradient for primary CTAs, active states, progress elements, and important highlights.
- Use **Warm Coral** as a softer secondary accent.
- Use black extrude/shadow only for logo, splash, selected hero cards, or playful printer illustrations.
- Maintain WCAG AA contrast for all readable text.

## Typography

### Primary Font
- **Montserrat Bold / ExtraBold** for headings, key numbers, logo, primary buttons.
- Use Montserrat SemiBold for section headers.
- Use Montserrat Medium/Regular for body text if available.

### Suggested Type Scale
- Display: 36–42 px / ExtraBold
- H1: 28–32 px / ExtraBold
- H2: 22–24 px / Bold
- Section title: 17–18 px / Bold
- Body: 14–16 px / Medium
- Caption: 12–13 px / Medium
- Button: 15–16 px / Bold

### Style Rules
- Rounded, confident, chunky headings.
- Body copy must remain highly readable.
- Avoid overly thin type.
- Use concise labels and direct action verbs.

## Visual Style

### Shape Language
- Cards: 20–28 px radius
- Buttons: 16–22 px radius
- Inputs/search bars: 16–20 px radius
- Bottom nav: pill-like, rounded top container or floating bar
- Icons: rounded stroke icons, 2–2.5 px stroke, consistent style

### Shadow / Elevation
Use soft premium shadows in the app UI:
```css
box-shadow: 0 10px 30px rgba(40, 40, 40, 0.08);
```

Use thick black extrude only for brand moments:
```css
text-shadow: 4px 5px 0 #111111;
```

### Component System
Create reusable components:
- Header with greeting/status
- Printer status pill
- Primary CTA button
- Secondary outline button
- Feature cards
- Template cards
- File cards
- Search/filter bar
- Stepper/progress indicator
- Bottom navigation
- Modal sheet
- Toast/status banners
- Empty/error/loading states

## Navigation Model
Suggested bottom nav:
1. Home
2. Templates
3. Import
4. History
5. Profile

Primary floating CTA can be **Print Now** or **Connect Printer** based on state.

---

# 18 Core Screens

## 1. Splash / Permission Onboarding
Purpose: Introduce OnePrint and request required access.

Design requirements:
- Cream or orange-gradient background.
- Large OnePrint logo with printer icon in the “i”.
- Thick black extrude effect on logo only.
- Friendly printer illustration or abstract paper roll shape.
- Permission cards for Bluetooth, Files, Photos, and Notifications.
- Primary CTA: **Get Started**
- Secondary text: **We only ask permissions needed to print.**

Premium detail:
- Add soft paper texture or subtle dots, very minimal.

## 2. Home Dashboard
Purpose: Main action hub.

Design requirements:
- Greeting: **Good morning, Arpit** or generic **Good morning**.
- Printer connection pill at top: Connected/Disconnected.
- Large primary card: **Print anything in seconds**.
- Quick actions grid:
  - PDF
  - Image
  - Excel/CSV
  - Receipt/POS
  - KOT
  - Templates
- Recent prints preview.
- Bottom navigation.

Premium detail:
- Use orange gradient for primary action card.
- Keep content highly scannable.

## 3. Printer Connection
Purpose: Detect and connect printer.

Design requirements:
- Header: **Connect printer**
- Bluetooth scanning animation/ring around printer icon.
- List of discovered printers with signal/status.
- Current printer model card.
- CTA: **Connect selected printer**
- Help link: **Can’t find your printer?**

States to show within screen:
- Searching
- Available devices
- Recently connected

## 4. Template Gallery
Purpose: Browse templates.

Design requirements:
- Search bar at top.
- Category chips:
  - Shipping Label
  - Barcode
  - Product Label
  - Address
  - Sticker
  - Receipt
- Template grid with preview thumbnails.
- Premium card shadows and rounded thumbnails.
- CTA on card: **Use template**

## 5. Template Search / Category
Purpose: Search and filter templates.

Design requirements:
- Active search field with query.
- Filter chips and sort dropdown.
- Results count.
- Category header: e.g. **Shipping Labels**
- Template list/grid with tags like 4×6, 2×1, barcode-ready.
- Empty state slot if no result.

## 6. Template Detail / Editor
Purpose: Edit template before printing.

Design requirements:
- Canvas preview with label/template.
- Bottom editing toolbar:
  - Text
  - Barcode
  - QR
  - Image
  - Align
- Field editor panel for selected object.
- CTA: **Preview print**
- Secondary: **Save template**

Premium detail:
- Use a light grid background behind the canvas.
- Use precise alignment handles.

## 7. Print Preview
Purpose: Final preview before sending print.

Design requirements:
- Large print preview card.
- Printer selection pill.
- Copies stepper.
- Paper size selector.
- Orientation toggle.
- Quality/density slider.
- CTA: **Print now**

Include small note:
- **Preview is optimized for thermal output.**

## 8. File Import Hub
Purpose: Select what to import.

Design requirements:
- Header: **Import file**
- Large import dropzone-style card.
- File type cards:
  - PDF Document
  - Image / Photo
  - Excel / CSV
  - From WhatsApp / Share Sheet
  - Cloud Drive
- Recent imported files section.

## 9. PDF Print Setup
Purpose: Configure PDF print.

Design requirements:
- PDF preview thumbnail.
- Page range selector.
- Fit to paper toggle.
- Scale slider.
- Paper width selector.
- Copies stepper.
- CTA: **Preview PDF print**

## 10. Image Print Setup
Purpose: Configure image print.

Design requirements:
- Image preview with crop handles.
- Crop mode: Fit / Fill / Custom.
- Brightness/contrast controls.
- Dither/thermal optimize toggle.
- Paper size selector.
- CTA: **Preview image print**

## 11. Excel/CSV Import Mapping
Purpose: Map spreadsheet columns to printable labels.

Design requirements:
- File name and row count card.
- Column mapping list:
  - Product Name → Text field
  - SKU → Barcode
  - Price → Text field
  - Quantity → Copies
- Preview first row.
- CTA: **Generate labels**
- Secondary: **Auto-map fields**

Premium detail:
- Make mapping easy and non-technical.

## 12. POS / Receipt Print
Purpose: Create or print receipt.

Design requirements:
- Receipt builder style.
- Store name, customer, items, tax, discount, total.
- Add item button.
- Receipt preview toggle.
- CTA: **Print receipt**

Visual style:
- Receipt preview should look like thermal paper.

## 13. KOT Print
Purpose: Kitchen order ticket print flow.

Design requirements:
- Restaurant/table/order card.
- Item list with quantity and notes.
- Priority tag: Normal / Urgent.
- Kitchen station selector.
- CTA: **Print KOT**

Premium detail:
- Use strong hierarchy for item names and quantities.

## 14. External Print Job Confirmation
Purpose: Confirm print job coming from Android/iOS share sheet or external app.

Design requirements:
- Header: **Ready to print**
- Source app chip: e.g. WhatsApp, Files, Chrome.
- File preview summary.
- Printer selected.
- Quick settings: copies, paper, density.
- CTA: **Confirm & print**
- Secondary: **Open editor**

## 15. Printer Settings
Purpose: Manage printer device.

Design requirements:
- Connected printer card with model, battery/power, Bluetooth status.
- Options list:
  - Rename printer
  - Test print
  - Default paper size
  - Print density
  - Firmware info
  - Disconnect
- CTA: **Print test page**

## 16. Paper / Settings Calibration
Purpose: Calibrate paper and print alignment.

Design requirements:
- Stepper: Paper → Alignment → Test
- Paper width selector.
- Gap/black mark detection toggle.
- Horizontal/vertical offset controls.
- Print density slider.
- CTA: **Run calibration**

Premium detail:
- Use a simple animated/illustrated paper feed preview.

## 17. Print History
Purpose: View previous print jobs.

Design requirements:
- Filters: All, Success, Failed, Templates, Files.
- History list with file/template name, printer, date, status.
- Reprint button on each item.
- Search history bar.
- Empty state for no history.

## 18. Profile / Help / Settings
Purpose: Account, help, preferences.

Design requirements:
- Profile card with name/business.
- Settings sections:
  - My printers
  - App permissions
  - Default print settings
  - Help center
  - Contact support
  - About OnePrint
- Premium icon list style.
- Footer version number.

---

# 6 Supporting States / Modals

## 19. Loading State
Use for scanning/importing/generating previews.

Design requirements:
- Centered animated printer/paper icon.
- Message: **Preparing your print…**
- Progress bar or pulsing dots.
- Cream background.

## 20. Empty State
Use for no templates, no history, no files.

Design requirements:
- Friendly rounded illustration.
- Title: **Nothing here yet**
- Body: **Start by importing a file or choosing a template.**
- CTA: **Create first print**

## 21. Error State
Use when file parsing or print job fails.

Design requirements:
- Clear error icon.
- Title: **Something went wrong**
- Body with human-readable reason.
- CTA: **Try again**
- Secondary: **Contact support**

## 22. Disconnected Printer State
Use when user tries to print without connected printer.

Design requirements:
- Bottom sheet or full screen modal.
- Printer disconnected illustration.
- Title: **Printer not connected**
- Body: **Connect your printer to continue printing.**
- CTA: **Connect printer**
- Secondary: **Print later**

## 23. Permission Needed State
Use when Bluetooth/files/photos permission is missing.

Design requirements:
- Permission-specific icon.
- Title: **Bluetooth permission needed** or relevant permission.
- Body: **OnePrint needs this permission to find and connect your printer.**
- CTA: **Open settings**
- Secondary: **Not now**

## 24. Print Success / Failure Modal
Purpose: Confirm job result.

Design requirements:
- Success version:
  - Big success check with paper confetti/detail.
  - Title: **Printed successfully**
  - Buttons: **Reprint**, **Done**
- Failure version:
  - Warning icon.
  - Title: **Print failed**
  - Possible reason and retry CTA.
  - Buttons: **Retry**, **Troubleshoot**

---

# Component Requirements

## Buttons
Primary:
- Orange gradient background
- White bold text
- 16–20 px radius
- Minimum height 52 px

Secondary:
- Cream/white background
- Charcoal text
- 1.5 px charcoal or border color

Danger:
- Error red text or background only where required

## Cards
- Cream/white card surfaces
- Rounded 22–28 px
- Soft shadow
- Clear icon/title/body/action hierarchy

## Status Pills
Use compact pills for:
- Connected
- Disconnected
- Scanning
- Success
- Failed
- Draft
- Thermal optimized

## Icons
- Rounded line icons
- Prefer custom printer, paper, Bluetooth, barcode, QR, image, PDF, CSV icons
- Maintain consistent stroke width

## Accessibility
- Minimum tap target: 44 × 44 px
- Text contrast must meet WCAG AA
- Avoid orange text on cream if contrast is low; use charcoal text with orange accents instead
- Provide clear error labels, not just color

---

# Design Execution Rule
Design the screens **one by one** in this order:
1. First create the design system board/tokens/components.
2. Then create frames 1–6.
3. Then create frames 7–12.
4. Then create frames 13–18.
5. Then create supporting states 19–24.

Before moving to the next batch, verify:
- Visual consistency
- Correct spacing
- Clear hierarchy
- Mobile usability
- Premium feel
- No unnecessary clutter
- All CTAs are obvious

# Final Deliverables
- 24 mobile app frames
- Component set
- Color and typography tokens
- Icon style guide
- Basic clickable prototype flow:
  - Onboarding → Home → Connect Printer → Import/Template → Preview → Print Success
- Developer handoff notes for each screen
