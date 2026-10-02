# Gym Basket 3D

Jogo de basquete 3D em primeira pessoa para navegador, inspirado no *Gym Class VR* — sem precisar de VR.
Feito com [three.js](https://threejs.org/) (incluído em `lib/`, funciona offline).

## Como jogar

Abra `index.html` por um servidor local (módulos ES não carregam via `file://`):

```bash
npx http-server .   # ou: python3 -m http.server
```

Depois acesse `http://localhost:8080`. Também funciona direto no GitHub Pages.

### Computador
| Tecla | Ação |
|---|---|
| W A S D / Shift | Andar / correr |
| Mouse | Olhar e mirar |
| Clique esquerdo (segurar) | Carregar força; soltar arremessa |
| Espaço | Pular — perto do aro com a bola, clique para **enterrar** |
| Q / clique direito | Driblar (segure para driblar sem parar) |
| E | Pegar bola próxima |
| R | Chamar a bola mais próxima |

### Celular
Joystick à esquerda para andar (empurre até o fim para correr), arraste à direita para mirar,
e botões **ARREMESSAR**, **PULAR**, **DRIBLAR**, **PEGAR** e **↺** (chamar bola).

## Recursos
- Quadra com medidas oficiais (aro a 3,05 m, linha de 3 a 6,75 m) e física real da bola:
  quique, tabela, aro, rede que segura a bola, efeito de giro.
- Arremesso pelo ângulo da câmera + força; cestas de 2 e 3, swish, tabela, enterrada com o aro envergando.
- Drible, rebote automático, 4 bolas (uma no rack), placar no ginásio, sequência e recorde.
- Sons sintetizados e marcador opcional de força ideal.
