---
title: Propriedade SAMIstyle IWMPClosedCaption
description: A propriedade SAMIstyle Obtém ou define o estilo de legendagem oculta.
ms.assetid: 0b1f92c6-b659-4ade-90c8-62a06e475f5c
keywords:
- Propriedade SAMIstyle Windows Media Player
- Propriedade SAMIstyle Windows Media Player, interface IWMPClosedCaption
- Interface IWMPClosedCaption Windows Media Player, Propriedade SAMIstyle
topic_type:
- apiref
api_name:
- IWMPClosedCaption.SAMIStyle
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9bd0b48fc1807d6ca1854651c7f222183a845be3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751133"
---
# <a name="iwmpclosedcaptionsamistyle-property"></a>Propriedade IWMPClosedCaption:: SAMIstyle

A propriedade **samistyle** Obtém ou define o estilo de legendagem oculta.

## <a name="syntax"></a>Syntax


```CSharp
public System.String SAMIStyle {get; set;}
```


```VB

Public Property SAMIStyle As System.String
```





## <a name="property-value"></a>Valor da propriedade

O **System. String** que é o nome especificado no identificador de estilo de um arquivo Sami.

## <a name="remarks"></a>Comentários

Um arquivo SAMI pode conter várias definições de estilo de formato. Os estilos SAMI são definidos entre as marcas <STYLE> e </STYLE> no arquivo Sami. Um estilo é definido com uma cadeia de caracteres de texto precedida por um \# caractere. Por exemplo:


```
#Emphasis1 {Name: Big Bold Italic; font-size: 14pt; text-align: center;
            color: blue; font-family: sans-serif; font-weight: bold;
            font-style: italic;}
```



Isso especifica um estilo que produz uma fonte específica.

Se nenhum estilo SAMI for especificado, o primeiro estilo definido no arquivo SAMI será usado por padrão.

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

 

 





