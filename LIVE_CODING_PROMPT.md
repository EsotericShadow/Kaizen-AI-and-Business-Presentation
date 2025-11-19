# Live Coding Demonstration Prompt

## Context

During the AI & Business Presentation on October 23, 2025, a live coding demonstration was performed using AI assisted development (Cursor). While continuing to present to the audience, this prompt was entered into Cursor, which then built a complete Next.js application in real time behind the scenes.

This demonstration showcased:
- AI assisted development capabilities
- Real time application building
- Practical business application development
- The power of modern AI coding tools

## The Prompt

```
Create a tip out calculator for a restaurant in Terrace, BC using Next.js 14, TypeScript, and Tailwind CSS.

Build a complete Next.js application with:

**Framework & Structure:**

- Next.js 14 with App Router
- TypeScript for type safety
- Tailwind CSS for styling
- React Hook Form for form management
- Zustand for state management
- Single page application with client-side routing
- Browser localStorage for data persistence (demo only, no real auth)

**Project Structure:**

/app
/login/page.tsx
/employee/page.tsx
/manager/page.tsx
/layout.tsx
/components
/ReceiptForm.tsx
/ReceiptList.tsx
/ManagerDashboard.tsx
/EmployeeManagement.tsx
/Settings.tsx
/Navigation.tsx
/lib
/types.ts
/calculations.ts
/store.ts

**Screen Structure:**

- Login screen: Employee ID input (Employee vs Manager role, no real auth)
- Employee Dashboard: Individual receipt input and personal totals
- Manager Dashboard: All employees' totals and tip out calculations
- Employee Management: Add/edit/delete employees, view receipts
- Settings: Different for employees vs managers

**Employee Interface (Main Screen):**

- Header: "Terrace Bistro Server Tip Out Calculator"
- Employee name and ID display
- "Add Receipt" button (plus icon)
- Receipt list showing: Receipt number, Subtotal, Tax, Tip, Total, Time, Status
- Personal totals: Total Sales, Total Tips, Tip out Amount, Take home
- "Submit to Manager" button
- Personal settings: Update name, employee ID, profile info

**Receipt Input Flow (Modal/Overlay):**

- Step 1: Receipt number input (auto-increment or manual)
- Step 2: Amount fields: Subtotal, Tax (auto-calculated at 12% GST), Tip, Total (auto-calculated)
- Step 3: Optional photo capture (camera icon), for reference only
- Step 4: Review and confirm receipt details
- Navigation: "Previous", "Next", "Save Receipt", "Cancel"
- Progress indicator: Step 1 of 4, Step 2 of 4, etc.
- Form validation with real time feedback
- "Add Another Receipt" or "Done" buttons

**Manager Interface:**

- Header: "Terrace Bistro Manager Dashboard"
- Employee list with totals: Name, Total Sales, Total Tips, Tip out, Take home
- Tip out percentages: Kitchen (1 to 2%), Support (0.5 to 1%)
- Calculate all tip outs button
- Export options: PDF, CSV
- "Back to Employee View" button

**Manager Employee Management:**

- Add new employee: Name, Employee ID, Role, Start date
- Edit employee: Update info, view all receipts, view photos
- Delete employee: Remove from system
- View individual employee: Full receipt history, photos, calculations
- Employee performance: Sales totals, tip averages, receipt counts

**Manager Settings:**

- Tip out percentages: Kitchen, Support, Custom rates
- Tax rates: GST, PST, Custom rates
- Restaurant settings: Name, address, contact info
- System settings: Auto-calculations, validations, export formats
- User management: Add/edit/delete employees, roles, permissions

**Employee Settings:**

- Personal info: Name, employee ID, contact info
- Preferences: Default tip out rates, notification settings
- Profile: Photo, bio, availability
- Receipt history: View own receipts, photos, totals

**TypeScript Types:**

```typescript
interface Receipt {
  id: string;
  receiptNumber: string;
  subtotal: number;
  tax: number;
  tip: number;
  total: number;
  timestamp: Date;
  image?: string;
  employeeId: string;
}

