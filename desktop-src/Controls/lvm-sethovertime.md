---
title: Mensagem de LVM_SETHOVERTIME (commctrl. h)
description: Define a quantidade de tempo que o cursor do mouse deve passar sobre um item antes de ser selecionado. Você pode enviar essa mensagem explicitamente ou usar a \_ macro Setfocalizetime do ListView.
ms.assetid: 454fbc38-f7fd-4dea-b223-56003b88528f
keywords:
- Controles de LVM_SETHOVERTIME de mensagens do Windows
topic_type:
- apiref
api_name:
- LVM_SETHOVERTIME
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f3aecd3c0d48cddc2cbaae49e7e888f91a985575
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085166"
---
# <a name="lvm_sethovertime-message"></a>Mensagem do LVM \_ SETfocalizetime

Define a quantidade de tempo que o cursor do mouse deve passar sobre um item antes de ser selecionado. Você pode enviar essa mensagem explicitamente ou usar a [**macro \_ setfocalizetime do ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_sethovertime) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lParam* 
</dt> <dd>

A nova quantidade de tempo, em milissegundos, que o cursor do mouse deve passar sobre um item antes de ser selecionado. Se esse valor for (**DWORD**)-1, o tempo de foco será definido como o tempo de foco padrão.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna o tempo de focalização anterior.

## <a name="remarks"></a>Comentários

O tempo de foco afeta apenas os controles de exibição de lista que têm o estilo de exibição de lista estendida [**LVS \_ ex \_ TRACKSELECT**](extended-list-view-styles.md), [**LVS \_ ex \_ ONECLICKACTIVATE**](extended-list-view-styles.md)ou [**LVS \_ ex \_ TWOCLICKACTIVATE**](extended-list-view-styles.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





