# TODO for Admin Dashboard Sidebar Implementation

## Step 1: Add State Management
- [x] Add state variables: activeView ('view', 'add', 'update'), selectedSubproduct ('gemstones', 'rudraksha', etc.), showAddModal (boolean), products (object with arrays for each type), newProduct (object for form).

## Step 2: Add Sidebar Component
- [x] Create sidebar JSX with menu items: 'View All Products' (expandable), 'Add Product', 'Update Product'.
- [x] Add click handlers to set activeView.

## Step 3: Implement View All Products
- [x] For 'View All Products', show subproduct buttons (gemstones, rudraksha, bracelet, mala, yantra).
- [x] On click, set selectedSubproduct and display table for that type (generalize current gemstone table).

## Step 4: Implement Add Product
- [x] Add popup modal for adding product.
- [x] Form: select product type, enter name, carat, shape, price, stock.
- [x] On submit, call API to add.

## Step 5: Implement Update Product
- [x] Similar to add, but for updating existing products (select product, edit fields).

## Step 6: Generalize API Calls
- [x] Create functions like fetchProducts(type), addProduct(type, data), etc.
- [x] Assume endpoints: /product/getall/{type}, /product/add/{type}, etc.

## Step 7: Update UI Layout
- [x] Wrap content in .admin-container, .admin-row, .admin-sidebar, .admin-main classes from CSS.

## Step 8: Test and Refine
- [x] Ensure navigation works, forms submit correctly, responsive design.
