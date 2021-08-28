---
title: Propriedade SAMILang IWMPClosedCaption
description: A propriedade SAMILang obtém ou define o idioma exibido para legendas fechadas.
ms.assetid: dcdd6bcd-b869-439f-b500-df26d3873b04
keywords:
- Propriedade SAMILang Windows Media Player
- A propriedade SAMILang Windows Media Player , interface IWMPClosedCaption
- Interface IWMPClosedCaption Windows Media Player , propriedade SAMILang
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
ms.openlocfilehash: a9577f7d9030a12a12596fe2cdc2a999922658ce
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122887176"
---
# <a name="iwmpclosedcaptionsamilang-property"></a>Propriedade IWMPClosedCaption::SAMILang

A **propriedade SAMILang** obtém ou define o idioma exibido para legendas fechadas.

## <a name="syntax"></a>Syntax


```CSharp
public System.String SAMILang {get; set;}
```


```VB

Public Property SAMILang As System.String
```





## <a name="property-value"></a>Valor da propriedade

O **System.String** que é o nome especificado no identificador de idioma de um arquivo SAMI.

## <a name="remarks"></a>Comentários

Um arquivo SAMI pode conter texto para um ou vários idiomas. Os idiomas disponíveis para legendas fechadas são definidos entre &lt; o STYLE e as marcas no arquivo &gt; </STYLE> SAMI. Um identificador de idioma é especificado com uma cadeia de caracteres alfanumérico exclusiva precedida por um ponto (.). O nome especificado para um idioma pode ser qualquer cadeia de caracteres. Por exemplo, o seguinte pode ser usado para definir o inglês dos EUA:


```
.ENUSCC {Name:'English Captions' lang: en-US; SAMIType:CC;}
```



Se nenhuma linguagem SAMI for especificada, o primeiro idioma definido no arquivo SAMI será usado por padrão.

A cadeia de caracteres definida **usando SAMILang** deve corresponder ao **atributo Name** no especificador de idioma.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versão<br/>   | Windows Media Player série 9 ou posterior<br/>                                                                      |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Adicionando legendas fechadas à mídia digital**](adding-closed-captions-to-digital-media.md)
</dt> <dt>

[**Interface IWMPClosedCaption (VB e C#)**](iwmpclosedcaption--vb-and-c.md)
</dt> <dt>

[**Interface IWMPClosedCaption2 (VB e C#)**](iwmpclosedcaption2--vb-and-c.md)
</dt> </dl>

 

 





