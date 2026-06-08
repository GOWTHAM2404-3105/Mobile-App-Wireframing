Wireframe Annotations — QuickBite
Platform: Android (Material Design 3)
Frame size: 412×915px (Pixel 7 reference)
Fidelity: Low-fidelity (greyscale, placeholder blocks)

Screen 1 — Home
Purpose: Entry point for discovery and quick reordering.

┌─────────────────────────┐
│  ≡   QuickBite   🔔  👤 │  ← Top app bar (M3)
├─────────────────────────┤
│  📍 Koramangala, Blr ▾  │  ← Location selector (tappable)
├─────────────────────────┤
│  🔍 Search restaurants  │  ← Search bar (full width)
├─────────────────────────┤
│  ┌──────────────────┐   │
│  │   PROMO BANNER   │   │  ← Auto-scrolling offers strip
│  └──────────────────┘   │
├─────────────────────────┤
│  Categories             │
│  🍕  🍜  🍔  🥗  🍣    │  ← Horizontal scroll chips
├─────────────────────────┤
│  Reorder               │
│  ┌────────┐ ┌────────┐  │  ← Last 2 orders (quick reorder)
│  │ [img]  │ │ [img]  │  │
│  │ Name   │ │ Name   │  │
│  │ ↻ Reorder│ ↻ Reorder│  │
│  └────────┘ └────────┘  │
├─────────────────────────┤
│  Restaurants near you   │
│  ┌───────────────────┐  │
│  │ [cover img]       │  │  ← Restaurant card
│  │ Restaurant Name   │  │
│  │ ⭐4.3 · 25 min · ₹₹│  │
│  └───────────────────┘  │
│  ┌───────────────────┐  │
│  │ [cover img]       │  │
│  │ Restaurant Name   │  │
│  │ ⭐4.1 · 30 min · ₹  │  │
│  └───────────────────┘  │
├─────────────────────────┤
│  🏠    🔍    📦    👤   │  ← Bottom nav (Home, Search, Orders, Profile)
└─────────────────────────┘
Annotations:

Location selector opens an address picker bottom sheet
Search bar is tappable — navigates to search screen (not inline search)
Reorder row is visible only for returning users
Bottom navigation uses Material 3 Navigation Bar component
Active tab: Home (filled icon)
Screen 2 — Restaurant Menu
Purpose: Browse the restaurant's menu and add items to cart.

┌─────────────────────────┐
│  ←   Restaurant Name    │  ← Top app bar with back arrow
├─────────────────────────┤
│  ┌───────────────────┐  │
│  │  COVER IMAGE      │  │  ← Restaurant cover (16:9)
│  └───────────────────┘  │
│  Restaurant Name        │
│  ⭐4.3  ·  25–35 min   │
│  ₹20 delivery · Veg 🟢  │
├─────────────────────────┤
│  🥦Veg  🍗All  🌶️Spicy  │  ← Sticky category filter chips
├─────────────────────────┤
│  Starters               │  ← Section header
│  ┌───────────────────┐  │
│  │ [img] Item name   │  │  ← Menu item card
│  │       ₹180   🟢   │  │    (green dot = veg)
│  │       ────────    │  │
│  │       Description │  │
│  │                [+]│  │  ← Add button (FAB-style)
│  └───────────────────┘  │
│  ┌───────────────────┐  │
│  │ [img] Item name   │  │
│  │       ₹220   🔴   │  │
│  │       Description │  │
│  │                [+]│  │
│  └───────────────────┘  │
├─────────────────────────┤
│      [ View Cart — 2 items · ₹400 ]     │  ← Persistent cart pill
├─────────────────────────┤
│  🏠    🔍    📦    👤   │
└─────────────────────────┘
Annotations:

Category filter chips are sticky (remain visible on scroll)
Veg/non-veg indicator uses standard Indian food app colour convention (green = veg, red = non-veg)
"View Cart" pill is persistent and updates in real time as items are added
Tapping [+] on an item with customisations opens a bottom sheet for options
Tapping the item itself opens the full item detail screen
Screen 3 — Cart
Purpose: Review selected items, apply offers, and proceed to checkout.

