---
title: Propriedade ActiveBasicDevice IsAudioSupported (PlayToDevice.h)
description: Obtém um valor que indica se o dispositivo dá suporte a áudio.
ms.assetid: 22ABB97B-58E7-4C21-B359-C10DFC9C7194
keywords:
- API de Streaming de Mídia da propriedade IsAudioSupported
- API de Streaming de Mídia da propriedade IsAudioSupported, interface ActiveBasicDevice
- API de Streaming de Mídia da interface ActiveBasicDevice, propriedade IsAudioSupported
topic_type:
- apiref
api_name:
- ActiveBasicDevice.IsAudioSupported
- ActiveBasicDevice.get_IsAudioSupported
api_location:
- playtodevice.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 20125114b6cd134d153ad6425af5af410faf524714a2e505a37fbf57dcda21e4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119462416"
---
# <a name="activebasicdeviceisaudiosupported-property"></a>Propriedade ActiveBasicDevice::IsAudioSupported

Obtém um valor que indica se o dispositivo dá suporte a áudio.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT get_IsAudioSupported(
  [out] boolean *value
);
```



## <a name="property-value"></a>Valor da propriedade

Um ponteiro para um **booliana** que indica se o dispositivo dá suporte a áudio.

**true** se o dispositivo for compatível com áudio; caso contrário, **false.**

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Windows 8.1 somente aplicativos da área de trabalho\]<br/>                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2012 Somente \[ aplicativos da área de trabalho R2\]<br/>                                     |
| parâmetro<br/>                   | <dl> <dt>PlayToDevice.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>PlayToDevice.idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Playtodevice.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ActiveBasicDevice**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85))
</dt> </dl>

 

