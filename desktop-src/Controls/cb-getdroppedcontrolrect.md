---
title: Mensagem de CB_GETDROPPEDCONTROLRECT (WinUser. h)
description: Um aplicativo envia uma \_ mensagem de GETDROPPEDCONTROLRECT CB para recuperar as coordenadas de tela de uma caixa de combinação em seu estado suspenso.
ms.assetid: fd8d78c0-e1a8-49c8-9e35-a105d00b863c
keywords:
- Controles de CB_GETDROPPEDCONTROLRECT de mensagens do Windows
topic_type:
- apiref
api_name:
- CB_GETDROPPEDCONTROLRECT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: adff5ad10ff91557b2579006dae6e1258650d74e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455352"
---
# <a name="cb_getdroppedcontrolrect-message"></a>\_Mensagem de GETDROPPEDCONTROLRECT CB

Um aplicativo envia uma mensagem de **\_ GETDROPPEDCONTROLRECT CB** para recuperar as coordenadas de tela de uma caixa de combinação em seu estado suspenso.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Este parâmetro não é usado.

</dd> <dt>

*lParam* 
</dt> <dd>

Um ponteiro para a estrutura [**Rect**](/previous-versions//dd162897(v=vs.85)) que recebe as coordenadas da caixa de combinação em seu estado suspenso.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se a mensagem tiver sucesso, o valor de retorno será diferente de zero.

Se a mensagem falhar, o valor de retorno será zero.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                                           |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                                     |
| parâmetro<br/>                   | <dl> <dt>WinUser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**RECT**](/previous-versions//dd162897(v=vs.85))
</dt> </dl>

 

