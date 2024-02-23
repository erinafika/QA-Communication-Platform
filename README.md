# Automation Test Rocket Chat

**Title**: Rocket Chat Testing\
**OverView**: Test yang dilakukan terdiri dari skrip end to end Regression test secara otomatis untuk semua fungsi dasar di https://www.rocket.chat, yang ditulis dalam Selenium webdriver dengan Python. Tujuan dari QA Regression adalah untuk memastikan bahwa seluruh sistem bekerja dengan sempurna setelah ada perubahan kode.

Skrip pengujian memungkinkan pengujian beberapa browser dengan semua kasus pengujian yang akan dijalankan pada sebagian besar browser populer: Chrome, Firefox, Safari, dan IE.\.
Proyek ini juga mendukung menjalankan pengujian Selenium Webdriver dengan Python di BrowserStack.\.
Laporan pengujian dapat dibuat dengan HTML dan Allure plugins.\

**Features**:

1. Masuk ke Rocket.chat dengan Nama Pengguna dan Kata Sandi
2. Buat Pengguna Baru
3. Buat DM Baru
4. Buat Saluran Baru
5. Menambahkan pengguna ke Saluran
6. Membuat Diskusi
7. Memposting Pesan di saluran Pribadi
8. Memposting Pesan di saluran Publik
9. Memposting emoji
10. Melakukan tindakan Favorite-Unfavorite di saluran
11. Melakukan tindakan Read-Unread Dibaca di saluran
12. Melakukan tindakan Hide-Show di saluran
13. Melakukan tindakan Leave-Join di saluran
14. Melakukan tindakan Favorite-Unfavorite dalam DM
15. Melakukan tindakan Read-Unread Dibaca di DM
16. Melakukan tindakan Hide-Show dalam DM
17. Menambahkan kutipan
18. Tambahkan Reaksi
19. Membalas di utas
20. Cari Pengguna
21. Cari Saluran Publik
22. Cari Saluran Pribadi
23. Melihat Mode Diperpanjang
24. Melihat Mode Sedang
25. Melihat Mode Ringkas
26. Keluar dari Rocket.chat

**Dependencies**

1. Download and Install Python 3.9 from the official link- [https://www.python.org/downloads/]
2. Periksa apakah python dan pip berhasil diinstal\
   `python --version`\
   `pip --version`
3. Set Environment Variable for Python.
4. Install selenium libraries\
   `pip install -U selenium`
5. Download PyCharm - community edition
   [https://www.jetbrains.com/pycharm/]
6. Download Chrome, Firefox and IE drivers.
   [https://www.selenium.dev/downloads/]

Pada Windows, buka unzip dan tempelkan driver di bawah folder Scripts di python
Pada Mac, buka jalur "/usr/local/bin" dan rekatkan driver yang sudah di-unzip.

7. Install Pytest: On terminal, run below command\
   `pip install pytest`
8. Install allure: \
   Windows: `scoop install allure`\
   Mac: `brew install allure`
9. Install html Report:\
   `pip install pytest-html`

10. Pycharm Installations - Go to Python Interpreter on pycharm and install below plugins:
    1. allure-pytest
    2. pytest-html
    3. browserstack-local
11. For Parallel Mode - run below command in terminal: \
    `pip install pytest-xdist`

    To execute tests:\
    `pytest filename.py -v -s -n 2` \
    (Give any value for n e.g n 2 will open two tabs simultaneously)

**Running the Project**\
 `git clone https://github.com/RocketChat/QA.Automation.git` \
 `cd QA.Automation`

**To run all the Test cases use below commands:**\
 1. `pytest Tests`\
 2. `pytest -v -s Tests`\
 3. `py.test -v -s Tests`

**To run a single Test case use below commands:**\
 1. `pytest Tests/filename.py`\
 2. `pytest -v -s Tests/filename.py`\
 3. `py.test -v -s Tests/filename.py`

**To generate html report in test execution use below command**\
 1. `Pytest -v -s —html = report.html filename.py`

**To generate allure report in test execution use below command**  
 1. `pytest -v -s --alluredir="<path of the folder>" Tests/filename.py`\
 Here path is : "./reports/allure_reports"

**View html reports in a browser**\
 Di pycharm, salin path report.html dan tempelkan di browser atau langsung buka file report.html
di pycharm dan klik ikon browser untuk melihat reports.

**View allure reports in a browser**\
 Copy the path allure_reports yang dihasilkan setelah eksekusi pengujian di pycharm.
Sekarang pergi ke terminal dan jalankan perintah di bawah ini:\
 `allure serve <path of the folder>`

**Browserstack Testing**\
 Ikuti dokumentasi Browserstack di sini: [https://www.browserstack.com/docs/]
