---
title: Mensagem de LVM_GETORIGIN (commctrl. h)
description: Recupera a origem da exibição atual para um controle de exibição de lista. Você pode enviar essa mensagem explicitamente ou usando a \_ macro getorigin de ListView.
ms.assetid: 913c8339-fbe4-43c8-a997-5a972920dc3b
keywords:
- Controles de LVM_GETORIGIN de mensagens do Windows
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
ms.openlocfilehash: 8af42f3d616aa609d6b9e41d3991adb9d68eb24e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086161"
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

## <a name="return-value"></a>Retornar valor

Retornará **true** se for bem-sucedido ou **false** se a exibição atual for lista ou relatório.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

