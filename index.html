<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8" />
<title>Virtual Museum</title>
<meta name="viewport" content="width=device-width, initial-scale=1" />
<style>
  html, body { margin:0; padding:0; overflow:hidden; height:100%; background:#0a0908; font-family: 'Georgia', 'Times New Roman', serif; }
  canvas { display:block; }

  #crosshair {
    position:fixed; top:50%; left:50%; width:6px; height:6px;
    margin:-3px 0 0 -3px; border-radius:50%;
    background:rgba(255,255,255,0.85); pointer-events:none; z-index:5;
    box-shadow:0 0 3px rgba(0,0,0,0.8);
  }

  #hint {
    position:fixed; left:50%; bottom:28px; transform:translateX(-50%);
    color:#e9e2d3; font-size:14px; letter-spacing:0.02em;
    background:rgba(15,12,10,0.55); padding:8px 16px; border-radius:20px;
    pointer-events:none; z-index:5; opacity:0; transition:opacity .25s ease;
  }
  #hint.show { opacity:1; }

  #caption {
    position:fixed; left:50%; bottom:60px; transform:translateX(-50%);
    text-align:center; color:#f3ecdd; z-index:6; pointer-events:none;
    opacity:0; transition:opacity .35s ease;
    background:rgba(10,9,8,0.6); padding:14px 26px; border-radius:6px;
    border:1px solid rgba(230,210,170,0.25);
    max-width:70vw;
  }
  #caption.show { opacity:1; }
  #caption .t { font-size:20px; letter-spacing:0.03em; margin-bottom:4px; }
  #caption .s { font-size:13px; color:#c9bfa8; font-style:italic; }

  #overlay {
    position:fixed; inset:0; background:radial-gradient(circle at 50% 40%, #241d16, #0a0908 75%);
    display:flex; align-items:center; justify-content:center; flex-direction:column;
    z-index:20; color:#f3ecdd; text-align:center; cursor:pointer;
  }
  #overlay h1 { font-weight:400; letter-spacing:0.12em; font-size:34px; margin:0 0 10px; }
  #overlay p { color:#c9bfa8; font-size:15px; max-width:480px; line-height:1.6; margin:6px 0; }
  #overlay .enter {
    margin-top:22px; padding:12px 34px; border:1px solid rgba(230,210,170,0.5);
    border-radius:2px; letter-spacing:0.08em; font-size:14px;
  }
  #overlay.hidden { display:none; }

  #loading {
    position:fixed; inset:0; background:#0a0908; z-index:30;
    display:flex; align-items:center; justify-content:center; color:#c9bfa8;
    font-size:14px; letter-spacing:0.1em;
  }
</style>
</head>
<body>

<div id="loading">LOADING GALLERY…</div>

<div id="overlay" class="hidden">
  <h1>THE GALLERY</h1>
  <p>Walk through the rooms with <b>W A S D</b> and look around with the mouse.
     Approach a painting and click it for a closer look - click again (or press Esc) to step back.</p>
  <div class="enter">CLICK TO ENTER</div>
</div>

<div id="crosshair"></div>
<div id="hint">Click to view</div>
<div id="caption"><div class="t"></div><div class="s"></div></div>

<script type="importmap">
{
  "imports": {
    "three": "https://cdn.jsdelivr.net/npm/three@0.160.0/build/three.module.js",
    "three/addons/": "https://cdn.jsdelivr.net/npm/three@0.160.0/examples/jsm/"
  }
}
</script>

<script type="module">
import * as THREE from 'three';
import { PointerLockControls } from 'three/addons/controls/PointerLockControls.js';

/* ---------------------------------------------------------------------
   CONFIG — swap artwork by replacing files in ./images/ named
   img1.jpg, img2.jpg, ... imgN.jpg (any count; they are reused/cycled
   across every frame in the museum). Keep similar portrait aspect
   ratios  900x1200) 
--------------------------------------------------------------------- */
const IMAGE_COUNT = 12;
const IMAGE_PATH = i => `images/img${((i - 1) % IMAGE_COUNT) + 1}.jpg`;
const TITLES = ['Hoa Lo','Interior','Chained','Departure',
                'Inhumane','Artileries','Independence','Strategy',
                'Communist','Supply Trail','Despair','Victory'];
const TITLE_FOR = i => TITLES[(i - 1) % TITLES.length];

const WALL_H = 4;
const WALL_T = 0.3;
const EYE_H = 1.65;
const PLAYER_R = 0.35;

