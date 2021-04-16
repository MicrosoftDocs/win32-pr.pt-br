---
title: Mensagem de MCIWNDM_GETSPEED (VFW. h)
description: A \_ mensagem GETspeed do MCIWNDM recupera a velocidade de reprodução de um dispositivo MCI. Você pode enviar essa mensagem explicitamente ou usando a macro MCIWndGetSpeed.
ms.assetid: d10a8f88-e85e-449b-8655-bb0832031d59
keywords:
- Multimídia do Windows de mensagem MCIWNDM_GETSPEED
topic_type:
- apiref
api_name:
- MCIWNDM_GETSPEED
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c84a8ebb3e97d4543f68f3a237add8eed7706ae2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455883"
---
# <a name="mciwndm_getspeed-message"></a>MCIWNDM \_ mensagem de GETspeed

A **mensagem \_ getspeed do MCIWNDM** recupera a velocidade de reprodução de um dispositivo MCI. Você pode enviar essa mensagem explicitamente ou usando a macro [**MCIWndGetSpeed**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetspeed) .


```C++
MCIWNDM_GETSPEED 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a>Valor Retornado

Retorna a velocidade de reprodução se for bem-sucedida. O valor da velocidade normal é de 1000. Valores maiores indicam velocidades mais rápidas, valores menores indicam velocidades mais lentas.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                       |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                             |
| Cabeçalho<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**MCIWndGetSpeed**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetspeed)
</dt> </dl>

 

 





