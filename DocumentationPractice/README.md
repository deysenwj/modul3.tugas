
## ConcertTicketSystem

**Concert Ticket System** adalah sebuah package Java yang dirancang untuk mengelola penjualan tiket konser. Package ini menyediakan berbagai fungsi untuk membeli tiket, memeriksa ketersediaan tiket, dan menghitung total biaya pembelian tiket.

## Cara Menggunakan

Anda dapat menggunakan package ini dengan cara berikut:

1. **Menambahkan Package ke Proyek Anda**
    - Salin package `tugas2` ke dalam proyek Java Anda.

2. **Membuat Instance ConcertTicketSystem**
    - Import package `tugas2.ConcertTicketSystem`.
    - Buat instance `ConcertTicketSystem` dengan memberikan nama konser, total tiket yang tersedia, dan harga tiket.

   ```java
   ConcertTicketSystem ticketSystem = new ConcertTicketSystem("Nama Konser", 100, 50.0);
   ```

3. **Membeli Tiket**
    - Menggunakan instance `ConcertTicketSystem`, Anda dapat membeli tiket dengan memanggil `purchaseTickets` dengan parameter jumlah tiket yang diinginkan.

   ```java
   double totalCost = ticketSystem.purchaseTickets(2); // Membeli 2 tiket
   ```

    - Jika permintaan pembelian tidak valid (lebih banyak tiket yang diminta daripada yang tersedia atau jumlah tiket yang negatif), akan menghasilkan `IllegalArgumentException`.

4. **Memeriksa Ketersediaan Tiket**
    - Anda dapat memeriksa ketersediaan tiket dengan memanggil `checkTicketAvailability`.

   ```java
   int availableTickets = ticketSystem.checkTicketAvailability(); // Mengembalikan sisa tiket yang tersedia
   ```

5. **Mengambil Nama Konser**
    - Anda juga dapat mengambil nama konser dengan memanggil `getConcertName`.

   ```java
   String concertName = ticketSystem.getConcertName(); // Mengembalikan nama konser
   ```

## Contoh Penggunaan

```java
ConcertTicketSystem ticketSystem = new ConcertTicketSystem("Konser A", 200, 75.0);

int availableTickets = ticketSystem.checkTicketAvailability(); // Memeriksa ketersediaan tiket

double totalCost = ticketSystem.purchaseTickets(4); // Membeli 4 tiket
```

## Catatan

Pastikan untuk menangani pengecualian (exception) yang dihasilkan jika permintaan pembelian tiket tidak valid dengan menggunakan `try` dan `catch`. Misalnya:

```java
try {
    double totalCost = ticketSystem.purchaseTickets(10); // Contoh permintaan tiket yang tidak valid
} catch (IllegalArgumentException e) {
    System.out.println("Error: " + e.getMessage());
}
```