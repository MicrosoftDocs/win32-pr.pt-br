---
title: TDN_TIMER código de notificação (commctrl. h)
description: Enviado por uma caixa de diálogo de tarefa aproximadamente a cada 200 milissegundos.
ms.assetid: 5a162d97-6912-45bc-8151-1ea56cc459ea
keywords:
- TDN_TIMER código de notificação Windows controles
topic_type:
- apiref
api_name:
- TDN_TIMER
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eaf3f5d72ef8267c6600decf070875b2dd109114f910d09a5ca343f8fde44005
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120104446"
---
# <a name="tdn_timer-notification-code"></a>\_Código de notificação do temporizador TDN

Enviado por uma caixa de diálogo de tarefa aproximadamente a cada 200 milissegundos. Esse código de notificação é enviado quando o \_ sinalizador do temporizador de retorno de chamada TDF foi \_ definido no membro **dwFlags** da estrutura [**TASKDIALOGCONFIG**](/windows/desktop/api/Commctrl/ns-commctrl-taskdialogconfig) que foi passada para a função [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) . Esse código de notificação é recebido somente por meio da função de retorno de chamada da caixa de diálogo de tarefa, que pode ser registrada usando o método **TaskDialogIndirect** .


```C++
TDN_TIMER    

   WPARAM wParam;
   LPARAM lParam;
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Um **DWORD** que especifica o número de milissegundos desde que a caixa de diálogo foi criada ou esse código de notificação retornou **S \_ false**.

</dd> <dt>

*lParam* 
</dt> <dd>

Deve ser zero.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Para redefinir o desejo, o aplicativo deve retornar **S \_ false**, caso contrário, o or continuará a ser incrementado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