/* ---------------------------------------------------------------------
   SCENE / RENDERER / CAMERA
--------------------------------------------------------------------- */
const scene = new THREE.Scene();
scene.background = new THREE.Color(0x0b0a09);
scene.fog = new THREE.Fog(0x0b0a09, 14, 34);

const camera = new THREE.PerspectiveCamera(70, window.innerWidth / window.innerHeight, 0.1, 200);
camera.position.set(0, EYE_H, 3);

const renderer = new THREE.WebGLRenderer({ antialias: true });
renderer.setPixelRatio(Math.min(window.devicePixelRatio, 2));
renderer.setSize(window.innerWidth, window.innerHeight);
renderer.shadowMap.enabled = true;
renderer.shadowMap.type = THREE.PCFSoftShadowMap;
renderer.outputColorSpace = THREE.SRGBColorSpace;
document.body.appendChild(renderer.domElement);

window.addEventListener('resize', () => {
  camera.aspect = window.innerWidth / window.innerHeight;
  camera.updateProjectionMatrix();
  renderer.setSize(window.innerWidth, window.innerHeight);
});

/* ---------------------------------------------------------------------
   LIGHTING
--------------------------------------------------------------------- */
scene.add(new THREE.HemisphereLight(0x9fa8b8, 0x2a2420, 0.55));

const sun = new THREE.DirectionalLight(0xfff3e0, 0.5);
sun.position.set(6, 10, 4);
sun.castShadow = true;
sun.shadow.mapSize.set(2048, 2048);
sun.shadow.camera.left = -16; sun.shadow.camera.right = 16;
sun.shadow.camera.top = 16; sun.shadow.camera.bottom = -16;
sun.shadow.camera.far = 40;
scene.add(sun);

/* ---------------------------------------------------------------------
   MATERIALS
--------------------------------------------------------------------- */
const floorMat = new THREE.MeshStandardMaterial({ color: 0x4a3a2c, roughness: 0.85, metalness: 0.05 });
const ceilMat  = new THREE.MeshStandardMaterial({ color: 0xece6da, roughness: 0.95 });
const wallMat  = new THREE.MeshStandardMaterial({ color: 0xdcd3c2, roughness: 0.9 });
const frameMat = new THREE.MeshStandardMaterial({ color: 0x1c140c, roughness: 0.5, metalness: 0.3 });

/* ---------------------------------------------------------------------
   ROOMS — floors / ceilings (axis-aligned rectangles)
--------------------------------------------------------------------- */
const rooms = [
  { x: [-6, 6],  z: [-5, 5]   },  // Entrance Hall
  { x: [-6, 6],  z: [-11, -5] }, // North Gallery
  { x: [6, 14],  z: [-5, 5]   }, // East Gallery
];

for (const r of rooms) {
  const w = r.x[1] - r.x[0], d = r.z[1] - r.z[0];
  const cx = (r.x[0] + r.x[1]) / 2, cz = (r.z[0] + r.z[1]) / 2;

  const floor = new THREE.Mesh(new THREE.PlaneGeometry(w, d), floorMat);
  floor.rotation.x = -Math.PI / 2;
  floor.position.set(cx, 0, cz);
  floor.receiveShadow = true;
  scene.add(floor);

  const ceil = new THREE.Mesh(new THREE.PlaneGeometry(w, d), ceilMat);
  ceil.rotation.x = Math.PI / 2;
  ceil.position.set(cx, WALL_H, cz);
  scene.add(ceil);
}

/* ---------------------------------------------------------------------
   WALLS — each entry: fixed axis + coordinate, running range, optional gap
--------------------------------------------------------------------- */
const wallDefs = [
  { axis: 'z', at: 5,   range: [-6, 6]  },            // Hall south (entrance wall)
  { axis: 'x', at: -6,  range: [-5, 5]  },            // Hall west
  { axis: 'z', at: -5,  range: [-6, 6],  gap: [-1.5, 1.5] }, // Hall/NorthGallery divider
  { axis: 'x', at: 6,   range: [-5, 5],  gap: [-1.5, 1.5] }, // Hall/EastGallery divider
  { axis: 'z', at: -11, range: [-6, 6]  },            // North Gallery far wall
  { axis: 'x', at: -6,  range: [-11, -5] },           // North Gallery west
  { axis: 'x', at: 6,   range: [-11, -5] },           // North Gallery east
  { axis: 'x', at: 14,  range: [-5, 5]  },            // East Gallery far wall
  { axis: 'z', at: -5,  range: [6, 14]  },            // East Gallery north
  { axis: 'z', at: 5,   range: [6, 14]  },            // East Gallery south
];

