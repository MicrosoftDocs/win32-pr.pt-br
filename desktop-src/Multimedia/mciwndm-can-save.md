---
title: Mensagem de MCIWNDM_CAN_SAVE (VFW. h)
description: O MCIWNDM \_ pode \_ salvar a mensagem determina se um dispositivo MCI pode salvar dados. Você pode enviar essa mensagem explicitamente ou usando a macro MCIWndCanSave.
ms.assetid: b4e27190-b095-494b-9ed3-10653bea187b
keywords:
- Multimídia do Windows de mensagem MCIWNDM_CAN_SAVE
topic_type:
- apiref
api_name:
- MCIWNDM_CAN_SAVE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 11b60b8a5d93ac80befc8beeb6665399efe44f1e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454801"
---
# <a name="mciwndm_can_save-message"></a>MCIWNDM \_ pode \_ salvar a mensagem

O **MCIWNDM \_ pode \_ salvar** a mensagem determina se um dispositivo MCI pode salvar dados. Você pode enviar essa mensagem explicitamente ou usando a macro [**MCIWndCanSave**](/windows/desktop/api/Vfw/nf-vfw-mciwndcansave) .


```C++
MCIWNDM_CAN_SAVE 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a>Valor Retornado

Retornará **true** se o dispositivo der suporte a salvar ou **false** caso contrário.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                       |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                             |
| Cabeçalho<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**MCIWndCanSave**](/windows/desktop/api/Vfw/nf-vfw-mciwndcansave)
</dt> </dl>

 

 





