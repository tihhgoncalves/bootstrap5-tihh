# bootstrap5-tihh
Acho o Bootstrap 5 muito bom. Gosto de utilizá-lo em meus projetos. Mas existem algumas particularidades que eu acho que poderiam ser melhor (pelo menos pra forma que eu gosto de trabalhar). Esse projeto, então, é um complemento pra ser usado junto com o Bootstrap 5.

## Como usar
Adicione esse script logo após o do Bootstrap 5 no seu projeto.
```html
<link rel="stylesheet" href="https://cdn.jsdelivr.net/gh//tihhgoncalves/bootstrap5-tihh@v1.0.0/dist/bootstrap5-tihh.css">
```
---

## Grids
Os grids do bootstrap por padrão utilizam 12 colunas como referência. Então de você usar uma classe `.col-6` ele vai colocar a largura de 50% (6/12). 
implementei para poder utilizar não só com 12, mas com até 24 divisões de colunas. Como no 50% que acabei de falar, poderia simplificar assim com `.col-1-2`.
E ele respeita os breaskpoints tmb, além dos espaços dos offsets. Veja o exemplo:

```html
<div class="container">
    <div class="row">
        <div class="col-1-3 col-md-1-2">[coluna 1]</div>
        <div class="col-1-3 offset-1-3 col-md-1-2 offset-md-0">[coluna 3]</div>
    </div>
</div>
```

## Margins e Paddings
Sim, o Bootstrap já tem esse recurso, mas eu acho muito limitado. Por isso desenvolvi um com um pouco de mais opções.
Trabalhamos com múltiplos de 25px. Ou seja, 1 é igual a 25px, 2 é 50px e assim sucessivamente.

Cada letra representa uma orientação:
 - x = horizontal
 - y = vertical
 - l = esquerda
 - r = direita
 - t = topo
 - b = fundo

Vamos ao exemplo:

```html
<div class="margin-lg-x3"> 
    <!-- no breakpoint lg, vai colocar margin-left e margim-right como 75px -->
</div>
<div class="padding-md-t1"> 
    <!-- no breakpoint md, vai colocar padding-top como 25px -->
</div>
```


## Informações de DEV

### Compilar
Abra seu terminal até a root do projeto e rode o comando:

```bash
sass src/start.scss dist/bootstrap5-tihh.css --style=compressed
```

---

## Autor
 - @tihhgoncalves
