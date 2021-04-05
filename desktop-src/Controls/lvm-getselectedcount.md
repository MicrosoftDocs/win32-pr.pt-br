---
title: Mensagem de LVM_GETSELECTEDCOUNT (commctrl. h)
description: Determina o número de itens selecionados em um controle de exibição de lista. Você pode enviar essa mensagem explicitamente ou usando a \_ macro GetSelectedCount do ListView.
ms.assetid: 38916227-e6ca-4efa-9821-13f0fdb29834
keywords:
- Controles de LVM_GETSELECTEDCOUNT de mensagens do Windows
topic_type:
- apiref
api_name:
- LVM_GETSELECTEDCOUNT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b23f0e8d1d87e2cc7dd60d32ac3dd4943611a36f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103824668"
---
# <a name="lvm_getselectedcount-message"></a>\_Mensagem GETSELECTEDCOUNT LVM

Determina o número de itens selecionados em um controle de exibição de lista. Você pode enviar essa mensagem explicitamente ou usando a macro [**\_ GetSelectedCount do ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getselectedcount) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lParam* 
</dt> <dd>Deve ser zero.</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna o número de itens selecionados.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





