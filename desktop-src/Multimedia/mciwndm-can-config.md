---
title: Mensagem de MCIWNDM_CAN_CONFIG (VFW. h)
description: A mensagem de configuração de MCIWNDM \_ pode \_ determinar se um dispositivo MCI pode exibir uma caixa de diálogo de configuração. Você pode enviar essa mensagem explicitamente ou usando a macro MCIWndCanConfig.
ms.assetid: f1eb22a8-d0fc-4d2c-a414-392e560cfbed
keywords:
- Multimídia do Windows de mensagem MCIWNDM_CAN_CONFIG
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
ms.openlocfilehash: 816a8c1dfaec6fc7d7854f8873ce05e74e4de6bc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455953"
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

 

 





