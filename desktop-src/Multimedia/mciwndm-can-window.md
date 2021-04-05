---
title: Mensagem de MCIWNDM_CAN_WINDOW (VFW. h)
description: A \_ mensagem de janela MCIWNDM pode \_ determinar se um dispositivo MCI dá suporte a comandos MCI orientados por janela. Você pode enviar essa mensagem explicitamente ou usando a macro MCIWndCanWindow.
ms.assetid: bf89c096-1272-441e-9334-2b4215dbc979
keywords:
- Multimídia do Windows de mensagem MCIWNDM_CAN_WINDOW
topic_type:
- apiref
api_name:
- MCIWNDM_CAN_WINDOW
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d638b61093483b6e834b57af1d5c892d77d0f1d4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918327"
---
# <a name="mciwndm_can_window-message"></a>MCIWNDM \_ pode \_ janela de mensagem

A mensagem de **\_ \_ janela MCIWNDM pode** determinar se um dispositivo MCI dá suporte a comandos MCI orientados por janela. Você pode enviar essa mensagem explicitamente ou usando a macro [**MCIWndCanWindow**](/windows/desktop/api/Vfw/nf-vfw-mciwndcanwindow) .


```C++
MCIWNDM_CAN_WINDOW 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a>Valor Retornado

Retornará **true** se o dispositivo der suporte a comandos MCI orientados por janela ou **false** caso contrário.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                       |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                             |
| Cabeçalho<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**MCIWndCanWindow**](/windows/desktop/api/Vfw/nf-vfw-mciwndcanwindow)
</dt> </dl>

 

 





