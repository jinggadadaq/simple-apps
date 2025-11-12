# 1. Mulai dari image dasar
FROM node:18.16

# 2. Tetapkan direktori kerja
WORKDIR /app

# 3. (FIX EFISIENSI) Salin hanya package.json dulu
# 'npm install' hanya akan jalan lagi jika file ini berubah
COPY package*.json ./

# 4. (FIX EFISIENSI) Jalankan npm install
RUN npm install

# 5. (FIX EFISIENSI) Salin sisa kode aplikasi Anda
COPY . .

# 6. (FIX KEAMANAN) Ini adalah perbaikan untuk SonarQube
# Ganti dari 'root' ke user 'node' yang sudah ada
USER node

# 7. Expose port dan Label Anda
EXPOSE 3000
LABEL author="jinggaadisaputra@gmail.com"

# 8. Perintah start (akan dijalankan sebagai user 'node')
CMD ["npm", "start"]