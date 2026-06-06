# 🐧 Linux Administration Course

---

## Episode 5 — Terminal & Shell

### TTY vs Terminal
- **TTY** (TeleType Terminal) → يُستخدم لما **مفيش GUI**
- **Terminal** → يُستخدم لما **عندك GUI**

> يمكنك الوصول لأكثر من TTY عن طريق: `Alt + Ctrl + F1` إلى `F6`
> - GUI بيكون في **TTY 2**
> - أمر `tty` بيعرفك أنت في أنهي TTY

---

### Shell Prompt

```
mahmoud @ kali  ~  :  $
   │        │    │     └─ Current Working Directory
   │        │    └─ Hostname
   └─ Username
```

| Symbol | Meaning |
|--------|---------|
| `$`    | Regular User |
| `#`    | Root User |

- **Shell الحالي:** `Bash`

---

## Episode 6 — Basic Commands

| Command    | Description                        |
|------------|------------------------------------|
| `date`     | يعطيك التاريخ والوقت               |
| `cal`      | يعطيك التقويم                      |
| `whoami`   | يعطيك اسم المستخدم الحالي          |
| `pwd`      | يطبع مسار الـ Working Directory    |
| `exit`     | يغلق الـ Session                   |
| `su`       | للتبديل بين المستخدمين             |

### استخدام `su`
```bash
su - username
```

### تنفيذ أكثر من أمر في سطر واحد
```bash
command1 ; command2 ; command3
```
> استخدم `;` للفصل بين الأوامر

---

## Episode 7 — Linux File System Hierarchy

### الفرق بين Windows وLinux

| | Windows | Linux |
|---|---------|-------|
| **البنية** | Partitions منفصلة | شجرة مقلوبة واحدة (Single Inverted Tree) |
| **مثال على المسار** | `C:\Users\Ali\Documents` | `/home/Ali/Documents` |
| **نقطة البداية** | Drive letters (C:, D:) | Root Directory `/` |

---

### 📁 Root Directories الأساسية

| # | Directory | Description |
|---|-----------|-------------|
| 1 | `/home`    | يحتوي على ملفات المستخدمين العاديين |
| 2 | `/root`    | الـ Home Directory الخاص بـ Root User |
| 3 | `/bin`     | System Binaries — يحتوي على الأوامر الأساسية |
| 4 | `/sbin`    | أوامر الـ Superuser (المدير) |
| 5 | `/boot`    | ملفات الإقلاع — يحتوي على **GRUB Boot Loader** |
| 6 | `/dev`     | الأجهزة المتصلة بالجهاز (Hard Disks, etc.) |
| 7 | `/etc`     | جميع ملفات الإعداد (users, groups, networks...) |
| 8 | `/tmp`     | الملفات المؤقتة |
| 9 | `/usr`     | الملفات المشتركة بين المستخدمين |
| 10 | `/var`    | الملفات المتغيرة باستمرار: Logs, Database, Email |
| 11 | `/media` & `/mnt` | نقاط تحميل الأجهزة الخارجية |
| 12 | `/lib` & `/lib64` | الملفات المشتركة بين البرامج (Shared Libraries) |
| 13 | `/opt`    | البرامج الاختيارية (Optional Software) |
| 14 | `/srv`    | بيانات الخدمات (Services Data) |

---

> 📌 *ملاحظة: هذه المذكرات مأخوذة من كورس Linux Administration — يتم التحديث بإضافة الصفحات الجديدة.*
