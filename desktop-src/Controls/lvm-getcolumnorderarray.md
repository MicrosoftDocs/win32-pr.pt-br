---
title: Mensagem de LVM_GETCOLUMNORDERARRAY (commctrl. h)
description: Obtém a ordem da esquerda para a direita atual de colunas em um controle de exibição de lista. Você pode enviar essa mensagem explicitamente ou usar a \_ macro GetColumnOrderArray do ListView.
ms.assetid: d4636aa8-c61e-4467-abc7-eea897bf370e
keywords:
- Controles de LVM_GETCOLUMNORDERARRAY de mensagens do Windows
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
ms.openlocfilehash: aee387f65abd3f30826e361778d5acac02dfab7c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104008867"
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

## <a name="return-value"></a>Retornar valor

Se for bem-sucedido, retornará zero e o buffer em *lParam* receberá o índice de coluna de cada coluna no controle na ordem em que aparecem da esquerda para a direita. Caso contrário, o valor de retorno será zero.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





