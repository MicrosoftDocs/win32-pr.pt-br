---
title: Mensagem de MCIWNDM_CAN_EJECT (VFW. h)
description: A MCIWNDM \_ pode \_ ejetar a mensagem para determinar se um dispositivo MCI pode ejetar sua mídia. Você pode enviar essa mensagem explicitamente ou usando a macro MCIWndCanEject.
ms.assetid: e9bd33c4-0ad8-4c0a-8b75-52011b58904d
keywords:
- mensagem de MCIWNDM_CAN_EJECT Windows multimídia
topic_type:
- apiref
api_name:
- MCIWNDM_CAN_EJECT
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fde4c9fec3972fe0e22b0a562454e1ef680e9ccae3851c272d28468fc2c91f74
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119429666"
---
# <a name="mciwndm_can_eject-message"></a>MCIWNDM \_ pode \_ ejetar a mensagem

A **MCIWNDM \_ pode \_ ejetar** a mensagem para determinar se um dispositivo MCI pode ejetar sua mídia. Você pode enviar essa mensagem explicitamente ou usando a macro [**MCIWndCanEject**](/windows/desktop/api/Vfw/nf-vfw-mciwndcaneject) .


```C++
MCIWNDM_CAN_EJECT 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a>Valor Retornado

Retornará **true** se o dispositivo puder ejetar sua mídia ou **false** .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                       |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                             |
| Cabeçalho<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**MCIWndCanEject**](/windows/desktop/api/Vfw/nf-vfw-mciwndcaneject)
</dt> </dl>

 

 





