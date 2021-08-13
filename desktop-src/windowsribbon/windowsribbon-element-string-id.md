---
title: String.Id propriedade
description: Representa a ID exclusiva de um recurso de cadeia de caracteres.
ms.assetid: 393da279-bdf6-4796-a546-1931cbe49113
keywords:
- String.Id propriedade Windows Faixa de Opções
topic_type:
- apiref
api_name:
- String.Id
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 15f9c1af4ba32982ce52ba470f6b3d1996abe11c81bdd520a4e50203adb56093
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119441646"
---
# <a name="stringid-property"></a>String.Id propriedade

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
| [**String**](windowsribbon-element-string.md)<br/> |



## <a name="remarks"></a>Comentários

Opcional.

Pode ocorrer no máximo uma vez para cada [**elemento String.**](windowsribbon-element-string.md)

O valor para **String.Id** deve ser exclusivo.

A ID está associada a uma definição de cadeia de caracteres no arquivo de header da Faixa de Opções, por exemplo, `#define strSave 59999` .

Esse elemento contém um valor da união dos tipos *xs:positiveInteger* *e xs:string*. O valor é restrito a um valor inteiro entre 2 e 59999, inclusive ou 0x2 e 0xea5f em hexadecimal, inclusivo.

O comprimento máximo é de 10 caracteres com zeros à esquerda opcionais.

## <a name="examples"></a>Exemplos

O exemplo a seguir demonstra a marcação para um [**elemento Command.LabelTitle**](windowsribbon-element-command-labeltitle.md) com uma **String.Id** de dados.


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



 

 





