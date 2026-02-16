      <div class="out-box" id="utj-out"><span class="ph">Результат появится здесь...</span></div>
      <button class="copy-btn" onclick="copyBox('utj-out')">COPY</button>
    </div>
  </div>
</div>

<!-- 3. ОБФУСКАЦИЯ -->
<div class="card" id="card-obf">
  <div class="card-head" onclick="toggle('card-obf')">
    <div class="icon-box" style="background:#f8fafc">🔒</div>
    <div class="card-meta">
      <div class="card-name" data-ru="ОБФУСКАЦИЯ КОДА" data-en="CODE OBFUSCATION">ОБФУСКАЦИЯ КОДА</div>
      <div class="card-sub" data-ru="Защитить JS · совместимо с QuickJS v2" data-en="Protect JS · QuickJS v2 compatible">Защитить JS · совместимо с QuickJS v2</div>
    </div>
    <span class="chevron">&#8964;</span>
  </div>
  <div class="card-body">
    <textarea id="obf-in" rows="6" placeholder="// JS код для Minecraft аддона&#10;function onPlayerJoin(player) {&#10;  player.sendMessage('Добро пожаловать!');&#10;}"></textarea>
    <div class="pills">
      <span class="pill on" data-g="obf-level" onclick="setPill(this,'obf-level')">Лёгкая</span>
      <span class="pill" data-g="obf-level" onclick="setPill(this,'obf-level')">Средняя</span>
      <span class="pill" data-g="obf-level" onclick="setPill(this,'obf-level')">Сильная</span>
    </div>
    <div class="row">
      <button class="btn btn-red" onclick="obfuscate()">&#9654; ОБФУСЦИРОВАТЬ</button>
      <button class="btn btn-ghost" onclick="clearCard('obf')">&#10005; Очистить</button>
    </div>
    <div class="status" id="obf-st"></div>
    <div class="lbl">РЕЗУЛЬТАТ</div>
    <div class="out-wrap">
      <div class="out-box" id="obf-out"><span class="ph">Результат появится здесь...</span></div>
      <button class="copy-btn" onclick="copyBox('obf-out')">COPY</button>
    </div>
  </div>
</div>

<!-- 4. ДЕОБФУСКАЦИЯ -->
<div class="card" id="card-dob">
  <div class="card-head" onclick="toggle('card-dob')">
    <div class="icon-box" style="background:#f0fdf6">🔓</div>
    <div class="card-meta">
      <div class="card-name" data-ru="ДЕОБФУСКАЦИЯ КОДА" data-en="CODE DEOBFUSCATION">ДЕОБФУСКАЦИЯ КОДА</div>
      <div class="card-sub" data-ru="Восстановить читаемый вид кода" data-en="Restore readable code form">Восстановить читаемый вид кода</div>
    </div>
    <span class="chevron">&#8964;</span>
  </div>
  <div class="card-body">
    <textarea id="dob-in" rows="6" placeholder="// Вставьте обфусцированный JS код..."></textarea>
    <div class="row">
      <button class="btn btn-red" onclick="deobfuscate()">&#9654; ДЕОБФУСЦИРОВАТЬ</button>
      <button class="btn btn-ghost" onclick="clearCard('dob')">&#10005; Очистить</button>
    </div>
    <div class="status" id="dob-st"></div>
    <div class="lbl">РЕЗУЛЬТАТ</div>
    <div class="out-wrap">
      <div class="out-box" id="dob-out"><span class="ph">Результат появится здесь...</span></div>
      <button class="copy-btn" onclick="copyBox('dob-out')">COPY</button>
    </div>
  </div>
</div>

