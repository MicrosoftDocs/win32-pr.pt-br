---
title: Mensagem de MCIWNDM_CAN_RECORD (VFW. h)
description: O MCIWNDM \_ pode \_ registrar a mensagem determina se um dispositivo MCI dá suporte à gravação. Você pode enviar essa mensagem explicitamente ou usando a macro MCIWndCanRecord.
ms.assetid: b5a789fa-6a88-487d-a374-8f4798ee5a62
keywords:
- mensagem de MCIWNDM_CAN_RECORD Windows multimídia
topic_type:
- apiref
api_name:
- MCIWNDM_CAN_RECORD
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5df46ce0cbffe17f890e50159a13a93192e67f60e323d6ba711bee6af7ac3f79
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119429646"
---
# <a name="mciwndm_can_record-message"></a>MCIWNDM \_ pode \_ registrar a mensagem

O **MCIWNDM \_ pode \_ registrar** a mensagem determina se um dispositivo MCI dá suporte à gravação. Você pode enviar essa mensagem explicitamente ou usando a macro [**MCIWndCanRecord**](/windows/desktop/api/Vfw/nf-vfw-mciwndcanrecord) .


```C++
MCIWNDM_CAN_RECORD 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a>Valor Retornado

Retornará **true** se o dispositivo der suporte à gravação ou **false** .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                       |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                             |
| Cabeçalho<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**MCIWndCanRecord**](/windows/desktop/api/Vfw/nf-vfw-mciwndcanrecord)
</dt> </dl>

 

 