┌─────────────────────────┐
│  ←   Your cart (2)      │
├─────────────────────────┤
│  Restaurant Name        │
│  ┌───────────────────┐  │
│  │ [img] Item 1      │  │  ← Cart item
│  │       ₹180    [-][1][+]│  ← Quantity controls
│  └───────────────────┘  │
│  ┌───────────────────┐  │
│  │ [img] Item 2      │  │
│  │       ₹220    [-][1][+]│
│  └───────────────────┘  │
│  + Add more items       │  ← Returns to menu
├─────────────────────────┤
│  Offers & coupons       │
│  [ Enter promo code → ] │
├─────────────────────────┤
│  Bill summary           │
│  Item total      ₹400   │
│  Delivery fee    ₹20    │
│  Platform fee    ₹5     │  ← Transparent fee breakdown
│  ──────────────────     │
│  Total           ₹425   │
├─────────────────────────┤
│  ┌─────────────────────┐│
│  │  Proceed to checkout││  ← Primary CTA (M3 Filled Button)
│  └─────────────────────┘│
└─────────────────────────┘
Annotations:

Fee breakdown is always visible — addresses Ravi persona's "hidden fees" pain point
Promo code field is collapsed by default; expands on tap
Removing all items from a restaurant prompts "Your cart is empty" with CTA to browse
No bottom navigation bar on this screen — full focus on checkout action
Screen 4 — Checkout
Purpose: Confirm delivery address, select payment, and place the order.

┌─────────────────────────┐
│  ←   Checkout           │
├─────────────────────────┤
│  Deliver to             │
│  ┌───────────────────┐  │
│  │ 📍 14/2, HSR Layout│  │  ← Saved address (tappable to change)
│  │    Bangalore 560102│  │
│  └───────────────────┘  │
│  + Add new address      │
├─────────────────────────┤
│  Payment method         │
│  ○ UPI (GPay)           │  ← Radio group
│  ● Debit card •••• 4521 │  ← Selected (last used)
│  ○ Cash on delivery     │
│  ○ Wallet (₹120 balance)│
│  + Add payment method   │
├─────────────────────────┤
│  Delivery instructions  │
│  [ Leave at door ▾ ]    │  ← Dropdown
├─────────────────────────┤
│  Order summary          │
│  2 items · ₹400 + ₹25 fees │
│  ──────────────────     │
│  Total: ₹425            │
├─────────────────────────┤
│  ┌─────────────────────┐│
│  │  Place order ₹425   ││  ← CTA shows final amount
│  └─────────────────────┘│
└─────────────────────────┘
Annotations:

Final total is shown on the CTA button itself — no surprise at confirmation
UPI auto-opens the selected UPI app on tap (GPay, PhonePe, etc.)
Address and payment are pre-filled from last session
"Place order" triggers a loading state → Order Confirmed screen
Screen 5 — Live Order Tracking
Purpose: Give users full visibility of their order status post-purchase.

┌─────────────────────────┐
│  ←  Order #QB-28471     │
├─────────────────────────┤
│  ┌───────────────────┐  │
│  │                   │  │
│  │    LIVE MAP       │  │  ← Google Maps embed (live rider pin)
│  │    [rider pin 🛵]  │  │
│  │                   │  │
│  └───────────────────┘  │
├─────────────────────────┤
│  Arriving in 18 min     │  ← Dynamic ETA (updates in real time)
├─────────────────────────┤
│  ● Order placed         │  ← Status step (filled = complete)
│  ● Preparing your food  │
│  ◉ Out for delivery     │  ← Active step (animated)
│  ○ Delivered            │
├─────────────────────────┤
│  Your delivery partner  │
│  ┌───────────────────┐  │
│  │ 👤 Arjun K.       │  │
│  │    ⭐ 4.8 · Hero   │  │
│  │    📞 Call  💬 Chat│  │  ← Contact options
│  └───────────────────┘  │
├─────────────────────────┤
│  Need help?    [ › ]    │  ← Support access
├─────────────────────────┤
│  🏠    🔍    📦    👤   │
│              ●           │  ← Orders tab active (with badge)
└─────────────────────────┘
Annotations:

Map takes ~40% of the screen height — prominent, not hidden
ETA updates every 60 seconds via backend polling
Status steps use M3 Stepper pattern
Rider contact options: Call opens phone dialler; Chat opens in-app chat
Bottom nav is present — user can navigate away and return to tracking
Orders tab shows a badge dot while an active order is in progress