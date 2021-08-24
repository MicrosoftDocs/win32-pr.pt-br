---
title: TDN_VERIFICATION_CLICKED de notificação (Commctrl.h)
description: Enviado por uma caixa de diálogo de tarefa quando o usuário clica na caixa de seleção de verificação da caixa de diálogo de tarefa. Esse código de notificação é recebido somente por meio da função de retorno de chamada da caixa de diálogo de tarefa, que pode ser registrada usando o método TaskDialogIndirect.
ms.assetid: cd7bc07a-9a70-4361-abfa-986a5a2e13e0
keywords:
- TDN_VERIFICATION_CLICKED código de notificação Windows Controles
topic_type:
- apiref
api_name:
- TDN_VERIFICATION_CLICKED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 642d247e95e77c797a5dbd8c2c5ecaf4c9b083261ea848479395f8bb22fa325d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118166639"
---
# <a name="tdn_verification_clicked-notification-code"></a>Código de notificação CLICADO EM VERIFICAÇÃO DE TDN \_ \_

Enviado por uma caixa de diálogo de tarefa quando o usuário clica na caixa de seleção de verificação da caixa de diálogo de tarefa. Esse código de notificação é recebido somente por meio da função de retorno de chamada da caixa de diálogo de tarefa, que pode ser registrada usando o [**método TaskDialogIndirect.**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect)


```C++
TDN_VERIFICATION_CLICKED

   WPARAM wParam;
   LPARAM lParam;
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Um **BOOL** que especifica o status da caixa de seleção de verificação. Será **TRUE se** a caixa de seleção de verificação estiver marcada ou **FALSE** se ela estiver desmarcada.

</dd> <dt>

*lParam* 
</dt> <dd>

Deve ser zero.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O valor de retorno é ignorado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Referência**
</dt> <dt>

[*TaskDialogCallbackProc*](/windows/win32/api/commctrl/nc-commctrl-pftaskdialogcallback)
</dt> </dl>

 

