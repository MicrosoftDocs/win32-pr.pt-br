---
title: Propriedade String.Id
description: Representa a ID exclusiva de um recurso de cadeia de caracteres.
ms.assetid: 393da279-bdf6-4796-a546-1931cbe49113
keywords:
- Faixa de String.Id da Propriedade do Windows
topic_type:
- apiref
api_name:
- String.Id
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c3ab87327ed4f11a901fb8a201e72137ab62c7a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086203"
---
# <a name="stringid-property"></a>Propriedade String.Id

Representa a ID exclusiva de um recurso de cadeia de caracteres.

## <a name="usage"></a>Uso

``` syntax
<String.Id/>
```

## <a name="attributes"></a>Atributos

Não há atributos.

## <a name="child-elements"></a>Elementos filho

Não há elementos filho.

## <a name="parent-elements"></a>Elementos pai



| Elemento                                                   |
|-----------------------------------------------------------|
| [**Strings**](windowsribbon-element-string.md)<br/> |



## <a name="remarks"></a>Comentários

Opcional.

Pode ocorrer no máximo uma vez para cada elemento de [**cadeia de caracteres**](windowsribbon-element-string.md) .

O valor de **String.ID** deve ser exclusivo.

A ID é associada a uma definição de cadeia de caracteres no arquivo de cabeçalho da faixa de, por exemplo, `#define strSave 59999` .

Esse elemento contém um valor da União de tipos *xs: positiveInteger* e *xs: String*. O valor é restrito a um valor inteiro entre 2 e 59999, inclusivo, ou 0x2 e 0xea5f em hexadecimal, inclusive.

O comprimento máximo é de 10 caracteres com zeros à esquerda opcionais.

## <a name="examples"></a>Exemplos

O exemplo a seguir demonstra a marcação para um elemento [**Command. LabelTitle**](windowsribbon-element-command-labeltitle.md) com uma declaração **String.ID** .


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
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 7\]<br/>              |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]<br/> |



 

 





