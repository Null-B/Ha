## After Installation Configurations

### Static IP Configuration
**Hinweis:** Diese Konfiguration muss nicht wiederholt werden, wenn sie bereits abgeschlossen ist.

### Zeitzonenkonfiguration
Gehen Sie im Hauptmenü wie folgt vor:

1. Klicken Sie auf das Symbol **Local Server**.
   ![Local Server Icon](image-9.png)
2. Scrollen Sie horizontal in den **Server Properties**, bis Sie die Einstellung für die **Time Zone** sehen.
   ![Time Zone Settings](image-10.png)

   Es sollte so aussehen, wenn Sie die Zeitzoneneinstellung gefunden haben:
   ![Gefundene Time Zone](image-11.png)

3. Klicken Sie auf den **Text der Time Zone**, um die Einstellung zu ändern.
   ![Zeit ändern](image-12.png)
4. Wählen Sie **Change Time and Date** aus.
   ![Change Time and Date](image-13.png)

Wählen Sie Ihre aktuelle Zeitzone aus.  
**Warum ist dies wichtig?**  
Die korrekte Zeitzone hilft, häufig auftretende Verbindungsprobleme zu vermeiden, die durch Zeitdifferenzen entstehen können.

---

## DHCP Post-Installationskonfiguration

Nach der Installation sehen Sie im Hauptmenü ein gelbes Warnsymbol in der oberen rechten Ecke des Bildschirms:
![Warnsymbol](image-3.png)

1. Klicken Sie auf das **Flagge-Symbol** mit dem gelben Dreieck.
   ![Flagge mit Warnung](image-6.png)
2. Wählen Sie **Complete DHCP Configuration** aus.
   ![Complete DHCP Configuration](image-7.png)
3. Ein Konfigurationsfenster wird angezeigt. Lesen Sie die Informationen durch und klicken Sie auf **Commit**.
   ![Commit Button](image-8.png)

**Hinweis:**  
Wenn der Server ohne Active Directory (AD) installiert wurde, verwendet der DHCP-Server das aktuelle Administratorkonto.  
Falls AD installiert ist, wird das Konto für Benutzerverwaltung notwendig. Dies ist jedoch für den Moment irrelevant.

**Ergebnis:**  
Die Installation und Post-Konfiguration des DHCP-Moduls ist abgeschlossen.

---

## DHCP Ranges Konfiguration

### Theorie
Bevor wir die DHCP-Ranges konfigurieren, behandeln wir kurz die theoretischen Grundlagen.  
Dies ist nicht zwingend erforderlich, hilft jedoch, die Konfiguration besser zu verstehen.

#### **Was sind DHCP-Ranges?**

Die **DHCP-Range** ist der Bereich von IP-Adressen, die ein **DHCP-Server** automatisch an Geräte im Netzwerk vergibt.

##### Kernpunkte:  
1. **Zweck**:  
   DHCP automatisiert die IP-Adressvergabe und reduziert manuelle Konfigurationsfehler.

2. **Definition**:  
   - Die **Range** gibt an, welche IP-Adressen automatisch vergeben werden.  
   - Beispiel: Eine Range von `192.168.1.100` bis `192.168.1.200` bedeutet, dass nur Adressen in diesem Bereich vergeben werden.

3. **Einstellungen**:  
   - Konfiguration erfolgt im Router oder Server.  
   - Außerhalb der Range können **statische IP-Adressen** (z. B. für Drucker oder Server) verwendet werden.

4. **Zusätzliche Parameter**:  
   Neben der IP-Adresse können Subnetzmaske, Gateway und DNS-Server automatisch verteilt werden.

##### Vorteile:  
- Automatisierung der Netzwerkkonfiguration  
- Reduzierung von Fehlern bei der manuellen IP-Vergabe

---

### IP Ranges festlegen
Vor der Konfiguration der Ranges ist es wichtig, den Unterschied zwischen **IPv4** und **IPv6** zu verstehen.

#### **Erklärung zu IPv4 und IPv6**

**IPv4** und **IPv6** sind Protokolle zur Adressierung von Geräten in Netzwerken. Sie stellen sicher, dass Datenpakete an die richtigen Geräte gesendet werden.

##### IPv4 (Internet Protocol Version 4)  
1. **Adressformat**:  
   - 32-Bit-Adressen, dargestellt als vier Zahlen (0-255), getrennt durch Punkte.  
   - Beispiel: `192.168.1.1`

2. **Kapazität**:  
   - Bis zu **4,3 Milliarden Adressen** verfügbar.  

3. **Merkmale**:  
   - Einfach einzusetzen und weit verbreitet.  
   - Unterstützt Broadcast.  
   - Keine eingebauten Sicherheitsfunktionen.

