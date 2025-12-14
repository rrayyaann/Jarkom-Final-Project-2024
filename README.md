# Laporan Final Project Jarkom 2024

| Nama | NRP | Tugas |
| ---- | --- | --- |
| Muhamad Arrayyan | 5027231014 | Topologi, Routing |
| Kevin Anugerah Faza | 5027231027 | DHCP, NAT Overload |
| Rafi' Afnaan Fathurrahman | 5027231040 | Generic Routing Encapsulation (GRE Tunnel) |
| Aryasatya Alaauddin | 5027231082 | Subnetting, Config Static IP |

# Laporan
https://docs.google.com/document/d/1g-jXxG1K3P_tM-L2JJjWoKGTUmt9KaQcS8HB_woNzdo/edit?usp=sharing

# Spreadsheet
https://docs.google.com/spreadsheets/d/1Squ1dY88zdvIH3a-5KMqAfZbmeSyyDW5joZg_GiuAYo/edit?usp=sharing

<details>
<summary>Gambar Topologi CPT</summary>
<img width="1500" alt="topologi" src="https://github.com/user-attachments/assets/7229529d-f622-4b83-a7a6-5df9e7fec38e">
</details>

<details>
<summary>Dokumentasi</summary>
## Dokumentasi Testing
<img width="1500" alt="Dept R&D" src="https://github.com/user-attachments/assets/a4b29e17-2fd8-4f08-8068-80e1e158bc46">
<img width="1500" alt="Dept Pemasaran" src="https://github.com/user-attachments/assets/96b8df5f-05b4-429b-8393-ea039a4c0993">
<img width="1500" alt="Dept Penjualan" src="https://github.com/user-attachments/assets/bc6eebd3-c9be-4595-b0ba-beff9b57c495">

<img width="1500" alt="Testing" src="https://github.com/user-attachments/assets/22a8105f-1ab7-460f-8af7-247a94929e8f">
<img width="1500" alt="DNS" src="https://github.com/user-attachments/assets/10b3de0c-8fc2-472c-85ef-1a7aed23b69e">
<img width="1500" alt="DNS Client" src="https://github.com/user-attachments/assets/149a3a2d-e613-474f-baae-0c865a44832e">
<img width="1500" alt="DNS Router" src="https://github.com/user-attachments/assets/6c6f39cd-11c5-4257-944c-03e268a0fcbb">

<img width="1500" alt="Routing GRE Gedung Utama" src="https://github.com/user-attachments/assets/bae97b8c-4e13-4a87-9de3-a0f1c8b8189e">
<img width="1500" alt="Routing GRE Cab Luar Kota" src="https://github.com/user-attachments/assets/6403da1c-62b1-4de3-8ac4-b89f9188827f">
<img width="1500" alt="Testing GRE Cab Gedung Utama" src="https://github.com/user-attachments/assets/9013cf9e-7b72-4796-a50a-31d7930a3968">
<img width="1500" alt="Testing GRE Cab Luar Kota" src="https://github.com/user-attachments/assets/9479a5c9-be41-4a95-875d-4a2beea7634c">
</details>

# Tugas
## 1. Buatlah Topologi 
> topologi jaringan yang mencakup gedung utama dengan lima lantai dan cabang yang terhubung melalui VPN di Cisco Packet Tracer. Gunakan perangkat aringan yang sesuai (misalnya router, switch, dan perangkat lain)
## Topologi
<img width="1500" alt="Subneting" src="https://github.com/user-attachments/assets/69931209-be1b-41dc-99fc-e1732c0c12e9">

## 2. Subnetting 
> subnetting pada jaringan dan tentukan Subnet Mask, Network ID, Broadcast Address, serta Range IP untuk setiap subnet. Buatlah tabel alokasi subnet untuk setiap departemen berdasarkan jumlah perangkat yang dibutuhkan di masingmasing subnet. Gunakan alamat IP Private sesuai dengan standar yang ada (misalnya 10.0.0.0/8, 172.16.0.0/12, atau 192.168.0.0/16).
## Subnetting
<img width="1500" alt="pembagian IP" src="https://github.com/user-attachments/assets/58bd500a-9867-4f17-a997-5ada0776c4a4">

