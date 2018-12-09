### ９九将棋

1. 概要  
JavaScript製将棋プログラムです。  
弱いＡＩ機能付き、人対人、人対ＡＩ、ＡＩ対ＡＩの対戦が可能です。ＡＩのレベルは２段階です。  
二ヶ国語（日本語、英語）対応。ブラウザの言語設定によって表示される言語が変わります。デフォルトは英語ですので日本語と英語以外が優先されているブラウザでは英語で表示されますが、日本語を優先しているブラウザであれば日本語表示されます。プログラム内で使用している文言は一箇所にまとめているので、他の言語に対応するのも容易だと思います。

1. インストール  
zipファイルを解凍してブラウザでindex.htmlを読み込んでください。

1. カスタマイズ  
    1. 駒のカスタマイズ  
    駒は全てsvgファイルで、盤上の駒（img/\*.svg）と持ち駒（css/\*.svg）があります。画像ファイルは使用していませんので、駒の見た目を変えたい場合は実行するPCにインストールされているフォントを指定することで変更することが出来ます。以下は先手の歩（img/f_fu.svg）だけを`sans-serif`から`monospace`に変更した場合の表示例です。
![駒の表示変更例][sample6_png]
    1. 言語カスタマイズ  
    プログラム内で使用しているメッセージはindex.htmlの上部に言語別に定義されているので、言語コードと翻訳語のブロックを追加すれば他の言語にも対応可能です。

---
        .init({
            lng: lng,
            fallbackLng: 'en',
            debug: true,
            resources: {
                en: {
                    translation: {
                        title: '99 Shogi（9x9 shogi）',
                        btn_first: 'Black',
                        btn_second: 'White',
                        btn_start: 'New Game',
                        btn_stop: 'Interrupt',
                        menu_title: 'Settings',
                        menu_turn: 'Turn',
                        menu_first: 'Black',
                        menu_second: 'White',
                        menu_person: 'Man',
                        menu_ai: 'AI',
                        menu_level: 'AI Level',
                        menu_beginner: 'Novice',
                        menu_average: 'Intermediate',
                        menu_longtime: 'Senior',
                        menu_meditation: 'Expert',
                        menu_placement: 'Initial Placement',
                        menu_about: 'About 99 Shogi',
                        dlg_promote: 'Promote?',
                        dlg_promote_yes: 'Promote',
                        dlg_promote_no: 'Not promote',
                        dlg_interrupt: 'Interrupt?',
                        dlg_interrupt_yes: 'Interrupt',
                        dlg_interrupt_no: 'Back',
                        dlg_check: 'The king is in check!',
                        dlg_utifudume: 'Utifudume!',
                        msgBlack: 'Black',
                        msgWhite: 'White',
                        msgTurn: '%s turn ',
                        msgEvaluate: '(Evaluation:%s)',
                        msgWinner: '%s Win',
                        msgRestart: 'Restart',
                        msgInterrupt: 'Interrupt',
                        msgFirstWin: 'Black Win',
                        msgSecondWin: 'White Win',
                        msgSennitite: 'Repetition Draw',
                        msgThinking: 'thinking...',
                        dlg2_exitTitle: 'Application Menu',
                        dlg2_exitItemYes: 'Exit',
                        dlg2_exitItemNo: 'Cancel',
                        dlg2_exit: 'Exit Application ?',
                        menu_description_html: 'It is a Shogi.'
                    }
                },
                ja: {
                    translation: {
                        title: '９九将棋（9x9 shogi）',
                        btn_first: '先手',
                        btn_second: '後手',
                        btn_start: '新規対局',
                        btn_stop: '中断',
                        menu_title: '設定',
                        menu_turn: '先手・後手',
                        menu_first: '先手',
                        menu_second: '後手',
                        menu_person: '人',
                        menu_ai: 'ＡＩ',
                        menu_level: 'ＡＩレベル',
                        menu_beginner: '弱い',
                        menu_average: '普通',
                        menu_longtime: '長考',
                        menu_meditation: '瞑想',
                        menu_placement: '初期配置',
                        menu_about: '「９九将棋」について',
                        dlg_promote: '成りますか？',
                        dlg_promote_yes: '成る',
                        dlg_promote_no: '成らない',
                        dlg_interrupt: '中断しますか？',
                        dlg_interrupt_yes: '中断',
                        dlg_interrupt_no: '戻る',
                        dlg_check: '玉が取られてしまいます',
                        dlg_utifudume: '打ち歩詰めです',
                        msgBlack: '先手',
                        msgWhite: '後手',
                        msgTurn: '%sの番です',
                        msgEvaluate: '（評価値:%s）',
                        msgWinner: '%sの勝ちです',
                        msgRestart: '再開',
                        msgInterrupt: '中断',
                        msgFirstWin: '先手の勝ちです',
                        msgSecondWin: '後手の勝ちです',
                        msgSennitite: '千日手です',
                        msgThinking: '考え中...',
                        dlg2_exitTitle: '終了メニュー',
                        dlg2_exitItemYes: '終了',
                        dlg2_exitItemNo: 'キャンセル',
                        dlg2_exit: 'アプリを終了しますか？',
        　　　　　　　　menu_description_html: 'JavaScript製将棋アプリです。'
                    }
                }
            }
        });

---


[sample6_png]:./sample6.png


