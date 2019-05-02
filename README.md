# Responsabilidades da Agência

* Experiecia da marca
* Performance da loja
* Campanhas


# Vtex IO

Todo o desenolvimento é passado direto para a nuvem no servidor da VTEX. Facilitando todo o processo de deploy e dependencias de desenvolvimento e mantendo toda a responsabilidade de manter a infra com a própria VTEX.


# Store Components

Componentes globais da VTEX podem ser extencíveis, porém existem componentes "Enterprise" que para o funcionamento do componente de forma personalisada na loja é necessario que o logista tenha permissão. Existem compoentes públicos também.


# Store Theme

Thema default do VTEX IO: https://storetheme.vtex.com/

# Interface & Blocos

## Allow & Required
* **Interfce**: Configuração de onde o bloco é requerido e as suas opções permitidas. (Ex: https://github.com/vtex-apps/search-result/blob/master/store/interfaces.json)
* **Blocks**: Define os blocos que vão na interface: https://github.com/vtex-apps/search-result/blob/master/store/blocks.json


## Composition
Permite que o componente seja modelado de acordo com a necessidade do cliente

## Before & After
Para templates de página é possível definir os compenets Before e After, que englobaram o template com o que foi definido definindo que esses componentes não poderam ter suas posições modificadas. Ex:
```json
"store": {
	"before": ["header"],
	"after": ["footer"]
}
```

## Extends

É possível extender um contrado para uma determinada interface. Lembrando que somente é possível em contas Enterprise. Ex:

```json
"store.home": {
	"before": ["header.full"]
}
```

# Style Builder

É possível mudar o estilo do componente utilizando css overwrite. Basta criar dentro da pasta `styles > css` com o nome `ves.compenetName.css`. Porém o recomendado é utilizar o  builder tachyons que define o estilo de css utilizado pela loja.
* VTEX Tachyons: https://github.com/vtex/vtex-tachyons











# Alguns motivos para a migração

* CMS com poderes de WhatYouSeeIsWhatYouGet
* Perfomance
* PWA Native
* carrinho off-line (por vir)