interface Employee {
  id: string;
  name: string;
  employeeId: string;
  role: 'server' | 'manager';
  receipts: Receipt[];
  totalSales: number;
  totalTips: number;
  tipOut: number;
  takeHome: number;
  profile: {
    photo?: string;
    bio?: string;
    contactInfo?: string;
  };
}

interface TipOutSettings {
  kitchenPercentage: number;
  supportPercentage: number;
  taxRate: number;
}

interface RestaurantSettings {
  name: string;
  address: string;
  contactInfo: string;
  tipOutRates: TipOutSettings;
}
```

**Calculation Functions:**

- Individual server total = Sum of all their receipts
- Tax calculation = Subtotal × Tax Rate (default 12% GST)
- Kitchen tip out = Total Sales × Kitchen Percentage (default 1.5%)
- Support tip out = Total Sales × Support Percentage (default 0.8%)
- Server take home = Total Tips minus Kitchen tip out minus Support tip out

**Functionality:**

- Step-by-step receipt input with clear navigation
- Manual receipt data input with auto-calculated tax
- Optional camera access for receipt photos (mobile/tablet optimized)
- Real time calculation as receipts are added
- Form validation (required fields, number formats)
- PDF/CSV export for manager
- Mobile/tablet responsive design for taking pictures
- Client-side state management with Zustand
- Employee management (add/edit/delete/view)
- Role-based access control (employee vs manager)
- Personal settings for employees
- System settings for managers
- Browser localStorage for data persistence (demo only)

**Sample Data (pre-filled):**

- Employee: Sarah, ID: 001, Role: server
- Receipts: number 1001 (Subtotal: $40.00, Tax: $4.80, Tip: $6.00, Total: $50.80)
- Total Sales: $50.80, Total Tips: $6.00
- Tip out: Kitchen 1.5%, Support 0.8%

**Styling Requirements:**

- Tailwind CSS for all styling
- Clean, professional restaurant management look
- High contrast for readability
- Hover effects on buttons and table rows
- Success/error states with appropriate colors
- Mobile/tablet responsive design optimized for taking pictures
- Clear navigation between employee and manager views
- Smooth transitions between receipt input steps
- Progress indicators for multi-step forms

**Testing & Quality Assurance:**

- After building the app, start the development server
- Test all screens and functionality in the browser
- Take screenshots of each screen (login, employee dashboard, manager dashboard, receipt form, employee management, settings)
- Check for UI content overflow issues on desktop and mobile
- Verify all buttons and forms work correctly
- Test the receipt input flow step-by-step
- Check responsive design on different screen sizes
- Fix any UI issues found during testing
- Ensure all calculations are accurate
- Verify navigation between screens works properly
- Test form validation and error handling
- Confirm PDF/CSV export functionality works
- Test employee management features
- Test role-based access control
- Take final screenshots showing the working application
```

## Demonstration Impact

This live coding demonstration effectively showed the audience:

1. **AI Assisted Development**: How AI tools like Cursor can accelerate development
2. **Real Time Capability**: Building a complete application while presenting
3. **Practical Application**: Creating a real business tool (restaurant tip out calculator)
4. **Modern Tech Stack**: Implementation of Next.js 14, TypeScript, and Tailwind CSS
5. **Business Value**: Demonstrating how AI can build practical solutions quickly

## Technical Details

- **Tool Used**: Cursor (AI assisted code editor)
- **Framework**: Next.js 14 with App Router
- **Language**: TypeScript
- **Styling**: Tailwind CSS
- **State Management**: Zustand
- **Form Management**: React Hook Form
- **Persistence**: Browser localStorage (demo purposes)

## Key Takeaways

This demonstration highlighted that:
- AI coding assistants can build complete applications from detailed prompts
- Real time development is possible with AI assistance
- Business applications can be prototyped quickly
- AI tools are practical for both learning and production development
- The intersection of AI and software development is rapidly evolving

---

*This prompt was used during the live coding demonstration at the October 23, 2025 AI & Business Presentation.*

