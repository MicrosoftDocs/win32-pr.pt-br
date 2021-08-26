---
title: Mensagem de TDM_CLICK_RADIO_BUTTON (commctrl. h)
description: Simula a ação de um botão de opção clique em uma caixa de diálogo de tarefa.
ms.assetid: ad1616fc-f64d-4575-8bd1-7ce63185d725
keywords:
- controles de Windows de mensagem de TDM_CLICK_RADIO_BUTTON
topic_type:
- apiref
api_name:
- TDM_CLICK_RADIO_BUTTON
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 80c1eb7e72030a3c2dadc61bfd90027dab032c3342a25c72e4da9dd9a7338142
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120104656"
---
# <a name="tdm_click_radio_button-message"></a>\_Mensagem do \_ botão de opção de clique do TDM \_

Simula a ação de um botão de opção clique em uma caixa de diálogo de tarefa.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* \[ no\]
</dt> <dd>

Um valor **int** que especifica a ID do botão de opção a ser clicado.

</dd> <dt>

*lParam* \[ no\]
</dt> <dd>

Deve ser zero.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O valor de retorno é ignorado.

## <a name="remarks"></a>Comentários

A ID do botão de opção especificado é enviada para a função de retorno de chamada [**TaskDialogCallbackProc**](/windows/win32/api/commctrl/nc-commctrl-pftaskdialogcallback) como parte de um [botão de \_ opção TDN \_ \_ clicado](tdn-radio-button-clicked.md) no código de notificação. Depois que a função de retorno de chamada retornar, o botão de opção será selecionado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

