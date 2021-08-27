---
title: Mensagem de CB_GETDROPPEDCONTROLRECT (WinUser. h)
description: Um aplicativo envia uma \_ mensagem de GETDROPPEDCONTROLRECT CB para recuperar as coordenadas de tela de uma caixa de combinação em seu estado suspenso.
ms.assetid: fd8d78c0-e1a8-49c8-9e35-a105d00b863c
keywords:
- controles de Windows de mensagem de CB_GETDROPPEDCONTROLRECT
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
ms.openlocfilehash: c140abb139cc47020f333ccf66f71cf36d890449be91d66f51b646db22091c39
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120089276"
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

## <a name="return-value"></a>Valor retornado

Se a mensagem tiver sucesso, o valor de retorno será diferente de zero.

Se a mensagem falhar, o valor de retorno será zero.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                                           |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                                     |
| Cabeçalho<br/>                   | <dl> <dt>Winuser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**RECT**](/previous-versions//dd162897(v=vs.85))
</dt> </dl>

 