<!-- 5. МИНИФИКАЦИЯ -->
<div class="card" id="card-min">
  <div class="card-head" onclick="toggle('card-min')">
    <div class="icon-box" style="background:#eff6ff">&#9889;</div>
    <div class="card-meta">
      <div class="card-name" data-ru="МИНИФИКАЦИЯ КОДА" data-en="CODE MINIFICATION">МИНИФИКАЦИЯ КОДА</div>
      <div class="card-sub" data-ru="Уменьшить размер JS / JSON файлов" data-en="Reduce file size of JS / JSON">Уменьшить размер JS / JSON файлов</div>
    </div>
    <span class="chevron">&#8964;</span>
  </div>
  <div class="card-body">
    <div class="pills">
      <span class="pill on" data-g="min-type" onclick="setPill(this,'min-type')">JavaScript</span>
      <span class="pill" data-g="min-type" onclick="setPill(this,'min-type')">JSON</span>
    </div>
    <textarea id="min-in" rows="6" placeholder="// Вставьте код для минификации..."></textarea>
    <div class="row">
      <button class="btn btn-red" onclick="minify()">&#9654; МИНИФИЦИРОВАТЬ</button>
      <button class="btn btn-ghost" onclick="clearCard('min')">&#10005; Очистить</button>
    </div>
    <div class="status" id="min-st"></div>
    <div class="lbl">РЕЗУЛЬТАТ</div>
    <div class="out-wrap">
      <div class="out-box" id="min-out"><span class="ph">Результат появится здесь...</span></div>
      <button class="copy-btn" onclick="copyBox('min-out')">COPY</button>
    </div>
  </div>
</div>

<!-- 6. ФОРМАТИРОВАНИЕ -->
<div class="card" id="card-fmt">
  <div class="card-head" onclick="toggle('card-fmt')">
    <div class="icon-box" style="background:#faf5ff">&#10022;</div>
    <div class="card-meta">
      <div class="card-name" data-ru="ФОРМАТИРОВАНИЕ КОДА" data-en="CODE FORMATTING">ФОРМАТИРОВАНИЕ КОДА</div>
      <div class="card-sub" data-ru="Красиво отформатировать JS / JSON" data-en="Prettify JS / JSON code">Красиво отформатировать JS / JSON</div>
    </div>
    <span class="chevron">&#8964;</span>
  </div>
  <div class="card-body">
    <div class="pills">
      <span class="pill on" data-g="fmt-type" onclick="setPill(this,'fmt-type')">JSON</span>
      <span class="pill" data-g="fmt-type" onclick="setPill(this,'fmt-type')">JavaScript</span>
    </div>
    <textarea id="fmt-in" rows="6" placeholder='{"a":1,"b":[1,2,3],"c":{"nested":true}}'></textarea>
    <div class="row">
      <span class="lbl" style="align-self:center">ОТСТУП</span>
      <select id="fmt-indent" style="width:auto;flex:0">
        <option value="2">2 пробела</option>
        <option value="4">4 пробела</option>
        <option value="	">Tab</option>
      </select>
      <button class="btn btn-red" onclick="formatCode()">&#9654; ФОРМАТИРОВАТЬ</button>
      <button class="btn btn-ghost" onclick="clearCard('fmt')">&#10005;</button>
    </div>
    <div class="status" id="fmt-st"></div>
    <div class="lbl">РЕЗУЛЬТАТ</div>
    <div class="out-wrap">
      <div class="out-box" id="fmt-out"><span class="ph">Результат появится здесь...</span></div>
      <button class="copy-btn" onclick="copyBox('fmt-out')">COPY</button>
    </div>
  </div>
</div>

<!-- 7. UUID ГЕНЕРАТОР -->
<div class="card" id="card-uuid">
  <div class="card-head" onclick="toggle('card-uuid')">
    <div class="icon-box" style="background:#fff1f2">&#127922;</div>
    <div class="card-meta">
      <div class="card-name" data-ru="UUID ГЕНЕРАТОР" data-en="UUID GENERATOR">UUID ГЕНЕРАТОР</div>
      <div class="card-sub" data-ru="UUID v4 для manifest.json Minecraft аддонов" data-en="UUID v4 for Minecraft addon manifest.json">UUID v4 для manifest.json Minecraft аддонов</div>
    </div>
    <span class="chevron">&#8964;</span>
  </div>
  <div class="card-body">
    <div class="row">
      <span class="lbl" style="align-self:center">КОЛ-ВО</span>
      <select id="uuid-count" style="width:auto;flex:0">
        <option>1</option><option selected>2</option><option>4</option><option>8</option>
      </select>
      <button class="btn btn-red" onclick="genUUIDs()">&#9654; ГЕНЕРИРОВАТЬ</button>
      <button class="btn btn-ghost" onclick="copyAllUUIDs()">&#8856; ВСЕ</button>
    </div>
    <div class="uuid-list" id="uuid-list">
      <div class="status">Нажмите «Генерировать»...</div>
    </div>
    <div class="divider">MANIFEST.JSON ШАБЛОН</div>
    <div class="out-wrap">
      <div class="out-box" style="min-height:180px" id="uuid-manifest"><span class="ph">Сначала сгенерируйте UUID...</span></div>
      <button class="copy-btn" onclick="copyBox('uuid-manifest')">COPY</button>
    </div>
  </div>