const collisionSegments = []; // {x1,z1,x2,z2}

function buildWallSegment(axis, at, a, b) {
  const len = b - a;
  if (len <= 0.05) return;
  let w, d, cx, cz;
  if (axis === 'z') { // runs along x, thin in z
    w = len; d = WALL_T; cx = (a + b) / 2; cz = at;
    collisionSegments.push({ x1: a, z1: at, x2: b, z2: at });
  } else { // axis === 'x', runs along z, thin in x
    w = WALL_T; d = len; cx = at; cz = (a + b) / 2;
    collisionSegments.push({ x1: at, z1: a, x2: at, z2: b });
  }
  const mesh = new THREE.Mesh(new THREE.BoxGeometry(w, WALL_H, d), wallMat);
  mesh.position.set(cx, WALL_H / 2, cz);
  mesh.castShadow = true;
  mesh.receiveShadow = true;
  scene.add(mesh);
}

for (const wdef of wallDefs) {
  const [a, b] = wdef.range;
  if (wdef.gap) {
    buildWallSegment(wdef.axis, wdef.at, a, wdef.gap[0]);
    buildWallSegment(wdef.axis, wdef.at, wdef.gap[1], b);
  } else {
    buildWallSegment(wdef.axis, wdef.at, a, b);
  }
}

/* ---------------------------------------------------------------------
   PAINTINGS
   Each: { x, y, z, nx, nz, title/img index, w, h }
--------------------------------------------------------------------- */
const paintingDefs = [
  // one landscape piece per wall face — 12 total
  { x:  0,    y: 2, z:  4.8,  nx: 0,  nz: -1, w: 2.6, h: 1.6 }, // Hall south (entrance)
  { x: -5.8,  y: 2, z:  0,    nx: 1,  nz: 0,  w: 2.4, h: 1.5 }, // Hall west
  { x: -3.75, y: 2, z: -4.8,  nx: 0,  nz: 1,  w: 2.0, h: 1.3 }, // Hall/NorthGallery divider — hall face
  { x: -3.75, y: 2, z: -5.2,  nx: 0,  nz: -1, w: 2.0, h: 1.3 }, // Hall/NorthGallery divider — gallery face
  { x:  5.8,  y: 2, z:  3.25, nx: -1, nz: 0,  w: 2.0, h: 1.3 }, // Hall/EastGallery divider — hall face
  { x:  6.2,  y: 2, z:  3.25, nx: 1,  nz: 0,  w: 2.0, h: 1.3 }, // Hall/EastGallery divider — gallery face
  { x:  0,    y: 2, z: -10.8, nx: 0,  nz: 1,  w: 2.6, h: 1.6 }, // North Gallery far wall
  { x: -5.8,  y: 2, z: -8,    nx: 1,  nz: 0,  w: 2.2, h: 1.4 }, // North Gallery west
  { x:  5.8,  y: 2, z: -8,    nx: -1, nz: 0,  w: 2.2, h: 1.4 }, // North Gallery east
  { x: 13.8,  y: 2, z:  0,    nx: -1, nz: 0,  w: 2.6, h: 1.6 }, // East Gallery far wall
  { x: 10,    y: 2, z: -4.8,  nx: 0,  nz: 1,  w: 2.2, h: 1.4 }, // East Gallery north
  { x: 10,    y: 2, z:  4.8,  nx: 0,  nz: -1, w: 2.2, h: 1.4 }, // East Gallery south
];

const textureLoader = new THREE.TextureLoader();
const placeholderCache = {};

function placeholderTexture(index) {
  if (placeholderCache[index]) return placeholderCache[index];
  const c = document.createElement('canvas');
  c.width = 683; c.height = 512;
  const ctx = c.getContext('2d');
  const hue = (index * 47) % 360;
  ctx.fillStyle = `hsl(${hue},35%,72%)`;
  ctx.fillRect(0, 0, c.width, c.height);
  ctx.fillStyle = `hsl(${hue},30%,45%)`;
  ctx.beginPath();
  ctx.ellipse(c.width * 0.5, c.height * 0.42, 150, 190, 0.4, 0, Math.PI * 2);
  ctx.fill();
  ctx.fillStyle = 'rgba(20,16,12,0.85)';
  ctx.fillRect(0, c.height - 46, c.width, 46);
  ctx.fillStyle = '#f0e9db';
  ctx.font = '24px Georgia';
  ctx.textAlign = 'center';
  ctx.fillText(TITLE_FOR(index), c.width / 2, c.height - 15);
  const tex = new THREE.CanvasTexture(c);
  tex.colorSpace = THREE.SRGBColorSpace;
  placeholderCache[index] = tex;
  return tex;
}

