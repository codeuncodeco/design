i want to create a new design system for my hiking community platform

use @design-system.html as a reference for what elements to have in it, but we follow a different color scheme and fonts

what also differs is how dark mode is implemented. dark mode should work without js, so respect the user os settings

ask me questions to get started on implementing my new designs system

i will give you some context beforehand:

1. font: serif
2. colors: earthy

present your plan first in this .md doc before implementing

wait for me to answer questions, tweak and review your plan before implementing

---

## Implementation Plan: BLRHikes Design System

### Overview

Creating a hiking community design system with an earthy, nature-inspired aesthetic that works seamlessly across light and dark modes without JavaScript dependency.

### Design Choices (Based on Your Responses)

**Typography:**

- Primary font: Georgia (web-safe serif)
- Fallback stack: Georgia, 'Times New Roman', Times, serif
- Natural, readable feel suitable for longer content

**Color Palette:**

- Theme: Warm earth tones (browns, terracotta, ochre, warm greens)
- Accent: Earthy orange/red (terracotta/rust tones)
- Constraint: 2-3 colors per mode (light/dark) to maintain simplicity

**Technical Stack:**

- Plain HTML + CSS
- Tailwind CSS via CDN
- Dark mode via CSS `@media (prefers-color-scheme: dark)` - NO JavaScript required

---

### Color System Proposal

#### Light Mode

```css
--bg-primary: #f5f0e8         /* Warm off-white, like sand */
--bg-secondary: #faf8f4       /* Lighter warm white */
--text-primary: #3d2e1f       /* Deep brown, like bark */
--text-secondary: #6b5842     /* Medium warm brown */
--border-color: #d4c4b0       /* Soft tan */
--accent: #c85a3a             /* Terracotta/rust - primary interactive color */
--accent-hover: #a84a2f       /* Darker terracotta for hover states */
```

#### Dark Mode

```css
--bg-primary: #1f1b16         /* Deep warm black, like rich soil */
--bg-secondary: #2a231d       /* Slightly lighter warm dark */
--text-primary: #e8dfd5       /* Warm off-white for text */
--text-secondary: #a89885     /* Muted tan */
--border-color: #3d352c       /* Subtle warm border */
--accent: #d67356             /* Slightly brighter terracotta for dark mode */
--accent-hover: #c85a3a       /* Hover state */
```

---

### Components to Include

Based on the reference design system, we'll create:

1. **Foundation**

   - Color palette showcase
   - Typography scale
   - Spacing system

2. **Buttons**

   - Primary (accent color)
   - Secondary (outlined)
   - Icon buttons
   - Disabled states

3. **Form Elements**

   - Text inputs
   - Textareas
   - Select dropdowns
   - Checkboxes & radio buttons
   - Range sliders
   - Toggle switches

4. **Cards**

   - Basic card
   - Hike/trail cards
   - User profile cards
   - Stats cards

5. **Navigation**

   - Top navigation bar
   - Tabs
   - Breadcrumbs
   - Pagination
   - Bottom navigation (mobile)
   - Drawer menu (mobile)

6. **Feedback Components**

   - Toast notifications
   - Modal windows
   - Loading states (spinner, skeleton)
   - Badges & tags

7. **Mobile Components**
   - Mobile headers
   - Bottom navigation
   - Action sheets
   - Compact cards

---

### Dark Mode Implementation Strategy

**Key Difference from Reference:**
The reference uses `.dark` class toggle with JavaScript. We'll use CSS media queries:

```css
:root {
  /* Light mode variables */
}

@media (prefers-color-scheme: dark) {
  :root {
    /* Dark mode variables - automatically applied */
  }
}
```

**Benefits:**

- Respects user OS/browser preferences automatically
- No JavaScript required
- No FOUC (Flash of Unstyled Content)
- Better accessibility
- Simpler implementation

---

### File Structure

I'll create a single HTML file named `blrhikes-design-system.html` that includes:

1. Tailwind CSS from CDN
2. Custom CSS with CSS variables for theming
3. All component showcases
4. Responsive design (mobile-first)

---

### Implementation Steps

1. **Setup** - HTML boilerplate with Tailwind CDN
2. **CSS Variables** - Define color system with light/dark mode support
3. **Typography** - Set up Georgia font stack and text scales
4. **Base Components** - Buttons, inputs, cards
5. **Navigation Components** - Desktop and mobile patterns
6. **Feedback Components** - Modals, toasts, loading states
7. **Mobile-Specific Components** - Bottom nav, action sheets
8. **Spacing & Layout System** - Consistent spacing scale
9. **Interactive States** - Hover, focus, active states
10. **Final Polish** - Accessibility checks, responsive refinements

---

### Questions / Clarifications Needed

1. **Component naming** - Should I use hiking-specific names (e.g., "trail card" instead of "project card")? yes
2. **Icons** - Continue using Font Awesome like the reference, or prefer a different icon library? fa
3. **Additional components** - Any hiking-specific components needed (difficulty badges, elevation charts, weather indicators)? none right now

Please review this plan and let me know:

- Do the colors feel right for your vision?
- Should I adjust anything in the approach?
- Ready to proceed with implementation?
