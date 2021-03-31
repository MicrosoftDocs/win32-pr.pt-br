---
title: Mensagem de MCIWNDM_SETTIMERS (VFW. h)
description: A \_ mensagem SETtimers MCIWNDM define os períodos de atualização usados pelo MCIWnd para atualizar o TrackBar na janela MCIWnd, atualizar as informações de posição exibidas na barra de título da janela e enviar mensagens de notificação para a janela pai.
ms.assetid: 06407c67-b620-4f80-9fe9-456cdf3d0666
keywords:
- Multimídia do Windows de mensagem MCIWNDM_SETTIMERS
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
ms.openlocfilehash: 7bba3fa2e474a15dc23deb9cdc6d00d148b8cd3a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644333"
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

Período de atualização usado pelo MCIWnd quando é a janela ativa. O valor padrão é 500 milissegundos. O armazenamento para esse valor é limitado a 16 bits.

</dd> <dt>

<span id="inactive"></span><span id="INACTIVE"></span>*inativo*
</dt> <dd>

Período de atualização usado pelo MCIWnd quando é a janela inativa. O valor padrão é 2000 milissegundos. O armazenamento para esse valor é limitado a 16 bits.

</dd> </dl>

## <a name="return-value"></a>Valor Retornado

Essa mensagem não retorna um valor.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                       |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                             |
| Cabeçalho<br/>                   | <dl> <dt>VFW. h</dt> </dl> |



## <a name="see-also"></a>Consulte também

<dl> <dt>

[**MCIWndSetTimers**](/windows/desktop/api/Vfw/nf-vfw-mciwndsettimers)
</dt> </dl>

 

 





