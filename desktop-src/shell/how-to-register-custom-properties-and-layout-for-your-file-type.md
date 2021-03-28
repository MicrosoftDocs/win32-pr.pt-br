---
description: Depois de entender o modo de resultado da pesquisa, o modo de procura e os padrões de layout, você pode registrar uma lista de propriedades Personalizada para o tipo de arquivo. Para registrar uma lista de propriedades personalizadas e um padrão de layout para o tipo de arquivo, siga estas etapas.
ms.assetid: 29B863B3-E5FD-4E0A-B76B-4AFE5A6A76E3
title: Como registrar Propriedades personalizadas e layout para o tipo de arquivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da55d0a90d4dd0f3ca109a3ca9f628a3c0912520
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104988978"
---
# <a name="how-to-register-custom-properties-and-layout-for-your-file-type"></a>Como registrar Propriedades personalizadas e layout para o tipo de arquivo

Depois de entender o modo de resultado da pesquisa, o modo de procura e os padrões de layout, você pode registrar uma lista de propriedades Personalizada para o tipo de arquivo.

Para registrar uma lista de propriedades personalizadas e um padrão de layout para o tipo de arquivo, siga estas etapas.

## <a name="instructions"></a>Instruções

### <a name="step-1"></a>Etapa 1:

Escolha entre os quatro padrões de layout: alfa, beta, gama ou Delta.

### <a name="step-2"></a>Etapa 2:

Considere as seguintes regras de formatação, que se aplicam igualmente a todos os quatro padrões de layout:

-   A propriedade 1 é sempre exibida em um tamanho de fonte maior. O tamanho de fonte grande geralmente usado para o nome do item, mas também pode ser usado para a propriedade de âncora ou outro item.
-   A propriedade 4 destina-se a trechos nos padrões de layout alfa, beta e gama. Essa propriedade é alocada mais espaço nesses padrões e é exibida em uma cor de fonte cinza, em oposição a preto, como as outras propriedades, para ajudá-lo a destacar.
-   As medidas de pixel abaixo estão em pixels relativos e o tamanho inclui o ícone/miniatura à esquerda das propriedades e o espaço entre o ícone/miniatura e o retângulo de seleção.
-   A maioria das propriedades tem um tamanho de exibição mínimo. Portanto, eles não serão exibidos se não houver espaço suficiente para eles em um tamanho de exibição específico. O tamanho mínimo geralmente é de 100 pixels de largura.
-   Cada padrão de layout define o número de linhas e o número de propriedades em cada linha.

### <a name="step-3"></a>Etapa 3:

Decida quais propriedades você deseja exibir no layout e qual Propriedade deseja exibir em cada local. Ao decidir qual propriedade será exibida em cada posição no layout, considere o comprimento típico da propriedade, sua importância para o usuário e se ela deve ser descartada quando o tamanho da janela for muito pequeno para conter todas as propriedades.

### <a name="step-4"></a>Etapa 4:

Registre um padrão de layout e uma lista de propriedades para o tipo de arquivo ou tipo de item adicionando as seguintes chaves na chave do registro ProgID para o tipo de arquivo ou item (neste exemplo, para o tipo de arquivo. xyz).

```
HKEY_CLASSES_ROOT\*
   Contoso.xyzfile
      (ContentViewModeForBrowse) = <Layout pattern name (Alpha, Beta, Delta, or Gamma)>
      (ContentViewModeForSearch) = <Layout pattern name (Alpha, Beta, Delta, or Gamma)>
      (ContentViewModeLayoutPatternForBrowse) = <PropertyList>
      (ContentViewModeLayoutPatternForSearch) = <PropertyList>
```

### <a name="step-5"></a>Etapa 5:

Observe as seguintes diretrizes de formatação para registrar Propriedades:

-   Cada registro começa com `prop:`
-   Cada propriedade requer o nome completo da propriedade.
-   As propriedades são separadas por um ponto-e-vírgula sem espaço.
-   As propriedades são exibidas na ordem definida pelo padrão de layout selecionado.
-   `~` indica que o rótulo da propriedade não deve ser exibido.
-   `~System.LayoutPattern.PlaceHolder` deve ser usado se você quiser deixar em branco uma propriedade especificada no padrão de layout.

A chave do registro de exemplo a seguir ilustra essas diretrizes de formatação.

```
HKEY_CLASSES_ROOT\
   Kind.Document
      (ContentViewModeForBrowse) = <PropertyList>
```

Os valores possíveis para (ContentViewModeForBrowse) incluem o seguinte: `prop:~System.ItemNameDisplay;System.Author;System.LayoutPattern.Placeholder;System.Keywords;System.DateModified;~System.Size`

 

 



