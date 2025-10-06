# Order Tracker - Norwex/Nutrimetics

A fully offline Progressive Web App (PWA) for tracking customer orders and payments. Works completely offline after first load - no internet or server required!

## Features

- **Customer Management**: Add, edit, and track customers with contact details
- **Order Tracking**: Create orders with multiple line items, automatic calculations, and payment status
- **Smart Calculations**: Auto-calculates subtotals, discounts (default 32%), shipping, and totals
- **Quick Add Helper**: Parse orders from text like "2x Hand Towel $15 each, shipping $8"
- **Data Management**: Export/import backups, all data stored locally
- **Fully Offline**: Works without internet after initial load
- **Mobile-Friendly**: Responsive design, can be added to phone home screen

## How to Use

### Getting Started

1. **Open the app**: Simply open `index.html` in any modern web browser (Chrome, Safari, Firefox, Edge)
   - Double-click the file, or
   - Right-click → Open with → [Your browser], or
   - Drag and drop into browser window

2. **First time**: The app comes with 3 example customers to help you get started. You can delete these or keep them as reference.

### Add to Phone Home Screen

#### iOS (iPhone/iPad)
1. Open `index.html` in Safari
2. Tap the Share button (square with arrow)
3. Scroll down and tap "Add to Home Screen"
4. Name it "Order Tracker" and tap "Add"
5. The app will appear on your home screen like a native app

#### Android
1. Open `index.html` in Chrome
2. Tap the three-dot menu (⋮)
3. Tap "Add to Home screen"
4. Name it "Order Tracker" and tap "Add"
5. The app will appear on your home screen

### Managing Customers

**Add a Customer:**
1. Click "Add Customer" button
2. Enter name (required), email, and phone (optional)
3. Click "Save Customer"

**Edit/Delete:**
- Click the edit (pencil) icon on any customer card
- Click the trash icon to delete (will ask for confirmation)

### Creating Orders

**Regular Method:**
1. Click "Add Order" on a customer card
2. Fill in order date (defaults to today)
3. Add line items:
   - Item name, quantity, and price
   - Click "Add Item" for more items
4. Adjust discount % (default is 32%)
5. Enter shipping cost
6. Toggle payment status (Paid/Unpaid)
7. Add notes if needed
8. Click "Save Order"

**Quick Add Method:**
1. Click "Quick Add" on a customer card
2. Paste order text like:
   ```
   2x Hand Towel $15 each
   1x Body Cloth $12
   shipping $8
   ```
3. Click "Parse and Add Order"
4. Review the pre-filled form and save

### Viewing Orders

- Click on any customer card to expand and see their orders
- Orders show newest first
- Each order displays:
  - Order date and total amount
  - All line items with prices
  - Discount and shipping breakdown
  - Payment status (Paid/Unpaid)
  - Any notes

### Editing/Deleting Orders

- Click the pencil icon on any order to edit
- Click the trash icon to delete (will ask for confirmation)

### Filtering and Search

- **Search bar**: Type to filter customers by name, email, or phone
- **Filter buttons**:
  - **All**: Show all customers
  - **Paid**: Show customers with paid orders
  - **Unpaid**: Show customers with unpaid orders

### Dashboard Summary

At the top of the app, you'll see:
- Total number of customers
- Total number of orders
- Total sales amount (NZD)
- Total unpaid amount (NZD)

## Data Management

### Backup Your Data

**IMPORTANT**: Your data is stored only on this device. Always keep backups!

1. Click the download icon (⬇) at the top
2. A file named `order-tracker-backup-[date].json` will download
3. Save this file somewhere safe (email it to yourself, save to cloud storage, etc.)

**Recommendation**: Export your data weekly or after major changes!

### Restore from Backup

1. Click the upload icon (⬆) at the top
2. Select your backup JSON file
3. Confirm that you want to replace current data
4. Your data will be restored

### Clear All Data

1. Click the trash icon at the top
2. Confirm TWICE (this cannot be undone!)
3. All customers and orders will be deleted

**WARNING**: This permanently deletes everything. Make a backup first!

## Tips & Tricks

### Calculations
- All amounts are in NZD ($)
- Calculations update live as you type
- Default discount is 32% but can be changed per order
- Formula: `Total = (Subtotal - Discount) + Shipping`

### Payment Tracking
- Mark orders as "Paid" when payment is received
- Payment date auto-fills with today's date (editable)
- Track unpaid amounts in the dashboard summary

### Data Safety
- All data is stored in your browser's localStorage
- Data persists even if you close the browser
- **Data is device-specific** - not synced between devices
- Always export backups before clearing browser data

### Best Practices
1. Export backups regularly
2. Use the Quick Add feature for faster order entry
3. Add notes to orders for special requests or details
4. Keep customer contact info updated
5. Review unpaid orders weekly

## Troubleshooting

**App won't load:**
- Make sure you're using a modern browser (Chrome, Safari, Firefox, Edge)
- Check that JavaScript is enabled
- Try clearing browser cache and reopening

**Data disappeared:**
- Check if you cleared browser data/cookies
- Restore from your backup JSON file
- If no backup, data may be unrecoverable

**Can't add to home screen:**
- On iOS, must use Safari browser
- On Android, must use Chrome browser
- Make sure the file is opened via HTTPS or file://

**Quick Add not working:**
- Use format: "2x Item Name $15 each"
- Each item on a new line
- Shipping: "shipping $8"
- Numbers and $ symbol are required

## Technical Details

- **Storage**: Browser localStorage (key: `order-tracker-data`)
- **Tech Stack**: React 18, Tailwind CSS, Lucide Icons
- **File Type**: Single HTML file with embedded JavaScript
- **No Internet Required**: Works completely offline after first load
- **No Server Needed**: All processing happens in your browser
- **Privacy**: Your data never leaves your device

## Quick Start Guide for Alysha

1. **Open** the file: Double-click `index.html`
2. **Explore** the 3 example customers already loaded
3. **Try adding** a real customer using the "Add Customer" button
4. **Create an order** using the "Quick Add" feature - paste in an order
5. **Export a backup** using the download icon
6. **Add to phone**: Follow the "Add to Home Screen" instructions above

Now you're ready to track all your Norwex orders offline!

## Support

For issues or questions, contact Stuart who can help with tweaks and updates.

---

**Version**: 1.0
**Last Updated**: October 2025
**Built for**: Alysha's Norwex/Nutrimetics business