</div>

</main>

<footer>
  <div><span class="mc-tag"><span class="mc-dot"></span>Minecraft Bedrock &middot; QuickJS v2</span></div>
  Multi Tools &mdash; Набор разработчика аддонов
</footer>

<div class="toast" id="toast"></div>

<script>

const S={lang:'ru'};
const pillState={};
let uuidStore=[];

// ── LANG ──
const NAV_RU=['JSON→UNI','UNI→JSON','ОБФУСКАЦИЯ','ДЕОБФУСКАЦИЯ','МИНИФИКАЦИЯ','ФОРМАТИРОВАНИЕ','UUID GEN'];
const NAV_EN=['JSON→UNI','UNI→JSON','OBFUSCATE','DEOBFUSCATE','MINIFY','FORMAT','UUID GEN'];
function setLang(l){
  S.lang=l;
  document.querySelectorAll('.lang-btn').forEach(b=>b.classList.toggle('on',b.textContent===l.toUpperCase()));
  document.getElementById('tagline').textContent=l==='ru'
    ?'Универсальный набор разработчика · Minecraft Bedrock Edition'
    :'Universal Developer Toolkit · Minecraft Bedrock Edition';
  document.querySelectorAll('[data-ru]').forEach(el=>el.textContent=el.dataset[l]);
  document.querySelectorAll('.nav-pill').forEach((p,i)=>p.textContent=(l==='ru'?NAV_RU:NAV_EN)[i]);
}

// ── TOGGLE ──
function toggle(id){document.getElementById(id).classList.toggle('open')}

// ── PILLS ──
function setPill(el,group){
  el.closest('.pills').querySelectorAll('.pill').forEach(p=>p.classList.remove('on'));
  el.classList.add('on');
  pillState[group]=[...el.closest('.pills').querySelectorAll('.pill')].indexOf(el);
}
function getPill(group){return pillState[group]||0}

// ── TOAST ──
function toast(msg){
  const t=document.getElementById('toast');
  t.textContent=msg;t.classList.add('show');
  clearTimeout(t._t);t._t=setTimeout(()=>t.classList.remove('show'),2000);
}

// ── STATUS ──
function st(id,ok,msg){
  const el=document.getElementById(id+'-st');
  if(el)el.innerHTML=ok?`<span class="ok">✓</span>&nbsp;${msg}`:`<span class="er">✕</span>&nbsp;${msg}`;
}

// ── OUTPUT ──
function setOut(id,text){
  const box=document.getElementById(id+'-out');
  box.textContent=text;
  const btn=document.createElement('button');
  btn.className='copy-btn';btn.textContent='COPY';
  btn.onclick=()=>copyBox(id+'-out');
  box.appendChild(btn);
}

function clearCard(id){
  const inp=document.getElementById(id+'-in');
  if(inp)inp.value='';
  const out=document.getElementById(id+'-out');
  if(out){out.innerHTML=`<span class="ph">Результат появится здесь...</span>`;addCopyBtn(out,id+'-out');}
  const s=document.getElementById(id+'-st');
  if(s)s.innerHTML='';
}

function addCopyBtn(box,boxId){
  const btn=document.createElement('button');
  btn.className='copy-btn';btn.textContent='COPY';
  btn.onclick=()=>copyBox(boxId);
  box.appendChild(btn);
}

// ── COPY BOX ──
function copyBox(boxId){
  const box=document.getElementById(boxId);
  let text='';
  box.childNodes.forEach(n=>{if(n.nodeType===3)text+=n.textContent;});
  if(!text.trim())text=box.innerText.replace(/^COPY\n?/,'').trim();
  navigator.clipboard.writeText(text.trim())
    .then(()=>toast(S.lang==='ru'?'✓ Скопировано!':'✓ Copied!'))
    .catch(()=>{});
}

