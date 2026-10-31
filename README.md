# LAB 07A: ROOM ENTITY & DAO CONSTRUCTION

- Họ tên: Bùi Duy Anh
- MSSV: 2474802010525

## Nội dung

- **Gradle & KSP:** plugin `com.google.devtools.ksp` (1.9.24-1.0.20), Room 2.6.1 (`room-runtime`, `room-ktx`, `ksp(room-compiler)`), `lifecycle-livedata-ktx` 2.8.0.
- **`data/local/ProductEntity.kt`:** bảng `products` gồm `id` (khóa chính tự tăng), `product_name`, `product_price`, `stock_quantity`.
- **`data/local/ProductDao.kt`:** `insertProduct` (REPLACE, suspend), `deleteProduct` (suspend), `getAllProducts()` trả về `LiveData<List<ProductEntity>>`, `getProductById()` (suspend, trả về `ProductEntity?`).
- **`data/local/AppDatabase.kt`:** `RoomDatabase` singleton để Room sinh code cho DAO.
