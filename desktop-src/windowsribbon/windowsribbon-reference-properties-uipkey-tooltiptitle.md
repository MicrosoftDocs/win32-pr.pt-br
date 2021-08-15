---
title: UI_PKEY_TooltipTitle
description: Identifica a \_ Propriedade PKEY TooltipTitle da interface do usuário \_ .
ms.assetid: ed9f422d-a782-4950-a579-060185550891
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae6a9e479d2f963acd4041d23e2b1ca075db609f9d45b556cd2aab34e6b2c6a7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118437781"
---
# <a name="ui_pkey_tooltiptitle"></a>\_TooltipTitle PKEY \_ UI

Identifica a \_ Propriedade PKEY TooltipTitle da interface do usuário \_ .

```
propertyDescription
   name = UI_PKEY_TooltipTitle
   shellPKey = UI_PKEY_TooltipTitle
   formatID = 00000006-7363-696e-8441798acf5aebb7
   propID = 6
   typeInfo
      type = VT_LPWSTR
```

## <a name="remarks"></a>Comentários

A interface do usuário \_ PKEY \_ TooltipTitle é usada por um aplicativo para consultar a dica de ferramenta de guias, grupos, botões, itens da galeria e outros controles da faixa de tipos.

O valor da propriedade é uma cadeia de caracteres restrita a qualquer sequência de caracteres, incluindo espaços em branco e caracteres de quebra de linha.

> [!Note]  
> Use a referência de caractere XML UCS (conjunto de caracteres universal) `&#xA;` para especificar uma quebra de linha.

 

Não há suporte para alinhamento à direita.

O comprimento máximo da interface do usuário \_ PKEY \_ TooltipTitle é não associado.

Para exibir um e comercial em uma dica de ferramenta, escape a designação de caractere especial com um e comercial duplo ( `&&` ), conforme mostrado no exemplo a seguir.


```XML
<Command.TooltipTitle>Tooltip title with &amp;&amp; for Save Command</Command.TooltipTitle>
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Propriedades do recurso](windowsribbon-reference-properties-resource.md)
</dt> <dt>

[**Comando. TooltipTitle**](windowsribbon-element-command-tooltiptitle.md)
</dt> <dt>

[\_TooltipDescription PKEY \_ UI](windowsribbon-reference-properties-uipkey-tooltipdescription.md)
</dt> </dl>

 

 




