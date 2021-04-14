---
title: Mensagem de PGM_RECALCSIZE (commctrl. h)
description: Força o controle de pager a recalcular o tamanho da janela contida. O envio dessa mensagem resultará na envio de uma \_ notificação PGN CALCSIZE. Você pode enviar essa mensagem explicitamente ou usar a \_ macro RecalcSize do pager.
ms.assetid: 51b75ce8-2b41-4f1a-830e-b25e7d77dccb
keywords:
- Controles de PGM_RECALCSIZE de mensagens do Windows
topic_type:
- apiref
api_name:
- PGM_RECALCSIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b407221543a42b4dbff4490508a02b570622d69c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455011"
---
# <a name="pgm_recalcsize-message"></a>\_Mensagem RECALCSIZE do PGM

Força o controle de pager a recalcular o tamanho da janela contida. O envio dessa mensagem resultará na envio de uma notificação [PGN \_ CALCSIZE](pgn-calcsize.md) . Você pode enviar essa mensagem explicitamente ou usar a [**macro \_ RecalcSize do pager**](/windows/desktop/api/Commctrl/nf-commctrl-pager_recalcsize) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lParam* 
</dt> <dd>Deve ser zero.</dd> </dl>

## <a name="return-value"></a>Retornar valor

O valor de retorno não é usado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





