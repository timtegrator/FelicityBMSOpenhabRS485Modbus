<!DOCTYPE html>
<html lang="de">
<head>
<meta charset="UTF-8">

</head>
<body>

<h1>Felicity BMS – Modbus Registermap</h1>
<p><em>Some rough estimates what the registers might be.</em></p>

<hr>

<div class="section">
<h2>🔋 Battery Info Block</h2>
<p><strong>Start:</strong> 0x1300 (= 4864)<br>
<strong>Länge:</strong> 42 Register</p>

<h3>📤 Request</h3>
<pre><code>01 03 13 00 00 2A C0 91</code></pre>
<p>01 Slave‑ID, 03 Function Code, 13 00 Startadresse, 00 2A Anzahl Register, C0 91 CRC‑16</p>

<table>
<tr><th>Dec</th><th>Hex</th><th>Beschreibung</th><th>Skalierung</th><th>Verified</th></tr>
<tr><td>4864</td><td>1300</td><td>Unbekannt</td><td>-</td><td></td></tr>
<tr><td>4865</td><td>1301</td><td>Unbekannt</td><td>-</td><td></td></tr>
<tr><td>4866</td><td>1302</td><td>Unbekannt</td><td>-</td><td></td></tr>
<tr><td>4867</td><td>1303</td><td>-</td><td>-</td><td></td></tr>
<tr><td>4868</td><td>1304</td><td>-</td><td>-</td><td></td></tr>
<tr><td>4869</td><td>1305</td><td>-</td><td>-</td><td></td></tr>
<tr><td>4870</td><td>1306</td><td>Batteriespannung</td><td>×0.01 V</td><td>OK</td></tr>
<tr><td>4871</td><td>1307</td><td>Batteriestrom (signed)</td><td>×0.1 A</td><td>OK</td></tr>
<tr><td>4872</td><td>1308</td><td>-</td><td>-</td><td></td></tr>
<tr><td>4873</td><td>1309</td><td>-</td><td>-</td><td></td></tr>
<tr><td>4874</td><td>1310</td><td>Batterietemperatur</td><td>°C</td><td></td></tr>
<tr><td>4875</td><td>1311</td><td>SOC</td><td>%</td><td>OK</td></tr>
<tr><td>4876</td><td>1312</td><td>SOH</td><td>%</td><td></td></tr>
<tr><td>4877</td><td>1313</td><td>Zyklen</td><td>-</td><td>OK</td></tr>
<tr><td>4878–4893</td><td>1314–1323</td><td>Diverse interne Werte</td><td>-</td><td></td></tr>
<tr><td>4894</td><td>1324</td><td>Unbekannt</td><td>-</td><td></td></tr>
<tr><td>4895</td><td>1325</td><td>Unbekannt</td><td>-</td><td></td></tr>
<tr><td>4896</td><td>1326</td><td>Max Cell Voltage (raw)</td><td>×0.001 V</td><td>OK</td></tr>
<tr><td>4897</td><td>1327</td><td>Max Cell Index</td><td>-</td><td></td></tr>
<tr><td>4898</td><td>1328</td><td>Min Cell Voltage (raw)</td><td>×0.001 V</td><td>OK</td></tr>
<tr><td>4899</td><td>1329</td><td>Min Cell Index</td><td>-</td><td></td></tr>
<tr><td>4900</td><td>132A</td><td>Cell Count</td><td>-</td><td></td></tr>
<tr><td>4901</td><td>132B</td><td>-</td><td>-</td><td></td></tr>
<tr><td>4902</td><td>132C</td><td>NTC Count</td><td>-</td><td></td></tr>
<tr><td>4903</td><td>132D</td><td>-</td><td>-</td><td></td></tr>
<tr><td>4904</td><td>132E</td><td>Temp (min/avg/max)</td><td>°C</td><td></td></tr>
<tr><td>4905</td><td>132F</td><td>Temp (min/avg/max)</td><td>°C</td><td></td></tr>
</table>
</div>

<hr>

<div class="section">
<h2>🔋 Cell Info Block</h2>
<p><strong>Start:</strong> 0x132A (= 4906)<br>
<strong>Länge:</strong> 32 Register</p>

<h3>📤 Request</h3>
<pre><code>01 03 13 2A 00 20 61 5E</code></pre>

<table>
<tr><th>Dec</th><th>Hex</th><th>Beschreibung</th><th>Skalierung</th><th>Verified</th></tr>
<tr><td>4906</td><td>132A</td><td>Max Cell Voltage (raw)</td><td>×0.001 V</td><td></td></tr>
<tr><td>4907</td><td>132B</td><td>Max Cell Index</td><td>-</td><td></td></tr>
<tr><td>4908</td><td>132C</td><td>Min Cell Voltage (raw)</td><td>×0.001 V</td><td></td></tr>
<tr><td>4909</td><td>132D</td><td>Min Cell Index</td><td>-</td><td></td></tr>
<tr><td>4910</td><td>132E</td><td>Temp Sensor 1</td><td>°C</td><td>OK</td></tr>
<tr><td>4911</td><td>132F</td><td>Temp Sensor 2</td><td>°C</td><td>OK</td></tr>
<tr><td>4912</td><td>1330</td><td>Temp Sensor 3</td><td>°C</td><td>OK</td></tr>
<tr><td>4913</td><td>1331</td><td>Temp Sensor 4</td><td>°C</td><td>OK</td></tr>
</table>

<h3>Zellspannungen (×0.001 V)</h3>

