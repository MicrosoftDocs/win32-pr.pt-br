---
title: Propriedade ActiveBasicDevice MaxVolume (PlayToDevice.h)
description: Obtém o volume máximo com suporte pelo dispositivo.
ms.assetid: EA0EC323-4A18-4CC1-8FA4-7BD302318863
keywords:
- PROPRIEDADE MaxVolume API de Streaming de Mídia
- Propriedade MaxVolume API de Streaming de Mídia, interface ActiveBasicDevice
- API de Streaming de Mídia da interface ActiveBasicDevice, propriedade MaxVolume
topic_type:
- apiref
api_name:
- ActiveBasicDevice.MaxVolume
- ActiveBasicDevice.get_MaxVolume
api_location:
- playtodevice.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 803e2e66306bce0d6fd308501edece61668d5f2e0d8041273d508b662f6cd66f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118736192"
---
# <a name="activebasicdevicemaxvolume-property"></a>Propriedade ActiveBasicDevice::MaxVolume

Obtém o volume máximo com suporte pelo dispositivo.

Esta propriedade é somente para leitura.

## <a name="syntax"></a>Sintaxe


```C++
HRESULT get_MaxVolume(
  [out] boolean *UINT32
);
```



## <a name="property-value"></a>Valor da propriedade

Um ponteiro para um **UINT32** que especifica o volume máximo com suporte pelo dispositivo.

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

 

