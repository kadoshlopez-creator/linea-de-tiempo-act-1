# linea-de-tiempo-act-1
Línea de tiempo interactiva: Origen y evolución del currículo
<!doctype html>
<html lang="es"><head><meta charset="utf-8"><meta name="viewport" content="width=device-width,initial-scale=1">
<title>Origen y evolución del currículo</title>
<style>
:root{--navy:#12304a;--teal:#087e8b;--gold:#e0a526;--paper:#f4f7fa;--ink:#1c2730}
*{box-sizing:border-box}body{margin:0;background:var(--paper);color:var(--ink);font-family:Arial,sans-serif;line-height:1.6}
header{background:linear-gradient(125deg,#12304a,#087e8b);color:white;padding:42px 22px;text-align:center}
header h1{max-width:900px;margin:0 auto 12px;font-size:clamp(1.8rem,4vw,3rem)}header p{max-width:800px;margin:auto}
main{max-width:1050px;margin:28px auto;padding:0 18px}
.timeline{display:flex;flex-wrap:wrap;gap:10px;justify-content:center;margin:24px 0;align-items:center}
.yearbtn{border:2px solid var(--teal);background:white;color:var(--navy);font-weight:bold;padding:12px 16px;border-radius:22px;cursor:pointer;white-space:nowrap}
.yearbtn:hover,.yearbtn:focus{background:var(--gold);color:#17212a;outline:3px solid #f2d28a}
.event{display:none;background:white;border-radius:18px;padding:clamp(20px,4vw,40px);box-shadow:0 8px 28px #12304a18;border-top:6px solid var(--gold)}
.event.active{display:block}.year{color:var(--teal);font-weight:800;font-size:1.2rem}h2{color:var(--navy);margin:.2rem 0 1rem;font-size:clamp(1.4rem,3vw,2rem)}
.impact{background:#eaf5f5;border-left:5px solid var(--teal);padding:12px 18px;margin:20px 0}
.source{font-size:.92rem;color:#465663}.read{background:var(--navy);color:white;border:0;border-radius:8px;padding:12px 16px;cursor:pointer;font-weight:bold}
footer{text-align:center;padding:25px;color:#53616d;font-size:.9rem}

.voicepanel{background:#fff;border-radius:12px;padding:10px 14px;margin:12px 0 18px;box-shadow:0 5px 20px #12304a12;display:flex;align-items:center;gap:10px;flex-wrap:wrap}
.stop{background:#6b2737;color:white;border:0;border-radius:8px;padding:12px 16px;cursor:pointer;font-weight:bold}
.hint{flex-basis:100%;font-size:.9rem;color:#53616d;margin:2px 0}
.yearbtn.speaking{background:var(--gold);border-color:#9b6d00;color:#17212a;box-shadow:0 0 0 4px #e0a52655;transform:translateY(-2px)}
.yearbtn.selected{border-color:var(--navy);box-shadow:0 0 0 2px #12304a30}

.milestone-icon{font-size:2rem;line-height:1.1;margin-bottom:6px}
.event{position:relative;overflow:hidden}
.event.active{animation:slideIn .42s ease both}
@keyframes slideIn{from{opacity:0;transform:translateX(22px)}to{opacity:1;transform:translateX(0)}}
.yearbtn{transition:background .25s ease,color .25s ease,transform .25s ease,box-shadow .25s ease}
.yearbtn.speaking{background:var(--gold)!important;border-color:#9b6d00!important;color:#17212a!important;box-shadow:0 0 0 5px #e0a52655,0 5px 14px #12304a22;transform:scale(1.06)}
.voicepanel{justify-content:space-between;padding:10px 14px}
.voicepanel .hint{flex:1;margin:0}
.source a{color:#087e8b;font-weight:bold;text-decoration:underline}
.source a:hover{color:#12304a}
@media(prefers-reduced-motion:no-preference){.event{animation:fade .25s ease}@keyframes fade{from{opacity:.3;transform:translateY(4px)}to{opacity:1;transform:translateY(0)}}}
</style></head><body>
<header><h1>Origen y evolución del currículo</h1><p>Una mirada histórica desde la teoría curricular moderna hasta los desafíos de la educación premedia y media panameña.</p></header>
<main><p><strong>Cómo explorar:</strong> Si el navegador bloquea el audio, selecciona un año para escuchar su narración. Los hitos internacionales se conectan con la evolución legal e institucional de Panamá.</p>
<nav class="timeline" aria-label="Seleccionar hito histórico">
    <button class="yearbtn" onclick="startTourAt(0)" aria-label="Mostrar hito 1918: La sistematización moderna del currículo">1918</button>
    <button class="yearbtn" onclick="startTourAt(1)" aria-label="Mostrar hito 1946: Ley Orgánica de Educación de Panamá">1946</button>
    <button class="yearbtn" onclick="startTourAt(2)" aria-label="Mostrar hito 1949: Planificación por objetivos">1949</button>
    <button class="yearbtn" onclick="startTourAt(3)" aria-label="Mostrar hito 1972: La educación como derecho constitucional">1972</button>
    <button class="yearbtn" onclick="startTourAt(4)" aria-label="Mostrar hito 1995–1996: Reforma de la Ley Orgánica de Educación">1995–1996</button>
    <button class="yearbtn" onclick="startTourAt(5)" aria-label="Mostrar hito 2000: Normativa para la educación inclusiva">2000</button>
    <button class="yearbtn" onclick="startTourAt(6)" aria-label="Mostrar hito 2010: Transformación curricular de la educación media">2010</button>
    <button class="yearbtn" onclick="startTourAt(7)" aria-label="Mostrar hito 2025–2026: Rediseño y actualización curricular">2025–2026</button>
</nav>
<div class="voicepanel" aria-label="Narración automática">
  <span id="voiceStatus" class="hint" aria-live="polite">La narración comenzará automáticamente en unos segundos.</span>
  <button class="stop" onclick="stopTour()">■ Detener narración</button>
</div>
<section class="event active" id="event0" aria-live="polite">
      <div class="milestone-icon" aria-hidden="true">📘</div><div class="year">1918</div><h2>La sistematización moderna del currículo</h2>
      <p>John Franklin Bobbitt publica The Curriculum en el contexto de la industrialización y la expansión de la escolarización. Propone analizar las actividades sociales y laborales para definir objetivos formativos. Su aporte fue convertir el diseño curricular en un campo de estudio sistemático; su límite fue el énfasis instrumental y la adaptación del estudiante al orden productivo.</p><div class="impact"><strong>Conexión con Panamá actual</strong><p>La educación media puede vincular saberes con la vida y el trabajo, sin reducir la formación a productividad.</p></div>
      <p class="source"><strong>Referencia breve:</strong> Bobbitt, 1918 · <a href="https://archive.org/search?query=John+Franklin+Bobbitt+The+Curriculum+1918" target="_blank" rel="noopener noreferrer">Consultar fuente ↗</a></p>
      <button class="read" onclick="speakEvent(0)">▶ Escuchar narración</button>
    </section>
<section class="event " id="event1" aria-live="polite">
      <div class="milestone-icon" aria-hidden="true">⚖️</div><div class="year">1946</div><h2>Ley Orgánica de Educación de Panamá</h2>
      <p>La Ley 47 de 24 de septiembre de 1946 estableció un marco jurídico general para organizar el sistema educativo panameño, incluyendo la educación secundaria y la administración de los procesos de enseñanza. Surgió en una etapa de consolidación institucional del Estado y dio una base legal duradera al sistema.</p><div class="impact"><strong>Conexión con Panamá actual</strong><p>La planificación curricular panameña requiere coherencia con el derecho a la educación y con las responsabilidades públicas del Estado.</p></div>
      <p class="source"><strong>Referencia breve:</strong> Ley 47 de 1946 · <a href="https://infojuridica.procuraduria-admon.gob.pa/norma_screen?numsec=7768" target="_blank" rel="noopener noreferrer">Consultar fuente ↗</a></p>
      <button class="read" onclick="speakEvent(2)">▶ Escuchar narración</button>
    </section>
<section class="event " id="event2" aria-live="polite">
      <div class="milestone-icon" aria-hidden="true">🎯</div><div class="year">1949</div><h2>Planificación por objetivos</h2>
      <p>Ralph W. Tyler publica Basic Principles of Curriculum and Instruction. Organiza la planificación en torno a propósitos educativos, experiencias de aprendizaje, organización y evaluación. El modelo influyó ampliamente en la elaboración de programas y en la alineación entre objetivos, enseñanza y evaluación.</p><div class="impact"><strong>Conexión con Panamá actual</strong><p>En premedia y media, los objetivos y criterios de evaluación deben ser claros; no obstante, conviene valorar procesos, pensamiento crítico y diversidad de formas de aprender.</p></div>
      <p class="source"><strong>Referencia breve:</strong> Tyler, 1949 · <a href="https://press.uchicago.edu/ucp/books/book/chicago/B/bo3684031.html" target="_blank" rel="noopener noreferrer">Consultar fuente ↗</a></p>
      <button class="read" onclick="speakEvent(1)">▶ Escuchar narración</button>
    </section>
<section class="event " id="event3" aria-live="polite">
      <div class="milestone-icon" aria-hidden="true">🏛️</div><div class="year">1972</div><h2>La educación como derecho constitucional</h2>
      <p>La Constitución Política de Panamá reconoce el derecho a la educación y atribuye al Estado la organización y dirección del servicio público educativo. También incorpora referencias a la identidad étnica y cultural de los pueblos indígenas. El marco constitucional ubica la educación dentro de los deberes públicos y de la vida democrática.</p><div class="impact"><strong>Conexión con Panamá actual</strong><p>El currículo debe contribuir a la ciudadanía, reconocer la diversidad cultural y promover oportunidades educativas sin discriminación.</p></div>
      <p class="source"><strong>Referencia breve:</strong> Constitución Política de Panamá · <a href="https://constitucion.te.gob.pa/constitucion-vigente/" target="_blank" rel="noopener noreferrer">Consultar fuente ↗</a></p>
      <button class="read" onclick="speakEvent(3)">▶ Escuchar narración</button>
    </section>
<section class="event " id="event4" aria-live="polite">
      <div class="milestone-icon" aria-hidden="true">📜</div><div class="year">1995–1996</div><h2>Reforma de la Ley Orgánica de Educación</h2>
      <p>La Ley 34 de 1995 modificó la Ley 47 de 1946 y reforzó principios humanísticos, democráticos, científicos, tecnológicos y vinculados con la cultura nacional. El Texto Único de 1996 ordenó las disposiciones modificadas. La normativa define el currículo como una concreción de políticas educativas que debe adaptarse a los cambios sociales.</p><div class="impact"><strong>Conexión con Panamá actual</strong><p>Da sustento a la actualización curricular, la articulación entre niveles y la pertinencia del aprendizaje para el contexto panameño.</p></div>
      <p class="source"><strong>Referencia breve:</strong> Ley 34 de 1995; Texto Único, 1996 · <a href="https://www.organojudicial.gob.pa/uploads/blogs.dir/3/2019/08/406/ley-34-de-6-de-julio-de-1995.pdf" target="_blank" rel="noopener noreferrer">Consultar fuente ↗</a></p>
      <button class="read" onclick="speakEvent(4)">▶ Escuchar narración</button>
    </section>
<section class="event " id="event5" aria-live="polite">
      <div class="milestone-icon" aria-hidden="true">♿</div><div class="year">2000</div><h2>Normativa para la educación inclusiva</h2>
      <p>El Decreto Ejecutivo n.º 1 de 2000 estableció normas para la atención educativa de estudiantes con necesidades educativas especiales en los subsistemas regular y no regular. Incluyó aspectos de acceso al currículo, adecuaciones, evaluación y promoción. Expresa el avance desde una visión centrada en la segregación hacia la integración en entornos educativos comunes.</p><div class="impact"><strong>Conexión con Panamá actual</strong><p>En premedia y media exige planificar apoyos y ajustes razonables para que la diversidad no se convierta en barrera de participación y aprendizaje.</p></div>
      <p class="source"><strong>Referencia breve:</strong> Decreto Ejecutivo n.º 1 de 2000 · <a href="https://infojuridica.procuraduria-admon.gob.pa/norma_screen?numsec=29458" target="_blank" rel="noopener noreferrer">Consultar fuente ↗</a></p>
      <button class="read" onclick="speakEvent(5)">▶ Escuchar narración</button>
    </section>
<section class="event " id="event6" aria-live="polite">
      <div class="milestone-icon" aria-hidden="true">🧭</div><div class="year">2010</div><h2>Transformación curricular de la educación media</h2>
      <p>MEDUCA impulsó una transformación de la educación media con nuevos bachilleratos, un tronco común y orientación hacia el aprendizaje por competencias. La reforma buscó que el alumnado no solo recordara información, sino que pudiera aplicarla en situaciones concretas. Su implementación requirió actualización docente, materiales y evaluación coherente.</p><div class="impact"><strong>Conexión con Panamá actual</strong><p>Refuerza la articulación entre competencias, saberes disciplinares y preparación para estudios superiores, ciudadanía y trabajo.</p></div>
      <p class="source"><strong>Referencia breve:</strong> MEDUCA; cobertura periodística de la reforma, 2010 · <a href="https://www.prensa.com/politica/inicia-periodo-escolar_0_2788971090.html" target="_blank" rel="noopener noreferrer">Consultar fuente ↗</a></p>
      <button class="read" onclick="speakEvent(6)">▶ Escuchar narración</button>
    </section>
<section class="event " id="event7" aria-live="polite">
      <div class="milestone-icon" aria-hidden="true">🤖</div><div class="year">2025–2026</div><h2>Rediseño y actualización curricular</h2>
      <p>En 2025, MEDUCA informó avances de un proceso de rediseño para la Educación Básica General y Media, con revisión de asignaturas y bachilleratos. Entre los ejes comunicados se mencionaron formación integral, salud mental, emprendimiento, inteligencia artificial y lectura y escritura. La propuesta evidencia que el currículo es dinámico y debe responder a cambios sociales y tecnológicos.</p><div class="impact"><strong>Conexión con Panamá actual</strong><p>El reto es integrar innovación y alfabetización digital sin descuidar lectura, ciencias, ciudadanía, inclusión, identidad cultural y brechas de acceso.</p></div>
      <p class="source"><strong>Referencia breve:</strong> MEDUCA, 2025 · <a href="https://www.meduca.gob.pa/avance-del-rediseno-curricular-un-nuevo-enfoque-para-el-aprendizaje/" target="_blank" rel="noopener noreferrer">Consultar fuente ↗</a></p>
      <button class="read" onclick="speakEvent(7)">▶ Escuchar narración</button>
    </section>
</main><footer>Universidad del Istmo | Actividad N° 1 - Asignatura: Currículo en la Educación Premedia y Media </br>Profesor Tutor: Msc. Santiago Ureña | Estudiante: Carlos E. López S. | C.I.P.: 8-751-544</br> Consulta las fuentes y contrasta la normativa vigente antes de aplicar sus disposiciones.</footer>
<script>
const narrations=['1918. La sistematización moderna del currículo. John Franklin Bobbitt publica su obra "El Currículo", en el contexto de la industrialización y la expansión escolar. Él propone analizar las actividades sociales y laborales para definir objetivos formativos. Su gran aporte fue convertir el diseño curricular en un campo de estudio sistemático, mientras que su límite fue el énfasis instrumental y la adaptación del estudiante al orden productivo. Conexión con el Panamá actual: la educación media puede vincular los saberes con la vida y el trabajo, sin reducir la formación a la simple productividad.',
'1946: Ley Orgánica de Educación de Panamá. La Ley 47, del 24 de septiembre de 1946, estableció un marco jurídico general para organizar el sistema educativo panameño, incluyendo la educación secundaria y la administración de los procesos de enseñanza. Surgió en una etapa de consolidación institucional del Estado, y dio una base legal duradera al sistema. Conexión con el Panamá actual: la planificación curricular panameña requiere total coherencia con el derecho a la educación y con las responsabilidades públicas del Estado.',
'1949: Planificación por objetivos. Ralph Tyler publica los "Principios Básicos del Currículo e Instrucción". Su obra organiza la planificación en torno a propósitos educativos, experiencias de aprendizaje, organización y evaluación. Este modelo influyó ampliamente en la elaboración de programas y en la alineación entre objetivos, enseñanza y evaluación. Conexión con el Panamá actual: en la premedia y la media, los objetivos y criterios de evaluación deben ser claros. No obstante, conviene valorar los procesos, el pensamiento crítico y la diversidad de formas de aprender.',
'1972: La educación como derecho constitucional. La Constitución Política de Panamá reconoce el derecho a la educación, y atribuye al Estado la organización y dirección del servicio público educativo. También incorpora referencias a la identidad étnica y cultural de los pueblos indígenas. Este marco constitucional ubica a la educación dentro de los deberes públicos y de la vida democrática. Conexión con el Panamá actual: el currículo debe contribuir a la ciudadanía, reconocer la diversidad cultural y promover oportunidades educativas sin discriminación.',
'Entre 1995 y 1996: Reforma de la Ley Orgánica de Educación. La Ley 34 de 1995 modificó la Ley 47 de 1946, y reforzó los principios humanísticos, democráticos, científicos, tecnológicos y vinculados con la cultura nacional. El Texto Único de 1996 ordenó las disposiciones modificadas. Esta normativa define al currículo como una concreción de políticas educativas que debe adaptarse a los cambios sociales. Conexión con el Panamá actual: da sustento a la actualización curricular, la articulación entre niveles y la pertinencia del aprendizaje para el contexto panameño.',
'2000: Normativa para la educación inclusiva. El Decreto Ejecutivo número uno del año 2000 estableció normas para la atención educativa de estudiantes con necesidades educativas especiales, en los subsistemas regular y no regular. Incluyó aspectos de acceso al currículo, adecuaciones, evaluación y promoción. Esto expresa el avance desde una visión centrada en la segregación, hacia la integración en entornos educativos comunes. Conexión con el Panamá actual: en la premedia y la media, exige planificar apoyos y ajustes razonables para que la diversidad no se convierta en una barrera de participación y aprendizaje.',
'2010: Transformación curricular de la educación media. El Ministerio de Educación impulsó una transformación de la educación media con nuevos bachilleratos, un tronco común y una orientación hacia el aprendizaje por competencias. La reforma buscó que el alumnado no solo recordara información, sino que pudiera aplicarla en situaciones concretas. Su implementación requirió actualización docente, materiales y una evaluación coherente. Conexión con el Panamá actual: refuerza la articulación entre competencias, saberes disciplinares y la preparación para los estudios superiores, la ciudadanía y el trabajo.',
'Entre 2025 y 2026: Rediseño y actualización curricular. En 2025, el Ministerio de Educación informó los avances de un proceso de rediseño para la Educación Básica General y Media, con una revisión de asignaturas y bachilleratos. Entre los ejes comunicados se mencionaron la formación integral, la salud mental, el emprendimiento, la inteligencia artificial, la lectura y la escritura. La propuesta evidencia que el currículo es dinámico y debe responder a los cambios sociales y tecnológicos. Conexión con el Panamá actual: el reto es integrar la innovación y la alfabetización digital, sin descuidar la lectura, las ciencias, la ciudadanía, la inclusión, la identidad cultural y las brechas de acceso.'];
let voices = [];
let preferredVoice = null;
let tourRunning = false;
let currentIndex = 0;
let currentUtterance = null;

function loadVoices() {
  if (!('speechSynthesis' in window)) {
    document.getElementById('voiceStatus').textContent = 'Este navegador no ofrece narración automática.';
    return;
  }
  voices = speechSynthesis.getVoices().filter(v => /^es([_-]|$)/i.test(v.lang));
   
  if (!voices.length) return;
  voices.sort((a,b) => {
    const score = v => (/Google|Microsoft/i.test(v.name) ? 3 : 0) +
      (/es-MX|es-PA|es-US|es-CO|es-ES/i.test(v.lang) ? 2 : 0) +
      (/natural|neural|online/i.test(v.name) ? 4 : 0);
    return score(b)-score(a);
  });
  // Se selecciona automáticamente la voz española con mayor probabilidad de sonar natural.
  preferredVoice = voices.find(v => /natural|neural|online/i.test(v.name)) ||
    voices.find(v => /Google|Microsoft/i.test(v.name)) ||
    voices.find(v => /es-MX|es-PA|es-US|es-CO/i.test(v.lang)) || voices[0];
}
if ('speechSynthesis' in window) {
  loadVoices();
  speechSynthesis.onvoiceschanged = loadVoices;
}

function showEvent(n) {
  document.querySelectorAll('.event').forEach(e => e.classList.remove('active'));
  document.getElementById('event'+n).classList.add('active');
  document.querySelectorAll('.yearbtn').forEach((b,i) => {
    b.classList.toggle('selected', i === n);
    b.setAttribute('aria-current', i === n ? 'step' : 'false');
  });
  currentIndex = n;
}
function setSpeaking(n, on) {
  document.querySelectorAll('.yearbtn').forEach((b,i) => b.classList.toggle('speaking', on && i === n));
  const status = document.getElementById('voiceStatus');
  if (on) status.textContent = `Narrando el hito ${narrations[n].split('.')[0]}…`;
}
function speakEvent(n) {
  if (!('speechSynthesis' in window)) {
    alert('La narración automática no está disponible en este navegador.');
    return;
  }
  tourRunning = false;
  speechSynthesis.cancel();
  currentIndex = n;
  showEvent(n);
  speakOne(n, false);
}
function speakOne(n, continueTour) {
  if (!('speechSynthesis' in window)) return;
  showEvent(n);
  setSpeaking(n, true);
  const u = new SpeechSynthesisUtterance(narrations[n]);
  const voice = preferredVoice || voices.find(v => /es-MX|es-PA|es-US|es-CO/i.test(v.lang)) || voices[0];
  if (voice) {
    u.voice = voice;
    u.lang = voice.lang;
  } else {
    u.lang = 'es-ES';
  }
  // Un ritmo moderado y tono ligeramente más cálido suele sonar menos mecánico.
  u.rate = 0.88;
  u.pitch = 1.04;
  u.volume = 1;
  currentUtterance = u;
  u.onend = () => {
    setSpeaking(n, false);
    currentUtterance = null;
    if (continueTour && tourRunning) {
      if (n < narrations.length - 1) {
        currentIndex = n + 1;
        showEvent(currentIndex);
        window.setTimeout(() => {
          if (tourRunning) speakOne(currentIndex, true);
        }, 700);
      } else {
        tourRunning = false;
        document.getElementById('voiceStatus').textContent = 'Recorrido completo. Has escuchado todos los hitos.';
      }
    }
  };
  u.onerror = () => {
    setSpeaking(n, false);
    currentUtterance = null;
    document.getElementById('voiceStatus').textContent = 'Para activar el audio, haz clic en uno de los años. Después la narración avanzará automáticamente.';
    tourRunning = false;
  };
  speechSynthesis.speak(u);
}
function startTourAt(n) {
  if (!('speechSynthesis' in window)) {
    document.getElementById('voiceStatus').textContent = 'Este navegador no admite narración automática.';
    return;
  }
  speechSynthesis.cancel();
  tourRunning = true;
  currentIndex = n;
  showEvent(n);
  speakOne(n, true);
}
function startTour() {
  if (!('speechSynthesis' in window)) {
    alert('Este navegador no permite narración automática.');
    return;
  }
  speechSynthesis.cancel();
  tourRunning = true;
  currentIndex = 0;
  showEvent(0);
  speakOne(0, true);
}
function stopTour() {
  tourRunning = false;
  if ('speechSynthesis' in window) speechSynthesis.cancel();
  document.querySelectorAll('.yearbtn').forEach(b => b.classList.remove('speaking'));
  currentUtterance = null;
  document.getElementById('voiceStatus').textContent = 'Narración detenida. Selecciona un año para continuar.';
}

window.addEventListener('load', () => {
  // Espera breve para que el navegador cargue sus voces antes de iniciar.
  window.setTimeout(() => {
    if ('speechSynthesis' in window) startTour();
    else document.getElementById('voiceStatus').textContent = 'Este navegador no admite narración automática. Prueba Chrome o Edge y haz clic en un año para activar el audio.';
  }, 2000);
});
</script></body></html>
