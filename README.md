<div align="center">
  <img src="insane-moodlight-v2.png" width="600" style="border-radius: 10px;">
  <br>
  <h1>INSANE MOODLIGHT OLED V2.0</h1>
  <p><i>Ein fortschrittliches Stimmungslicht auf Basis von ESPHome. Fokus auf Hardware-Stabilität, Signalintegrität und Langlebigkeit.</i></p>
</div>

<br>
<hr>
<br>

<table width="100%" border="0">
  <tr>
    <td width="50%" valign="top">
      <h3>KONZEPT</h3>
      Das Insane Moodlight V2.0 adressiert typische Probleme von DIY-LED-Projekten durch präzise Spannungsregulierung und intelligentes Software-Management für Display und Energieversorgung.
    </td>
    <td width="50%" valign="top">
      <h3>HARDWARE-SPECS</h3>
      <ul>
        <li>Levelshifter: SN74AHCT125N (5V)</li>
        <li>Schutz: 62-Ohm Datenwiderstände</li>
        <li>Pufferung: 220uF (ESP) / 3x 470uF (LEDs)</li>
        <li>Akku: 18650 Li-Ion mit TP4056</li>
      </ul>
    </td>
  </tr>
</table>

<br>

<h3>ELEKTRONIK-ARCHITEKTUR</h3>

<p><b>Signalqualität und Schutz</b><br>
Einsatz eines Levelshifters zur Anhebung der Datenpegel auf 5V, unterstützt durch einen 100nF Keramikkondensator. 62-Ohm-Widerstände in den Datenleitungen eliminieren Reflexionen und garantieren ein sauberes Signalbild.</p>

<p><b>Spannungsglättung</b><br>
Umfassende kapazitive Pufferung verhindert LED-Flackern bei Lastspitzen. Die Schaltung ist durch eine Glassicherung und einen LiPo-Laderegler für den autarken Betrieb abgesichert.</p>

<p><b>Sensorik und Telemetrie</b><br>
Erfassung von Umgebungsdaten via DHT-Sensor. Die Batterieüberwachung erfolgt präzise über einen Spannungsteiler am Analog-Eingang A0.</p>

<br>
<hr>
<br>

<h3>SOFTWARE-LOGIK</h3>

<p><b>Betriebssicherheit</b><br>
Ein integrierter Pixel-Shift verschiebt den Bildinhalt alle zwei Minuten, um ein Einbrennen des OLED-Displays dauerhaft zu verhindern. Die Boot-Logik schützt gespeicherte Nutzer-Nachrichten im Flash-Speicher.</p>

<p><b>Interaktion</b><br>
Der Master-Toggle speichert aktuelle Farb- und Helligkeitswerte beim Ausschalten global. Beim Neustart wird der exakte vorherige Zustand wiederhergestellt. Der Gruß-Modus ermöglicht animierte Symbole (Herz, Stern, Smiley) und individuelle Texte.</p>

<p><b>Energiemanagement</b><br>
Automatisches Warnsystem bei kritischer Spannung:<br>
&bull; Unter 10% Kapazität: Rotes Blinken (10s Intervall)<br>
&bull; Unter 5% Kapazität: Rotes Blinken (5s Intervall)</p>

<br>
<hr>
<br>

<div align="center">
  <h3>MECHANISCHER AUFBAU</h3>
  <p>Gehäuse: 15x15 cm Basis | 5 cm Sockel | 3D-Druck optimiert</p>
</div>

<p><b>Design</b><br>
Die Pyramidenflächen sind für optimale Lichtdiffusion konstruiert. Ein transparenter Streifen am Sockel sorgt für ein dezentes "Passive Light".</p>

<p><b>Bedienung</b><br>
Zentrales OLED-Display mit drei darunterliegenden haptischen Mikroschaltern für die direkte Systemsteuerung ohne App-Zwang.</p>

<br>

<h3>INSTALLATION</h3>
<ol>
  <li>secrets.yaml mit Netzwerkdaten konfigurieren.</li>
  <li>Kompilierung und Upload via ESPHome.</li>
  <li>Integration in Home Assistant zur Steuerung der Lichteffekte.</li>
</ol>

<br>
<hr>
<br>

<div align="right">
  <i>Entwickelt für Angelina.</i>
</div>
