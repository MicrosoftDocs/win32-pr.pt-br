---
title: Mensagem de MCIWNDM_GETDEVICEID (VFW. h)
description: A \_ mensagem MCIWNDM DeviceID recupera o identificador do dispositivo MCI aberto no momento para usar com a função mciSendCommand. Você pode enviar essa mensagem explicitamente ou usando a macro MCIWndGetDeviceID.
ms.assetid: 188f15fa-579a-438e-a812-9a2b684127c0
keywords:
- Multimídia do Windows de mensagem MCIWNDM_GETDEVICEID
topic_type:
- apiref
api_name:
- MCIWNDM_GETDEVICEID
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b2f2271b18dcf8f295594031ab2c7c80dd8dec06
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104008977"
---
# <a name="mciwndm_getdeviceid-message"></a>\_Mensagem MCIWNDM DeviceID

A mensagem **MCIWNDM DeviceID \_** recupera o identificador do dispositivo MCI aberto no momento para usar com a função [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) . Você pode enviar essa mensagem explicitamente ou usando a macro [**MCIWndGetDeviceID**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetdeviceid) .


```C++
MCIWNDM_GETDEVICEID 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a>Valor Retornado

Retorna o identificador do dispositivo.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                       |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                             |
| Cabeçalho<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**mciSendCommand**](/previous-versions//dd757160(v=vs.85))
</dt> <dt>

[**MCIWndGetDeviceID**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetdeviceid)
</dt> </dl>

 

