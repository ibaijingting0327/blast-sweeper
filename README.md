# ⚡ Blast Asset Sweeper

一个 **100% 纯前端、零私钥、单文件开源** 的 Blast 链遗留资产批量查询与一键归集工具。

针对多钱包/指纹浏览器用户（如 MetaMask / AdsPower），无需导出私钥，即可：
1. **批量查询任意数量钱包地址** 在 Blast 主网上的遗留余额（`ETH`、`WETH`、`USDB`、`VUSDB`、`BLAST` 等），一键过滤空钱包并导出 CSV 报表。
2. **连接浏览器钱包自动加入监控列表**，实时检测当前账户余额与其它 ERC-20 代币（自动过滤钓鱼广告代币）。
3. **一键归集资产到主地址**：
   - 支持一键赎回 `VUSDB` (ERC-4626) 为 `USDB`
   - 一键转出全部 `USDB` / `WETH` / `BLAST`
   - 一键将 `WETH` 解包装（Unwrap）为原生 `ETH`
   - 自动预留极少量 L2 安全 Gas Buffer (`0.00003 ETH`)，一键清空剩余原生 `ETH`

## 🔒 安全说明
- **零外部依赖、零后端**：整个工具仅由单个静态 HTML 文件 (`index.html`) 构成，无任何第三方 JS 库，代码完全透明可审计。
- **不接触私钥**：所有交易均通过浏览器插件钱包（`window.ethereum` / EIP-6963）弹窗签名确认。
- **本地存储**：输入的查询地址与收款主地址仅保存在你本地浏览器的 `localStorage` 中，绝不上传任何服务器。

## 🚀 使用方法

### 方式一：通过 GitHub Pages 在线打开（推荐，支持所有指纹浏览器）
直接访问本仓库开启 GitHub Pages 后的地址即可使用。

### 方式二：本地运行
```bash
git clone https://github.com/ibaijingting0327/blast-sweeper.git
cd blast-asset-sweeper
python3 -m http.server 8899
```
然后在浏览器打开 `http://localhost:8899` 即可。

## 📄 License
MIT License
