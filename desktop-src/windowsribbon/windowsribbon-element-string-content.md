---
title: Propriedade String.Content
description: Representa o conteúdo de um recurso de cadeia de caracteres.
ms.assetid: 86f34cdc-1311-4f52-979f-201d71bbb9e9
keywords:
- Propriedade String.Content Windows Faixa de Opções
topic_type:
- apiref
api_name:
- String.Content
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 526062956c6ab7498caac8712ba932d6e7ac1f2dd6307359183d2529e35fc8a3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118439501"
---
# <a name="stringcontent-property"></a>Propriedade String.Content

Representa o conteúdo de um recurso de cadeia de caracteres.

## <a name="usage"></a>Uso

``` syntax
<String.Content/>
```

## <a name="attributes"></a>Atributos

Não há atributos.

## <a name="child-elements"></a>Elementos filho

Não há elementos filho.

## <a name="parent-elements"></a>Elementos pai



| Elemento                                                   |
|-----------------------------------------------------------|
| [**String**](windowsribbon-element-string.md)<br/> |



## <a name="remarks"></a>Comentários

Opcional.

Pode ocorrer no máximo uma vez para cada [**elemento String.**](windowsribbon-element-string.md)

Esse elemento contém um valor do tipo *xs:string*. O valor é restrito a uma cadeia de caracteres composta por qualquer sequência de caracteres, incluindo espaços em branco e caracteres de quebra de linha.

O comprimento máximo não é desaconsudido.

## <a name="examples"></a>Exemplos

O exemplo a seguir demonstra a marcação para um [**elemento Command.LabelTitle**](windowsribbon-element-command-labeltitle.md) com uma declaração **String.Content.**


```XML
<Command.LabelTitle>
  <String>
    <String.Content>Label for Save</String.Content>
    <String.Id>59999</String.Id>
    <String.Symbol>strSave</String.Symbol>
  </String>
</Command.LabelTitle>
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 7 \[ aplicativos da área de trabalho\]<br/>              |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho do Server 2008 R2 \[\]<br/> |



 

 





