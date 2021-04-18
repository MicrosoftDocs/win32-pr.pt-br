---
title: TDN_EXPANDO_BUTTON_CLICKED código de notificação (commctrl. h)
description: Enviado pela caixa de diálogo de tarefa quando o usuário clica no botão expando da caixa de diálogo. Essa notificação é recebida somente por meio da função de retorno de chamada da caixa de diálogo de tarefa, que pode ser registrada usando o método TaskDialogIndirect.
ms.assetid: 15e2a9d0-9986-4fb1-a15e-dd4839e45146
keywords:
- TDN_EXPANDO_BUTTON_CLICKED de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- TDN_EXPANDO_BUTTON_CLICKED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4f3c36379a8efc40c7873d817b832705b3c1e084
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105748854"
---
# <a name="tdn_expando_button_clicked-notification-code"></a>O \_ botão expanda TDN \_ \_ clicou no código de notificação

Enviado pela caixa de diálogo de tarefa quando o usuário clica no botão expando da caixa de diálogo. Essa notificação é recebida somente por meio da função de retorno de chamada da caixa de diálogo de tarefa, que pode ser registrada usando o método [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) .


```C++
TDN_EXPANDO_BUTTON_CLICKED
        
   WPARAM wParam;
   LPARAM lParam;
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Um **bool** que será **verdadeiro** se a caixa de diálogo for expandida ou **false** se não.

</dd> <dt>

*lParam* 
</dt> <dd>

Deve ser zero.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O valor de retorno é ignorado.

## <a name="remarks"></a>Comentários

O exemplo na seção sintaxe mostra a conversão para wParam antes de enviar a notificação. **LParam** não é usado e deve ser zero.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





