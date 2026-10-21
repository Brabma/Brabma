# Moje IT projekty

Na vlastních projektech si zkouším správu Linuxu a Windows. Domácí server nepřetržitě sbírá zprávy ze světových médií a vzniká z nich web [mujlinux.cloud](https://mujlinux.cloud/). Ve virtuální síti s Windows Serverem spravuji uživatele, sdílené složky a skupinové zásady. Na Asterisku mi běží telefonní linka, na kterou se dá zavolat z běžného mobilu.

## [Linuxový server pro sběr zpráv](https://github.com/Brabma/linux-server)

Tablet s Androidem mi slouží jako domácí server. Je tichý, má malou spotřebu a běží i při vypnutém počítači. Každých 15 minut stahuje nové články z veřejné databáze světového tisku GDELT a z kanálů vybraných redakcí a ukládá je do databáze. Z nasbíraných zpráv vzniká přehled, který běží na pronajatém serveru s Ubuntu a může si ho přečíst kdokoli: [mujlinux.cloud](https://mujlinux.cloud/).

<a href="https://mujlinux.cloud/"><img src="https://github.com/Brabma/linux-server/raw/main/assets/svet-reader.png" alt="Přehled světových zpráv na mujlinux.cloud" width="640"></a>

**Co v projektu najdete**

- Programy v Pythonu, které na tabletu stahují a ukládají data, a SQL dotazy, které hlídají, že žádné čtvrthodinové stahování nechybí.
- Veřejný web s Nginx a HTTPS, certifikát Let's Encrypt s naplánovanou obnovou a správu obou serverů přes SSH s klíči.
- Zálohy s kontrolními součty a vyzkoušenou obnovou databáze ze zálohy.
- [Rozbor závady](https://github.com/Brabma/linux-server/blob/main/docs/incident-wifi.md), kdy se větší přenosy na tablet přes Wi-Fi zastavovaly, a porovnání s USB.

## [Windows Server a Active Directory](https://github.com/Brabma/windows-support-lab)

Na jednom počítači mi ve VirtualBoxu běží dva virtuální stroje: server s Windows Serverem 2025 a pracovní stanice s Windows 11. Spolu tvoří malou firemní doménu se dvěma testovacími uživateli, Annou a Petrem. Na stanici je vidět, jak se změna na serveru projeví u uživatele.

**Co v projektu najdete**

- Uživatele a skupiny v Active Directory a přihlášení do domény na pracovní stanici.
- Sdílenou složku, do které má přístup jen jedna skupina.
- Skupinovou zásadu (GPO), která běžným uživatelům zablokuje Ovládací panely, ověřenou přímo v jejich relaci.
- Skript v PowerShellu, který zkontroluje síť, DNS a služby a uloží výsledek.
- [Tři závady zpracované jako tiket](https://github.com/Brabma/windows-support-lab/tree/main/tickets) od hlášení po kontrolu výsledku: chybný DNS, chybějící členství ve skupině a zakázaný účet.

## [Telefonní hra na Asterisku](https://github.com/Brabma/asterisk-telefonni-hra)

Krátká hra, kterou si zahrajete po telefonu. Dovoláte se na firemní linku, jejíž automat nechce být vypnutý, a volbami rozhodujete, jak to dopadne.

**Zavolejte na 222 765 757 a vybírejte tlačítky 1 a 2.** Stačí běžný mobil, žádná aplikace ani registrace.

Děj a texty vytvořila AI, jde jen o ukázku. Hra běží na mém serveru s Ubuntu a Asteriskem. Operátor Odorik na něj předává hovory přes SIP. Spravuji připojení k operátorovi, přehrávání hlášek, reakce na tlačítka a zabezpečení serveru. V repozitáři je scénář, konfigurace a postup kontroly hovorů.
