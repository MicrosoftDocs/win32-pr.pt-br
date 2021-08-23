---
title: LVM_GETHOTCURSOR mensagem (Commctrl.h)
description: Recupera o valor HCURSOR usado quando o ponteiro está sobre um item enquanto o acompanhamento a quente está habilitado. Você pode enviar essa mensagem explicitamente ou usar a \_ macro ListView GetHotCursor.
ms.assetid: 064d04b2-d74e-4a80-aec6-97a3c53fc4fb
keywords:
- LVM_GETHOTCURSOR controles de Windows mensagem
topic_type:
- apiref
api_name:
- LVM_GETHOTCURSOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1e5703d252d239124b78656c4a5991efdecb2107552fb6e2ab0f87701af4e18d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119540796"
---
# <a name="lvm_gethotcursor-message"></a>Mensagem \_ GETHOTCURSOR LVM

Recupera o valor HCURSOR usado quando o ponteiro está sobre um item enquanto o acompanhamento a quente está habilitado. Você pode enviar essa mensagem explicitamente ou usar a macro [**\_ ListView GetHotCursor.**](/windows/desktop/api/Commctrl/nf-commctrl-listview_gethotcursor)

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lParam* 
</dt> <dd>Deve ser zero.</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um valor HCURSOR que é o alçador para o cursor que o controle de exibição de lista usa quando o acompanhamento a quente está habilitado.

## <a name="remarks"></a>Comentários

Um controle de exibição de lista usa o acompanhamento a quente e a seleção de foco quando o [**estilo LVS \_ EX \_ TRACKSELECT**](extended-list-view-styles.md) é definido.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