## Pembagian IP
<img width="1500" alt="pembagian IP" src="https://github.com/user-attachments/assets/91d3ce3c-7143-4a52-a06d-7cc41c668104">

## 3. Konfigurasi Static IP
>  pada setiap perangkat jaringan di semua departemen, kecuali lantai 2. Karena untuk lantai 2 menggunakan DHCP.
### Lantai 2 (R&D, Pemasaran, Penjualan)
<img width="1500" alt="Dept R&D" src="https://github.com/user-attachments/assets/a4b29e17-2fd8-4f08-8068-80e1e158bc46">
<img width="1500" alt="Dept Pemasaran" src="https://github.com/user-attachments/assets/96b8df5f-05b4-429b-8393-ea039a4c0993">
<img width="1500" alt="Dept Penjualan" src="https://github.com/user-attachments/assets/bc6eebd3-c9be-4595-b0ba-beff9b57c495">

## 4. Konfigurasikan DHCP
> Departemen R&D, Pemasaran, dan Penjualan akan menggunakan DHCP untuk mengalokasikan alamat IP secara dinamis kepada perangkat mereka. Konfigurasikan DHCP server pada router dan pastikan perangkat di tiga departemen tersebut mendapatkan IP otomatis sesuai dengan rentang yang telah ditentukan. 

### Router Lantai 2
```jsx
ip dhcp pool A4
 network 192.168.0.0 255.255.255.128
 default-router 192.168.0.1
 dns-server 8.8.8.8
```

### R&D, Pemasaran, Penjualan
<details>
<summary>Dokumentasi DHCP</summary>
<img width="1500" alt="Dept R&D" src="https://github.com/user-attachments/assets/a4f06b81-390c-4350-8dee-a26d31dd4d9a">
<img width="1500" alt="Dept Pemasaran" src="https://github.com/user-attachments/assets/386b4ad0-4d1c-4601-a2a3-60672bdf6331">
<img width="1500" alt="Dept Penjualan" src="https://github.com/user-attachments/assets/e2fb1067-66d3-45cb-a97d-665a378b68f0">
</details>

Ubah konfigurasi IP dari static ke DHCP agar dapat mendapatkan IP address dari DHCP server

### Testing
pada router Lantai 2 buka CLI dan jalankan command berikut untuk mengetahui apakah client sudah mendapatkan IP dari DHCP Server
```
show ip dhcp binding
```
<img width="1500" alt="Testing" src="https://github.com/user-attachments/assets/22a8105f-1ab7-460f-8af7-247a94929e8f">

## 5. Konfigurasi Static Routing
>  Routing agar perangkat di setiap departemen dapat berkomunikasi lintas subnet. Jangan menggunakan default route untuk menghubungkan subnetsubnet yang ada. Pastikan setiap router pada masing-masing lantai terhubung dengan benar dan dapat melakukan routing antar subnet.
## Konfigurasi
### Router Gedung Utama
Interfaces
```jsx
interface FastEthernet0/0
 ip address 192.168.1.225 255.255.255.252
 no shut

interface FastEthernet0/1
 ip address 192.168.1.229 255.255.255.252
 no shut

interface Ethernet1/0
 ip address 192.168.1.233 255.255.255.252
 no shut

interface Ethernet1/1
 ip address 192.168.1.237 255.255.255.252
 no shut

interface Ethernet1/2
 ip address 192.168.1.241 255.255.255.252
 no shut

interface Ethernet1/3
 ip address 192.168.1.245 255.255.255.252
 no shut
```

