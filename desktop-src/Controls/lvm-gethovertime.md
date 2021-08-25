---
title: LVM_GETHOVERTIME mensagem (Commctrl.h)
description: Recupera a quantidade de tempo que o cursor do mouse deve passar sobre um item antes de ser selecionado. Você pode enviar essa mensagem explicitamente ou usar a \_ macro ListView GetHoverTime.
ms.assetid: e7646024-f868-459f-88be-b232b6b4bb2a
keywords:
- LVM_GETHOVERTIME controles de Windows mensagem
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
ms.openlocfilehash: 150a8eff54f8b3c27f0e7783ceda67af60c326e370d1a518d83e6bdd214fb529
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119920096"
---
# <a name="lvm_gethovertime-message"></a>Mensagem \_ GETHOVERTIME LVM

Recupera a quantidade de tempo que o cursor do mouse deve passar sobre um item antes de ser selecionado. Você pode enviar essa mensagem explicitamente ou usar a [**macro \_ ListView GetHoverTime.**](/windows/desktop/api/Commctrl/nf-commctrl-listview_gethovertime)

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lParam* 
</dt> <dd>Deve ser zero.</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna a quantidade de tempo, em milissegundos, que o cursor do mouse deve passar o mouse sobre um item antes de ser selecionado. Se o valor de retorno for (**DWORD**)-1, o tempo de foco será o tempo de foco padrão.

## <a name="remarks"></a>Comentários

O tempo de foco afeta apenas os controles de exibição de lista que têm o estilo de exibição de lista estendido [**LVS \_ EX \_ TRACKSELECT**](extended-list-view-styles.md), [**LVS \_ EX \_ ONECLICKACTIVATE**](extended-list-view-styles.md)ou [**LVS \_ EX \_ TWOCLICKACTIVATE.**](extended-list-view-styles.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





