---
title: Mensagem de LVM_GETHOVERTIME (commctrl. h)
description: Recupera a quantidade de tempo que o cursor do mouse deve passar sobre um item antes de ser selecionado. Você pode enviar essa mensagem explicitamente ou usar a \_ macro Getfocalizetime de ListView.
ms.assetid: e7646024-f868-459f-88be-b232b6b4bb2a
keywords:
- Controles de LVM_GETHOVERTIME de mensagens do Windows
topic_type:
- apiref
api_name:
- LVM_GETHOVERTIME
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 83e243ece42f06ffe35eb31954d9ca0dd44957be
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455432"
---
# <a name="lvm_gethovertime-message"></a>Mensagem do LVM \_ GETfocalizetime

Recupera a quantidade de tempo que o cursor do mouse deve passar sobre um item antes de ser selecionado. Você pode enviar essa mensagem explicitamente ou usar a [**macro \_ getfocalizetime de ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_gethovertime) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lParam* 
</dt> <dd>Deve ser zero.</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna o período de tempo, em milissegundos, que o cursor do mouse deve passar sobre um item antes de ser selecionado. Se o valor de retorno for (**DWORD**)-1, o tempo de foco será o tempo de focalização padrão.

## <a name="remarks"></a>Comentários

O tempo de foco afeta apenas os controles de exibição de lista que têm o estilo de exibição de lista estendida [**LVS \_ ex \_ TRACKSELECT**](extended-list-view-styles.md), [**LVS \_ ex \_ ONECLICKACTIVATE**](extended-list-view-styles.md)ou [**LVS \_ ex \_ TWOCLICKACTIVATE**](extended-list-view-styles.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