Static Routing
```jsx
ip route 192.168.1.192 255.255.255.224 192.168.1.238 
ip route 192.168.0.0 255.255.255.128 192.168.1.230 
ip route 192.168.1.64 255.255.255.192 192.168.1.242 
ip route 192.168.1.0 255.255.255.192 192.168.1.234 
ip route 192.168.0.128 255.255.255.128 192.168.1.226 
ip route 8.8.8.0 255.255.255.0 192.168.1.246 
ip route 192.168.1.128 255.255.255.192 192.168.2.2 
ip route 192.168.1.248 255.255.255.252 192.168.1.246 
ip route 192.168.1.128 255.255.255.192 192.168.1.246 

```
### Router Lantai 1
Interfaces
```jsx
interface FastEthernet0/0
 ip address 192.168.1.226 255.255.255.252
 no shut

interface FastEthernet0/1
 ip address 192.168.0.129 255.255.255.128
 no shut

```

Static Routing
```jsx
ip route 192.168.1.228 255.255.255.252 192.168.1.225 
ip route 192.168.0.0 255.255.255.128 192.168.1.225 
ip route 192.168.1.236 255.255.255.252 192.168.1.225 
ip route 192.168.1.192 255.255.255.224 192.168.1.225 
ip route 192.168.1.240 255.255.255.252 192.168.1.225 
ip route 192.168.1.64 255.255.255.192 192.168.1.225 
ip route 192.168.1.232 255.255.255.252 192.168.1.225 
ip route 192.168.1.0 255.255.255.192 192.168.1.225 
ip route 8.8.8.0 255.255.255.0 192.168.1.225 
ip route 192.168.1.244 255.255.255.252 192.168.1.225 
ip route 192.168.1.248 255.255.255.252 192.168.1.225 
ip route 192.168.1.128 255.255.255.192 192.168.1.225

```
### Route Lantai 2
Interfaces
```jsx
interface FastEthernet0/0
 ip address 192.168.1.230 255.255.255.252
 no shut

interface FastEthernet0/1
 ip address 192.168.0.1 255.255.255.128
 no shut

```
Static Routing
```jsx
ip route 192.168.1.236 255.255.255.252 192.168.1.229 
ip route 192.168.1.192 255.255.255.224 192.168.1.229 
ip route 192.168.1.240 255.255.255.252 192.168.1.229 
ip route 192.168.1.64 255.255.255.192 192.168.1.229 
ip route 192.168.1.232 255.255.255.252 192.168.1.229 
ip route 192.168.1.0 255.255.255.192 192.168.1.229 
ip route 192.168.1.224 255.255.255.252 192.168.1.229 
ip route 192.168.0.128 255.255.255.128 192.168.1.229 
ip route 8.8.8.0 255.255.255.0 192.168.1.229 
ip route 192.168.1.244 255.255.255.252 192.168.1.229 
ip route 192.168.1.248 255.255.255.252 192.168.1.229 
ip route 192.168.1.128 255.255.255.192 192.168.1.229

```
### Route Lantai 3
Interfaces
```jsx
interface FastEthernet0/0
 ip address 192.168.1.234 255.255.255.252
 no shut
interface FastEthernet0/1
 ip address 192.168.1.1 255.255.255.192
 no shut

```
Static Routing
```jsx
ip route 192.168.1.228 255.255.255.252 192.168.1.233 
ip route 192.168.0.0 255.255.255.128 192.168.1.233 
ip route 192.168.1.236 255.255.255.252 192.168.1.233 
ip route 192.168.1.192 255.255.255.224 192.168.1.233 
ip route 192.168.1.240 255.255.255.252 192.168.1.233 
ip route 192.168.1.64 255.255.255.192 192.168.1.233 
ip route 192.168.1.224 255.255.255.252 192.168.1.233 
ip route 192.168.0.128 255.255.255.128 192.168.1.233 
ip route 8.8.8.0 255.255.255.0 192.168.1.233 
ip route 192.168.1.244 255.255.255.252 192.168.1.233 
ip route 192.168.1.248 255.255.255.252 192.168.1.233 
ip route 192.168.1.128 255.255.255.192 192.168.1.233

```
### Route Lantai 4
Interfaces
```jsx
interface FastEthernet0/0
 ip address 192.168.1.238 255.255.255.252
 no shut

interface FastEthernet0/1
 ip address 192.168.1.193 255.255.255.224
 no shut

```
Static Routing
```jsx
ip route 192.168.1.228 255.255.255.252 192.168.1.237 
ip route 192.168.0.0 255.255.255.128 192.168.1.237 
ip route 192.168.1.240 255.255.255.252 192.168.1.237 
ip route 192.168.1.64 255.255.255.192 192.168.1.237 
ip route 192.168.1.232 255.255.255.252 192.168.1.237 
ip route 192.168.1.0 255.255.255.192 192.168.1.237 
ip route 192.168.1.224 255.255.255.252 192.168.1.237 
ip route 192.168.0.128 255.255.255.128 192.168.1.237 
ip route 8.8.8.0 255.255.255.0 192.168.1.237 
ip route 192.168.1.244 255.255.255.252 192.168.1.237 
ip route 192.168.1.248 255.255.255.252 192.168.1.237 
ip route 192.168.1.128 255.255.255.192 192.168.1.237

```
### Route Lantai 5
Interfaces
```jsx
interface FastEthernet0/0
 ip address 192.168.1.242 255.255.255.252
 no shut

interface FastEthernet0/1
 ip address 192.168.1.65 255.255.255.192
 no shut

```

