---
title: Mensagem de MCIWNDM_GETVOLUME (VFW. h)
description: A \_ mensagem GETVOLUME MCIWNDM recupera a configuração de volume atual de um dispositivo MCI. Você pode enviar essa mensagem explicitamente ou usando a macro MCIWndGetVolume.
ms.assetid: 3f1de023-4da8-4899-accc-409701d6e921
keywords:
- Multimídia do Windows de mensagem MCIWNDM_GETVOLUME
topic_type:
- apiref
api_name:
- MCIWNDM_GETVOLUME
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4aa11fb13a56dda7cb83e3d6c98b4b66083e91b9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369884"
---
# <a name="mciwndm_getvolume-message"></a>\_Mensagem GETVOLUME MCIWNDM

A **mensagem \_ GetVolume MCIWNDM** recupera a configuração de volume atual de um dispositivo MCI. Você pode enviar essa mensagem explicitamente ou usando a macro [**MCIWndGetVolume**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetvolume) .


```C++
MCIWNDM_GETVOLUME 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a>Valor Retornado

Retorna a configuração de volume atual. O valor padrão é 1000. Valores mais altos indicam volumes mais altos, valores mais baixos indicam volumes mais silenciosos.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                       |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                             |
| Cabeçalho<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**MCIWndGetVolume**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetvolume)
</dt> </dl>

 

 