const paintingMeshes = []; // raycast targets, each has userData {title, index, group, normal}

paintingDefs.forEach((p, i) => {
  const index = i + 1; // 1-based, used for image cycling + title
  const yaw = Math.atan2(p.nx, p.nz); // rotates default +z-facing plane to (nx,0,nz)

  const group = new THREE.Group();
  group.position.set(p.x, p.y, p.z);
  group.rotation.y = yaw;

  // frame
  const frameDepth = 0.06;
  const frame = new THREE.Mesh(
    new THREE.BoxGeometry(p.w + 0.14, p.h + 0.14, frameDepth),
    frameMat
  );
  frame.position.z = -0.02;
  frame.castShadow = true;
  group.add(frame);

  // canvas / photo
  const artMat = new THREE.MeshBasicMaterial({ color: 0xffffff, side: THREE.DoubleSide });
  const art = new THREE.Mesh(new THREE.PlaneGeometry(p.w, p.h), artMat);
  art.position.z = 0.02;
  art.userData.isPainting = true;
  group.add(art);

  // small accent light
  const spot = new THREE.SpotLight(0xfff1d8, 6, 5, Math.PI / 6, 0.6, 1.5);
  spot.position.set(0, p.h / 2 + 0.9, 0.9);
  spot.target = art;
  group.add(spot);
  group.add(spot.target);

  scene.add(group);

  // texture: try real image, fall back to placeholder
  artMat.map = placeholderTexture(index);
  artMat.needsUpdate = true;
  const imgUrl = IMAGE_PATH(index);
  textureLoader.load(
    imgUrl,
    (tex) => {
      tex.colorSpace = THREE.SRGBColorSpace;
      artMat.map = tex;
      artMat.needsUpdate = true;
      console.log('%cLoaded', 'color:#4caf50', imgUrl);
    },
    undefined,
    (err) => {
      console.warn('Failed to load', imgUrl, err);
    }
  );

  paintingMeshes.push(art);
  art.userData.title = TITLE_FOR(index);
  art.userData.normal = new THREE.Vector3(p.nx, 0, p.nz);
  art.userData.worldPos = new THREE.Vector3(p.x, p.y, p.z);
});

/* ---------------------------------------------------------------------
   CONTROLS / MOVEMENT
--------------------------------------------------------------------- */
const controls = new PointerLockControls(camera, renderer.domElement);
scene.add(controls.getObject());

const overlay = document.getElementById('overlay');
const loading = document.getElementById('loading');
const hint = document.getElementById('hint');
const caption = document.getElementById('caption');

loading.style.display = 'none';
overlay.classList.remove('hidden');

overlay.addEventListener('click', () => {
  if (!zoomed) controls.lock();
});
controls.addEventListener('lock', () => { overlay.classList.add('hidden'); });
controls.addEventListener('unlock', () => {
  if (!zoomed) overlay.classList.remove('hidden');
});

const keys = {};
document.addEventListener('keydown', (e) => { keys[e.code] = true; });
document.addEventListener('keyup', (e) => { keys[e.code] = false; });

const velocity = new THREE.Vector3();
const MOVE_SPEED = 4.2;

function resolveCollision(pos) {
  for (const seg of collisionSegments) {
    const sx = seg.x2 - seg.x1, sz = seg.z2 - seg.z1;
    const len2 = sx * sx + sz * sz || 1;
    let t = ((pos.x - seg.x1) * sx + (pos.z - seg.z1) * sz) / len2;
    t = Math.max(0, Math.min(1, t));
    const cx = seg.x1 + sx * t, cz = seg.z1 + sz * t;
    const dx = pos.x - cx, dz = pos.z - cz;
    const dist = Math.hypot(dx, dz);
    const minDist = PLAYER_R + WALL_T / 2;
    if (dist < minDist && dist > 0.0001) {
      const push = (minDist - dist);
      pos.x += (dx / dist) * push;
      pos.z += (dz / dist) * push;
    }
  }
  return pos;
}

