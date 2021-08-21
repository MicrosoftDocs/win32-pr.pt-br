---
title: MCIWNDM_CAN_PLAY mensagem (Vfw.h)
description: A mensagem MCIWNDM CAN PLAY determina se um dispositivo MCI pode reproduzir um arquivo de dados ou \_ conteúdo de algum outro \_ tipo. Você pode enviar essa mensagem explicitamente ou usando a macro MCIWndCanPlay.
ms.assetid: dbb742b0-b8ab-4b80-96da-c4823a4747c9
keywords:
- MCIWNDM_CAN_PLAY mensagem Windows Multimídia
topic_type:
- apiref
api_name:
- MCIWNDM_CAN_PLAY
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 84d067b01dbce8aaab7c78ab24c3d11fc5d4a3a19b9bfdb663eb653ebc0c553c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118374238"
---
# <a name="mciwndm_can_play-message"></a>Mensagem MCIWNDM \_ CAN \_ PLAY

A **mensagem MCIWNDM \_ CAN \_ PLAY** determina se um dispositivo MCI pode reproduzir um arquivo de dados ou conteúdo de algum outro tipo. Você pode enviar essa mensagem explicitamente ou usando a macro [**MCIWndCanPlay.**](/windows/desktop/api/Vfw/nf-vfw-mciwndcanplay)


```C++
MCIWNDM_CAN_PLAY 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a>Valor Retornado

Retornará **TRUE se** o dispositivo for compatível com a reprodução dos dados ou **false** caso contrário.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                       |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                             |
| Cabeçalho<br/>                   | <dl> <dt>Vfw.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**MCIWndCanPlay**](/windows/desktop/api/Vfw/nf-vfw-mciwndcanplay)
</dt> </dl>

 

 





