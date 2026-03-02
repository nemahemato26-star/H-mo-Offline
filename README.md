<!DOCTYPE html>
<html lang="ar" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Hémo-Offline | خريطة المصلحة</title>
    <style>
        body { font-family: sans-serif; background-color: #f0f4f8; margin: 0; padding: 20px; }
        h1 { text-align: center; color: #2c3e50; }
        .ward-container { display: grid; grid-template-columns: repeat(auto-fit, minmax(280px, 1fr)); gap: 20px; }
        .room { background: white; border-radius: 12px; padding: 15px; box-shadow: 0 4px 6px rgba(0,0,0,0.1); border-top: 5px solid #3498db; }
        .room-title { font-weight: bold; font-size: 1.2em; margin-bottom: 15px; color: #2980b9; border-bottom: 1px solid #eee; padding-bottom: 5px; }
        .beds { display: flex; justify-content: space-between; gap: 10px; }
        .bed { flex: 1; background: #ecf0f1; padding: 15px; border-radius: 8px; text-align: center; cursor: pointer; transition: 0.3s; border: 1px solid #dcdde1; }
        .bed:hover { background: #dff9fb; transform: translateY(-2px); }
        .bed-label { display: block; font-size: 0.8em; color: #7f8c8d; }
        .patient-name { font-weight: bold; color: #2c3e50; display: block; margin-top: 5px; }
        .btn-passation { display: block; width: 100%; max-width: 400px; margin: 30px auto; padding: 15px; background: #27ae60; color: white; border: none; border-radius: 30px; font-size: 1.1em; font-weight: bold; cursor: pointer; text-align: center; }
    </style>
</head>
<body>

    <h1>مصلحة أمراض الدم - Hémo-Offline</h1>

    <div class="ward-container">
        <script>
            for(let i=1; i<=6; i++) {
                document.write(`
                    <div class="room">
                        <div class="room-title">غرفة رقم ${i}</div>
                        <div class="beds">
                            <div class="bed"><span class="bed-label">سرير A</span><span class="patient-name">فارغ</span></div>
                            <div class="bed"><span class="bed-label">سرير B</span><span class="patient-name">فارغ</span></div>
                        </div>
                    </div>
                `);
            }
        </script>
    </div>

    <button class="btn-passation">تسجيل تسليم المناوبة (Passation)</button>

</body>
</html>