##### IPv6 (Internet Protocol Version 6)  
1. **Adressformat**:  
   - 128-Bit-Adressen, dargestellt in Hexadezimalgruppen, getrennt durch Doppelpunkte.  
   - Beispiel: `2001:0db8:85a3:0000:0000:8a2e:0370:7334`

2. **Kapazität**:  
   - Theoretisch **340 Sextillionen Adressen**.

3. **Merkmale**:  
   - Integrierte Sicherheitsfunktionen (z. B. IPsec).  
   - Effizientere Datenweiterleitung.  
   - Unterstützt automatische Adresskonfiguration.

##### Unterschiede zwischen IPv4 und IPv6  

| **Eigenschaft**        | **IPv4**                  | **IPv6**                  |
|------------------------|---------------------------|---------------------------|
| **Adresslänge**        | 32 Bit                   | 128 Bit                  |
| **Adressformat**       | Dezimal (z. B. 192.0.2.1) | Hexadezimal (z. B. 2001:db8::1) |
| **Adressanzahl**       | 4,3 Milliarden           | 340 Sextillionen         |
| **Sicherheit**         | Extern (z. B. Firewalls) | Integriert (IPsec)       |
| **Kompatibilität**     | Veraltet, aber weit verbreitet | Modern, noch im Aufbau   |

##### Zusammenfassung  
- **IPv4** ist bewährt und weit verbreitet, aber aufgrund der begrenzten Adressanzahl zunehmend problematisch.  
- **IPv6** ist moderner, zukunftssicher und leistungsfähiger, wird jedoch noch nicht flächendeckend eingesetzt.

# After Installation Configurations

## Static IP Configuration
**Hinweis:** Diese Konfiguration muss nur einmal durchgeführt werden.

### Zeitzonen-Konfiguration
Um die Zeitzone einzustellen, folgen Sie diesen Schritten:

1. Öffnen Sie das **Main Menu** und klicken Sie auf das **Local Server**-Symbol.  
   ![Local Server](image-9.png)

2. Scrollen Sie horizontal durch die **Server Properties**, bis Sie die Einstellung **Time Zone** finden.  
   ![Time Zone Settings](image-10.png)

   So sieht es aus, wenn die Einstellung sichtbar ist:  
   ![Time Zone gefunden](image-11.png)

3. Klicken Sie auf den angezeigten Zeitzonentext, um Änderungen vorzunehmen.  
   ![Text bearbeiten](image-12.png)

4. Klicken Sie auf **Change Time and Date**.  
   ![Change Time and Date](image-13.png)

5. Wählen Sie Ihre aktuelle Zeitzone aus.  

**Wichtig:** Die richtige Zeitzoneneinstellung hilft, Verbindungsprobleme durch inkorrekte Zeitstempel zu vermeiden.

---

## DHCP Post-Install Configuration

Nach der Installation sehen Sie im **Main Menu** oben rechts ein gelbes Warnsymbol.  
![Gelbes Dreieck](image-3.png)

### Schritte:
1. Klicken Sie auf das Symbol mit der gelben Flagge.  
   ![Gelbe Flagge](image-6.png)

2. Wählen Sie **Complete DHCP Configuration** aus.  
   ![DHCP Konfiguration](image-7.png)

3. Ein Konfigurationsassistent öffnet sich. Lesen Sie die Informationen durch und klicken Sie anschließend auf **Commit**.  
   ![Commit](image-8.png)

**Hinweis:**  
- Falls kein Active Directory (AD) installiert ist, verwendet der DHCP-Server das aktuelle Administratorkonto.  
- Bei Servern mit AD wird die AD-Benutzerkonfiguration verwendet.  
  ![AD Beispiel](image-14.png)

Nachdem diese Schritte abgeschlossen sind, ist die Installation und grundlegende Konfiguration des DHCP-Servers abgeschlossen.

---

## DHCP Ranges Configuration

### Theorie: Was ist eine DHCP-Range?
Eine **DHCP-Range** definiert den Bereich von IP-Adressen, die ein DHCP-Server automatisch an Geräte im Netzwerk vergibt.  

#### Vorteile von DHCP:
- **Automatische IP-Zuweisung:** Erleichtert die Netzwerkkonfiguration.  
- **Effizienz:** Minimiert Fehler und beschleunigt den Prozess.

Beispiel einer Range:  
`192.168.1.100` – `192.168.1.200`  

#### Zusätzliche Parameter:
- Subnetzmaske
- Gateway
- DNS-Server

---

### Unterschiede: IPv4 vs. IPv6

