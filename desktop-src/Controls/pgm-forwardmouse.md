---
title: PGM_FORWARDMOUSE mensagem (Commctrl.h)
description: Habilita ou desabilita o encaminhamento do mouse para o controle de pager. Quando o encaminhamento do mouse está habilitado, o controle de pager encaminha mensagens WM \_ MOUSEMOVE para a janela contida. Você pode enviar essa mensagem explicitamente ou usar a \_ macro ForwardMouse do Pager.
ms.assetid: 269972fe-50b3-4c9f-b5ac-65e768b30684
keywords:
- PGM_FORWARDMOUSE controles de Windows mensagem
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
ms.openlocfilehash: 705b63ad39faea86e1f38a5b59dc73c6fc12f1e19fc17d0619c9a4b3dd5c6d26
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120046966"
---
# <a name="pgm_forwardmouse-message"></a>Mensagem PGM \_ FORWARDMOUSE

Habilita ou desabilita o encaminhamento do mouse para o controle de pager. Quando o encaminhamento do mouse está habilitado, o controle de pager encaminha mensagens [**WM \_ MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove) para a janela contida. Você pode enviar essa mensagem explicitamente ou usar a macro [**\_ ForwardMouse do Pager.**](/windows/desktop/api/Commctrl/nf-commctrl-pager_forwardmouse)

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

**Valor BOOL** que determina se o encaminhamento do mouse está habilitado ou desabilitado. Se esse valor for não zero, o encaminhamento do mouse será habilitado. Se esse valor for zero, o encaminhamento do mouse será desabilitado.

</dd> <dt>

*lParam* 
</dt> <dd>Deve ser zero.</dd> </dl>

## <a name="return-value"></a>Valor retornado

O valor de retorno não é usado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

