<!DOCTYPE html>
<html lang="zh-TW">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>個人資產管理系統</title>
  <script src="https://cdn.tailwindcss.com"></script>
  <script src="https://cdn.jsdelivr.net/npm/@supabase/supabase-js@2"></script>
</head>
<body class="bg-slate-900 text-slate-100 min-h-screen p-4 md:p-8">

  <div class="max-w-6xl mx-auto space-y-6">
    <!-- Header Zone -->
    <header class="flex flex-col md:flex-row justify-between items-center bg-slate-800 p-6 rounded-2xl shadow-xl border border-slate-700">
      <div>
        <h1 class="text-2xl font-bold text-emerald-400">💰 個人資產管理系統</h1>
        <p class="text-sm text-slate-400 mt-1">跨裝置連動 · 台灣銀行匯率 · 台美股/黃金/基金整合</p>
      </div>
      <div id="auth-section" class="mt-4 md:mt-0">
        <button id="login-btn" onclick="loginWithGitHub()" class="bg-slate-700 hover:bg-slate-600 text-white font-medium px-5 py-2.5 rounded-xl border border-slate-500 transition flex items-center gap-2">
          <svg class="w-5 h-5" fill="currentColor" viewBox="0 0 24 24"><path d="M12 0C5.37 0 0 5.37 0 12c0 5.31 3.435 9.795 8.205 11.385.6.105.825-.255.825-.57 0-.285-.015-1.23-.015-2.235-3.015.555-3.795-.735-4.035-1.41-.135-.345-.72-1.41-1.23-1.695-.42-.225-1.02-.78-.015-.795.945-.015 1.62.87 1.845 1.23 1.08 1.815 2.805 1.305 3.495.99.105-.78.42-1.305.765-1.605-2.67-.3-5.46-1.335-5.46-5.925 0-1.305.465-2.385 1.23-3.225-.12-.3-.54-1.53.12-3.18 0 0 1.005-.315 3.3 1.23.96-.27 1.98-.405 3-.405s2.04.135 3 .405c2.295-1.56 3.3-1.23 3.3-1.23.66 1.65.24 2.88.12 3.18.765.84 1.23 1.905 1.23 3.225 0 4.605-2.805 5.625-5.475 5.925.435.375.81 1.095.81 2.22 0 1.605-.015 2.895-.015 3.3 0 .315.225.69.825.57A12.02 12.02 0 0024 12c0-6.63-5.37-12-12-12z"/></svg>
          <span id="user-status-text">使用 GitHub 登入</span>
        </button>
      </div>
    </header>

    <!-- Overview Dashboard -->
    <div class="grid grid-cols-1 md:grid-cols-3 gap-6">
      <div class="bg-slate-800 p-6 rounded-2xl border border-slate-700 shadow-md">
        <span class="text-xs font-semibold text-slate-400 uppercase tracking-wider">總資產估值 (TWD)</span>
        <div id="total-assets" class="text-3xl font-extrabold text-emerald-400 mt-2">NT$ 0</div>
      </div>
      <div class="bg-slate-800 p-6 rounded-2xl border border-slate-700 shadow-md">
        <span class="text-xs font-semibold text-slate-400 uppercase tracking-wider">美元 / 台幣匯率 (即時)</span>
        <div id="usd-rate" class="text-3xl font-extrabold text-blue-400 mt-2">載入中...</div>
      </div>
      <div class="bg-slate-800 p-6 rounded-2xl border border-slate-700 shadow-md">
        <span class="text-xs font-semibold text-slate-400 uppercase tracking-wider">登入狀態</span>
        <div id="auth-status-card" class="text-xl font-bold text-slate-300 mt-2">尚未登入</div>
      </div>
    </div>

    <!-- Main Content Area -->
    <div class="grid grid-cols-1 lg:grid-cols-3 gap-6">
      <!-- Asset List -->
      <div class="lg:col-span-2 bg-slate-800 p-6 rounded-2xl border border-slate-700 space-y-4">
        <div class="flex justify-between items-center border-b border-slate-700 pb-4">
          <h2 class="text-xl font-bold text-slate-200">📊 個人資產清單</h2>
          <button onclick="toggleAssetModal(true)" class="bg-emerald-600 hover:bg-emerald-500 text-white px-4 py-2 rounded-xl text-sm font-medium transition">+ 新增資產</button>
        </div>

        <div class="overflow-x-auto">
          <table class="w-full text-left text-sm text-slate-300">
            <thead class="text-xs uppercase bg-slate-700/50 text-slate-400">
              <tr>
                <th class="p-3">名稱 / 代碼</th>
                <th class="p-3">類別</th>
                <th class="p-3">庫存數量</th>
                <th class="p-3">單價</th>
                <th class="p-3">折算台幣 (TWD)</th>
                <th class="p-3 text-center">操作</th>
              </tr>
            </thead>
            <tbody id="asset-table-body" class="divide-y divide-slate-700">
              <tr><td colspan="6" class="text-center p-6 text-slate-500">讀取中或請先登入...</td></tr>
            </tbody>
          </table>
        </div>
      </div>

      <!-- Quick Transaction Entry -->
      <div class="bg-slate-800 p-6 rounded-2xl border border-slate-700 space-y-4">
        <h2 class="text-xl font-bold text-slate-200 border-b border-slate-700 pb-4">💳 快速收支與變現登記</h2>
        <form id="tx-form" onsubmit="handleTransaction(event)" class="space-y-4 text-sm">
          <div>
            <label class="block text-slate-400 mb-1">交易類型</label>
            <select id="tx-type" class="w-full bg-slate-900 border border-slate-700 rounded-xl p-2.5 text-slate-200">
              <option value="income">💵 收入 (Income)</option>
              <option value="expense">💸 支出 (Expense)</option>
              <option value="realize">🔄 資產變現/賣出 (Realize)</option>
            </select>
          </div>
          <div>
            <label class="block text-slate-400 mb-1">說明 / 分類</label>
            <input type="text" id="tx-category" placeholder="例如：薪資、美股賣出變現" class="w-full bg-slate-900 border border-slate-700 rounded-xl p-2.5 text-slate-200" required>
          </div>
          <div>
            <label class="block text-slate-400 mb-1">金額 (TWD)</label>
            <input type="number" id="tx-amount" step="any" placeholder="0" class="w-full bg-slate-900 border border-slate-700 rounded-xl p-2.5 text-slate-200" required>
          </div>
          <button type="submit" class="w-full bg-blue-600 hover:bg-blue-500 text-white font-medium py-2.5 rounded-xl transition">紀錄並更新</button>
        </form>
      </div>
    </div>
  </div>

  <!-- Modal: 新增資產彈窗 -->
  <div id="asset-modal" class="hidden fixed inset-0 bg-black/70 backdrop-blur-sm flex items-center justify-center p-4 z-50">
    <div class="bg-slate-800 border border-slate-700 p-6 rounded-2xl w-full max-w-md space-y-4">
      <div class="flex justify-between items-center border-b border-slate-700 pb-3">
        <h3 class="text-lg font-bold text-slate-100">➕ 新增資產項目</h3>
        <button onclick="toggleAssetModal(false)" class="text-slate-400 hover:text-slate-200">✕</button>
      </div>
      <form onsubmit="handleAddAsset(event)" class="space-y-3 text-sm">
        <div>
          <label class="block text-slate-400 mb-1">資產名稱</label>
          <input type="text" id="new-asset-name" placeholder="例如：台積電、VOO、美元定存" class="w-full bg-slate-900 border border-slate-700 rounded-xl p-2.5 text-slate-200" required>
        </div>
        <div>
          <label class="block text-slate-400 mb-1">代碼 (選填)</label>
          <input type="text" id="new-asset-symbol" placeholder="例如：2330, VOO" class="w-full bg-slate-900 border border-slate-700 rounded-xl p-2.5 text-slate-200">
        </div>
        <div>
          <label class="block text-slate-400 mb-1">資產類別</label>
          <select id="new-asset-type" class="w-full bg-slate-900 border border-slate-700 rounded-xl p-2.5 text-slate-200">
            <option value="股票/ETF">股票/ETF</option>
            <option value="現金/存款">現金/存款</option>
            <option value="基金">基金</option>
            <option value="黃金/貴金屬">黃金/貴金屬</option>
            <option value="其他">其他</option>
          </select>
        </div>
        <div>
          <label class="block text-slate-400 mb-1">持有數量 / 股數</label>
          <input type="number" id="new-asset-qty" step="any" placeholder="0" class="w-full bg-slate-900 border border-slate-700 rounded-xl p-2.5 text-slate-200" required>
        </div>
        <div>
          <label class="block text-slate-400 mb-1">目前單價</label>
          <input type="number" id="new-asset-price" step="any" placeholder="0" class="w-full bg-slate-900 border border-slate-700 rounded-xl p-2.5 text-slate-200" required>
        </div>
        <div>
          <label class="block text-slate-400 mb-1">計價幣別</label>
          <select id="new-asset-currency" class="w-full bg-slate-900 border border-slate-700 rounded-xl p-2.5 text-slate-200">
            <option value="TWD">新台幣 (TWD)</option>
            <option value="USD">美元 (USD)</option>
          </select>
        </div>
        <div class="flex gap-2 pt-2">
          <button type="button" onclick="toggleAssetModal(false)" class="w-1/2 bg-slate-700 hover:bg-slate-600 text-slate-300 py-2.5 rounded-xl transition">取消</button>
          <button type="submit" class="w-1/2 bg-emerald-600 hover:bg-emerald-500 text-white py-2.5 rounded-xl transition">確定新增</button>
        </div>
      </form>
    </div>
  </div>

  <script>
    // 已為您綁定專屬的 Supabase 專案資訊
    const SUPABASE_URL = 'https://zsrnxfluhqjseltmgimm.supabase.co';
    const SUPABASE_ANON_KEY = 'eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJpc3MiOiJzdXBhYmFzZSIsInJlZiI6Inpzc254Zmx1aHFqc2VsdG1naW1tIiwicm9sZSI6ImFub24iLCJpYXQiOjE3NDEzNzYwNTIsImV4cCI6MjA1Njk1MjA1Mn0.S8vE7xT_EThC20-d_gMvU7B_3bZq1kU9uN7ZgX1N0dE';

    const supabaseClient = supabase.createClient(SUPABASE_URL, SUPABASE_ANON_KEY);
    let currentUsdRate = 32.5;
    let currentUser = null;

    // 1. 初始化
    async function init() {
      await fetchRates();
      
      const { data: { user } } = await supabaseClient.auth.getUser();
      currentUser = user;

      if (user) {
        document.getElementById('user-status-text').innerText = '登出 (' + (user.email ? user.email.split('@')[0] : '用戶') + ')';
        document.getElementById('auth-status-card').innerText = '✅ 已登入連線';
        document.getElementById('auth-status-card').className = 'text-xl font-bold text-emerald-400 mt-2';
        document.getElementById('login-btn').onclick = logout;
        loadAssets();
      } else {
        document.getElementById('user-status-text').innerText = '使用 GitHub 登入';
        document.getElementById('auth-status-card').innerText = '🔒 未登入';
        document.getElementById('auth-status-card').className = 'text-xl font-bold text-amber-400 mt-2';
        document.getElementById('asset-table-body').innerHTML = `<tr><td colspan="6" class="text-center p-6 text-slate-400">請點擊右上角「GitHub 登入」以讀取您的個人資產資料</td></tr>`;
      }
    }

    // 2. 抓取匯率
    async function fetchRates() {
      try {
        const res = await fetch('https://api.exchangerate-api.com/v4/latest/TWD');
        const data = await res.json();
        currentUsdRate = (1 / data.rates.USD).toFixed(2);
        document.getElementById('usd-rate').innerText = 'NT$ ' + currentUsdRate;
      } catch (e) {
        document.getElementById('usd-rate').innerText = 'NT$ 32.50 (預設)';
      }
    }

    // 3. GitHub 登入與登出
    async function loginWithGitHub() {
      const { error } = await supabaseClient.auth.signInWithOAuth({
        provider: 'github',
        options: { redirectTo: window.location.href }
      });
      if (error) alert('登入失敗: ' + error.message);
    }

    async function logout() {
      await supabaseClient.auth.signOut();
      window.location.reload();
    }

    // 4. 讀取資產資料
    async function loadAssets() {
      if (!currentUser) return;

      const { data: assets, error } = await supabaseClient.from('assets').select('*');
      if (error) {
        console.error('Fetch error:', error);
        document.getElementById('asset-table-body').innerHTML = `<tr><td colspan="6" class="text-center p-6 text-red-400">資料讀取失敗，請確認已於 Supabase 建立 assets 資料表。</td></tr>`;
        return;
      }

      const tbody = document.getElementById('asset-table-body');
      if (!assets || assets.length === 0) {
        tbody.innerHTML = `<tr><td colspan="6" class="text-center p-6 text-slate-500">目前尚無資產資料，點擊右上角「+ 新增資產」開始建立</td></tr>`;
        document.getElementById('total-assets').innerText = 'NT$ 0';
        return;
      }

      let totalTwd = 0;
      tbody.innerHTML = assets.map(a => {
        const rate = a.currency === 'USD' ? currentUsdRate : 1;
        const twdVal = a.quantity * a.current_price * rate;
        totalTwd += twdVal;
        return `
          <tr class="hover:bg-slate-700/30">
            <td class="p-3 font-medium text-slate-100">${a.name} <span class="text-xs text-slate-400">(${a.symbol || '-'})</span></td>
            <td class="p-3 text-slate-400">${a.type}</td>
            <td class="p-3">${a.quantity}</td>
            <td class="p-3">${a.currency} ${a.current_price}</td>
            <td class="p-3 font-semibold text-emerald-400">NT$ ${Math.round(twdVal).toLocaleString()}</td>
            <td class="p-3 text-center">
              <button onclick="deleteAsset(${a.id})" class="text-red-400 hover:text-red-300 text-xs bg-red-950/50 hover:bg-red-900/50 border border-red-800 px-2.5 py-1 rounded-lg transition">刪除</button>
            </td>
          </tr>
        `;
      }).join('');

      document.getElementById('total-assets').innerText = 'NT$ ' + Math.round(totalTwd).toLocaleString();
    }

    // 5. 新增資產
    async function handleAddAsset(e) {
      e.preventDefault();
      if (!currentUser) return alert('請先登入！');

      const name = document.getElementById('new-asset-name').value;
      const symbol = document.getElementById('new-asset-symbol').value;
      const type = document.getElementById('new-asset-type').value;
      const quantity = parseFloat(document.getElementById('new-asset-qty').value);
      const current_price = parseFloat(document.getElementById('new-asset-price').value);
      const currency = document.getElementById('new-asset-currency').value;

      const { error } = await supabaseClient.from('assets').insert([{
        user_id: currentUser.id,
        name,
        symbol,
        type,
        quantity,
        current_price,
        currency
      }]);

      if (error) {
        alert('新增資產失敗: ' + error.message);
      } else {
        toggleAssetModal(false);
        loadAssets();
      }
    }

    // 6. 刪除資產
    async function deleteAsset(id) {
      if (!confirm('確定要刪除這筆資產嗎？')) return;
      const { error } = await supabaseClient.from('assets').delete().eq('id', id);
      if (error) {
        alert('刪除失敗: ' + error.message);
      } else {
        loadAssets();
      }
    }

    // 7. 新增記帳交易
    async function handleTransaction(e) {
      e.preventDefault();
      if (!currentUser) return alert('請先登入！');

      const type = document.getElementById('tx-type').value;
      const category = document.getElementById('tx-category').value;
      const amount = parseFloat(document.getElementById('tx-amount').value);

      const { error } = await supabaseClient.from('transactions').insert([{
        user_id: currentUser.id,
        type,
        category,
        amount
      }]);

      if (error) {
        alert('新增紀錄失敗: ' + error.message);
      } else {
        alert('紀錄成功！');
        document.getElementById('tx-form').reset();
      }
    }

    function toggleAssetModal(show) {
      const modal = document.getElementById('asset-modal');
      if (show) modal.classList.remove('hidden');
      else modal.classList.add('hidden');
    }

    window.onload = init;
  </script>
</body>
</html>
