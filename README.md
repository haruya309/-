<!DOCTYPE html>
<html lang="ja">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>表作成が爆速になる！オートフィル＆書式コピーの使い方</title>
    <style>
        @media print {
            body { margin: 0; }
            .page-break { page-break-before: always; }
        }
        
        body {
            font-family: 'Noto Sans JP', 'Hiragino Sans', 'Yu Gothic', sans-serif;
            line-height: 1.6;
            color: #333;
            max-width: 210mm;
            margin: 0 auto;
            padding: 20px;
            background-color: #fff;
        }
        
        .header {
            text-align: center;
            margin-bottom: 40px;
            padding: 30px 0;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            color: white;
            border-radius: 15px;
        }
        
        .header h1 {
            font-size: 28px;
            margin: 0 0 10px 0;
            font-weight: bold;
        }
        
        .header .subtitle {
            font-size: 16px;
            opacity: 0.9;
        }
        
        .section {
            margin: 30px 0;
            padding: 25px;
            background: #f8f9ff;
            border-radius: 10px;
            border-left: 5px solid #667eea;
        }
        
        .section h2 {
            color: #667eea;
            font-size: 22px;
            margin: 0 0 20px 0;
            display: flex;
            align-items: center;
        }
        
        .section h2::before {
            content: "✨";
            margin-right: 10px;
        }
        
        .technique-box {
            background: white;
            padding: 20px;
            border-radius: 8px;
            margin: 20px 0;
            box-shadow: 0 2px 8px rgba(0,0,0,0.1);
        }
        
        .technique-title {
            color: #764ba2;
            font-size: 20px;
            font-weight: bold;
            margin-bottom: 15px;
            display: flex;
            align-items: center;
        }
        
        .technique-title::before {
            content: "🚀";
            margin-right: 8px;
        }
        
        .step-list {
            background: #fff;
            padding: 20px;
            border-radius: 8px;
            border: 2px solid #e8f2ff;
            margin: 15px 0;
        }
        
        .step {
            margin: 15px 0;
            padding: 15px;
            background: linear-gradient(90deg, #f8f9ff 0%, #ffffff 100%);
            border-radius: 8px;
            border-left: 4px solid #667eea;
        }
        
        .step-number {
            background: #667eea;
            color: white;
            width: 30px;
            height: 30px;
            border-radius: 50%;
            display: inline-flex;
            align-items: center;
            justify-content: center;
            font-weight: bold;
            margin-right: 15px;
            font-size: 14px;
        }
        
        .step-content {
            display: inline-block;
            vertical-align: top;
            width: calc(100% - 50px);
        }
        
        .tip-box {
            background: #fff9e6;
            border: 2px solid #ffd700;
            padding: 20px;
            border-radius: 10px;
            margin: 20px 0;
        }
        
        .tip-box h3 {
            color: #ff8c00;
            margin: 0 0 10px 0;
            display: flex;
            align-items: center;
        }
        
        .tip-box h3::before {
            content: "💡";
            margin-right: 8px;
        }
        
        .warning-box {
            background: #fff5f5;
            border: 2px solid #ff6b6b;
            padding: 20px;
            border-radius: 10px;
            margin: 20px 0;
        }
        
        .warning-box h3 {
            color: #d63031;
            margin: 0 0 10px 0;
            display: flex;
            align-items: center;
        }
        
        .warning-box h3::before {
            content: "⚠️";
            margin-right: 8px;
        }
        
        .example-box {
            background: #f0fff4;
            border: 2px solid #00c851;
            padding: 20px;
            border-radius: 10px;
            margin: 20px 0;
        }
        
        .example-box h3 {
            color: #00695c;
            margin: 0 0 15px 0;
            display: flex;
            align-items: center;
        }
        
        .example-box h3::before {
            content: "📝";
            margin-right: 8px;
        }
        
        .shortcut {
            background: #667eea;
            color: white;
            padding: 8px 15px;
            border-radius: 20px;
            font-weight: bold;
            display: inline-block;
            margin: 5px 5px 5px 0;
            font-size: 14px;
        }
        
        .time-save {
            background: linear-gradient(135deg, #ff6b6b, #ffa500);
            color: white;
            padding: 15px;
            border-radius: 10px;
            text-align: center;
            font-weight: bold;
            margin: 20px 0;
            font-size: 18px;
        }
        
        .footer {
            text-align: center;
            margin-top: 40px;
            padding: 20px;
            background: #f8f9ff;
            border-radius: 10px;
            color: #666;
        }
        
        ul, ol {
            padding-left: 20px;
        }
        
        li {
            margin: 8px 0;
        }
        
        strong {
            color: #667eea;
        }
        
        .highlight {
            background: #fff3cd;
            padding: 2px 6px;
            border-radius: 4px;
            font-weight: bold;
        }
    </style>
</head>
<body>
    <div class="header">
        <h1>表作成が爆速になる！</h1>
        <div class="subtitle">オートフィル＆書式コピーの使い方完全マスター</div>
    </div>

    <div class="section">
        <h2>なぜ手入力は時間の無駄なのか？</h2>
        <p>多くのExcel初心者が陥る最大の落とし穴、それが<strong>「1つずつ手入力」</strong>です。</p>
        
        <div class="time-save">
            手入力：30分 → オートフィル：3分<br>
            <span style="font-size: 14px;">なんと驚異の10倍時短！</span>
        </div>
        
        <p>日報作成、顧客リスト管理、売上表作成...これらすべてでオートフィルを使えば、作業時間を劇的に短縮できます。</p>
    </div>

    <div class="section">
        <h2>オートフィル基本テクニック</h2>
        
        <div class="technique-box">
            <div class="technique-title">連続データの自動入力</div>
            
            <div class="step-list">
                <div class="step">
                    <span class="step-number">1</span>
                    <div class="step-content">
                        <strong>開始値を入力</strong><br>
                        A1セルに「1」、A2セルに「2」を入力
                    </div>
                </div>
                
                <div class="step">
                    <span class="step-number">2</span>
                    <div class="step-content">
                        <strong>範囲を選択</strong><br>
                        A1からA2までをドラッグして選択
                    </div>
                </div>
                
                <div class="step">
                    <span class="step-number">3</span>
                    <div class="step-content">
                        <strong>フィルハンドルをドラッグ</strong><br>
                        選択範囲の右下角にある小さな■をドラッグ
                    </div>
                </div>
            </div>
            
            <div class="tip-box">
                <h3>プロの超時短テクニック</h3>
                <p>フィルハンドルを<strong>ダブルクリック</strong>すると、隣接する列のデータがある最後の行まで自動でフィルできます！数百行でも一瞬で完了。</p>
            </div>
        </div>
        
        <div class="technique-box">
            <div class="technique-title">日付の連続入力</div>
            
            <div class="example-box">
                <h3>実践例：日報の日付欄作成</h3>
                <ul>
                    <li>A1に「2024/1/1」を入力</li>
                    <li>フィルハンドルをドラッグ</li>
                    <li>→ 自動で「2024/1/2」「2024/1/3」...と1年分も瞬時に完成！</li>
                </ul>
            </div>
            
            <div class="step-list">
                <div class="step">
                    <span class="step-number">1</span>
                    <div class="step-content">
                        <strong>基準日付を入力</strong><br>
                        任意のセルに日付を入力（例：2024/5/1）
                    </div>
                </div>
                
                <div class="step">
                    <span class="step-number">2</span>
                    <div class="step-content">
                        <strong>セルを選択してドラッグ</strong><br>
                        フィルハンドルを下方向にドラッグ
                    </div>
                </div>
            </div>
            
            <div class="tip-box">
                <h3>応用テクニック</h3>
                <p>「月曜日」と入力してドラッグすると、曜日の連続データも作成可能！平日のみのスケジュール表作成に便利。</p>
            </div>
        </div>
    </div>

    <div class="section">
        <h2>書式コピーで見た目も統一</h2>
        
        <div class="technique-box">
            <div class="technique-title">書式のコピー＆ペースト</div>
            
            <div class="step-list">
                <div class="step">
                    <span class="step-number">1</span>
                    <div class="step-content">
                        <strong>コピー元を選択</strong><br>
                        書式をコピーしたいセル（見出しなど）を選択
                    </div>
                </div>
                
                <div class="step">
                    <span class="step-number">2</span>
                    <div class="step-content">
                        <strong>書式のコピー</strong><br>
                        <span class="shortcut">Ctrl + C</span> でコピー
                    </div>
                </div>
                
                <div class="step">
                    <span class="step-number">3</span>
                    <div class="step-content">
                        <strong>ペースト先を選択</strong><br>
                        書式を適用したい範囲を選択
                    </div>
                </div>
                
                <div class="step">
                    <span class="step-number">4</span>
                    <div class="step-content">
                        <strong>形式を選択して貼り付け</strong><br>
                        <span class="shortcut">Ctrl + Shift + V</span> → 「書式」を選択
                    </div>
                </div>
            </div>
        </div>
        
        <div class="technique-box">
            <div class="technique-title">書式ペイント機能（超おすすめ！）</div>
            
            <div class="step-list">
                <div class="step">
                    <span class="step-number">1</span>
                    <div class="step-content">
                        <strong>書式元を選択</strong><br>
                        コピーしたい書式のセルをクリック
                    </div>
                </div>
                
                <div class="step">
                    <span class="step-number">2</span>
                    <div class="step-content">
                        <strong>書式ペイントをクリック</strong><br>
                        ホームタブの「書式ペイント」ボタン（刷毛のアイコン）をクリック
                    </div>
                </div>
                
                <div class="step">
                    <span class="step-number">3</span>
                    <div class="step-content">
                        <strong>適用先をクリック</strong><br>
                        書式を適用したいセルや範囲をクリック
                    </div>
                </div>
            </div>
            
            <div class="tip-box">
                <h3>連続適用の神テクニック</h3>
                <p>書式ペイントボタンを<strong>ダブルクリック</strong>すると、複数箇所に連続で適用可能！終了は<span class="shortcut">Esc</span>キー。表全体の統一が一瞬で完了します。</p>
            </div>
        </div>
    </div>

    <div class="section">
        <h2>実践的な活用例</h2>
        
        <div class="example-box">
            <h3>日報テンプレートの作成（30分→3分）</h3>
            <ol>
                <li><strong>日付列</strong>：「2024/5/1」からオートフィルで1ヶ月分自動生成</li>
                <li><strong>曜日列</strong>：「月曜日」からオートフィルで自動生成</li>
                <li><strong>書式統一</strong>：ヘッダー行の書式を全体にコピー</li>
                <li><strong>完成</strong>：美しく統一された日報テンプレートが瞬時に完成！</li>
            </ol>
        </div>
        
        <div class="example-box">
            <h3>顧客管理リストの効率化</h3>
            <ol>
                <li><strong>連番</strong>：「No.1」「No.2」からオートフィルで数百件も一瞬</li>
                <li><strong>書式コピー</strong>：見出し行の書式を全体に適用</li>
                <li><strong>日付管理</strong>：契約日、更新日も自動で連続入力</li>
            </ol>
        </div>
        
        <div class="example-box">
            <h3>売上表の作成</h3>
            <ol>
                <li><strong>月度管理</strong>：「2024年1月」からオートフィルで年間分</li>
                <li><strong>計算式</strong>：「=B2*C2」も自動でコピーされる</li>
                <li><strong>書式統一</strong>：数値の桁区切りや色分けを一括適用</li>
            </ol>
        </div>
    </div>

    <div class="section">
        <h2>よくある失敗とその対策</h2>
        
        <div class="warning-box">
            <h3>失敗例1：想定外のパターンになる</h3>
            <p><strong>症状</strong>：「1, 2」が「1, 2, 1, 2」の繰り返しになる<br>
            <strong>原因</strong>：Excelが独自のパターンを判断<br>
            <strong>対策</strong>：オートフィルオプションで「連続データ」を明示的に選択</p>
        </div>
        
        <div class="warning-box">
            <h3>失敗例2：書式が崩れる</h3>
            <p><strong>症状</strong>：色や罫線がバラバラになる<br>
            <strong>原因</strong>：データと書式を同時にコピーしている<br>
            <strong>対策</strong>：「形式を選択して貼り付け」で書式のみを選択</p>
        </div>
        
        <div class="warning-box">
            <h3>失敗例3：フィルハンドルが見つからない</h3>
            <p><strong>症状</strong>：右下に■が表示されない<br>
            <strong>原因</strong>：セルの選択範囲が不適切<br>
            <strong>対策</strong>：単一セルを正確に選択し、右下角にマウスを合わせる（カーソルが+になればOK）</p>
        </div>
    </div>

    <div class="section">
        <h2>応用テクニック</h2>
        
        <div class="technique-box">
            <div class="technique-title">カスタム連続データの作成</div>
            <p>「営業部」「経理部」「総務部」のような独自のリストも作成可能！</p>
            
            <div class="step-list">
                <div class="step">
                    <span class="step-number">1</span>
                    <div class="step-content">
                        ファイル → オプション → 詳細設定
                    </div>
                </div>
                
                <div class="step">
                    <span class="step-number">2</span>
                    <div class="step-content">
                        「ユーザー設定リストの編集」をクリック
                    </div>
                </div>
                
                <div class="step">
                    <span class="step-number">3</span>
                    <div class="step-content">
                        独自のリストを登録して完了
                    </div>
                </div>
            </div>
        </div>
        
        <div class="technique-box">
            <div class="technique-title">数式のオートフィル</div>
            <p>計算式も自動でコピー可能！相対参照で自動調整されます。</p>
            
            <div class="example-box">
                <h3>売上計算の例</h3>
                <p>C2に「=A2*B2」（単価×個数）を入力してオートフィルすると<br>
                自動で「=A3*B3」「=A4*B4」...に変換。数百行でも一瞬で計算完了！</p>
            </div>
        </div>
        
        <div class="technique-box">
            <div class="technique-title">条件付きオートフィル</div>
            <p>平日のみ、特定の曜日のみなど、条件に応じたフィルも可能です。</p>
            
            <div class="tip-box">
                <h3>平日のみの日付作成</h3>
                <p>月曜日の日付を入力 → オートフィルオプションで「平日の入力」を選択 → 土日を除いた平日のみの日付が自動生成！</p>
            </div>
        </div>
    </div>

    <div class="section">
        <h2>便利なショートカット一覧</h2>
        
        <div class="technique-box">
            <div class="technique-title">覚えておきたいキー操作</div>
            
            <div style="display: grid; grid-template-columns: 1fr 1fr; gap: 15px; margin: 20px 0;">
                <div>
                    <span class="shortcut">Ctrl + D</span><br>
                    <small>上のセルの内容を下にコピー</small>
                </div>
                
                <div>
                    <span class="shortcut">Ctrl + R</span><br>
                    <small>左のセルの内容を右にコピー</small>
                </div>
                
                <div>
                    <span class="shortcut">Ctrl + Shift + V</span><br>
                    <small>形式を選択して貼り付け</small>
                </div>
                
                <div>
                    <span class="shortcut">Ctrl + 1</span><br>
                    <small>セルの書式設定を開く</small>
                </div>
                
                <div>
                    <span class="shortcut">Ctrl + Shift + End</span><br>
                    <small>データ範囲の最後まで選択</small>
                </div>
                
                <div>
                    <span class="shortcut">F4</span><br>
                    <small>直前の操作を繰り返す</small>
                </div>
            </div>
        </div>
    </div>

    <div class="section">
        <h2>時短効果まとめ</h2>
        
        <div class="time-save">
            🕐 従来の手入力作業：30分<br>
            ⚡ オートフィル活用後：3分<br>
            <br>
            💰 時給換算で90%のコストカット！<br>
            📈 月20時間の作業時間短縮効果
        </div>
        
        <div class="tip-box">
            <h3>今日から実践すべき3つのポイント</h3>
            <ul>
                <li><strong>日報作成</strong>：必ずオートフィルで日付と連番を自動化</li>
                <li><strong>書式設定</strong>：一度作ったらコピーで統一（手作業禁止）</li>
                <li><strong>意識改革</strong>：「手入力できること＝自動化できること」と考える</li>
            </ul>
        </div>
        
        <div class="example-box">
            <h3>明日から変わる！作業効率化チェックリスト</h3>
            <ul>
                <li>☑️ 連続データは必ずオートフィルを使う</li>
                <li>☑️ 書式コピーでデザインを統一する</li>
                <li>☑️ フィルハンドルのダブルクリックを覚える</li>
                <li>☑️ ショートカットキーを1日1つ覚える</li>
                <li>☑️ 同じ作業を2回繰り返したら自動化を検討する</li>
            </ul>
        </div>
    </div>
    <div class="footer">
        <p><strong>🎉 おめでとうございます！</strong></p>
        <p>これでオートフィル＆書式コピーの基本から応用まで完全マスターしました。<br>
        明日からの作業効率が劇的にアップし、残業時間の大幅削減も期待できます！</p>
        <br>
        <p style="font-size: 14px; color: #888;">
        このテクニックを活用して、より生産的で充実したExcelライフを送ってください。<br>
        浮いた時間で、本当に大切な業務に集中しましょう！
        </p>
    </div>
</body>
</html>