// ══ 1. JSON → UNICODE ══
function jsonToUnicode(){
  const inp=document.getElementById('jtu-in').value;
  if(!inp.trim())return st('jtu',false,'Введите текст или JSON');
  try{
    const cyrOnly=getPill('jtu-mode')===1;
    const result=inp.replace(cyrOnly?/[\u0400-\u04FF]/g:/[\u0080-\uffff]/g,
      c=>'\\u'+c.charCodeAt(0).toString(16).padStart(4,'0'));
    setOut('jtu',result);
    st('jtu',true,`${inp.length} → ${result.length} символов`);
  }catch(e){st('jtu',false,e.message);}
}

// ══ 2. UNICODE → JSON ══
function unicodeToJson(){
  const inp=document.getElementById('utj-in').value;
  if(!inp.trim())return st('utj',false,'Введите строку с \\uXXXX');
  try{
    const result=inp.replace(/\\u([0-9a-fA-F]{4})/g,(_,h)=>String.fromCharCode(parseInt(h,16)));
    setOut('utj',result);
    st('utj',true,`${inp.length} → ${result.length} символов`);
  }catch(e){st('utj',false,e.message);}
}

// ══ 3. ОБФУСКАЦИЯ ══
function stripComments(c){return c.replace(/\/\/[^\n]*/g,'').replace(/\/\*[\s\S]*?\*\//g,'').trim();}

function obfLight(code){
  let c=stripComments(code);
  const map={};let n=0;
  const gen=()=>{let s='_$',x=n++;do{s+=String.fromCharCode(97+x%26);x=Math.floor(x/26);}while(x>0);return s;};
  const defs=new Set();
  c.replace(/\b(?:let|const|var|function)\s+([a-zA-Z_$][a-zA-Z0-9_$]*)/g,(_,nm)=>defs.add(nm));
  defs.forEach(nm=>{if(!map[nm])map[nm]=gen();});
  defs.forEach(nm=>{c=c.replace(new RegExp('\\b'+nm+'\\b','g'),map[nm]);});
  return c.replace(/[ \t]{2,}/g,' ').replace(/\n\s*\n/g,'\n');
}
function obfMedium(code){
  let c=obfLight(code);
  c=c.replace(/('(?:[^'\\]|\\.)*'|"(?:[^"\\]|\\.)*")/g,m=>{
    const q=m[0],inner=m.slice(1,-1);
    const hex=[...inner].map(ch=>'\\x'+ch.charCodeAt(0).toString(16).padStart(2,'0')).join('');
    return q+hex+q;
  });
  return c.replace(/\s*([{}();,=+\-*/<>!&|?:\[\]])\s*/g,'$1').replace(/\s+/g,' ').trim();
}
function obfHeavy(code){
  const med=obfMedium(code);
  const b64=btoa(unescape(encodeURIComponent(med)));
  return `eval(decodeURIComponent(escape(atob("${b64}"))))`;
}
function obfuscate(){
  const code=document.getElementById('obf-in').value.trim();
  if(!code)return st('obf',false,'Введите JS код');
  try{
    const lvl=getPill('obf-level');
    let result=lvl===0?obfLight(code):lvl===1?obfMedium(code):obfHeavy(code);
    setOut('obf',result);
    const names=['Лёгкая','Средняя','Сильная'];
    st('obf',true,`Уровень: ${names[lvl]} · ${code.length} → ${result.length} байт`);
  }catch(e){st('obf',false,e.message);}
}

