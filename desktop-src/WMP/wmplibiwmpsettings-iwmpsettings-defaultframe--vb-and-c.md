---
title: Propriedade DefaultFrame do IWMPSettings
description: A propriedade DefaultFrame Obtém ou define o nome do quadro usado para exibir uma URL recebida em um \_ evento AxWindowsMediaPlayer WMPOCXEvents \_ ScriptCommandEvent.
ms.assetid: 92c775ac-5ff1-4d21-b21d-491bc48a033f
keywords:
- Propriedade DefaultFrame do Windows Media Player
- Propriedade DefaultFrame do Windows Media Player, interface IWMPSettings
- Interface IWMPSettings do Windows Media Player, Propriedade DefaultFrame
topic_type:
- apiref
api_name:
- IWMPSettings.defaultFrame
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 28539640214165ab5b2808762ed854b19b434311
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105815490"
---
# <a name="iwmpsettingsdefaultframe-property"></a>IWMPSettings: Propriedade efaultFrame de:d

A propriedade **DefaultFrame** Obtém ou define o nome do quadro usado para exibir uma URL recebida em um evento **AxWindowsMediaPlayer \_ WMPOCXEvents \_ ScriptCommandEvent** .

## <a name="syntax"></a>Syntax


```CSharp
public System.String defaultFrame {get; set;}
```


```VB

Public Property defaultFrame As System.String
```





## <a name="property-value"></a>Valor da propriedade

Um **System. String** que é o valor do atributo Name do elemento de **quadro** de destino.

## <a name="remarks"></a>Comentários

Se um quadro de destino for especificado no evento **\_ WMPOCXEvents \_ ScriptCommandEvent** em si, essa propriedade será ignorada.

Essa propriedade é ignorada ao usar o miniaplicativo Java do Netscape Navigator. No Netscape Navigator, cada comando de script de URL recebido exibirá a URL em uma nova janela do navegador, independentemente do valor de **DefaultFrame**.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versão<br/>   | Windows Media Player 9 Series ou posterior<br/>                                                                      |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Evento AxWindowsMediaPlayer. ScriptCommand (VB e C#)**](axwmplib-axwindowsmediaplayer-scriptcommand.md)
</dt> <dt>

[**Interface IWMPSettings (VB e C#)**](iwmpsettings--vb-and-c.md)
</dt> </dl>

 

 





