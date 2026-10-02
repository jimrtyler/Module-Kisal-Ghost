# 👻 Moduul Kisal Ghost
**Kaɗe Ñamtinde Kisal Windows e Azure nder PowerShell**

> **Ñamtinde kisal noddirgal ko waawi waɗde e doole Windows e Azure.** Ghost waawi ardude golɗe ñamtinde nder PowerShell ɗe mbaawi haɗde kuutoragol kuutorɗe e purotagol ɗe njokkondiraama ngam ñaañude yeewtere yamirooje keewɗe.

## ⚠️ Jeertine Muhiime

**EƊEN NDI CEƊTINGOL**: Yejjit ceɗto Ghost nder doole alaa yamirooje araande hade ma fuɗɗii. Daaƴde kuutorɗe mbaawi waɗɗi golle ngenndiije alaa ɓesngu.

**ALAA LAACOL**: Sabu Ghost jokki e yeewtere yamirooje keewɗe, alaa kaɗe kisal haɗde fof yamirooje. Oo ko fedde e yamre kisal ɓurngal.

**GOLLE WAƊƊE**: Goɗɗe golle mbaawi waɗɗi no sisteem golli. Yejjit ɓeydito kala seetaaji hade ngonaa toppitde.

**ƁEYDAGOL JANNGINOOWO**: Nder doole yamirde, naamno jannginooɓe kisal ngam teeŋtinde seetaaji njogii e jaaɓɗe jamirgol maa.

## 📊 Nder Kisal

Bonɗe ransomware heɓii haa **$57 biyoŋ nder 2025**, njiylawu holliti wonde yamirooje keewɗe ɓurɗe kuutorɗe Windows pellital e geɗe moƴƴingol. Yeewtere yamirooje keewɗe ena waɗi:

- **90% golle ransomware** ena nana yamirde RDP
- **Ɓoyngol SMBv1** waɗɗi yamirooje no WannaCry e NotPetya
- **Makro fiilannde** ko yaltere yamirde malware woodnde
- **Yamirooje USB** ena jokkondira nettaaji air-gapped
- **Yamirde moƴƴingol PowerShell** ɓeydii ko tagi nder duuɓi ɗii

## 🛡️ Golle Kisal Ghost

Ghost ena waɗi **16 golle ñamtinde Windows** e **jokku kisal Azure**:

### Ñamtinde Endpoint Windows

| Golle | Daɓɓere | Miijo |
|----------|---------|----------------|
| `Set-RDP` | Jeyaa naatde desktop woote | Mbaawi waɗɗi jeyagol woote |
| `Set-SMBv1` | Jeyaa purotagol SMB kiiɗo | Ena sokli sisteem kiiɗɗo keewɗo |
| `Set-AutoRun` | Jeyaa AutoPlay/AutoRun | Mbaawi waɗɗi sabu kuutorɓe |
| `Set-USBStorage` | Haaɗtin kaɗe USB | Mbaawi waɗɗi kuutorɗe USB ɓesɗe |
| `Set-Macros` | Jeyaa tammitirgol makro Office | Mbaawi waɗɗi fiilannde ena makro |
| `Set-PSRemoting` | Jeyaa remoting PowerShell | Mbaawi waɗɗi jeyagol woote |
| `Set-WinRM` | Jeyaa Windows Remote Management | Mbaawi waɗɗi jeyagol woote |
| `Set-LLMNR` | Jeyaa purotagol innde yiɗde | Ko sabu daaƴde oo |
| `Set-NetBIOS` | Jeyaa NetBIOS dow TCP/IP | Mbaawi waɗɗi jaaynirɗe kiiɗɗe |
| `Set-AdminShares` | Jeyaa jeertine jeyɗinooɓe | Mbaawi waɗɗi naatde fiilde woote |
| `Set-Telemetry` | Jeyaa jamlude keɓe | Mbaawi waɗɗi jaabawol |
| `Set-GuestAccount` | Jeyaa konte seede | Ko sabu daaƴde oo |
| `Set-ICMP` | Jeyaa jaabiraaji ping | Mbaawi waɗɗi jaabawol network |
| `Set-RemoteAssistance` | Jeyaa Remote Assistance | Mbaawi waɗɗi golle ballal |
| `Set-NetworkDiscovery` | Jeyaa yiɗde network | Mbaawi waɗɗi njogoraade network |
| `Set-Firewall` | Jeyaa Windows Firewall | Ena huunde to kisal network |

