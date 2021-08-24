---
title: Propriedade SAMIstyle IWMPClosedCaption
description: A propriedade SAMIstyle Obtém ou define o estilo de legendagem oculta.
ms.assetid: 0b1f92c6-b659-4ade-90c8-62a06e475f5c
keywords:
- Windows Media Player da propriedade SAMIstyle
- propriedade samistyle Windows Media Player, interface IWMPClosedCaption
- interface IWMPClosedCaption Windows Media Player, propriedade samistyle
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
ms.openlocfilehash: 2cede8964636073c393cb34bfa1be22855467f4cb243834bd1e11a4ffc492665
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120031416"
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

 

 





