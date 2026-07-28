# DS-shadcn

Registry de componentes **DS-shadcn**, distribuída no padrão [shadcn/ui](https://ui.shadcn.com). Os componentes usam os tokens do tema `pinatls-theme` (style `radix-luma`, base `neutral`) e podem ser instalados diretamente em qualquer projeto shadcn a partir deste repositório.

- **Registry:** `ds-shadcn`
- **Homepage:** https://github.com/pinatls-stack/DS-shadcn
- **Manifesto:** [`registry.json`](./registry.json)

## Pré-requisitos

O projeto de destino precisa já estar inicializado com shadcn (ter um `components.json` na raiz). Se ainda não estiver:

```bash
npx shadcn@latest init
```

## Instalando componentes

Use o namespace do repositório (`pinatls-stack/DS-shadcn`) seguido do nome do componente:

```bash
npx shadcn@latest add pinatls-stack/DS-shadcn/button
```

Exemplos com outros itens:

```bash
npx shadcn@latest add pinatls-stack/DS-shadcn/dialog
npx shadcn@latest add pinatls-stack/DS-shadcn/table
npx shadcn@latest add pinatls-stack/DS-shadcn/use-mobile
```

Os arquivos são colocados nos diretórios configurados no seu `components.json` (`components/ui/`, `hooks/`, `lib/`).

> Dica: antes de instalar, você pode inspecionar um item sem alterar nada com
> `npx shadcn@latest view pinatls-stack/DS-shadcn/button`.

## Usando os componentes

```tsx
import { Button } from "@/components/ui/button";

export function Example() {
  return <Button>Confirmar</Button>;
}
```

## Componentes disponíveis

### UI (`registry:ui`)

`accordion` · `alert` · `alert-dialog` · `aspect-ratio` · `attachment` · `avatar` · `badge` · `breadcrumb` · `bubble` · `button` · `button-group` · `calendar` · `card` · `carousel` · `chart` · `checkbox` · `collapsible` · `combobox` · `command` · `context-menu` · `dialog` · `direction` · `drawer` · `dropdown-menu` · `empty` · `field` · `hover-card` · `input` · `input-group` · `input-otp` · `item` · `kbd` · `label` · `marker` · `menubar` · `message` · `message-scroller` · `native-select` · `navigation-menu` · `pagination` · `popover` · `progress` · `radio-group` · `resizable` · `scroll-area` · `select` · `separator` · `sheet` · `sidebar` · `skeleton` · `slider` · `sonner` · `spinner` · `switch` · `table` · `tabs` · `textarea` · `toggle` · `toggle-group` · `tooltip`

### Hooks (`registry:hook`)

`use-mobile`

### Lib (`registry:lib`)

`utils`

## Desenvolvimento local

Este repositório também é um projeto Next.js completo (usado como fonte dos componentes).

```bash
pnpm install
pnpm dev
```

Para revalidar a registry após alterações no `registry.json`:

```bash
npx shadcn@latest registry validate ./registry.json
```
