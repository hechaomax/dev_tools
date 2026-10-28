# datasets

## insta150k.zip

InSTA 150k v3 —— 带 Playwright 调用序列的网页任务数据集，压缩包内为两个 parquet 分片。

| 项 | 值 |
|---|---|
| 文件大小 | 54,408,223 字节 (51.9 MiB) |
| SHA256 | `03bba30ca6212931d3bab89a07df2509a3e22f158ebe38493c33f91d95e8d1b0` |
| 存储方式 | Git LFS（`datasets/*.zip`） |
| 来源 | https://huggingface.co/datasets/data-for-agents/insta-150k-v3 |
| 许可 | MIT |

### 内容

| 分片 | 行数 | 大小 |
|---|---|---|
| `data/train-00000-of-00001.parquet` | 143,508 | 57.1 MB |
| `data/test-00000-of-00001.parquet` | 2,933 | 1.13 MB |

字段共 4 个，**不含截图与 DOM**：

- `website` —— 域名，例如 `wikipedia.org`
- `instruction` —— 任务描述
- `steps` —— `list[str]`，每个元素是一条 Playwright API 调用串
- `criteria` —— `list[str]`，判定任务是否完成的标准

### 获取

```bash
git lfs install
git clone https://github.com/hechaomax/dev_tools.git
git lfs pull
```

不想装 LFS 时，可在 GitHub 文件页面点击 Download 直接取到实体文件。

### 校验

```bash
sha256sum insta150k.zip
# 03bba30ca6212931d3bab89a07df2509a3e22f158ebe38493c33f91d95e8d1b0
```
