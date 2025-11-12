# 1. Mulai dari image dasar
FROM node:18.16

# 2. Tetapkan direktori kerja
WORKDIR /app

ADD . /app

# 3. (FIX EFISIENSI) Jalankan npm install
RUN npm install

# 4. (FIX EFISIENSI) Salin sisa kode aplikasi Anda
COPY . .

# 5. (FIX KEAMANAN) Ini adalah perbaikan untuk SonarQube
# Ganti dari 'root' ke user 'node' yang sudah ada
USER node

# 6. Expose port dan Label Anda
EXPOSE 3000
LABEL author="jinggaadisaputra@gmail.com"

# 7. Perintah start (akan dijalankan sebagai user 'node')
CMD ["npm", "start"]