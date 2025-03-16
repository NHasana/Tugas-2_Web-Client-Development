# Tugas-2_Web-Client-Development
// 1. Langkah Inisialisasi Git
1. Buat direktori proyek baru:
   ```
   mkdir my-js-project
   cd my-js-project
2. Inisialisasi repositori Git:
   ```
   git init
   ```
3. Buat file JavaScript sederhana:
   ```
   echo "console.log('Hello, Git!');" > index.js
4. Tambahkan file ke Git dan lakukan commit pertama:
   ```
   git add index.js
   git commit -m "Initial commit with index.js"
   ```
5. Tambahkan repository remote jika menggunakan GitHub:
   ```
   git remote add origin https://github.com/username/my-js-project.git
   git push -u origin main
   ```
// 2. langkah untuk Membuat Perubahan
1. Edit file dalam repositori
   Misalnya, kita menambahkan baris baru ke file `index.js`:
   ```
   echo "console.log('Modified version');" >> index.js
   ```
2. Cek status perubahan:
   ```
   git status
   ```
3. Stage perubahan:
   ```
   git add index.js
   ```
4. Lakukan commit dengan pesan deskriptif:
   ```
   git commit -m "Updated index.js with a new log statement"
   ```
5. Push perubahan ke GitHub:
   ```
   git push origin main
   ```

//3. Langkah dengan Branch 
1. Buat branch baru dan berpindah ke branch tersebut:
   ```
   git checkout -b feature-branch
   ```
   (`feature-branch` adalah nama branch baru yang dibuat.)
2. Buat perubahan pada file:
   ```
   echo "console.log('New feature added');" >> index.js
   ```
3. Stage dan commit perubahan:
   ```
   git add index.js
   git commit -m "Added a new feature in feature-branch"
   ```
4. Beralih kembali ke branch `main`:
   ```
   git checkout main
   ```
5. Gabungkan branch baru ke `main`:
   ```
   git merge feature-branch
   ```
6. Push perubahan ke GitHub:
   ```
   git push origin main
   ```

// 4. langkah untuk Bekerja di Branch Baru
1. Pastikan berada di branch baru:
   ```
   git checkout -b new-branch
   ```
2. ubah file dalam branch tersebut:
   ```
   echo "console.log('Changes in new branch');" >> index.js
   ```
3. Cek status perubahan:
   ```
   git status
   ```
4. Stage perubahan:
   ```
   git add index.js
   ```
5. Commit dengan pesan deskriptif:
   ```
   git commit -m "Updated index.js in new-branch"
   ```

// 5. langkah Membuat Pull Request
1. Pastikan sudah melakukan push branch
   ```
   git push origin new-branch
   ```
2. Buka GitHub dan navigasikan ke repository
3. Klik "Compare & pull request"
   GitHub akan menampilkan perbedaan antara `branch new-branch` dan `main`.
   Tambahkan deskripsi mengenai perubahan yang telah dilakukan.
4. Lakukan Code Review
   Jika Anda bekerja dalam tim, minta anggota tim untuk memberikan masukan sebelum
   merge.
5. Klik 'Merge pull requsr'
   Setelah direview, gabungkan branch ke `main` dengan mengklik tombol Merge pull
   request.
6. Hapus branch yang sudah digabungkan
   ```
   git branch -d new-branch
   git push origin --delete new-branch
   ```
