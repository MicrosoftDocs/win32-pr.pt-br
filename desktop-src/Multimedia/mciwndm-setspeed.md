---
title: MCIWNDM_SETSPEED mensagem (Vfw.h)
description: A mensagem MCIWNDM \_ SETSPEED define a velocidade de reprodução de um dispositivo MCI. Você pode enviar essa mensagem explicitamente ou usando a macro MCIWndSetSpeed.
ms.assetid: 7658dd25-dc68-4bd1-b995-df06b509be16
keywords:
- MCIWNDM_SETSPEED mensagem Windows Multimídia
topic_type:
- apiref
api_name:
- MCIWNDM_SETSPEED
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6de0d78fef7723dab0ae2e2d3923f73f872e38dfd9c3e0f42443f7141f020336
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119782986"
---
# <a name="mciwndm_setspeed-message"></a>Mensagem MCIWNDM \_ SETSPEED

A **mensagem MCIWNDM \_ SETSPEED** define a velocidade de reprodução de um dispositivo MCI. Você pode enviar essa mensagem explicitamente ou usando a macro [**MCIWndSetSpeed.**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetspeed)


```C++
MCIWNDM_SETSPEED 
wParam = 0; 
lParam = (LPARAM) (UINT) iSpeed; 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="iSpeed"></span><span id="ispeed"></span><span id="ISPEED"></span>*iSpeed*
</dt> <dd>

Velocidade de reprodução. Especifique 1000 para velocidade normal, valores maiores para velocidades mais rápidas e valores menores para velocidades mais lentas.

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Retornará zero se for bem-sucedido ou um erro, caso contrário.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                       |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                             |
| Cabeçalho<br/>                   | <dl> <dt>Vfw.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**MCIWndSetSpeed**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetspeed)
</dt> </dl>

 

 





