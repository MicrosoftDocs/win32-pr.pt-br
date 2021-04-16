---
title: Mensagem de MCIWNDM_CAN_PLAY (VFW. h)
description: O MCIWNDM \_ pode \_ reproduzir a mensagem para determinar se um dispositivo MCI pode reproduzir um arquivo de dados ou conteúdo de algum outro tipo. Você pode enviar essa mensagem explicitamente ou usando a macro MCIWndCanPlay.
ms.assetid: dbb742b0-b8ab-4b80-96da-c4823a4747c9
keywords:
- Multimídia do Windows de mensagem MCIWNDM_CAN_PLAY
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
ms.openlocfilehash: 043a0fc15260f7448df8d009a6b468616244269d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105757771"
---
# <a name="mciwndm_can_play-message"></a>MCIWNDM \_ pode \_ reproduzir a mensagem

O **MCIWNDM \_ pode \_ reproduzir** a mensagem para determinar se um dispositivo MCI pode reproduzir um arquivo de dados ou conteúdo de algum outro tipo. Você pode enviar essa mensagem explicitamente ou usando a macro [**MCIWndCanPlay**](/windows/desktop/api/Vfw/nf-vfw-mciwndcanplay) .


```C++
MCIWNDM_CAN_PLAY 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a>Valor Retornado

Retornará **true** se o dispositivo der suporte à reprodução dos dados ou **false** caso contrário.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                       |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                             |
| Cabeçalho<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**MCIWndCanPlay**](/windows/desktop/api/Vfw/nf-vfw-mciwndcanplay)
</dt> </dl>

 

 