// ══ 4. ДЕОБФУСКАЦИЯ ══
function jsBeautify(code){
  let depth=0,out='',i=0;
  const ind=()=>'  '.repeat(Math.max(0,depth));
  while(i<code.length){
    const c=code[i];
    if(c==='{'){out+=c+'\n';depth++;out+=ind();}
    else if(c==='}'){depth=Math.max(0,depth-1);out=out.trimEnd()+'\n'+ind()+c;}
    else if(c===';'){out+=c+'\n'+ind();}
    else{out+=c;}
    i++;
  }
  return out.replace(/\n\s*\n/g,'\n').trim();
}
function deobfuscate(){
  const code=document.getElementById('dob-in').value.trim();
  if(!code)return st('dob',false,'Введите обфусцированный код');
  try{
    let r=code;
    const m1=r.match(/eval\(decodeURIComponent\(escape\(atob\("([^"]+)"\)\)\)\)/);
    if(m1)r=decodeURIComponent(escape(atob(m1[1])));
    r=r.replace(/\\x([0-9a-fA-F]{2})/g,(_,h)=>String.fromCharCode(parseInt(h,16)));
    r=r.replace(/\\u([0-9a-fA-F]{4})/g,(_,h)=>String.fromCharCode(parseInt(h,16)));
    r=jsBeautify(r);
    setOut('dob',r);
    st('dob',true,'Деобфусцировано (частичное восстановление)');
  }catch(e){st('dob',false,'Ошибка: '+e.message);}
}

// ══ 5. МИНИФИКАЦИЯ ══
function minify(){
  const code=document.getElementById('min-in').value.trim();
  if(!code)return st('min',false,'Введите код');
  try{
    let result;
    if(getPill('min-type')===1){
      result=JSON.stringify(JSON.parse(code));
    }else{
      result=code
        .replace(/\/\/[^\n]*/g,'')
        .replace(/\/\*[\s\S]*?\*\//g,'')
        .replace(/\s*([{}();,=+\-*/<>!&|?:\[\]])\s*/g,'$1')
        .replace(/\s+/g,' ').trim();
    }
    const pct=(100*(1-result.length/code.length)).toFixed(1);
    setOut('min',result);
    st('min',true,`${code.length} → ${result.length} байт · −${pct}%`);
  }catch(e){st('min',false,e.message);}
}

// ══ 6. ФОРМАТИРОВАНИЕ ══
function formatCode(){
  const code=document.getElementById('fmt-in').value.trim();
  if(!code)return st('fmt',false,'Введите код');
  const indVal=document.getElementById('fmt-indent').value;
  const ind=indVal==='\t'?'\t':' '.repeat(Number(indVal));
  try{
    let result;
    if(getPill('fmt-type')===0){
      result=JSON.stringify(JSON.parse(code),null,ind);
    }else{
      result=jsBeautify(code);
    }
    setOut('fmt',result);
    st('fmt',true,`Отформатировано · ${result.split('\n').length} строк`);
  }catch(e){st('fmt',false,e.message);}
}

// ══ 7. UUID ══
function uuidv4(){
  return 'xxxxxxxx-xxxx-4xxx-yxxx-xxxxxxxxxxxx'.replace(/[xy]/g,c=>{
    const r=crypto.getRandomValues(new Uint8Array(1))[0]&15;
    return(c==='x'?r:(r&0x3|0x8)).toString(16);
  });
}
function genUUIDs(){
  const count=Number(document.getElementById('uuid-count').value);
  uuidStore=Array.from({length:count},uuidv4);
  const list=document.getElementById('uuid-list');
  list.innerHTML='';
  uuidStore.forEach(u=>{
    const row=document.createElement('div');
    row.className='uuid-row';
    row.innerHTML=`<span>${u}</span><button onclick="cpText('${u}')" title="Copy">&#8856;</button>`;
    list.appendChild(row);
  });
  const h=uuidStore[0]||uuidv4();
  const m=uuidStore[1]||uuidv4();
  const manifest=JSON.stringify({
    format_version:2,
    header:{description:"My Addon",name:"My Addon",uuid:h,version:[1,0,0],min_engine_version:[1,20,0]},
    modules:[{description:"Behaviour Pack",type:"data",uuid:m,version:[1,0,0]}]
  },null,2);
  const box=document.getElementById('uuid-manifest');
  box.textContent=manifest;
  addCopyBtn(box,'uuid-manifest');
  toast(S.lang==='ru'?`✓ ${count} UUID сгенерировано`:`✓ ${count} UUIDs generated`);
}
function copyAllUUIDs(){
  if(!uuidStore.length)return toast('Сначала генерируйте UUID');
  navigator.clipboard.writeText(uuidStore.join('\n')).then(()=>toast('✓ Все UUID скопированы'));
}
function cpText(text){
  navigator.clipboard.writeText(text).then(()=>toast('✓ UUID скопирован'));
}

// open first card
document.getElementById('card-jtu').classList.add('open');
</script>
</body>
</html>
