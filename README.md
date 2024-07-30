Animação de relógio - 3D ⌚
Objetivo: Criar uma animação utilizando WebGL e a biblioteca Three.js que siga os seguintes critérios:

Utilize pelo menos 3 tipos diferentes de geometrias
Utilize pelo menos 2 tipos de materiais
Carregue pelo menos 1 textura
Possua pelo menos 2 fontes de iluminação
Carregue pelo menos um modelo externo
Tecnologias Usadas 🔧
HTML
CSS
JavaScript
Paint.net
WebGL
Three.js: Biblioteca para renderização 3D.
GSAP: Biblioteca para animações suaves.
Este projeto é uma animação interativa em 3D desenvolvida utilizando a biblioteca Three.js, onde três formas geométricas giram em um ambiente 3D, acompanhadas de um fundo dinâmico e um relógio digital.

Demonstração
Funcionalidades
Três formas geométricas :

Rosquinha (Torus)
Cubo (Caixa)
Pirâmide (Cone)
Materiais variados :

Material com textura para toro.
Material com textura para o cubo.
Material com textura para a pirâmide.
Requisitos Atendentes
1. Utilização de pelo menos 3 tipos diferentes de geometrias :

TorusGeometrypara a rosquinha.

BoxGeometrypara o cubo.

CylinderGeometrypara a pirâmide.

const mesh1 = new THREE.Mesh(new THREE.TorusGeometry(0.5, 0.2, 16, 60), torusMaterial);
const cube = new THREE.Mesh(new THREE.BoxGeometry(1, 1, 1), cubeMaterial);
const pyramid = new THREE.Mesh(new THREE.CylinderGeometry(0, 0.5, 1, 4), pyramidMaterial);
2. Utilização de pelo menos 2 tipos de materiais :

MeshStandardMaterial para o cubo e a pirâmide.

MeshToonMaterial para uma rosquinha.

const torusMaterial = new THREE.MeshToonMaterial({ map: torusTexture }); // Material da rosquinha
const cubeMaterial = new THREE.MeshStandardMaterial({ map: cubeTexture, metalness: 0.5, roughness: 0.5 }); // Material do cubo
const pyramidMaterial = new THREE.MeshStandardMaterial({ map: pyramidTexture, metalness: 0.5, roughness: 0.5 }); // Material da pirâmide
3. Carregamento de pelo menos 1 textura :

Textura fornecida para o toro.

Textura fornecida para o cubo.

Textura adicionada para a pirâmide.

const torusTexture = textureLoader.load('/src/textures/torusTexture.jpg');
const cubeTexture = textureLoader.load('/src/textures/cubeTexture.jpg');
const pyramidTexture = textureLoader.load('/src/textures/pyramidTexture.jpg'); 
4. Possui pelo menos 2 fontes de iluminação :

A cena utiliza uma luz direcional e uma luz ambiente.

const directionalLight = new THREE.DirectionalLight('#ffffff', 3);
const ambientLight = new THREE.AmbientLight('#ffffff', 0.5);
Autora
