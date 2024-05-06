# Advance Programming Tutorial 10
Tutorial for Advanced Programming 2024 Module 10 - Faculty of Computer Science, Universitas Indonesia

---
## Reflection - Yew Webchat 🦀

---
### 3.1. Original code

Berikut adalah tampilan Yew Webchat setelah saya run dan coba mengirimkan pesan untuk 2 user pada window `localhost:8000` yang berbeda:

![](image/3.1.png)

### 3.2. Add some creativities to the webclient

Untuk bagian kedua yang menggunakan kreativitas, saya menambahkan icon avatar random untuk setiap user dengan menggunakan API Dicebear. Saya menambahkan avatar tersebut dengan mengubah beberapa bagian kode, terutama dalam html:

```html
src={format!("https://api.dicebear.com/8.x/notionists/svg?seed={}", user.avatar)}
```

Sehingga menghasilkan output tampilan sebagai berikut:

![](image/3.2.(Avatar).png)

Kemudian secara fungsionalitas, saya menambahkan fungsi `keypress` yaitu untuk memastikan pesan dapat dikirim hanya dengan menggunakan tombol enter pada keyboard, tanpa perlu menekan button kirim yang ditampilkan. Saya menambahkan sedikit block code untuk chat yaitu:

```rust
impl Chat {
    fn keypress(&self, event: KeyboardEvent) -> Msg {
        Msg::Keypress(event)
    }
}
```

Secara keseluruhan, saya mengubah tampilan webchat Yew menjadi Dark Mode karena preferensi pribadi yang lebih suka menggunakan Dark Mode untuk aplikasi chat. Berikut adalah tampilan akhirnya:

![](image/3.2.(Login).png)
![](image/3.2.(Chat).png)