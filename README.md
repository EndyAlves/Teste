# Gym Basket 3D

Jogo de basquete 3D em primeira pessoa para navegador, inspirado no *Gym Class VR* — sem precisar de VR.
Dois modos: **1 contra 1** contra a CPU (até 21) e **treino livre**.
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
| Clique esquerdo (segurar) | Arremesso: solte na **faixa verde** = cesta garantida · infiltrando: bandeja (ou enterrada com Shift) · sem a bola: roubar |
| S + clique | Fadeaway |
| Espaço | Pular · na defesa, pule para dar toco |
| Q / clique direito | Crossover |
| F | Entre as pernas |
| X | Por trás das costas |
| C | Step back |
| V | Bandeja reversa (infiltrando) |
| E / R / Esc | Pegar bola / chamar bola (treino) / pausar |

### Celular
Joystick à esquerda (até o fim = correr), arraste à direita para mirar. Botões **ARREMESSAR**, **PULAR**,
**CROSS**, **PERNAS**, **COSTAS** e **STEP BACK**. Os botões mudam conforme a jogada: infiltrando,
ARREMESSAR vira BANDEJA/ENTERRAR e STEP BACK vira REVERSA; sem a bola, CROSS vira ROUBAR e STEP BACK vira PEGAR.
Joystick puxado para trás + ARREMESSAR = fadeaway.

### 1 contra 1
- Jogo até 21, cestas de 2 e 3. Quem sofre a cesta fica com a bola.
- Depois de rebote de defesa ou roubo, leve a bola para trás da linha de 3 (**limpar a bola**); sem isso a cesta não vale.
- Bola que sai pela linha de fundo/lateral vai para o adversário de quem tocou por último.
- A CPU (3 dificuldades) infiltra, faz crossover, entre as pernas, por trás das costas, step back, fadeaway,
  bandeja, bandeja reversa e enterrada; na defesa marca, contesta, tenta roubar e dá toco.
- Seus dribles podem fazer a CPU morder a finta (e até cair: *ankle breaker*). Drible em sequência rápida demais não engana.
- A marcação diminui a faixa verde, mas **soltar no verde continua sendo cesta garantida**. Fora do verde, a CPU pode dar toco.

### Arremesso, bandeja e enterrada
- **Arremesso:** segure o botão e solte quando a barra estiver na faixa verde → cesta 100%.
  Fora do verde a bola sai curta (cedo) ou longa (tarde). A faixa fica menor de longe e correndo.
- **Bandeja:** correndo em direção à cesta (até ~4 m) com a bola, aperte o arremesso — o jogador
  sobe sozinho; solte no verde (topo do pulo) para converter.
- **Enterrada:** a mesma infiltração correndo no máximo (Shift / joystick no fim). Também dá
  para pular perto do aro e apertar o arremesso.
- **Bandeja reversa:** infiltrando, aperte V (ou REVERSA): passa por baixo do aro e finaliza do outro lado.
- **Fadeaway:** arremesso andando para trás (S / joystick para trás).
- **Drible automático:** andar com a bola faz o jogador quicá-la.

## Recursos
- Quadra com medidas oficiais (aro a 3,05 m, linha de 3 a 6,75 m) e física real da bola:
  quique, tabela, aro, rede que segura a bola, efeito de giro.
- Arremesso pelo ângulo da câmera + força; cestas de 2 e 3, swish, tabela, enterrada com o aro envergando.
- Drible, rebote automático, 4 bolas (uma no rack), placar no ginásio, sequência e recorde.
- Sons sintetizados e marcador opcional de força ideal.
