# TR Ses Paketi

Türk pop kültüründen ikonik repliklerle Claude Code'u seslendir. [peon-ping](https://github.com/nicobailon/peon-ping) eklentisi için Türkçe ses paketi.

**98 ses efekti. 4 efsane kaynak. 21 olay kategorisi.**

## Kaynaklar

| Kaynak | Tür |
|--------|-----|
| **Recep İvedik** | Sinema |
| **G.O.R.A.** | Sinema |
| **Deep Turkish Web** | YouTube |
| **Akasya Durağı** | Dizi |

## Kurulum / Installation

> **Ön koşul:** [peon-ping](https://github.com/nicobailon/peon-ping) kurulu olmalı.
>
> **Prerequisite:** [peon-ping](https://github.com/nicobailon/peon-ping) must be installed first.

### macOS / Linux

```bash
# 1. Repoyu klonla / Clone the repo
git clone https://github.com/coruhsimsek/peonping-tr.git

# 2. Packs klasörüne kopyala / Copy to packs directory
cp -r peonping-tr ~/.claude/hooks/peon-ping/packs/tr-ses-paketi

# 3. Aktif pack olarak ayarla / Set as active pack
#    Seçenek A: Claude Code içinden
#    Option A: From within Claude Code
#    /peon-ping-use tr-ses-paketi
#
#    Seçenek B: Terminal komutu ile
#    Option B: Via terminal command
bash ~/.claude/hooks/peon-ping/peon.sh --pack tr-ses-paketi
```

### Windows

```powershell
# 1. Repoyu klonla / Clone the repo
git clone https://github.com/coruhsimsek/peonping-tr.git

# 2. Packs klasörüne kopyala / Copy to packs directory
Copy-Item -Recurse peonping-tr "$env:USERPROFILE\.claude\hooks\peon-ping\packs\tr-ses-paketi"

# 3. Aktif pack olarak ayarla / Set as active pack
#    Seçenek A: Claude Code içinden
#    Option A: From within Claude Code
#    /peon-ping-use tr-ses-paketi
#
#    Seçenek B: Terminal komutu ile
#    Option B: Via terminal command
powershell -File "$env:USERPROFILE\.claude\hooks\peon-ping\peon.ps1" --pack tr-ses-paketi
```

### Windows Notu / Windows Note

Windows'ta ses dosyası adlarındaki Türkçe karakterler (İ, ş, ü, ö, ç, ğ) encoding sorunu yaratabilir. `peon.ps1` dosyasında manifest okuma satırında `-Encoding UTF8` parametresinin olduğundan emin olun:

On Windows, Turkish characters (İ, ş, ü, ö, ç, ğ) in sound filenames can cause encoding issues. Make sure the manifest reading line in `peon.ps1` includes `-Encoding UTF8`:

```powershell
# peon.ps1 içinde / inside peon.ps1 — manifest okuma satırı / manifest reading line
$manifest = Get-Content $manifestPath -Raw -Encoding UTF8 | ConvertFrom-Json
```

## Olay Eşleşmeleri / Event Mappings

| Olay | Örnek Replik |
|------|-------------|
| `session.start` | *"Merhaba Abi"* — Arif Işık (G.O.R.A.) |
| `task.acknowledge` | *"Seni Seçtim Çünkü Sen Farklısın"* — G.O.R.A. |
| `task.complete` | *"Helal Olsun Ulan"* — Recep İvedik |
| `task.error` | *"Vaa Dolandırıldım Lan Vaa"* — Deep Turkish Web |
| `input.required` | *"Nedir Problem Gardaş"* — Recep İvedik |
| `resource.limit` | *"Sen Benim Değerli Zamanımı Nasıl Çalarsın Hadsiz"* — DTW |
| `user.spam` | *"Konuşma Lan"* — Recep İvedik |
| `tool.bash` | *"Say Lan"* — Recep İvedik |
| `tool.bash.success` | *"Ne Ka Güzel Ne Ka Güzel"* — Osman Ağa |
| `tool.edit` | *"Geri Bas, Geri Bas"* — Recep İvedik |
| `tool.edit.success` | *"Sarıyo"* — Deep Turkish Web |
| `tool.write` | *"Kopernik Pizzası"* — Recep İvedik |
| `tool.write.success` | *"Fikir Güzel, Mekan Güzel, Ama Yemezler"* — G.O.R.A. |
| `tool.read` | *"Sende Sinsilik Var"* — Recep İvedik |
| `tool.grep` | *"Asla Tıbbı Sorgulama"* — Deep Turkish Web |
| `tool.glob` | *"Saydın Mı Lan"* — Recep İvedik |
| `tool.webfetch` | *"Taksi Lazımdır Ağabey"* — Akasya Durağı |
| `tool.websearch` | *"Napıyorsunuz Lan Kader Mahkumları"* — DTW |
| `tool.task` | *"Akşama Güreş Mi Var Lee"* — Recep İvedik |
| `tool.subagent.stop` | *"Ne Ölmesi Kardeşim Bayılmışım"* — DTW |
| `tool.task.done` | *"Gülüş Böhöhöyt"* — Recep İvedik |

## Format

[OpenPeon (CESP 1.0)](https://github.com/nicobailon/peon-ping) formatını kullanır. `openpeon.json` manifest dosyası tüm ses eşlemelerini içerir.

## Lisans

CC-BY-NC-4.0

Ses klipleri ilgili yapımlara aittir ve eğitim/eğlence amaçlı kullanılmaktadır.
