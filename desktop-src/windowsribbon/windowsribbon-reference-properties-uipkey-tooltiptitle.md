---
title: UI_PKEY_TooltipTitle
description: Identifica a propriedade \_ PKEY TooltipTitle da interface do \_ usuário.
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
# <a name="ui_pkey_tooltiptitle"></a>Dica de \_ ferramenta PKEY \_ da interface do usuário

Identifica a propriedade \_ PKEY TooltipTitle da interface do \_ usuário.

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

A ferramenta PKEY da interface do usuárioTipTitle é usada por um aplicativo para consultar a dica de ferramenta de \_ guias, grupos, botões, itens da galeria e outros controles de Faixa \_ de Opções.

O valor da propriedade é uma cadeia de caracteres restrita a qualquer sequência de caracteres, incluindo espaços em branco e caracteres de quebra de linha.

> [!Note]  
> Use a referência de caractere XML do Conjunto de Caracteres Universal (UCS) `&#xA;` para especificar uma quebra de linha.

 

Não há suporte para o alinhamento à direita.

O comprimento máximo da ferramenta PKEY da interface do \_ \_ usuárioTipTitle é ilimitado.

Para exibir um e ampersand em uma dica de ferramenta, escape da designação de caractere especial com um e ampersand duplo ( ), conforme `&&` mostrado no exemplo a seguir.


```XML
<Command.TooltipTitle>Tooltip title with &amp;&amp; for Save Command</Command.TooltipTitle>
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Propriedades do recurso](windowsribbon-reference-properties-resource.md)
</dt> <dt>

[**Command.TooltipTitle**](windowsribbon-element-command-tooltiptitle.md)
</dt> <dt>

[Dica \_ de ferramenta PKEY \_ da interface do usuárioDescription](windowsribbon-reference-properties-uipkey-tooltipdescription.md)
</dt> </dl>

 

 




