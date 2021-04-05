---
title: Mensagem de LVM_GETNUMBEROFWORKAREAS (commctrl. h)
description: Recupera o número de áreas de trabalho em um controle de exibição de lista. Você pode enviar essa mensagem explicitamente ou usar a \_ macro GetNumberOfWorkAreas do ListView.
ms.assetid: ce0bcccd-62a2-45a4-959e-9959c9ca0c46
keywords:
- Controles de LVM_GETNUMBEROFWORKAREAS de mensagens do Windows
topic_type:
- apiref
api_name:
- LVM_GETNUMBEROFWORKAREAS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a73c62b7184ba60b979356a98a93d2579c8f74a8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918968"
---
# <a name="lvm_getnumberofworkareas-message"></a>\_Mensagem GETNUMBEROFWORKAREAS LVM

Recupera o número de áreas de trabalho em um controle de exibição de lista. Você pode enviar essa mensagem explicitamente ou usar a [**macro \_ GetNumberOfWorkAreas do ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getnumberofworkareas) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lParam* 
</dt> <dd>

Ponteiro para um valor UINT que recebe o número de áreas de trabalho no controle de exibição de lista. Se zero for colocado nessa variável, nenhuma área de trabalho estará definida no momento. Esse valor não pode ser **nulo**.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O valor retornado para esta mensagem não é usado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Usando controles de List-View](using-list-view-controls.md)
</dt> </dl>

 

 





