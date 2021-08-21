---
title: Propriedade defaultFrame IWMPSettings
description: A propriedade defaultFrame obtém ou define o nome do quadro usado para exibir uma URL recebida em um evento AxWindowsMediaPlayer \_ WMPOCXEvents \_ ScriptCommandEvent.
ms.assetid: 92c775ac-5ff1-4d21-b21d-491bc48a033f
keywords:
- propriedade defaultFrame Windows Media Player
- a propriedade defaultFrame Windows Media Player interface , IWMPSettings
- Interface IWMPSettings Windows Media Player , propriedade defaultFrame
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
ms.openlocfilehash: b39352b2c49bfdcd50f3e5c74d88a9fafef6752034dbd220cda3bb34dc0ed5de
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119053434"
---
# <a name="iwmpsettingsdefaultframe-property"></a>Propriedade IWMPSettings::d efaultFrame

A **propriedade defaultFrame** obtém ou define o nome do quadro usado para exibir uma URL recebida em um evento **AxWindowsMediaPlayer \_ WMPOCXEvents \_ ScriptCommandEvent.**

## <a name="syntax"></a>Syntax


```CSharp
public System.String defaultFrame {get; set;}
```


```VB

Public Property defaultFrame As System.String
```





## <a name="property-value"></a>Valor da propriedade

Um **System.String** que é o valor do atributo name do elemento **FRAME de** destino.

## <a name="remarks"></a>Comentários

Se um quadro de destino for especificado no evento **\_ WMPOCXEvents \_ ScriptCommandEvent** em si, essa propriedade será ignorada.

Essa propriedade é ignorada ao usar o applet Java do Netscape Navigator. No Netscape Navigator, cada comando de script de URL recebido exibirá a URL em uma nova janela do navegador, independentemente do valor **de defaultFrame**.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Versão<br/>   | Windows Media Player série 9 ou posterior<br/>                                                                      |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Evento AxWindowsMediaPlayer.ScriptCommand (VB e C#)**](axwmplib-axwindowsmediaplayer-scriptcommand.md)
</dt> <dt>

[**Interface IWMPSettings (VB e C#)**](iwmpsettings--vb-and-c.md)
</dt> </dl>

 

 





