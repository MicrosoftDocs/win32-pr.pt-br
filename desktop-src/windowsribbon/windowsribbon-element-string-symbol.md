---
title: Propriedade String.Symbol
description: Representa o nome de um recurso de cadeia de caracteres.
ms.assetid: 7c1d0197-2c9b-4f42-afba-73fd1c366deb
keywords:
- Propriedade String.Symbol Windows Faixa de Opções
topic_type:
- apiref
api_name:
- String.Symbol
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe6c071461fcdeb5f2bbbdbb15fce0f3f6e6031edddf4bd18e034416ba8c49e1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118706857"
---
# <a name="stringsymbol-property"></a>Propriedade String.Symbol

Representa o nome de um recurso de cadeia de caracteres.

## <a name="usage"></a>Uso

``` syntax
<String.Symbol/>
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

O símbolo está associado a uma definição de cadeia de caracteres no arquivo de header da Faixa de Opções, por exemplo, `#define strSave 59999` .

Esse elemento contém um valor do tipo *xs:string*. O valor é restrito a uma cadeia de caracteres composta por uma letra ou sublinhado seguido por qualquer sequência de letras, dígitos ou sublinhados.

O comprimento máximo é de 100 caracteres.

## <a name="examples"></a>Exemplos

O exemplo a seguir demonstra a marcação para um [**elemento Command.LabelTitle**](windowsribbon-element-command-labeltitle.md) com uma declaração **String.Symbol.**


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



 

 





