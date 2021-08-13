---
title: Mensagem de LVM_GETORIGIN (commctrl. h)
description: Recupera a origem da exibição atual para um controle de exibição de lista. Você pode enviar essa mensagem explicitamente ou usando a \_ macro getorigin de ListView.
ms.assetid: 913c8339-fbe4-43c8-a997-5a972920dc3b
keywords:
- controles de Windows de mensagem de LVM_GETORIGIN
topic_type:
- apiref
api_name:
- LVM_GETORIGIN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a274e81c276d70eb1ab6c7f214b62ae5c346a59dda026bb13c5ab6b3ce80f68d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118411353"
---
# <a name="lvm_getorigin-message"></a>\_Mensagem de GETorigin do LVM

Recupera a origem da exibição atual para um controle de exibição de lista. Você pode enviar essa mensagem explicitamente ou usando a macro [**\_ getorigin de ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getorigin) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma estrutura de [**ponto**](/previous-versions//dd162805(v=vs.85)) que recebe a origem da exibição.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retornará **true** se for bem-sucedido ou **false** se a exibição atual for lista ou relatório.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

