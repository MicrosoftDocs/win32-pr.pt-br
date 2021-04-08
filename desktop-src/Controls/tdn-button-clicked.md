---
title: TDN_BUTTON_CLICKED código de notificação (commctrl. h)
description: Enviado por uma caixa de diálogo de tarefa quando o usuário seleciona um botão ou link de comando na caixa de diálogo de tarefa. Esse código de notificação é recebido somente por meio da função de retorno de chamada da caixa de diálogo de tarefa, que pode ser registrada usando o método TaskDialogIndirect.
ms.assetid: eefe48f8-8a80-4280-8a7e-244d9b699ec7
keywords:
- TDN_BUTTON_CLICKED de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- TDN_BUTTON_CLICKED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a7a0b799f4163633194306edaa1703e068e93c9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103919163"
---
# <a name="tdn_button_clicked-notification-code"></a>O \_ botão TDN \_ clicou em código de notificação

Enviado por uma caixa de diálogo de tarefa quando o usuário seleciona um botão ou link de comando na caixa de diálogo de tarefa. Esse código de notificação é recebido somente por meio da função de retorno de chamada da caixa de diálogo de tarefa, que pode ser registrada usando o método [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) .


```C++
TDN_BUTTON_CLICKED  

   WPARAM wParam;
   LPARAM lParam;
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Um **int** que especifica a ID do botão ou link o que foi selecionado.

</dd> <dt>

*lParam* 
</dt> <dd>

Deve ser zero.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Para impedir que a caixa de diálogo de tarefa seja fechada, o aplicativo deve retornar **S \_ false**, caso contrário, a caixa de diálogo de tarefa será fechada e a ID do botão será retornada por meio da chamada de aplicativo original.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





