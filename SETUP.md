# Olist Setup

Bu proje için Olist veri seti ve Python import yapısı hazırlanmıştır.

## Dataset

Olist veri setindeki 9 CSV dosyası aşağıdaki klasöre yerleştirilmiştir:

```text
~/.workintech/olist/data/csv

```

CSV dosyalarının sayısı kontrol edilmiştir:

```powershell
(Get-ChildItem "$HOME\.workintech\olist\data\csv" -Filter *.csv).Count
```

Beklenen sonuç:
```text
9
```

## PYTHONPATH

Proje ana dizini kullanıcı seviyesinde `PYTHONPATH` olarak tanımlanmıştır.

Windows PowerShell:

```powershell
[Environment]::SetEnvironmentVariable("PYTHONPATH", (Get-Location).Path, "User")
```

Yeni terminal oturumunda aşağıdaki komut ile kontrol edilmiştir:

```powershell
$env:PYTHONPATH
```

## Import Test

IPython içerisinde aşağıdaki test uygulanmıştır:

```python
from olist.data import Olist
Olist().ping()
```

Beklenen ve alınan sonuç:

```text
pong
```

Kurulum başarıyla tamamlanmıştır.
