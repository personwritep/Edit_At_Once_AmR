// ==UserScript==
// @name        Edit At Once AmR
// @namespace        http://tampermonkey.net/
// @version        2.5
// @description        Edit Entry_ID Page  レトロタイプスキン専用
// @author        Ameba Blog User
// @match        https://ameblo.jp/*
// @match        https://blog.ameba.jp/ucs/entry/srventry*
// @exclude        https://ameblo.jp/*/image*
// @icon        https://www.google.com/s2/favicons?sz=64&domain=ameblo.jp
// @noframes
// @grant        none
// @updateURL        https://github.com/personwritep/Edit_At_Once_AmR/raw/main/Edit_At_Once_AmR.user.js
// @downloadURL        https://github.com/personwritep/Edit_At_Once_AmR/raw/main/Edit_At_Once_AmR.user.js
// ==/UserScript==


let svg_e=
    '<svg class="eaoa_svg" viewBox="-1 -2 26 26">'+
    '<path d="m19.6 9.2-4.9-4.9c-.2-.2-.2-.5 0-.7l1.8-1.8c.4-.4 1-.4 1.4 0L22.1 6c.4.4.4 '+
    '1 0 1.4l-1.8 1.8c-.2.2-.5.2-.7 0zm-7-3.5-8.1 8.1L3 19.7c-.2.7.5 1.4 1.2 1.2l5.8-1.4 '+
    '8.1-8.1c.2-.2.2-.5 0-.7l-4.9-4.9c-.1-.3-.5-.3-.6-.1z"></path></svg>';

let svg_l=
    '<svg class="eaoa_svg" viewBox="0 0 300 300">'+
    '<path d="M85 41C79 42 73 46 71 52C69 56 70 61 74 62C79 63 86 62 91 62L126 '+
    '62C133 62 141 61 147 64C163 73 149 97 170 103C176 104 182 103 188 103L223 '+
    '103C231 103 240 101 246 107C253 114 252 124 252 133L252 189C252 195 252 '+
    '202 252 208C252 211 253 214 257 214C264 213 273 204 274 197C275 189 274 '+
    '179 274 171L274 119C274 109 276 97 269 88C261 79 251 80 241 80L202 80C196 '+
    '80 189 81 183 80C177 78 178 70 178 65C178 57 175 49 169 44C162 39 153 40 145 '+
    '40L106 40C99 40 92 39 85 41M44 81C28 85 28 101 28 114L28 214L28 237C28 243 '+
    '28 248 31 253C42 267 62 263 77 263L173 263L200 263C206 263 213 263 219 '+
    '261C233 256 234 245 234 232L234 159C234 149 236 135 229 127C221 119 211 '+
    '119 201 119L163 119C157 119 150 120 144 119C136 116 138 106 138 100C137 94 '+
    '135 89 130 85C122 79 114 80 105 80L66 80C59 80 51 79 44 81z">'+
    '</path><path d="M59 104C48 107 51 123 51 132L51 209L51 228C51 231 51 234 '+
    '53 237C55 239 60 239 63 239L89 239L171 239L195 239C199 239 203 240 207 '+
    '238C214 235 212 224 212 218L212 165C212 159 214 150 210 145C205 141 193 '+
    '143 187 143L149 143C143 143 135 144 129 143C127 142 125 141 123 140C111 '+
    '130 121 117 113 107C110 103 105 103 100 103L73 103C69 103 63 102 59 104z" '+
    'style="fill:#fff"></path></svg>';

let svg_v=
    '<svg class="eaoa_svg" viewBox="-15 -15 230 230">'+
    '<path d="M8 17C4 19 4 23 4 27C4 36 4 44 4 53L4 148L4 171C4 174 3 179 6 182C9 '+
    '185 14 184 18 184L49 184L148 184L177 184C181 184 187 185 191 183C195 181 '+
    '196 177 196 173C196 164 196 156 196 147L196 52L196 29C196 26 197 21 194 '+
    '18C191 15 186 16 182 16L151 16L50 16L22 16C18 16 12 15 8 17z" ></path>'+
    '<path d="M165 62C150 65 155 89 170 85C185 82 180 58 165 62M19 62L19 '+
    '180L138 180L138 62L19 62z" style="fill:#fff;"></path></svg>';


