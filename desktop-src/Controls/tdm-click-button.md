---
title: Mensagem de TDM_CLICK_BUTTON (commctrl. h)
description: Simula a ação de um clique de botão em uma caixa de diálogo de tarefa.
ms.assetid: cc8a8252-3418-4a28-bfb7-11d6e3fee903
keywords:
- Controles de TDM_CLICK_BUTTON de mensagens do Windows
topic_type:
- apiref
api_name:
- TDM_CLICK_BUTTON
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e5933668eca907f36414113091b8901bfb9c110
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105751301"
---
# <a name="tdm_click_button-message"></a>Mensagem do botão de \_ clique do TDM \_

Simula a ação de um clique de botão em uma caixa de diálogo de tarefa.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* \[ no\]
</dt> <dd>

Um **int** que especifica a ID do botão a ser clicado.

</dd> <dt>

*lParam* \[ no\]
</dt> <dd>

Deve ser zero.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O valor de retorno é ignorado.

## <a name="remarks"></a>Comentários

A ID do botão especificada por *wParam* é enviada para a função de retorno de chamada [**TaskDialogCallbackProc**](/windows/win32/api/commctrl/nc-commctrl-pftaskdialogcallback) como parte de um código de notificação [ \_ \_ clicado no botão TDN](tdn-button-clicked.md) . Depois que a função de retorno de chamada retornar, a caixa de diálogo de tarefa será fechada se S \_ OK tiver retornado da função de retorno de chamada. Se S \_ false for retornado da função de retorno de chamada, a caixa de diálogo de tarefa permanecerá ativa.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

