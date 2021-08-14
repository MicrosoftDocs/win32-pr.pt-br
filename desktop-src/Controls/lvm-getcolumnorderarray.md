---
title: Mensagem de LVM_GETCOLUMNORDERARRAY (commctrl. h)
description: Obtém a ordem da esquerda para a direita atual de colunas em um controle de exibição de lista. Você pode enviar essa mensagem explicitamente ou usar a \_ macro GetColumnOrderArray do ListView.
ms.assetid: d4636aa8-c61e-4467-abc7-eea897bf370e
keywords:
- controles de Windows de mensagem de LVM_GETCOLUMNORDERARRAY
topic_type:
- apiref
api_name:
- LVM_GETCOLUMNORDERARRAY
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ea54c633c7ffc9bc580609678e8ba5f62e29429aaea6f866bb7d72b6ea326eb2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118411492"
---
# <a name="lvm_getcolumnorderarray-message"></a>\_Mensagem GETCOLUMNORDERARRAY LVM

Obtém a ordem da esquerda para a direita atual de colunas em um controle de exibição de lista. Você pode enviar essa mensagem explicitamente ou usar a [**macro \_ GetColumnOrderArray do ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getcolumnorderarray) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

O número de colunas no controle de exibição de lista.

</dd> <dt>

*lParam* 
</dt> <dd>

Um ponteiro para uma matriz de inteiros que recebe os valores de índice das colunas no controle de exibição de lista. A matriz deve ser grande o suficiente para conter elementos *wParam* .

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se for bem-sucedido, retornará zero e o buffer em *lParam* receberá o índice de coluna de cada coluna no controle na ordem em que aparecem da esquerda para a direita. Caso contrário, o valor de retorno será zero.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





