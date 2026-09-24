<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <title>NÚCLEO - Reator Betavoltaico</title>
    <style>
        body { background: #080000; color: #ff5555; font-family: monospace; display: flex; justify-content: center; align-items: center; min-height: 100vh; margin:0; }
        .hud { border: 2px solid #ff5555; background: rgba(30, 0, 0, 0.8); padding: 25px; width: 440px; border-radius: 8px; box-shadow: 0 0 20px rgba(255, 85, 85, 0.2); }
        h2 { text-align: center; border-bottom: 1px solid #ff5555; padding-bottom: 8px; }
        .warning-panel { border: 1px dashed #ff5555; padding: 10px; background: #1a0000; margin: 15px 0; font-size: 0.9em; text-align: center; }
        .btn-core { width: 100%; padding: 12px; background: #ff5555; border: none; color: #000; font-weight: bold; cursor: pointer; text-transform: uppercase; }
        .btn-core:hover { background: #ff0000; box-shadow: 0 0 15px #ff0000; color: #fff; }
    </style>
</head>
<body>
    <div class="hud">
        <h2>REACTOR // BETAVOLTAIC_CORE</h2>
        <table style="width:100%; margin: 10px 0;">
            <tr><td>Fonte Isótopo:</td><td style="color:#fff;">Diamante C-14</td></tr>
            <tr><td>Produção de Energia:</td><td style="color:#00ff00;">4.2 MW Sustentado</td></tr>
            <tr><td>Temperatura do Núcleo:</td><td id="c-temp" style="color:#fff;">42°C</td></tr>
        </table>
        <div class="warning-panel" id="warn">SISTEMA OPERANDO EM ESTABILIDADE TÉRMICA</div>
        <button class="btn-core" onclick="ejetarNucleo()">Protocolo de Ejeção Crítica</button>
    </div>

    <script>
        function ejetarNucleo() {
            document.getElementById('c-temp').innerText = "SUPERAQUECIMENTO / ESTRUTURA EXPELIDA";
            document.getElementById('c-temp').style.color = "#ff0000";
            const warn = document.getElementById('warn');
            warn.innerText = "PERIGO: NÚCLEO BETAVOLTAICO EJETADO. TRAJE OPERANDO EM SUPER_CAPACITORES DE RESERVA (FALTA DE ENERGIA IMINENTE).";
            warn.style.background = "#ff0000";
            warn.style.color = "#000";
        }
    </script>
</body>
</html>