| **Eigenschaft**        | **IPv4**                  | **IPv6**                  |
|------------------------|---------------------------|---------------------------|
| **Adresslänge**        | 32 Bit                   | 128 Bit                  |
| **Adressformat**       | Dezimal (z. B. 192.0.2.1) | Hexadezimal (z. B. 2001:db8::1) |
| **Kapazität**          | 4,3 Milliarden           | 340 Sextillionen         |
| **Sicherheit**         | Extern (z. B. Firewalls) | Integriert (IPsec)       |

IPv4 ist aktuell noch weit verbreitet, jedoch limitiert in der Kapazität. IPv6 ist die moderne Lösung, aber nicht überall etabliert.

---

### Schritte zur DHCP-Range-Konfiguration

1. Öffnen Sie das **Tools-Menü**.  
   ![Tools-Menü](image-15.png)

2. Wählen Sie **DHCP**.  
   ![DHCP auswählen](image-16.png)  
   ![DHCP-Manager](image-17.png)

3. Klicken Sie im linken Menü auf den gewünschten Server.  
   ![Server auswählen](image-19.png)

4. Navigieren Sie zum **IPv4**-Abschnitt und klicken Sie mit der rechten Maustaste darauf.  
   ![IPv4 auswählen](image-20.png)

5. Wählen Sie **New Scope**.  
   ![New Scope](image-21.png)

6. Ein Assistent wird geöffnet. Füllen Sie die Felder wie folgt aus:  
   - **Name des Scopes:** Wählen Sie einen eindeutigen Namen.  
     ![Scope Name](image-24.png)

   - **IP-Range:** Definieren Sie Start- und Endadresse basierend auf Ihrem IP-Plan.  
     ![IP-Range festlegen](image-25.png)

7. **Exclusions and Delays:** Konfigurieren Sie Ausschlüsse für statische IP-Adressen.  
   - Beispiel: Reservierte Adressen für Server oder Drucker.  
     ![Ausschlüsse](image-26.png)

8. **Lease-Dauer:** Wählen Sie die Standardwerte aus.  
   ![Lease-Dauer](image-27.png)

9. **Default Gateway:** Geben Sie die Gateway-IP ein (z. B. `10.0.0.254`).  
   ![Gateway](image-29.png)

10. **Weitere Konfigurationen:**  
    - DNS-Server: Falls nicht vorhanden, überspringen.  
    - WINS-Server: Überspringen.  
    ![DNS-Überspringen](image-30.png)  
    ![WINS-Überspringen](image-31.png)

11. Fertigstellen des Assistenten.  
    ![Fertigstellen](image-33.png)

12. Starten Sie den DHCP-Server neu:  
    - Rechte Maustaste auf den Server → **All Tasks → Restart**.  
      ![Server neu starten](image-36.png)

Nach dem Neustart können Sie den Server über den DHCP-Manager verwalten.  
![DHCP-Manager](image-34.png)

---

## Client Configuration

Stellen Sie sicher, dass der Client so konfiguriert ist, dass er eine IP-Adresse automatisch per DHCP bezieht:

1. Öffnen Sie die **Systemsteuerung** und navigieren Sie zu **Netzwerk und Internet → Netzwerk- und Freigabecenter**.  
   ![Systemsteuerung](image-39.png)

2. Klicken Sie auf **Adaptereinstellungen ändern**.  
   ![Adaptereinstellungen](image-42.png)

3. Wählen Sie Ihren Netzwerkadapter und öffnen Sie die **Eigenschaften**.  
   ![Adaptereigenschaften](image-44.png)

4. Markieren Sie **Internetprotokoll Version 4 (TCP/IPv4)** und klicken Sie auf **Eigenschaften**.  
   ![TCP/IPv4](image-45.png)

5. Stellen Sie sicher, dass **IP-Adresse automatisch beziehen** und **DNS-Serveradresse automatisch beziehen** aktiviert sind.  
   ![Automatische IP](image-46.png)

6. Bestätigen Sie mit **OK**.

---

## Testen der Konfiguration

### Serverseitig:
1. Stellen Sie sicher, dass der DHCP-Dienst läuft (`services.msc`).  
   ![Dienst prüfen](image-51.png)

2. Überprüfen Sie im DHCP-Manager, ob der Client eine Lease erhalten hat.  
   ![Lease prüfen](image-52.png)

### Clientseitig:
1. Führen Sie `ipconfig /renew` in der Eingabeaufforderung aus.  
   ![ipconfig /renew](image-47.png)

2. Überprüfen Sie die erhaltene IP-Adresse mit `ipconfig`.  
   ![ipconfig prüfen](image-53.png)

---

**Hinweis:** Weitere Schritte wie Fehlerbehebung und Feinabstimmung können erforderlich sein, um die Konnektivität zu optimieren.
