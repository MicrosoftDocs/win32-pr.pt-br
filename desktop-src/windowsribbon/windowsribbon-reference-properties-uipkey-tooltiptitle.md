---
title: UI_PKEY_TooltipTitle
description: Identifica a \_ Propriedade PKEY TooltipTitle da interface do usuário \_ .
ms.assetid: ed9f422d-a782-4950-a579-060185550891
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e62fe9ebdb6418f5790e0073e32e81d7f7aba75
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105798379"
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

 

 




