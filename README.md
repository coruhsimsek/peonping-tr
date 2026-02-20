# TR Ses Paketi

Turk pop kulturunden ikonik repliklerle Claude Code'u seslendir. [peon-ping](https://github.com/nicobailon/peon-ping) eklentisi icin Turkce ses paketi.

98 ses efekti. 4 efsane kaynak. 21 olay kategorisi.

## Kaynaklar

| Kaynak | Tur |
|--------|-----|
| **Recep Ivedik** | Sinema |
| **G.O.R.A.** | Sinema |
| **Deep Turkish Web** | YouTube |
| **Akasya Duragi** | Dizi |

## Olay Eslesmeleri

| Olay | Ornek Replik |
|------|-------------|
| `session.start` | *"Merhaba Abi"* - Arif Isik (G.O.R.A.) |
| `task.acknowledge` | *"Seni Sectim Cunku Sen Farklisin"* - G.O.R.A. |
| `task.complete` | *"Helal Olsun Ulan"* - Recep Ivedik |
| `task.error` | *"Vaa Dolandirildin Lan Vaa"* - Deep Turkish Web |
| `input.required` | *"Nedir Problem Gardas"* - Recep Ivedik |
| `resource.limit` | *"Sen Benim Degerli Zamanimi Nasil Calarsun Hadsiz"* - DTW |
| `user.spam` | *"Konusma Lan"* - Recep Ivedik |
| `tool.bash` | *"Say Lan"* - Recep Ivedik |
| `tool.bash.success` | *"Ne Ka Guzel Ne Ka Guzel"* - Osman Aga |
| `tool.edit` | *"Geri Bas, Geri Bas"* - Recep Ivedik |
| `tool.edit.success` | *"Sariyo"* - Deep Turkish Web |
| `tool.write` | *"Kopernik Pizzasi"* - Recep Ivedik |
| `tool.write.success` | *"Fikir Guzel, Mekan Guzel, Ama Yemezler"* - G.O.R.A. |
| `tool.read` | *"Sende Sinsilik Var"* - Recep Ivedik |
| `tool.grep` | *"Asla Tibbi Sorgulama"* - Deep Turkish Web |
| `tool.glob` | *"Saydin Mi Lan"* - Recep Ivedik |
| `tool.webfetch` | *"Taksi Lazimdir Agabey"* - Akasya Duragi |
| `tool.websearch` | *"Napiyorsunuz Lan Kader Mahkumlari"* - DTW |
| `tool.task` | *"Aksama Gures Mi Var Lee"* - Recep Ivedik |
| `tool.subagent.stop` | *"Ne Olmesi Kardesim Bayilmisim"* - DTW |
| `tool.task.done` | *"Gulush Bohohoytt"* - Recep Ivedik |

## Kurulum

```bash
# peon-ping packs klasorune kopyala
cp -r . ~/.claude/hooks/peon-ping/packs/tr-ses-paketi
```

Veya `openpeon.json` dosyasini peon-ping ayarlarindan aktif pakete ekleyin.

## Format

[OpenPeon (CESP 1.0)](https://github.com/nicobailon/peon-ping) formatini kullanir. `openpeon.json` manifest dosyasi tum ses eslemelerini icerir.

## Lisans

CC-BY-NC-4.0

Ses klipleri ilgili yapimlara aittir ve egitim/eglence amacli kullanilmaktadir.
