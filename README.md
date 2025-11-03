### Dokmentasi TA 2 PJK
#### Link Youtube:

#### Capture Pada Saat Gagal PING
<img width="856" height="426" alt="Screenshot 2025-11-02 201841" src="https://github.com/user-attachments/assets/89d746cc-952c-4ff2-a5a2-f41db3715a20" />
Ping tidak berhasil karena interface router (default gateway) belum dikonfigurasi, sehingga trafik Layer 3 belum dirutekan antar-subnet.
Ping dari PC-A ke PC-B gagal karena router belum dikonfigurasi untuk meneruskan (route) trafik antar-subnet.
Masing-masing PC berada pada subnet berbeda, dan karena router belum memiliki konfigurasi interface IP/default gateway yang aktif, paket ICMP berhenti di layer 2 (switch) tanpa bisa melewati router.


#### Capture Pada Saat Berhasil PING
<img width="865" height="669" alt="Screenshot 2025-11-02 202629" src="https://github.com/user-attachments/assets/da589e9e-8fcb-49a1-ae84-58dd7023213c" />
Ping berhasil karena router sudah merutekan trafik antar dua subnet dan switch 2960 secara default mengaktifkan interface yang terhubung ke perangkat aktif.
Setelah router dikonfigurasi, router mulai merutekan paket ICMP antar-subnet.
Hasilnya, ping dari PC-B ke PC-A berhasil karena router sudah berfungsi sebagai default gateway dan switch mengaktifkan port-port yang terhubung.