### Kisal Azure Cloud

| Golle | Daɓɓere | Jaaɓɗe |
|----------|---------|--------------|
| `Set-AzureSecurityDefaults` | Huɓɓin kisal pellital Azure AD | Jaabondiral Microsoft Graph |
| `Set-AzureConditionalAccess` | Teelto daɓɓitaare naatde | Lisaŋs Azure AD P1/P2 |
| `Set-AzurePrivilegedUsers` | Njaaɗndi konte ena yamirooje | Jaabondiral Global Admin |

### Cuɓe Toppitde Enterprise

| Hono | Kuutorɗe | Jaaɓɗe |
|--------|----------|--------------|
| **Tammitaade Yaajɗe** | Ceɗtol, doole keɗɗe | Jamirooje admin koyngol |
| **Group Policy** | Doole domain | Admin domain, jeyagol GP |
| **Microsoft Intune** | Kaɗe cloud leyɗi | Lisaŋs Intune, Graph API |

## 🚀 Fuɗɗoode Yaawnde

### Njaaɗndu Kisal
```powershell
# Loowtin moduul Ghost
Invoke-WebRequest 'https://raw.githubusercontent.com/jimrtyler/Ghost/main/Ghost.ps1' -OutFile .\Ghost.ps1
Get-Content .\Ghost.ps1
. .\Ghost.ps1

# Ƴeew haalre kisal jooni
Get-Ghost
```

### Ñamtinde Pellital (Ceɗto Hade)
```powershell
# Ñamtinde ena sokli - ceɗto nder labo hade
Set-Ghost -SMBv1 -AutoRun -Macros

# Yejjit coppitte
Get-Ghost
```

### Toppitde Enterprise
```powershell
# Toppitde Group Policy (doole domain)
Set-Ghost -SMBv1 -AutoRun -GroupPolicy

# Toppitde Intune (kaɗe cloud leyɗi)
Set-Ghost -SMBv1 -RDP -USBStorage -Intune
```

## 📋 Njuɓɓudi Ngaañaangol

### Cuɓal 1: Aawtaade Yaajɗe (Ceɗtol)
```powershell
Invoke-WebRequest 'https://raw.githubusercontent.com/jimrtyler/Ghost/main/Ghost.ps1' -OutFile .\Ghost.ps1
Get-Content .\Ghost.ps1
. .\Ghost.ps1
```

### Cuɓal 2: Ngaañaangol Moduul
```powershell
# Aaf ummaade e PowerShell Gallery (so tawii)
Install-Module Ghost -Scope CurrentUser
Import-Module Ghost
```

### Cuɓal 3: Toppitde Enterprise
```powershell
# Kopi to nokkuure network to toppitde Group Policy
# Teelto terɓe PowerShell Intune to toppitde cloud
```

## 💼 Miisaale Kuutorɗe

### Cillol Keɗɗo
```powershell
# Kisal pellital wonaa waɗɗi keewɗo
Set-Ghost -SMBv1 -AutoRun -Macros -ICMP
```

### Doole Cellal Ngenndi
```powershell
# Ñamtinde HIPAA
Set-Ghost -SMBv1 -RDP -USBStorage -AdminShares -Telemetry
```

### Kuutorɗe Kooje
```powershell
# Teeltol kisal jokkondingol
Set-Ghost -RDP -SMBv1 -AutoRun -USBStorage -Macros -PSRemoting -AdminShares
```

### Jamirgol Cloud Araande
```powershell
# Toppitde Intune-leyɗi
Connect-IntuneGhost -Interactive
Set-Ghost -SMBv1 -RDP -AutoRun -Macros -Intune
```

## 🔍 Cariiɗe Golle

### Golle Ñamtinde Pellital

#### Kuutorɗe Network
- **RDP**: Ñippu naatde desktop woote walla woppu port
- **SMBv1**: Daame purotagol jeertine fiilde kiiɗo
- **ICMP**: Haɗtu jaabiraaji ping ngam yiɗde kadi
- **LLMNR/NetBIOS**: Ñippu purotagol yiɗde innde kiiɗo

#### Kisal Jaaynirɗe
- **Macros**: Daame tammitirgol makro nder jaaynirɗe Office
- **AutoRun**: Haɗtu tammitirgol jaajol dey media njiɗtaama

