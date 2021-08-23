---
title: Mensagem de MCIWNDM_CAN_CONFIG (VFW. h)
description: A mensagem de configuração de MCIWNDM \_ pode \_ determinar se um dispositivo MCI pode exibir uma caixa de diálogo de configuração. Você pode enviar essa mensagem explicitamente ou usando a macro MCIWndCanConfig.
ms.assetid: f1eb22a8-d0fc-4d2c-a414-392e560cfbed
keywords:
- mensagem de MCIWNDM_CAN_CONFIG Windows multimídia
topic_type:
- apiref
api_name:
- MCIWNDM_CAN_CONFIG
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ef5b8e4f8e1ab09f128b1294034bbb715c834c3e867f31bbaae0cb6bd620be5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119525526"
---
# <a name="mciwndm_can_config-message"></a>MCIWNDM \_ pode \_ Configurar a mensagem

A mensagem de **\_ \_ configuração de MCIWNDM pode** determinar se um dispositivo MCI pode exibir uma caixa de diálogo de configuração. Você pode enviar essa mensagem explicitamente ou usando a macro [**MCIWndCanConfig**](/windows/desktop/api/Vfw/nf-vfw-mciwndcanconfig) .


```C++
MCIWNDM_CAN_CONFIG 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a>Valor Retornado

Retorna **true** se o dispositivo der suporte à configuração ou **false** caso contrário.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                       |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                             |
| Cabeçalho<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**MCIWndCanConfig**](/windows/desktop/api/Vfw/nf-vfw-mciwndcanconfig)
</dt> </dl>

 

 