/* ---------------------------------------------------------------------
   PAINTING ZOOM INTERACTION
--------------------------------------------------------------------- */
const raycaster = new THREE.Raycaster();
raycaster.far = 4.2;
const screenCenter = new THREE.Vector2(0, 0);

let zoomed = false;
let zoomTarget = null;
const camReturnPos = new THREE.Vector3();
const camReturnQuat = new THREE.Quaternion();
const camStart = new THREE.Vector3();
const camEnd = new THREE.Vector3();
const quatStart = new THREE.Quaternion();
const quatEnd = new THREE.Quaternion();
let animT = 1; // 1 = animation finished
const ANIM_TIME = 0.7;
let animClock = 0;

function tryFocusHovered() {
  raycaster.setFromCamera(screenCenter, camera);
  const hits = raycaster.intersectObjects(paintingMeshes, false);
  if (hits.length) startZoom(hits[0].object);
}

function startZoom(art) {
  zoomed = true;
  zoomTarget = art;
  controls.unlock ? null : null; // keep pointer lock active for smoothness

  camReturnPos.copy(camera.position);
  camReturnQuat.copy(camera.quaternion);

  const normal = art.userData.normal;
  const wp = new THREE.Vector3();
  art.getWorldPosition(wp);
  const dist = 1.5;
  camStart.copy(camera.position);
  camEnd.copy(wp).addScaledVector(normal, dist);
  camEnd.y = Math.max(1.2, Math.min(2.6, wp.y));

  quatStart.copy(camera.quaternion);
  const lookMat = new THREE.Matrix4().lookAt(camEnd, wp, new THREE.Vector3(0, 1, 0));
  quatEnd.setFromRotationMatrix(lookMat);

  animT = 0; animClock = 0;

  caption.querySelector('.t').textContent = art.userData.title;
  caption.querySelector('.s').textContent = 'Gallery by Nguyen Trong Dung';
}

function endZoom() {
  camStart.copy(camera.position);
  camEnd.copy(camReturnPos);
  quatStart.copy(camera.quaternion);
  quatEnd.copy(camReturnQuat);
  animT = 0; animClock = 0;
  zoomed = false;
  caption.classList.remove('show');
  zoomTargetPending = null;
}
let zoomTargetPending = null;

renderer.domElement.addEventListener('click', () => {
  if (!controls.isLocked) return;
  if (zoomed) {
    endZoom();
  } else {
    tryFocusHovered();
  }
});

document.addEventListener('keydown', (e) => {
  if (e.code === 'Escape' && zoomed) endZoom();
});

/* ---------------------------------------------------------------------
   MAIN LOOP
--------------------------------------------------------------------- */
const clock = new THREE.Clock();

function animate() {
  requestAnimationFrame(animate);
  const dt = Math.min(clock.getDelta(), 0.05);

  // hover hint (only when not zoomed & locked)
  if (controls.isLocked && !zoomed) {
    raycaster.setFromCamera(screenCenter, camera);
    const hits = raycaster.intersectObjects(paintingMeshes, false);
    hint.classList.toggle('show', hits.length > 0);
  } else {
    hint.classList.remove('show');
  }

  if (animT < 1) {
    animClock += dt;
    animT = Math.min(1, animClock / ANIM_TIME);
    const e = 1 - Math.pow(1 - animT, 3); // ease-out cubic
    camera.position.lerpVectors(camStart, camEnd, e);
    camera.quaternion.slerpQuaternions(quatStart, quatEnd, e);
    if (animT >= 1 && zoomed) caption.classList.add('show');
  } else if (controls.isLocked && !zoomed) {
    // walking
    const forward = (keys['KeyW'] || keys['ArrowUp'] ? 1 : 0) - (keys['KeyS'] || keys['ArrowDown'] ? 1 : 0);
    const strafe = (keys['KeyD'] || keys['ArrowRight'] ? 1 : 0) - (keys['KeyA'] || keys['ArrowLeft'] ? 1 : 0);

    velocity.set(strafe, 0, forward);
    if (velocity.lengthSq() > 0) velocity.normalize().multiplyScalar(MOVE_SPEED * dt);

    controls.moveRight(velocity.x);
    controls.moveForward(velocity.z);

    const obj = controls.getObject();
    const pos2 = new THREE.Vector3(obj.position.x, 0, obj.position.z);
    resolveCollision(pos2);
    obj.position.x = pos2.x;
    obj.position.z = pos2.z;
    obj.position.y = EYE_H;
  }

  renderer.render(scene, camera);
}
animate();
</script>
</body>
</html>