let zoom_f;
let title=document.title;

let target=document.querySelector('head');
let monitor=new MutationObserver(main);
monitor.observe(target, { childList: true });

main();

function main(){
    let path=location.pathname;
    if(path.includes('/entrylist') || path.includes('/archive') ||
       path.includes('/theme') || path.includes('/amemberentrylist')){ // 記事一覧
        panel_sync();
        menu_set();
        blog_archive(); }
    else if(path.includes('/srventrylist')){ // 記事の編集・削除
        srventrylist(); }
    else if(path.includes('/srventryup') || path.includes('/srventryin')){ // 編集画面
        editor(); }
    else if(document.querySelector('.js-entryWrapper')){ // ブログ画面・アメンバーブログ画面
        panel_sync();
        menu_set();
        blog_page(); }




    function body_wcon_off(){
        if(document.querySelector('#BW_con')){
            document.querySelector('#BW_con').remove(); }}

    function panel_sync(){
        if(title!=document.title){
            title=document.title;
            body_wcon_off(); }} // ページ変更毎にリセット




    function menu_set(){
        let menu=
            '<div id="eao_menu">'+
            '<span class="retouch">'+ svg_e +' 再編集</span>'+
            '<span class="file_list">'+ svg_l +' リスト表示</span>'+
            '<span class="view_page">'+ svg_v +' ブログ</span></div>'+
            '<style>#eao_menu { position: absolute; z-index: 20; font: normal 14px Meiryo; '+
            'padding: 3px 10px 2px; border: 1px solid #dadce0; color: #333; background: #eceff1; '+
            'box-shadow: 4px 4px 2px -2px rgba(0, 0, 0, 0.48); white-space: nowrap; '+
            'cursor: default; display: none; } '+
            '.eaoa_svg { width: 26px; height: 26px; vertical-align: -10px; padding: 2px; '+
            'border: 1px solid #aaa; border-radius: 4px; background: #fff; fill: #000; } '+
            '.file_list, .view_page { margin-left: 12px; } '+
            '#eao_menu span:hover .eaoa_svg { fill: red; } '+
            '#eao_menu.c_active span .eaoa_svg { fill: #90a4ae; } '+
            '#eao_menu.c_active span:hover .eaoa_svg { fill: #0069ff; }</style>';

        if(!document.querySelector('#eao_menu')){
            document.body.insertAdjacentHTML('beforeend', menu); }
    } // menu_set()




    function blog_page(){
        let menu=document.querySelector('#eao_menu');
        let view_page=document.querySelector('.view_page');
        if(view_page){
            view_page.style.display='none'; }

        let article=document.querySelector('.js-entryWrapper'); //記事全体
        let title_h; // 記事タイトル部のh要素
        let ctrl_f=0; // Ctrlキー 押下フラグ


        title_h=call_h();
        if(title_h){
            title_h.setAttribute("onContextmenu", 'return false;'); // コンテキスト非表示
            title_h.addEventListener('contextmenu', function(e){ // 専用メニュー表示
                if(ctrl_f==0){
                    zoom_f=mag_fix();
                    menu.style.display="block";
                    menu.style.left=e.pageX/zoom_f+"px";
                    menu.style.top=e.pageY/zoom_f+"px"; }}); }


        document.addEventListener('keydown', function(event){
            if(event.ctrlKey && event.keyCode!=118){
                ctrl_f=1;
                if(title_h){
                    title_h.removeAttribute("onContextmenu", 'return false;'); }} // コンテキスト表示
            else if(event.ctrlKey && event.keyCode==118){ // Ctrl + F7
                event.preventDefault();
                event.stopImmediatePropagation();
                if(document.querySelector('#BW_con')){
                    body_wcon_off(); }
                else{
                    body_wcon(); }}
            else if(event.shiftKey){
                menu.classList.add('c_active');
                BW_shift(1); }});


        document.addEventListener('keyup', function(event){
            ctrl_f=0;
            if(title_h){
                title_h.setAttribute("onContextmenu", 'return false;'); } // コンテキスト非表示
            menu.classList.remove('c_active');
            BW_shift(0); });


        document.addEventListener('click', function(event){
            menu.style.display="none";
            ctrl_f=0;
            if(title_h){
                title_h.setAttribute("onContextmenu", 'return false;'); }}); // コンテキスト非表示


        let retouch=document.querySelector('.retouch');
        if(retouch){
            edit_do(retouch); }


        let file_list=document.querySelector('.file_list');
        if(file_list){
            list_do(file_list); }


        function BW_shift(n){
            let BW_control=document.querySelector('#BW_control');
            if(BW_control){
                if(n==0){
                    BW_control.classList.remove('c_active'); }
                else{
                    BW_control.classList.add('c_active'); }}}



        function body_wcon(){
            let act=0; // 幅変更　起動時は「0」
            let org_w; // デフォルトの本文幅
            org_w=document.querySelector('#entryBody').getBoundingClientRect().width;
            org_w=Math.round(org_w); // 四捨五入

            let mw=localStorage.getItem('SmartH_I'); // ブログ本文 記録幅値 🔵
            if(!mw){
                mw=360; }
            if(mw>org_w){
                mw=org_w;
                localStorage.setItem('SmartH_I', mw); } // ブログ本文 幅値をセット 🔵


            let help_url="https://ameblo.jp/personwritep/entry-12833160795.html";

            let svg_help=
                '<svg class="BW_help" width="22" height="22" viewBox="0 0 150 150">'+
                '<path d="M66 13C56 15 47 18 39 24C-12 60 18 146 82 137C92 135 102 131 110 '+
                '126C162 90 128 4 66 13M68 25C131 17 145 117 81 125C16 133 3 34 68 25M69 '+
                '40C61 41 39 58 58 61C66 63 73 47 82 57C84 60 83 62 81 65C77 70 52 90 76 '+
                '89C82 89 82 84 86 81C92 76 98 74 100 66C105 48 84 37 69 40M70 94C58 99 66 '+
                '118 78 112C90 107 82 89 70 94z"></path></svg>';

            let control=
                '<div id="BW_con">'+
                '<div id="page_title">　</div>'+
                '<div id="BW_control">'+
                '<span class="BW_e">'+ svg_e +'</span>'+
                '<span class="BW_l">'+ svg_l +'</span>'+
                'ブログ本文幅 <span class="BW_disp BW"></span>'+
                '<input class="BW_set" type="range" min="280" max="'+ org_w + '" value="360">'+
                '<a href="'+ help_url +'" target="_blank" rel="noopener">'+ svg_help +'</a>'+
                '<span class="BW_close BW">✖</span>'+
                '</div>'+
                '<style>'+
                '#BW_con { position: fixed; top: 0; z-index: 4000; width: 100%; font: 16px Meiryo; '+
                'display: flex; justify-content: space-between; align-items: center; color: #000; '+
                'background: #fff; border: 1px solid #aaa; box-shadow: 0 8px 16px #00000040; }'+
                '#page_title { padding: 10px 20px 4px; height: 28px; white-space: nowrap; '+
                'font: normal 21px/26px Meiryo; text-shadow: 1px 1px 2px rgba(0, 0, 0, 0.3); '+
                'background: #f4f6f7; border-right: 1px solid #ccc; position: relative; z-index: 0; } '+
                '#page_title:hover { z-index: 1; } '+
                '#BW_control { position: absolute; right: 0; padding: 5px 15px 3px 20px; '+
                'height: 34px; background: #fff; border-left: 1px solid #ccc; } '+
                '.BW { background: linear-gradient(0, #f1f2f3, transparent); border-radius: 4px; '+
                'cursor: pointer; } '+
                '.BW:hover { background: #fff; } '+
                '.BW_e, .BW_l { margin-right: 15px; cursor: pointer; } '+
                '.BW_e svg, .BW_l svg { background: linear-gradient(0, #f1f2f3, transparent); } '+
                '.BW_e svg:hover, .BW_l svg:hover { fill: red; background: #fff; } '+
                '#BW_control.c_active .eaoa_svg { fill: #90a4ae; } '+
                '#BW_control.c_active .eaoa_svg:hover { fill: #0069ff; } '+
                '.BW_close { margin-left: 20px; padding: 4px 6px 2px; border: 1px solid #aaa; } '+
                '.BW_disp { display: inline-block; width: 60px; padding: 4px 0 2px; '+
                'text-align: center; border: 1px solid #aaa; } '+
                '.BW_disp:hover { border: 1px solid #1976d2; color: #1976d2; } '+
                '.BW_set { width: 120px; vertical-align: -2px; margin: 0 10px; } '+
                '.BW_set:focus { outline: 1px solid #2196f3; outline-offset: 2px; } '+
                '.BW_help { vertical-align: -5px; fill: #2196f3; } '+
                '._35xlqQQK { display: none; } '+
                '</style>'+
                '<style id="BW_style"></style>'+
                '</div>';

            if(!document.querySelector('#BW_con')){
                document.body.insertAdjacentHTML('beforeend', control); }


            let BW_disp=document.querySelector('.BW_disp');
            if(act==0){
                disp_set(org_w, 0); }
            else{
                disp_set(mw, 1); }

            BW_disp.onclick=function(){
                if(act==0){
                    act=1;
                    disp_set(mw, 1); }
                else{
                    act=0;
                    disp_set(org_w, 0); }}


            function disp_set(t_w, n){
                let BW_disp=document.querySelector('.BW_disp');
                BW_disp.textContent=t_w +'px';
                if(n==0){
                    BW_disp.style.fontWeight='normal'; }
                else{
                    BW_disp.style.fontWeight='bold'; }
                let BW_set=document.querySelector('.BW_set');
                BW_set.value=t_w;
                let BW_style=document.querySelector('#BW_style');
                BW_style.textContent=
                    '#entryBody { margin-left: auto; margin-right: auto; width: '+ t_w +'px; }'; }


            let BW_set=document.querySelector('.BW_set');
            let BW_style=document.querySelector('#BW_style');
            BW_set.addEventListener('input', function(){
                mw=BW_set.value;
                act=1;
                disp_set(mw, 1);
                localStorage.setItem('SmartH_I', mw); }); // ブログ本文 幅値をセット 🔵



            let title_text=call_h().textContent; // 記事タイトル
            let page_title=document.querySelector('#page_title');
            if(title_text && page_title){
                page_title.textContent=title_text; } // パネルに記事タイトルを表示


            document.onkeydown=function(event){
                let BW_con=document.querySelector('#BW_con');
                if(BW_con){
                    if(event.keyCode==13){
                        let article=document.querySelector('.js-entryWrapper'); //記事全体
                        if(article){
                            let entry_id=article.getAttribute('data-unique-entry-id');
                            if(entry_id){
                                event.preventDefault();
                                event.stopImmediatePropagation();
                                body_wcon_off();
                                let path=
                                    'https://blog.ameba.jp/ucs/entry/srventryupdateinput.do?id='+
                                    entry_id +'&edit_top='+ to_top();
                                window.open(path, "_blank"); }}}
                    if(event.keyCode==27){
                        event.preventDefault();
                        event.stopImmediatePropagation();
                        body_wcon_off(); }}}


            let BW_close=document.querySelector('.BW_close');
            if(BW_close){
                BW_close.onclick=function(event){
                    event.preventDefault();
                    body_wcon_off(); }}


            let BW_e=document.querySelector('.BW_e');
            if(BW_e){
                edit_do(BW_e); }


            let BW_l=document.querySelector('.BW_l');
            if(BW_l){
                list_do(BW_l); }

        } // body_wcon()



        function edit_do(sw){
            let article=document.querySelector('.js-entryWrapper'); //記事全体
            if(article){
                let entry_id=article.getAttribute('data-unique-entry-id');
                if(entry_id){
                    sw.onclick=function(event){
                        event.preventDefault();
                        let path=
                            'https://blog.ameba.jp/ucs/entry/srventryupdateinput.do?id='+
                            entry_id +'&edit_top='+ to_top();
                        if(!event.shiftKey){
                            window.open(path, "_blank"); }
                        else{
                            window.location.href=path; }
                    }}}} // edit_do()


        function to_top(){
            let entryBody=document.querySelector('#entryBody');
            let body_top=-(entryBody.getBoundingClientRect().top);
            let top;
            if(body_top<-60){
                top=0; }
            else{
                top=Math.round(body_top) +60; }
            return top; }



        function list_do(sw){
            let article=document.querySelector('.js-entryWrapper'); //記事全体
            if(article){
                let entry_id=article.getAttribute('data-unique-entry-id');
                let user=article.getAttribute('data-unique-ameba-id');
                let time=article.querySelector('.date');
                let date;
                let entry_ym;
                if(time){
                    date=time.textContent;
                    entry_ym=date.slice(0, 4) + date.slice(5, 7); }

                if(entry_id && user && entry_ym){
                    sw.onclick=function(event){
                        event.preventDefault();
                        let path=
                            'https://blog.ameba.jp/ucs/entry/srventrylist.do?pageID='+
                            '1&entry_ym='+entry_ym+'&user='+user+'&entry_id='+entry_id;
                        if(!event.shiftKey){
                            window.open(path, "_blank"); }
                        else{
                            window.location.href=path; }
                    }}}} // list_do()



        function call_h(){
            let title_h;
            let article=document.querySelector('.js-entryWrapper'); //記事全体
            if(article){
                if(article.querySelector('h3.title')){
                    title_h=article.querySelector('h3.title'); }} // レトロタイプスキン
            return title_h; }

    } // blog_page()




    function blog_archive(){
        let menu=document.querySelector('#eao_menu');
        let retouch=document.querySelector('.retouch');
        let file_list=document.querySelector('.file_list');
        let view_page=document.querySelector('.view_page');
        if(view_page){
            view_page.style.display='inline'; }

        let ctrl_f=0; // Ctrlキー 押下フラグ
        let ac_list={}; // 記事リスト
        let skin_type=0; // 新タイプ 2 旧タイプ 1 その他 0

        let ac_search=document.querySelector('#recent_entries_list'); // レトロタイプスキン
        if(ac_search){
            skin_type=0;
            ac_list=document.querySelectorAll('#recent_entries_list li'); }

        for(let k=0; k<ac_list.length; k++){
            ac_list[k].setAttribute("onContextmenu", 'return false;'); // コンテキスト非表示
            ac_list[k].addEventListener('contextmenu', function(e){ // 専用メニュー表示
                menu_disp(e, ac_list[k]); }); }


        function menu_disp(event, target){
            if(ctrl_f==0){
                zoom_f=mag_fix();
                menu.style.display="block";
                menu.style.left=event.pageX/zoom_f+"px";
                menu.style.top=event.pageY/zoom_f+"px"; }
            retouch_item(target);
            file_item(target);
            page_item(target); }

        document.addEventListener('keydown', function(event){
            if(event.ctrlKey){
                ctrl_f=1;
                for(let k=0; k<ac_list.length; k++){
                    ac_list[k].removeAttribute("onContextmenu", 'return false;'); }} // コンテキスト表示
            if(event.shiftKey){
                menu.classList.add('c_active'); }});

        document.addEventListener('keyup', function(event){
            ctrl_f=0;
            for(let k=0; k<ac_list.length; k++){
                ac_list[k].setAttribute("onContextmenu", 'return false;'); } // コンテキスト非表示
            menu.classList.remove('c_active'); });

        document.addEventListener('click', function(event){
            menu.style.display="none"; // 専用メニュー非表示
            ctrl_f=0;
            for(let k=0; k<ac_list.length; k++){
                ac_list[k].setAttribute("onContextmenu", 'return false;'); }}); // コンテキスト非表示


        function retouch_item(target){
            retouch.onclick=function(event){
                event.preventDefault();

                let title_link=target.querySelector('.contentTitle');
                let entry_id_a=title_link.getAttribute('href').split('entry-');
                if(entry_id_a[1]){
                    let entry_id=entry_id_a[1].slice(0, 11);
                    if(entry_id){
                        let path=
                            'https://blog.ameba.jp/ucs/entry/srventryupdateinput.do?id='+entry_id;
                        if(!event.shiftKey){
                            window.open(path, "_blank"); }
                        else{
                            window.location.href=path; }}}}}


        function file_item(target){
            file_list.onclick=function(event){
                event.preventDefault();

                let user;
                let entry_id;
                let entry_ym;
                let date;

                date=target.querySelector('.updatetime').textContent;
                let title_link=target.querySelector('.contentTitle');


                let user_a=title_link.getAttribute('href').split('/');
                user=user_a[1];

                let entry_id_a=title_link.getAttribute('href').split('entry-');
                if(date && user && entry_id_a[1]){
                    entry_ym=date.replace(/[^0-9]/g, '').slice(0, 6);
                    entry_id=entry_id_a[1].slice(0, 11);
                    let path=
                        'https://blog.ameba.jp/ucs/entry/srventrylist.do?pageID='+
                        '1&entry_ym='+entry_ym+'&user='+user+'&entry_id='+entry_id;
                    if(!event.shiftKey){
                        window.open(path, "_blank"); }
                    else{
                        window.location.href=path; }}}}


        function page_item(target){
            view_page.onclick=function(event){
                event.preventDefault();

                let title_link=target.querySelector('.contentTitle');
                if(title_link){
                    let path=title_link.getAttribute('href');
                    if(!event.shiftKey){
                        window.open(path, "_blank"); }
                    else{
                        window.location.href=path; }}}}

    } // blog_archive()




    function srventrylist(){
        let arg=new Object;
        let pair=location.search.substring(1).split('&');
        for(let i=0; pair[i]; i++){
            let key=pair[i].split('=');
            arg[key[0]]=key[1]; } // key[0]がkey, key[1]がvalue

        let entry_ym=arg.entry_ym;
        let pageID=parseInt( arg.pageID, 10); // 数値に変換
        let user=arg.user;
        let entry_id=arg.entry_id;

        let amebaId=document.querySelector('#gHeaderRight .amebaId').textContent;
        let entryList_li=document.querySelectorAll('#entryList li');

        if(user!=null){
            if(amebaId!=user){ // 他ユーザーのブログでリスト表示を押した場合
                if(history.length>1){
                    window.history.back(); }
                else{
                    window.close(); }}
            else{
                let k;
                for(k=0; k<entryList_li.length; k++){
                    let entryList_a=entryList_li[k].querySelector('h2 a');
                    if(entryList_a){
                        if(entryList_a.getAttribute('href').indexOf(entry_id)!=-1){
                            entryList_li[k].style.outline='2px solid red';
                            entryList_li[k].style.zIndex='2';
                            entryList_li[k].scrollIntoView({block: "center"});
                            break; }}}
                if(k==entryList_li.length){
                    pageID+=1;
                    let path=
                        'https://blog.ameba.jp/ucs/entry/srventrylist.do?pageID='+
                        pageID+'&entry_ym='+entry_ym+'&user='+user+'&entry_id='+entry_id;
                    window.location.href=path; }}}

    } // srventrylist()




    function editor(){
        if(document.querySelector('.l-form form > .error')){ // 他ユーザで再編集を押した場合
            if(history.length>1){
                window.history.back(); }
            else{
                window.close(); }}


        let searchParams=new URLSearchParams(window.location.search);
        let to_top=searchParams.get('edit_top');
        if(to_top){ //「Edit At Once Am」を使わず編集画面を開いた場合は スクロール動作をしない

            let retry=0;
            let interval=setInterval(wait_target, 20);
            function wait_target(){
                retry++;
                if(retry>200){ // リトライ制限 100回 4secまで
                    clearInterval(interval); }
                let editor_iframe=document.querySelector('.cke_wysiwyg_frame'); // 監視 target
                if(editor_iframe){
                    clearInterval(interval);
                    scroll(editor_iframe); }}


            function scroll(editor_iframe){
                let if_height=editor_iframe.getBoundingClientRect().height;

                let retry=0;
                let interval=setInterval(wait_target, 20);
                function wait_target(){
                    retry++;
                    if(retry>200){ // リトライ制限 100回 4secまで
                        clearInterval(interval); }

                    let body_h=get_height(editor_iframe); // 監視 target
                    if(body_h>if_height){
                        clearInterval(interval);
                        let html=editor_iframe.contentDocument.documentElement;
                        html.scrollTop=to_top; }}

                function get_height(iframe){
                    let f_body=iframe.contentDocument.body;
                    if(f_body){
                        let f_height=f_body.getBoundingClientRect().height;
                        if(f_height){
                            return f_height; }}}
            }} // scroll()

    } // editor()




    function mag_fix(){
        let body=document.body;
        let zoom_f=window.getComputedStyle(body).getPropertyValue('zoom');
        if(!zoom_f){
            zoom_f=1; } // 拡大ツールがない環境の場合
        return zoom_f; }

} // main()
