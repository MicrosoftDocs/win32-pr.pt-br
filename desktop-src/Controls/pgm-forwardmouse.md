---
title: Mensagem de PGM_FORWARDMOUSE (commctrl. h)
description: Habilita ou desabilita o encaminhamento do mouse para o controle de pager. Quando o encaminhamento do mouse está habilitado, o controle de pager encaminha \_ as mensagens MOUSEMOVE do WM para a janela contida. Você pode enviar essa mensagem explicitamente ou usar a \_ macro ForwardMouse do pager.
ms.assetid: 269972fe-50b3-4c9f-b5ac-65e768b30684
keywords:
- Controles de PGM_FORWARDMOUSE de mensagens do Windows
topic_type:
- apiref
api_name:
- PGM_FORWARDMOUSE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: addc1c6bf762f540e9d7d785a5af2ba3fb7da93c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105756234"
---
# <a name="pgm_forwardmouse-message"></a>\_Mensagem FORWARDMOUSE do PGM

Habilita ou desabilita o encaminhamento do mouse para o controle de pager. Quando o encaminhamento do mouse está habilitado, o controle de pager encaminha as mensagens [**\_ MOUSEMOVE do WM**](/windows/desktop/inputdev/wm-mousemove) para a janela contida. Você pode enviar essa mensagem explicitamente ou usar a [**macro \_ ForwardMouse do pager**](/windows/desktop/api/Commctrl/nf-commctrl-pager_forwardmouse) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Valor **bool** que determina se o encaminhamento do mouse está habilitado ou desabilitado. Se esse valor for diferente de zero, o encaminhamento do mouse será habilitado. Se esse valor for zero, o encaminhamento do mouse será desabilitado.

</dd> <dt>

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



 

