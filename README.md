# ArgoJurno
```html
<!-- ... existing code ... -->
          <!-- Tindakan Reset & Cadangan Database -->
          <div class="bg-white rounded-3xl p-5 border border-slate-200 shadow-sm space-y-3">
            <h3 class="text-sm font-black text-slate-800 border-b pb-2">Cadangan Database & Setelan Standar</h3>
            <p class="text-xs text-slate-500">Gunakan tombol di bawah ini untuk mengamankan data atau mengembalikan sistem ke kondisi awal (603 ekor ayam & 10 anggota awal).</p>
            <div class="flex flex-wrap gap-2">
              <button onclick="downloadDatabaseJson()" class="px-4 py-2 bg-blue-600 hover:bg-blue-700 text-white font-bold rounded-xl text-xs transition">
                <i class="fas fa-download mr-1"></i> Unduh Cadangan JSON
              </button>
              <button onclick="resetToFactoryDefault()" class="px-4 py-2 bg-rose-600 hover:bg-rose-700 text-white font-bold rounded-xl text-xs transition">
                <i class="fas fa-rotate-left mr-1"></i> Kembalikan Pengaturan Awal
              </button>
            </div>
          </div>

          <!-- PANDUAN & TOOLS PUBLIKASI HOSTING GRATIS (ONLINE URL) -->
          <div class="bg-gradient-to-br from-emerald-900 to-brand-darkgreen text-white rounded-3xl p-5 shadow-lg border border-emerald-700 space-y-4">
            <div class="flex flex-col sm:flex-row sm:items-center sm:justify-between gap-2 border-b border-emerald-700/60 pb-3">
              <div>
                <span class="inline-block px-2.5 py-0.5 rounded-full bg-amber-400 text-slate-950 font-black text-[10px] uppercase mb-1">Online & Free Hosting</span>
                <h3 class="text-base font-black text-white">Publikasikan Website ArgoJurno Farm (100% Gratis)</h3>
                <p class="text-xs text-emerald-200">Aplikasi ini adalah file mandiri (Single-File HTML). Anda dapat mempublikasikannya secara online tanpa biaya selamanya.</p>
              </div>
              <button onclick="downloadCurrentHtmlFile()" class="px-4 py-2 bg-amber-400 hover:bg-amber-500 text-slate-950 font-bold rounded-xl text-xs shadow transition flex items-center space-x-1.5 shrink-0">
                <i class="fas fa-file-arrow-down"></i>
                <span>Unduh File index.html Siap Publish</span>
              </button>
            </div>

            <div class="grid grid-cols-1 md:grid-cols-3 gap-3 text-xs">
              <!-- Opsi 1: Netlify Drop -->
              <div class="bg-emerald-950/60 p-4 rounded-2xl border border-emerald-800 space-y-2">
                <div class="flex items-center space-x-2 text-amber-300 font-bold">
                  <i class="fas fa-cloud-arrow-up text-base"></i>
                  <span>1. Netlify Drop (Paling Mudah)</span>
                </div>
                <p class="text-slate-300 text-[11px] leading-relaxed">
                  1. Masukkan file <code>index.html</code> ke dalam satu folder bernama <code>argojurno</code>.<br>
                  2. Buka <strong class="text-white underline">app.netlify.com/drop</strong>.<br>
                  3. Drag & drop folder tersebut. Website langsung online dalam 10 detik dan memiliki link resmi HTTPS gratis!
                </p>
                <a href="https://app.netlify.com/drop" target="_blank" rel="noopener noreferrer" class="inline-block mt-1 text-[11px] px-3 py-1 bg-emerald-800 hover:bg-emerald-700 text-amber-300 font-bold rounded-lg transition">
                  Buka Netlify Drop <i class="fas fa-arrow-up-right-from-square ml-1"></i>
                </a>
              </div>

              <!-- Opsi 2: Vercel -->
              <div class="bg-emerald-950/60 p-4 rounded-2xl border border-emerald-800 space-y-2">
                <div class="flex items-center space-x-2 text-amber-300 font-bold">
                  <i class="fas fa-triangle-circle-square text-base"></i>
                  <span>2. Vercel Hosting</span>
                </div>
                <p class="text-slate-300 text-[11px] leading-relaxed">
                  1. Buka <strong class="text-white underline">vercel.com</strong> & daftar gratis.<br>
                  2. Upload folder atau tautkan via GitHub repository.<br>
                  3. Dapatkan domain gratis berkecepatan tinggi, contoh: <code>argojurno-farm.vercel.app</code>.
                </p>
                <a href="https://vercel.com" target="_blank" rel="noopener noreferrer" class="inline-block mt-1 text-[11px] px-3 py-1 bg-emerald-800 hover:bg-emerald-700 text-amber-300 font-bold rounded-lg transition">
                  Buka Vercel <i class="fas fa-arrow-up-right-from-square ml-1"></i>
                </a>
              </div>

              <!-- Opsi 3: GitHub Pages -->
              <div class="bg-emerald-950/60 p-4 rounded-2xl border border-emerald-800 space-y-2">
                <div class="flex items-center space-x-2 text-amber-300 font-bold">
                  <i class="fab fa-github text-base"></i>
                  <span>3. GitHub Pages</span>
                </div>
                <p class="text-slate-300 text-[11px] leading-relaxed">
                  1. Buat repository publik di <strong class="text-white underline">github.com</strong>.<br>
                  2. Upload berkas <code>index.html</code>.<br>
                  3. Buka menu <em>Settings &rarr; Pages</em> lalu aktifkan. Tautan Anda: <code>username.github.io/argojurno</code>.
                </p>
                <a href="https://github.com" target="_blank" rel="noopener noreferrer" class="inline-block mt-1 text-[11px] px-3 py-1 bg-emerald-800 hover:bg-emerald-700 text-amber-300 font-bold rounded-lg transition">
                  Buka GitHub <i class="fas fa-arrow-up-right-from-square ml-1"></i>
                </a>
              </div>
            </div>

            <div class="p-3 bg-emerald-950/80 rounded-2xl border border-amber-400/30 flex items-center justify-between text-xs">
              <span class="text-amber-200">
                <i class="fas fa-link mr-1.5"></i> Tautan aktif website Anda saat ini: <strong class="text-white font-mono break-all" id="current-url-display"></strong>
              </span>
              <button onclick="shareAppUrl()" class="px-3 py-1 bg-amber-400 hover:bg-amber-500 text-slate-950 font-bold rounded-lg transition shrink-0 ml-2">
                Salin & Bagikan URL
              </button>
            </div>
          </div>

          <!-- Audit Log Lengkap (Before & After) -->
<!-- ... existing code ... -->
    /* =========================================================================
       SHARE URL & PWA INSTALL HANDLER
       ========================================================================= */
    function shareAppUrl() {
      const url = window.location.href;
      if (navigator.share) {
        navigator.share({
          title: "ArgoJurno Farm App",
          text: "Sistem Manajemen Peternakan Ayam Petelur Kelompok Usaha ArgoJurno Farm",
          url: url
        }).catch(() => copyToClipboard(url));
      } else {
        copyToClipboard(url);
      }
    }

    function copyToClipboard(text) {
      // Gunakan execCommand fallback jika running di iframe sandbox
      try {
        const tempInput = document.createElement("input");
        tempInput.style.position = "absolute";
        tempInput.style.left = "-9999px";
        tempInput.value = text;
        document.body.appendChild(tempInput);
        tempInput.select();
        document.execCommand("copy");
        document.body.removeChild(tempInput);
        showToast("Tautan web berhasil disalin ke clipboard!", "success");
      } catch (err) {
        if (navigator.clipboard && navigator.clipboard.writeText) {
          navigator.clipboard.writeText(text).then(() => {
            showToast("Tautan web berhasil disalin ke clipboard!", "success");
          }).catch(() => {
            showToast("Gagal menyalin tautan: " + text, "warning");
          });
        } else {
          showToast("Alamat URL: " + text, "info");
        }
      }
    }

    function downloadCurrentHtmlFile() {
      const htmlContent = "<!DOCTYPE html>\n" + document.documentElement.outerHTML;
      const blob = new Blob([htmlContent], { type: "text/html;charset=utf-8" });
      const downloadAnchor = document.createElement('a');
      downloadAnchor.href = URL.createObjectURL(blob);
      downloadAnchor.download = "index.html";
      document.body.appendChild(downloadAnchor);
      downloadAnchor.click();
      downloadAnchor.remove();
      showToast("File 'index.html' siap hosting berhasil diunduh!", "success");
    }

    function promptInstallPwa() {
<!-- ... existing code ... -->
    // Inisialisasi Aplikasi Saat Halaman Selesai Dimuat
    window.addEventListener('DOMContentLoaded', () => {
      loadAppData();
      checkCurrentSession();
      updateUserDisplay();
      renderCurrentMenu();
      runOpeningLoading();

      // Perbarui tampilan URL terkini jika ada
      const urlEl = document.getElementById('current-url-display');
      if (urlEl) urlEl.textContent = window.location.href;
    });
  </script>
</body>
</html>
```