<table>
<tr><th>Dec</th><th>Hex</th><th>Cell</th><th>Verified</th></tr>
<tr><td>4914</td><td>1332</td><td>Cell 1</td><td>OK</td></tr>
<tr><td>4915</td><td>1333</td><td>Cell 2</td><td>OK</td></tr>
<tr><td>4916</td><td>1334</td><td>Cell 3</td><td>OK</td></tr>
<tr><td>4917</td><td>1335</td><td>Cell 4</td><td>OK</td></tr>
<tr><td>4918</td><td>1336</td><td>Cell 5</td><td>OK</td></tr>
<tr><td>4919</td><td>1337</td><td>Cell 6</td><td>OK</td></tr>
<tr><td>4920</td><td>1338</td><td>Cell 7</td><td>OK</td></tr>
<tr><td>4921</td><td>1339</td><td>Cell 8</td><td>OK</td></tr>
<tr><td>4922</td><td>133A</td><td>Cell 9</td><td>OK</td></tr>
<tr><td>4923</td><td>133B</td><td>Cell 10</td><td>OK</td></tr>
<tr><td>4924</td><td>133C</td><td>Cell 11</td><td>OK</td></tr>
<tr><td>4925</td><td>133D</td><td>Cell 12</td><td>OK</td></tr>
<tr><td>4926</td><td>133E</td><td>Cell 13</td><td>OK</td></tr>
<tr><td>4927</td><td>133F</td><td>Cell 14</td><td>OK</td></tr>
<tr><td>4928</td><td>1340</td><td>Cell 15</td><td>OK</td></tr>
<tr><td>4929</td><td>1341</td><td>Cell 16</td><td>OK</td></tr>
</table>
</div>

<hr>

<div class="section">
<h2>⚙️ Status / Limits Block</h2>
<p><strong>Start:</strong> 0x2320 (= 8992)<br>
<strong>Länge:</strong> 64 Register</p>

<h3>📤 Request</h3>
<pre><code>01 03 23 20 00 40 4E 74</code></pre>
<p>01 Slave‑ID, 03 Read Holding Registers, 23 20 Startadresse, 00 40 Anzahl Register, 4E 74 CRC‑16</p>

<table>
<tr><th>Dec</th><th>Hex</th><th>Beschreibung</th><th>Skalierung</th><th>Verified</th></tr>
<tr><td>8992</td><td>2320</td><td>Status</td><td>-</td><td></td></tr>
<tr><td>8993</td><td>2321</td><td>-</td><td>-</td><td></td></tr>
<tr><td>8994</td><td>2322</td><td>Charge Limit (A×10)</td><td>×0.1 A</td><td></td></tr>
<tr><td>8995</td><td>2323</td><td>NTC Count</td><td>-</td><td></td></tr>
<tr><td>8996</td><td>2324</td><td>Min Cell Voltage (raw)</td><td>×0.001 V</td><td></td></tr>
<tr><td>8997</td><td>2325</td><td>Cell High Alarm</td><td>×0.001 V</td><td></td></tr>
<tr><td>8998</td><td>2326</td><td>Cell High Alarm Back</td><td>×0.001 V</td><td></td></tr>
<tr><td>8999</td><td>2327</td><td>-</td><td>-</td><td></td></tr>
<tr><td>9000</td><td>2328</td><td>-</td><td>-</td><td></td></tr>
<tr><td>9001</td><td>2329</td><td>Max Cell Voltage (Soll)</td><td>×0.001 V</td><td>OK</td></tr>
<tr><td>9002</td><td>232A</td><td>95% SoC Voltage</td><td>×0.001 V</td><td>OK</td></tr>
<tr><td>9003</td><td>232B</td><td>5% SoC Voltage</td><td>×0.001 V</td><td>OK</td></tr>
<tr><td>9004</td><td>232C</td><td>Empty Voltage</td><td>×0.001 V</td><td>OK</td></tr>
<tr><td>9005</td><td>232D</td><td>Cell High Alarm</td><td>×0.001 V</td><td>OK</td></tr>
<tr><td>9006</td><td>232E</td><td>Temp High Alarm</td><td>°C?</td><td></td></tr>
<tr><td>9007</td><td>232F</td><td>Temperatur</td><td>°C</td><td></td></tr>
<tr><td>9008–9023</td><td>2330–233F</td><td>Diverse interne Werte</td><td>-</td><td></td></tr>
</table>

<h3>🌡️ Temperatur‑Rohwerte</h3>

<table>
<tr><th>Dec</th><th>Hex</th><th>Beschreibung</th></tr>
<tr><td>9024</td><td>2360</td><td>Temp raw 1</td></tr>
<tr><td>9025</td><td>2361</td><td>Temp raw 2</td></tr>
<tr><td>9026</td><td>2362</td><td>Temp raw 3</td></tr>
<tr><td>9027</td><td>2363</td><td>Temp raw 4</td></tr>
<tr><td>9028</td><td>2364</td><td>Temp raw 5</td></tr>
<tr><td>9029</td><td>2365</td><td>Temp raw 6</td></tr>
<tr><td>9030</td><td>2366</td><td>Temp raw 7</td></tr>
<tr><td>9031</td><td>2367</td><td>Temp raw 8</td></tr>
</table>

<h3>⚡ Stromlimits</h3>

<table>
<tr><th>Dec</th><th>Hex</th><th>Beschreibung</th><th>Skalierung</th></tr>
<tr><td>9032</td><td>2370</td><td>Charge Limit</td><td>×0.1 A</td></tr>
<tr><td>9033</td><td>2371</td><td>Charge Limit Back</td><td>×0.1 A</td></tr>
<tr><td>9034</td><td>2372</td><td>Discharge Limit</td><td>×0.1 A</td></tr>
</table>

<h3>⚠️ Fehlerflags / Statusbits</h3>
<p>Registerbereich: <strong>9035–9055</strong> (0x2373–0x238F)</p>

</div>

<hr>

</body>
</html>
