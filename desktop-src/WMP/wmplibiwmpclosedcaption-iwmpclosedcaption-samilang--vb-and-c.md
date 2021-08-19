---
title: Propriedade IWMPClosedCaption SAMILang
description: A propriedade SAMILang Obtém ou define o idioma exibido para Legendagem oculta.
ms.assetid: dcdd6bcd-b869-439f-b500-df26d3873b04
keywords:
- Windows Media Player da propriedade SAMILang
- propriedade SAMILang Windows Media Player, interface IWMPClosedCaption
- Windows Media Player de interface IWMPClosedCaption, propriedade SAMILang
topic_type:
- apiref
api_name:
- IWMPClosedCaption.SAMILang
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 98354d5e1e4f796442dd0347a4ed2796cafdf7297d3829af9b8839d48df00c3a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117930309"
---
# <a name="iwmpclosedcaptionsamilang-property"></a>Propriedade IWMPClosedCaption:: SAMILang

A propriedade **SAMILang** Obtém ou define o idioma exibido para Legendagem oculta.

## <a name="syntax"></a>Syntax


```CSharp
public System.String SAMILang {get; set;}
```


```VB

Public Property SAMILang As System.String
```





## <a name="property-value"></a>Valor da propriedade

O **System. String** que é o nome especificado no identificador de idioma de um arquivo Sami.

## <a name="remarks"></a>Comentários

Um arquivo SAMI pode conter texto para uma ou várias linguagens. Os idiomas disponíveis para legendas codificadas são definidos entre as marcas <STYLE> e </STYLE> no arquivo Sami. Um identificador de idioma é especificado com uma cadeia de caracteres alfanumérica exclusiva que é precedida por um ponto (.). O nome especificado para um idioma pode ser qualquer cadeia de caracteres. Por exemplo, o seguinte pode ser usado para definir o inglês dos EUA:


```
.ENUSCC {Name:'English Captions' lang: en-US; SAMIType:CC;}
```



Se nenhum idioma SAMI for especificado, o primeiro idioma definido no arquivo SAMI será usado por padrão.

A cadeia de caracteres que você define usando **SAMILang** deve corresponder ao atributo **Name** no especificador de idioma.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versão<br/>   | Windows Media Player 9 Series ou posterior<br/>                                                                      |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Adicionando legendas ocultas à mídia digital**](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[**Interface IWMPClosedCaption (VB e C#)**](iwmpclosedcaption--vb-and-c.md)
</dt> <dt>

[**Interface IWMPClosedCaption2 (VB e C#)**](iwmpclosedcaption2--vb-and-c.md)
</dt> </dl>

 

 





