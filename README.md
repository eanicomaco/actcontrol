# actcontrol

Este template deve ajudá-lo a começar a desenvolver com Vue 3 no Vite.

## Configuração de IDE Recomendada

[VSCode](https://code.visualstudio.com/) + [Vue Official](https://marketplace.visualstudio.com/items?itemName=Vue.volar) (e desabilite o Vetur).

## Suporte de Tipo para Importações .vue em TS

O TypeScript não pode lidar com informações de tipo para importações .vue por padrão, então substituímos o CLI tsc pelo vue-tsc para verificação de tipos. Nos editores, precisamos do [Vue Official](https://marketplace.visualstudio.com/items?itemName=Vue.volar) para tornar o serviço de linguagem TypeScript ciente dos tipos .vue.

## Personalizar Configuração

Veja [Referência de Configuração do Vite](https://vitejs.dev/config/).

## Configuração do Projeto

```sh
npm install
```

### Compilação e Hot-Reload para Desenvolvimento

```sh
npm run dev
```

### Verificação de Tipos, Compilação e Minificação para Produção

```sh
npm run build
```
