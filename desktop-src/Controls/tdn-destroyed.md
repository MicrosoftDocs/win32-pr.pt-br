---
title: TDN_DESTROYED código de notificação (commctrl. h)
description: Enviado por uma caixa de diálogo de tarefa quando é destruído e seu identificador de janela não é mais válido. Esse código de notificação é recebido somente por meio da função de retorno de chamada da caixa de diálogo de tarefa, que pode ser registrada usando o método TaskDialogIndirect.
ms.assetid: bbebb77f-e078-46bf-a42d-65dab4f8a972
keywords:
- TDN_DESTROYED de código de notificação controles do Windows
topic_type:
- apiref
api_name:
- TDN_DESTROYED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3d3da93435371e696de3d4dce8deeea43926b73b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824789"
---
# <a name="tdn_destroyed-notification-code"></a>\_Código de notificação destruído TDN

Enviado por uma caixa de diálogo de tarefa quando é destruído e seu identificador de janela não é mais válido. Esse código de notificação é recebido somente por meio da função de retorno de chamada da caixa de diálogo de tarefa, que pode ser registrada usando o método [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) .


```C++
TDN_DESTROYED

   WPARAM wParam;
   LPARAM lParam;
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Deve ser zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Deve ser zero.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O valor de retorno é ignorado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





