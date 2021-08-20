---
title: Mensagem de MCIWNDM_SETINACTIVETIMER (VFW. h)
description: A \_ mensagem MCIWNDM SETINACTIVETIMER define o período de atualização usado pelo MCIWnd para atualizar o TrackBar na janela MCIWnd, atualizar as informações de posição exibidas na barra de título da janela e enviar mensagens de notificação para a janela pai quando a janela MCIWnd estiver inativa. Você pode enviar essa mensagem explicitamente ou usando a macro MCIWndSetInactiveTimer.
ms.assetid: 8900c372-0493-4a63-a027-ef6ecf8f8254
keywords:
- mensagem de MCIWNDM_SETINACTIVETIMER Windows multimídia
topic_type:
- apiref
api_name:
- MCIWNDM_SETINACTIVETIMER
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0e4161d52335e050fb8e9bcb702986492b5cd230713fcd15810a71590a92b030
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118137643"
---
# <a name="mciwndm_setinactivetimer-message"></a>\_Mensagem MCIWNDM SETINACTIVETIMER

A mensagem **MCIWNDM \_ SETINACTIVETIMER** define o período de atualização usado pelo MCIWnd para atualizar o TrackBar na janela MCIWnd, atualizar as informações de posição exibidas na barra de título da janela e enviar mensagens de notificação para a janela pai quando a janela MCIWnd estiver inativa. Você pode enviar essa mensagem explicitamente ou usando a macro [**MCIWndSetInactiveTimer**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetinactivetimer) .


```C++
MCIWNDM_SETINACTIVETIMER 
wParam = (WPARAM) (UINT) inactive; 
lParam = 0; 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="inactive"></span><span id="INACTIVE"></span>*inativo*
</dt> <dd>

Período de atualização, em milissegundos. O padrão é 2000 milissegundos.

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Essa mensagem não retorna um valor.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                       |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                             |
| Cabeçalho<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**MCIWndSetInactiveTimer**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetinactivetimer)
</dt> </dl>

 

 





