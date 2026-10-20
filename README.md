# Moje IT projekty

Provozuji domácí server pro sběr a zpracování zpráv, ze kterých vzniká web mujlinux.cloud. Ve virtuální síti s Windows Serverem spravuji uživatele, sdílené složky a skupinové zásady. Doplňkem je krátká telefonní hra.

## [Linuxový server pro sběr zpráv](https://github.com/Brabma/linux-server)

Starý tablet s Androidem mi slouží jako domácí server. Je tichý, má malou spotřebu a běží i při vypnutém počítači. Každých 15 minut stahuje nové články z veřejné databáze světového tisku GDELT a z kanálů vybraných redakcí a ukládá je do databáze. Z nasbíraných zpráv vzniká přehled, který běží na pronajatém serveru s Ubuntu a může si ho přečíst kdokoli: [mujlinux.cloud](https://mujlinux.cloud/).

<a href="https://mujlinux.cloud/"><img src="https://github.com/Brabma/linux-server/raw/main/assets/svet-reader.png" alt="Přehled světových zpráv na mujlinux.cloud" width="640"></a>

**Co v projektu najdete**

- Programy v Pythonu, které na tabletu stahují a ukládají data, a SQL dotazy, které hlídají, že žádné čtvrthodinové stahování nechybí.
- Veřejný web s Nginx a HTTPS, certifikát s automatickou obnovou a správu obou serverů přes SSH s klíči.
- Zálohy s kontrolními součty a vyzkoušenou obnovou databáze ze zálohy.

## [Windows Server a Active Directory](https://github.com/Brabma/windows-support-lab)

Na jednom počítači mi ve VirtualBoxu běží dva virtuální stroje: server s Windows Serverem 2025 a pracovní stanice s Windows 11. Spolu tvoří malou firemní doménu se dvěma testovacími uživateli, Annou a Petrem. Na stanici je vidět, jak se změna na serveru projeví u uživatele.

**Co v projektu najdete**

- Uživatele a skupiny v Active Directory a přihlášení do domény na pracovní stanici.
- Sdílenou složku, do které má přístup jen jedna skupina.
- Skupinovou zásadu (GPO), která běžným uživatelům zablokuje Ovládací panely, ověřenou přímo v jejich relaci.
- Skript v PowerShellu, který zkontroluje síť, DNS a služby a uloží výsledek.

## [Telefonní hra na Asterisku](https://github.com/Brabma/asterisk-telefonni-hra)

Krátká hra, kterou si zahrajete po telefonu. Ozve se firemní ústředna a tlačítky 1 a 2 rozhodujete, jak příběh dopadne. Zabere přibližně minutu.

**Zavolejte na 222 765 757 a vybírejte tlačítky 1 a 2.** Stačí běžný mobil, žádná aplikace ani registrace.

Hra běží na mém serveru s Ubuntu a Asteriskem. Operátor Odorik na něj předává hovory přes SIP. Spravuji připojení k operátorovi, přehrávání hlášek, reakce na tlačítka a zabezpečení serveru. V repozitáři je scénář, konfigurace a postup kontroly hovorů.
