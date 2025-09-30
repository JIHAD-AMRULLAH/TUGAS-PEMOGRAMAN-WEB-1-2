# Penjelasan Layout Responsive dengan Tailwind CSS

## 📐 Keputusan Grid & Gap di Tiap Breakpoint
Dalam membuat layout, penggunaan **grid-cols** dan **gap** disesuaikan dengan kebutuhan tampilan pada berbagai ukuran layar:

- **Mobile (sm < 640px)**
  - `grid-cols-1` → Konten ditampilkan dalam satu kolom agar mudah dibaca.
  - `gap-2` atau `gap-4` → Jarak antar elemen lebih rapat karena ruang layar terbatas.

- **Tablet (md ≥ 768px)**
  - `grid-cols-2` → Mulai membagi konten jadi dua kolom, memanfaatkan ruang lebih lebar.
  - `gap-6` → Memberi jarak yang lebih longgar agar layout tidak terlihat padat.

- **Desktop (lg ≥ 1024px)**
  - `grid-cols-3` atau lebih → Bisa menampilkan lebih banyak item dalam satu baris.
  - `gap-8` → Memberi kesan lega dan teratur karena layar besar punya ruang kosong lebih banyak.

- **Extra Large (xl ≥ 1280px)**
  - `grid-cols-4` atau sesuai kebutuhan → Cocok untuk galeri, dashboard, atau e-commerce.
  - `gap-10` → Memberi keseimbangan antara kepadatan informasi dan kenyamanan visual.

👉 Prinsipnya: semakin besar layar → semakin banyak kolom → semakin besar gap.

---

## 📱 Memanfaatkan Utility Responsive Tailwind
Tailwind menyediakan **prefix responsive** untuk mengatur layout berbeda di tiap breakpoint:

- `sm:`, `md:`, `lg:`, `xl:`, `2xl:`  
- Contoh penggunaan:

```html
<div class="grid grid-cols-1 gap-4 sm:grid-cols-2 md:grid-cols-3 lg:grid-cols-4">
  <div class="bg-blue-200">Item 1</div>
  <div class="bg-blue-200">Item 2</div>
  <div class="bg-blue-200">Item 3</div>
  <div class="bg-blue-200">Item 4</div>
</div>
