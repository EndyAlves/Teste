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
| Clique esquerdo (segurar) | Sobe a barra; solte na **faixa verde** = cesta garantida |
| Espaço | Pular — perto do aro com a bola, clique para **enterrar** |
| Q / clique direito | Driblar (segure para driblar sem parar) |
| E | Pegar bola próxima |
| R | Chamar a bola mais próxima |

### Celular
Joystick à esquerda para andar (empurre até o fim para correr), arraste à direita para mirar,
e botões **ARREMESSAR**, **PULAR**, **DRIBLAR**, **PEGAR** e **↺** (chamar bola).

### Arremesso, bandeja e enterrada
- **Arremesso:** segure o botão e solte quando a barra estiver na faixa verde → cesta 100%.
  Fora do verde a bola sai curta (cedo) ou longa (tarde). A faixa fica menor de longe e correndo.
- **Bandeja:** correndo em direção à cesta (até ~4 m) com a bola, aperte o arremesso — o jogador
  sobe sozinho; solte no verde (topo do pulo) para converter.
- **Enterrada:** a mesma infiltração correndo no máximo (Shift / joystick no fim). Também dá
  para pular perto do aro e apertar o arremesso.
- **Drible automático:** andar com a bola faz o jogador quicá-la.

## Recursos
- Quadra com medidas oficiais (aro a 3,05 m, linha de 3 a 6,75 m) e física real da bola:
  quique, tabela, aro, rede que segura a bola, efeito de giro.
- Arremesso pelo ângulo da câmera + força; cestas de 2 e 3, swish, tabela, enterrada com o aro envergando.
- Drible, rebote automático, 4 bolas (uma no rack), placar no ginásio, sequência e recorde.
- Sons sintetizados e marcador opcional de força ideal.