Static Routing
```jsx
ip route 192.168.1.228 255.255.255.252 192.168.1.241 
ip route 192.168.0.0 255.255.255.128 192.168.1.241 
ip route 192.168.1.236 255.255.255.252 192.168.1.241 
ip route 192.168.1.192 255.255.255.224 192.168.1.241 
ip route 192.168.1.232 255.255.255.252 192.168.1.241 
ip route 192.168.1.0 255.255.255.192 192.168.1.241 
ip route 192.168.1.224 255.255.255.252 192.168.1.241 
ip route 192.168.0.128 255.255.255.128 192.168.1.241 
ip route 8.8.8.0 255.255.255.0 192.168.1.241 
ip route 192.168.1.244 255.255.255.252 192.168.1.241 
ip route 192.168.1.248 255.255.255.252 192.168.1.241 
ip route 192.168.1.128 255.255.255.192 192.168.1.241

```

### Router ISP (Internet Service Provider)
```jsx
interface FastEthernet0/0
 ip address 192.168.1.246 255.255.255.252
 
interface FastEthernet0/1
 ip address 192.168.1.249 255.255.255.252

interface FastEthernet1/0
 ip address 8.8.8.1 255.255.255.0

```
Static Routing
```jsx
ip route 192.168.1.128 255.255.255.192 192.168.1.250 
ip route 192.168.1.224 255.255.255.252 192.168.1.245 
ip route 192.168.0.128 255.255.255.128 192.168.1.245 
ip route 192.168.1.232 255.255.255.252 192.168.1.245 
ip route 192.168.1.0 255.255.255.192 192.168.1.245 
ip route 192.168.1.240 255.255.255.252 192.168.1.245 
ip route 192.168.1.64 255.255.255.192 192.168.1.245 
ip route 192.168.1.236 255.255.255.252 192.168.1.245 
ip route 192.168.1.192 255.255.255.224 192.168.1.245 
ip route 192.168.1.228 255.255.255.252 192.168.1.245 
ip route 192.168.0.0 255.255.255.128 192.168.1.245

```

### Router Cabang Luar Kota
```jsx
interface FastEthernet0/0
 ip address 192.168.1.250 255.255.255.252
 no shut

interface FastEthernet0/1
 ip address 192.168.1.129 255.255.255.192
 no shut

```

