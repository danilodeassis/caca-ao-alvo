# Caça ao Alvo

Um mini-jogo de mira feito em uma única página HTML, sem dependências nem build.
Os alvos surgem e **encolhem** com o tempo: quanto menor o alvo no momento do
acerto, mais pontos. Acertos seguidos aumentam o combo; errar o clique zera o
combo. Cada rodada dura **30 segundos**.

## Como jogar

Abra o arquivo [`index.html`](index.html) diretamente no navegador — clique duas
vezes nele ou arraste-o para uma aba. Não é preciso servidor.

Se preferir servir localmente:

```bash
python -m http.server 8000
# depois abra http://localhost:8000
```

## Controles

| Ação | Como |
|------|------|
| Acertar um alvo | Clique / toque sobre ele |
| Iniciar ou reiniciar | Botão na tela ou tecla `Espaço` |

## Pontuação

- Cada alvo vale de **10 a 100 pontos**, proporcional a quão pequeno ele está no
  momento do acerto.
- O combo multiplica os pontos: `+15%` por acerto consecutivo.
- Deixar um alvo sumir ou errar o clique zera o combo.
- O recorde fica salvo no navegador (`localStorage`).

## Tecnologias

HTML, CSS e JavaScript puro. O desenho é feito em `<canvas>` e os efeitos
sonoros são gerados via Web Audio API — nenhum arquivo externo.