#### Jeyagol Woote
- **PSRemoting**: Daame sesiwoŋ PowerShell woote
- **WinRM**: Daaƴ Windows Remote Management
- **Remote Assistance**: Ñippu seŋorde Remote Assistance

#### Jeyagol Naatde
- **Admin Shares**: Daame jeertinde C$, ADMIN$
- **Guest Account**: Daame naatde konte seede
- **USB Storage**: Haaɗtin kuutorɗe kaɗe USB

### Jokku Azure
```powershell
# Seŋo e tenant Azure
Connect-AzureGhost -Interactive

# Huɓɓin kisal pellital
Set-AzureSecurityDefaults -Enable

# Teelto naatde sarɗiyankoore
Set-AzureConditionalAccess -BlockLegacyAuth -RequireMFA

# Njaaɗndi kuutorɓe ena yamirooje
Set-AzurePrivilegedUsers -AuditOnly
```

### Jokku Intune (Kesol nder v2)
```powershell
# Seŋo e Intune
Connect-IntuneGhost -Interactive

# Toppit humpito daɓɓitaare Intune
Set-IntuneGhost -Settings @{
    RDP = $true
    SMBv1 = $true
    USBStorage = $true
    Macros = $true
}
```

## ⚠️ Miijo Muhiimɗi

### Jaaɓɗe Ceɗtol
- **Doole Labo**: Ceɗto seetaaji fof nder doole toppaa hade
- **Toppitde Ndee Ndee**: Toppit ndee ndee ngam yiɗde caɗeele
- **Daɓɓere Ruttinde**: Teeŋtin aɗa waawi ruttinde coppitte so sokli
- **Winnditagol**: Windito seetaaji golli to doole maa

### Waɗɗe Mbaawi Waɗde
- **Golli Kuutorɓe**: Goɗɗe seetaaji mbaawi waɗɗi golle ñalawma fof
- **Jaaynirɗe Kiiɗɗe**: Sisteem kiiɗɗe mbaawi sokla purotagol keeɓɗe
- **Naatde Woote**: Miijo waɗɗe jeyagol woote ɓesngol
- **Golle Cillol**: Teeŋtin seetaaji ƴitaako golle muhiimɗe

### Ɓoyngal Kisal
- **Kisal Juuɗe**: Ghost ko fedde kisal, wonaa yamre fof
- **Jeyagol Jokkondirngol**: Kisal ena sokla yejjitaade e kesɗitine jokkondirde
- **Eɗen Kuutorɓe**: Jeyagol teknolosi ena njogii e annduɓe kisal
- **Coppitte Yamirooje**: Njuɓɓudi yamirooje kesi mbaawi yaawde kisal hannde

## 🎯 Miisaale Yamirooje

Kono Ghost ena jokki e yeewtere yamirooje keewɗe, haɗtinde keeɓal ena dogga e tammitaade ɓesnde e ceɗtol:

### Yamirooje hono WannaCry
- **Ñaañude**: `Set-Ghost -SMBv1` daame purotagol ɓoyngol
- **Miijo**: Teeŋtin alaa sisteem kiiɗo ena sokla SMBv1

### Ransomware RDP
- **Ñaañude**: `Set-Ghost -RDP` ñippu naatde desktop woote
- **Miijo**: Mbaawi sokla njuɓɓudi naatde woote goɗɗi

### Malware Nder Fiilannde
- **Ñaañude**: `Set-Ghost -Macros` daame tammitirgol makro
- **Miijo**: Mbaawi waɗɗi fiilannde ena makro ɓesɗe

### Yamirooje USB
- **Ñaañude**: `Set-Ghost -USBStorage -AutoRun` haaɗtin golle USB
- **Miijo**: Mbaawi waɗɗi kuutorɗe kaɗe USB ɓesɗe

## 🏢 Humpito Enterprise

### Wallondiral Group Policy
```powershell
# Gollu seetaaji humpito registere Group Policy
Set-Ghost -SMBv1 -RDP -AutoRun -GroupPolicy

# Seetaaji ena golla e domain fof caggal kesɗitinde GP
gpupdate /force
```

### Jokku Microsoft Intune
```powershell
# Mahɗin daɓɓitaare Intune to seetaaji Ghost
Set-IntuneGhost -Settings $GhostSettings -Interactive

# Daɓɓitaare ena toppit e kaɗe leyɗi jaajol
```