Static Routing
```jsx
ip route 8.8.8.0 255.255.255.0 192.168.1.249 
ip route 192.168.1.244 255.255.255.252 192.168.2.1 
ip route 192.168.1.244 255.255.255.252 192.168.1.249 
ip route 192.168.1.228 255.255.255.252 192.168.1.249 
ip route 192.168.0.0 255.255.255.128 192.168.1.249 
ip route 192.168.1.236 255.255.255.252 192.168.1.249 
ip route 192.168.1.192 255.255.255.224 192.168.1.249 
ip route 192.168.1.240 255.255.255.252 192.168.1.249 
ip route 192.168.1.64 255.255.255.192 192.168.1.249 
ip route 192.168.1.232 255.255.255.252 192.168.1.249 
ip route 192.168.1.0 255.255.255.192 192.168.1.249 
ip route 192.168.1.224 255.255.255.252 192.168.1.249 
ip route 192.168.0.128 255.255.255.128 192.168.1.249

```

## 6. Konfigurasi NAT
>Perusahaan membutuhkan akses ke internet untuk semua perangkat yang terhubung. Konfigurasikan NAT Overload (PAT) pada router utama untuk memungkinkan perangkat dalam jaringan lokal mengakses internet, misalnya dengan melakukan ping ke 8.8.8.8.

### Router Gedung Utama
Tambahkan command `ip nat outside` atau `ip nat inside` di setiap interface
```jsx
interface Ethernet1/3
 ip address 192.168.1.245 255.255.255.252
 ip nat outside

interface FastEthernet0/0
 ip address 192.168.1.225 255.255.255.252
 ip nat inside

interface FastEthernet0/1
 ip address 192.168.1.229 255.255.255.252
 ip nat inside

interface Ethernet1/0
 ip address 192.168.1.233 255.255.255.252
 ip nat inside

interface Ethernet1/1
 ip address 192.168.1.237 255.255.255.252
 ip nat inside

interface Ethernet1/2
 ip address 192.168.1.241 255.255.255.252
 ip nat inside
```

Jalankan command berikut untuk menerapkan NAT pada semua alamat IP sumber dari jaringan internal agar dapat mengakses internet:
```
access-list 1 permit any 
ip nat inside source list 1 interface Ethernet1/3 overload
```
### Router ISP
```jsx
interface FastEthernet0/0
 ip address 192.168.1.246 255.255.255.252
 
interface FastEthernet0/1
 ip address 192.168.1.249 255.255.255.252

interface FastEthernet1/0
 ip address 8.8.8.1 255.255.255.0

```
Static Routing
```jsx
ip route 192.168.1.128 255.255.255.192 192.168.1.250 
ip route 192.168.1.224 255.255.255.252 192.168.1.245 
ip route 192.168.0.128 255.255.255.128 192.168.1.245 
ip route 192.168.1.232 255.255.255.252 192.168.1.245 
ip route 192.168.1.0 255.255.255.192 192.168.1.245 
ip route 192.168.1.240 255.255.255.252 192.168.1.245 
ip route 192.168.1.64 255.255.255.192 192.168.1.245 
ip route 192.168.1.236 255.255.255.252 192.168.1.245 
ip route 192.168.1.192 255.255.255.224 192.168.1.245 
ip route 192.168.1.228 255.255.255.252 192.168.1.245 
ip route 192.168.0.0 255.255.255.128 192.168.1.245

```

### Server 8.8.8.8 (www.google.com)
```jsx
IP Address: 8.8.8.8
netmask: 255.255.255.0
```
### Server 8.8.8.9 (cisco.com
```jsx
IP Address: 8.8.8.9
netmask: 255.255.255.0
```
### Server 8.8.8.10 (facebook.com)
```jsx
IP Address: 8.8.8.10
netmask: 255.255.255.0
```

