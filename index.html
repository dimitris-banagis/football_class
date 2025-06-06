<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Football Class 3D</title>
  <style>
    body { margin: 0; overflow: hidden; }
    canvas { display: block; }
    #score { position: absolute; top: 10px; left: 10px; color: white; font-size: 24px; font-family: sans-serif; }
  </style>
</head>
<body>
  <div id="score">Score: 0</div>
  <script src="https://cdn.jsdelivr.net/npm/three@0.157.0/build/three.min.js"></script>
  <script>
    let scene, camera, renderer, ball, player, goal, score = 0;
    const speed = 0.2;

    init();
    animate();

    function init() {
      scene = new THREE.Scene();
      scene.background = new THREE.Color(0x202020);

      camera = new THREE.PerspectiveCamera(75, window.innerWidth / window.innerHeight, 0.1, 1000);
      camera.position.set(0, 5, 10);

      renderer = new THREE.WebGLRenderer();
      renderer.setSize(window.innerWidth, window.innerHeight);
      document.body.appendChild(renderer.domElement);

      const light = new THREE.DirectionalLight(0xffffff, 1);
      light.position.set(5, 10, 7.5);
      scene.add(light);

      const floorGeometry = new THREE.PlaneGeometry(20, 20);
      const floorMaterial = new THREE.MeshStandardMaterial({ color: 0x555555 });
      const floor = new THREE.Mesh(floorGeometry, floorMaterial);
      floor.rotation.x = -Math.PI / 2;
      scene.add(floor);

      const playerGeometry = new THREE.BoxGeometry(1, 1, 1);
      const playerMaterial = new THREE.MeshStandardMaterial({ color: 0x00ff00 });
      player = new THREE.Mesh(playerGeometry, playerMaterial);
      player.position.set(0, 0.5, 0);
      scene.add(player);

      const ballGeometry = new THREE.SphereGeometry(0.3, 32, 32);
      const ballMaterial = new THREE.MeshStandardMaterial({ color: 0xffffff });
      ball = new THREE.Mesh(ballGeometry, ballMaterial);
      ball.position.set(0, 0.3, -3);
      scene.add(ball);

      const goalGeometry = new THREE.BoxGeometry(4, 2, 0.2);
      const goalMaterial = new THREE.MeshStandardMaterial({ color: 0xff0000 });
      goal = new THREE.Mesh(goalGeometry, goalMaterial);
      goal.position.set(0, 1, -9);
      scene.add(goal);

      window.addEventListener('resize', onWindowResize, false);
      document.addEventListener('keydown', onKeyDown);
    }

    function onWindowResize() {
      camera.aspect = window.innerWidth / window.innerHeight;
      camera.updateProjectionMatrix();
      renderer.setSize(window.innerWidth, window.innerHeight);
    }

    function onKeyDown(event) {
      switch (event.key.toLowerCase()) {
        case 'w': player.position.z -= speed; break;
        case 's': player.position.z += speed; break;
        case 'a': player.position.x -= speed; break;
        case 'd': player.position.x += speed; break;
        case ' ': // kick
          const dx = ball.position.x - player.position.x;
          const dz = ball.position.z - player.position.z;
          const dist = Math.sqrt(dx*dx + dz*dz);
          if (dist < 1.5) {
            ball.position.x += dx * 2;
            ball.position.z += dz * 2;
          }
          break;
      }
    }

    function animate() {
      requestAnimationFrame(animate);

      camera.position.x = player.position.x;
      camera.position.z = player.position.z + 10;
      camera.lookAt(player.position);

      checkGoal();
      renderer.render(scene, camera);
    }

    function checkGoal() {
      if (
        ball.position.z < -8 &&
        ball.position.x > -2 && ball.position.x < 2
      ) {
        score++;
        document.getElementById('score').innerText = 'Score: ' + score;
        ball.position.set(0, 0.3, -3);
      }
    }
  </script>
</body>
</html>
