---
title: Mensagem de MCIWNDM_SETACTIVETIMER (VFW. h)
description: A \_ mensagem MCIWNDM SETACTIVETIMER define o período de atualização usado pelo MCIWnd para atualizar o TrackBar na janela MCIWnd, atualizar as informações de posição exibidas na barra de título da janela e enviar mensagens de notificação para a janela pai quando a janela MCIWnd estiver ativa. Você pode enviar essa mensagem explicitamente ou usando a macro MCIWndSetActiveTimer.
ms.assetid: a30c0091-d9bb-44a3-a7b0-d1be30adcd9c
keywords:
- Multimídia do Windows de mensagem MCIWNDM_SETACTIVETIMER
topic_type:
- apiref
api_name:
- MCIWNDM_SETACTIVETIMER
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1924a991f0627009a8e622c8f8be086b2e045635
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085900"
---
# <a name="mciwndm_setactivetimer-message"></a>\_Mensagem MCIWNDM SETACTIVETIMER

A mensagem **MCIWNDM \_ SETACTIVETIMER** define o período de atualização usado pelo MCIWnd para atualizar o TrackBar na janela MCIWnd, atualizar as informações de posição exibidas na barra de título da janela e enviar mensagens de notificação para a janela pai quando a janela MCIWnd estiver ativa. Você pode enviar essa mensagem explicitamente ou usando a macro [**MCIWndSetActiveTimer**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetactivetimer) .


```C++
MCIWNDM_SETACTIVETIMER 
wParam = (WPARAM) (UINT) active; 
lParam = 0L; 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="active"></span><span id="ACTIVE"></span>*activo*
</dt> <dd>

Período de atualização, em milissegundos. O padrão é 500 milissegundos.

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

[**MCIWndSetActiveTimer**](/windows/desktop/api/Vfw/nf-vfw-mciwndsetactivetimer)
</dt> </dl>

 

 





