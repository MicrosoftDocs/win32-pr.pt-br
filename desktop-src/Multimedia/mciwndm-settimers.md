---
title: Mensagem de MCIWNDM_SETTIMERS (VFW. h)
description: A \_ mensagem SETtimers MCIWNDM define os períodos de atualização usados pelo MCIWnd para atualizar o TrackBar na janela MCIWnd, atualizar as informações de posição exibidas na barra de título da janela e enviar mensagens de notificação para a janela pai.
ms.assetid: 06407c67-b620-4f80-9fe9-456cdf3d0666
keywords:
- mensagem de MCIWNDM_SETTIMERS Windows multimídia
topic_type:
- apiref
api_name:
- MCIWNDM_SETTIMERS
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e9c17a131827459555ae51adc5d5bd48d98fabb88fc4c1f0dbbcd1eb3673466
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119807547"
---
# <a name="mciwndm_settimers-message"></a>\_Mensagem SETtimers MCIWNDM

A **mensagem \_ settimers MCIWNDM** define os períodos de atualização usados pelo MCIWnd para atualizar o TrackBar na janela MCIWnd, atualizar as informações de posição exibidas na barra de título da janela e enviar mensagens de notificação para a janela pai. Você pode enviar essa mensagem explicitamente ou usando a macro [**MCIWndSetTimers**](/windows/desktop/api/Vfw/nf-vfw-mciwndsettimers) .


```C++
MCIWNDM_SETTIMERS 
wParam = (WPARAM) (UINT) active; 
lParam = (LPARAM) (UINT) inactive; 
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

<span id="active"></span><span id="ACTIVE"></span>*activo*
</dt> <dd>

Período de atualização usado pelo MCIWnd quando é a janela ativa. O valor padrão é 500 milissegundos. Armazenamento para esse valor é limitado a 16 bits.

</dd> <dt>

<span id="inactive"></span><span id="INACTIVE"></span>*inativo*
</dt> <dd>

Período de atualização usado pelo MCIWnd quando é a janela inativa. O valor padrão é 2000 milissegundos. Armazenamento para esse valor é limitado a 16 bits.

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

[**MCIWndSetTimers**](/windows/desktop/api/Vfw/nf-vfw-mciwndsettimers)
</dt> </dl>

 

 