### Jaŋtingol Jokkaade
```powershell
# Mah jaŋtol njaaɗndu kisal
Get-Ghost | Export-Csv -Path "SecurityAudit-$(Get-Date -Format 'yyyy-MM-dd').csv"

# Jaŋtol haalre kisal Azure
Get-AzureGhost | Out-File "AzureSecurityReport.txt"
```

## 📚 Golle Ɓurɗe

### Hade-Toppitde
1. **Windito Haalre Jooni**: Yiil `Get-Ghost` hade coppitte
2. **Ceɗto Fof**: Teeŋtin nder doole alaa yamirde
3. **Daɓɓere Ruttinde**: Andito hono ruttinde kala seetaaji
4. **Yejjitaade Wallitooɓe**: Teeŋtin fedde cillol jaabii coppitte

### Nder Toppitde
1. **Hono Ndee Ndee**: Toppit nder kume pilot hade
2. **Yejjit Waɗɗe**: Ƴeew ƴeewnde kuutorɓe walla caɗeele sisteem
3. **Windito Caɗeele**: Windito caɗe fof to yiɗde yeeso
4. **Haalto Coppitte**: Haalto kuutorɓe baɗte kisal ɓeydi

### Caggal Toppitde
1. **Njaaɗndu Yejjitirde**: Yiil `Get-Ghost` nde e nde ngam teeŋtinde seetaaji
2. **Kesɗito Winnditagol**: Rewto teelte kisal jooni
3. **Yejjit Golli**: Yejjit golle kisal ɗe waɗi
4. **Ɓeydagol Jokkondirngol**: Coppito seetaaji e yamirooje kesɗi

## 🔧 Yiɗde Caɗeele

### Caɗeele Woodnde
- **Juumɗe Jaabondiral**: Teeŋtin sesiwoŋ PowerShell jokkondirngol
- **Dogondiral Kuutorɗe**: Goɗɗe kuutorɗe mbaawi ena dogga
- **Jokkaade Jaaynirɗe**: Ceɗto e jaaynirɗe cillol
- **Seŋorde Network**: Teeŋtin naatde woote ena golli hannde

### Cuɓe Artinde
```powershell
# Huɓɓito kuutorɗe keeɓɗe kadi so sokli
Set-RDP -Enable
Set-SMBv1 -Enable
Set-AutoRun -Enable
Set-Macros -Enable
```

## 👨‍💻 Baɗte Winnduɗo

**Jim Tyler** - Microsoft MVP to PowerShell
- **YouTube**: [@PowerShellEngineer](https://youtube.com/@PowerShellEngineer) (10,000+ jokkaɓe)
- **Newsletter**: [PowerShell.News](https://powershell.news) - Keɓe kisal yontere
- **Winnduɗo**: "PowerShell for Systems Engineers"
- **Anndal**: Duuɓi jokkondirde PowerShell e kisal Windows

## 📄 Lisaŋs e Haalaaji

### Lisaŋs MIT
Ghost ena wardi huunde lisaŋs MIT to kuutorɗe alaa kooje, coppital, e jeytinal.

### Haalaaji Kisal
- **Alaa Laacol**: Ghost ena wardi "hono noon" alaa laacol kala gooto
- **Ceɗtol Ena Sokli**: Yejjit ceɗto nder doole alaa yamirde hade
- **Yiillo Jannginoojo**: To toppitde yamirde, haalo jannginooɓe kisal
- **Waɗɗe Golle**: Winnduɓe alaa jejeɓe to pettaade golle
- **Kisal Ɓurngal**: Ghost ko fedde yamre kisal ɓurngal

### Wallondiral
- **Caɗeele GitHub**: [Jaŋto caɗe walla ɗaɓɓit humpito](https://github.com/jimrtyler/Ghost/issues)
- **Winnditagol**: Huutoro `Get-Help <function> -Full` to ballal cariiɗal
- **Renndo**: Galle PowerShell e kisal

---

**🔒 Ñamto haalre kisal maa humpito Ghost - kono yejjit ceɗto hade.**

```powershell
# Fuɗɗo humpito njaaɗndu, wonaa naamnal
Get-Ghost
```

**⭐ So Ghost walliima ɓeydude haalre kisal maa, star ndee repository!**