Pada **Server 8.8.8.8** Jangan lupa nyalakan DNS Service dan tambahkan domain `www.google.com` dengan IP `8.8.8.8`, `cisco.com` dengan IP `8.8.8.9`, dan `facebook.com` dengan IP `8.8.8.10`

<img width="1500" alt="DNS" src="https://github.com/user-attachments/assets/10b3de0c-8fc2-472c-85ef-1a7aed23b69e">

### semua nodes
Tambahkan DNS server di CLI router 
```
ip name-server 8.8.8.8
```
<img width="1500" alt="DNS Router" src="https://github.com/user-attachments/assets/6c6f39cd-11c5-4257-944c-03e268a0fcbb">

Tambahkan juga di client langsung dibagian config

<img width="1500" alt="DNS Client" src="https://github.com/user-attachments/assets/149a3a2d-e613-474f-baae-0c865a44832e">

jangan lupa juga untuk menambahkan **Static Routing ke 8.8.8.0** pada setiap nodes

### Testing
pada router gedung utama buka CLI dan jalankan command berikut untuk mengetahui apakah berhasil
```
sh ip nat translations
```
#### NAT di CLI Router Gedung Utama
<img width="1500" alt="Tes Ping" src="https://github.com/user-attachments/assets/5c0c1471-1d25-45a8-93b2-782098b6809a">

### Ping 8.8.8.8 / Keluar NAT
<img width="1500" alt="Tes Ping" src="https://github.com/user-attachments/assets/89c014b3-678b-4ffd-a088-7e8258825357">

## 7. Generic Routing Encapsulation (GRE Tunnel)
>Hubungkan Gedung Utama ke Cabang menggunakan GRE Tunnel. Konfigurasikan Generic Routing Encapsulation (GRE Tunnel) antara router di gedung utama dan router di cabang untuk membangun koneksi virtual yang aman. Pastikan kedua router dapat saling berkomunikasi melalui GRE Tunnel dan verifikasi konektivitasnya dengan melakukan ping antar router atau perangkat di masing-masing jaringan.
## Konfigurasi GRE Tunnel
### Command
```jsx
interface Tunnel0
 ip address `192.168.[...].[...]` (IP buat tunnel + Mask)
 tunnel source (Interface tunnel asal di router utama)
 tunnel destination `192.168.[...].[...]` (tujuan tunnel, IP A13)

ip route `192.168.[...].[...]` `255.255.[...].[...]` `192.168.[...].[...]` (subnet yang dituju + Mask + pake gateway tunnel)
```

### Router Gedung Utama
```jsx
interface Tunnel0
 ip address 192.168.2.1 255.255.255.252
 tunnel source Ethernet1/3
 tunnel destination 192.168.1.250 (IP A12 Fa0/0)

ip route 192.168.1.128 255.255.255.192 192.168.2.2 
```


<img width="1500" alt="Routing GRE Gedung Utama" src="https://github.com/user-attachments/assets/bae97b8c-4e13-4a87-9de3-a0f1c8b8189e">

### Router Cabang Luar Kota
```jsx
interface Tunnel0
 ip address 192.168.2.2 255.255.255.252
 tunnel source FastEthernet0/0
 tunnel destination 192.168.1.245 (IP A11 Eth1/3)

ip route 192.168.1.244 255.255.255.252 192.168.2.1
```
<img width="1500" alt="Routing GRE Cabang Luar Kota" src="https://github.com/user-attachments/assets/6403da1c-62b1-4de3-8ac4-b89f9188827f">

### Testing
coba dari router utama ping ke cabang lain dengan gateway tunnel pada cabang luar kota

<img width="1500" alt="Testing GRE Cab Gedung Utama" src="https://github.com/user-attachments/assets/9013cf9e-7b72-4796-a50a-31d7930a3968">

coba lagi sebaliknya dengan gateway tunnel pada router utama

<img width="1500" alt="Testing GRE Cab Luar Kota" src="https://github.com/user-attachments/assets/9479a5c9-be41-4a95-875d-4a2beea7634c">

