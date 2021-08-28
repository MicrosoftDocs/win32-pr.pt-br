---
title: LVM_GETITEMSPACING mensagem (Commctrl.h)
description: Determina o espaçamento entre itens em um controle de exibição de lista. Você pode enviar essa mensagem explicitamente ou usando a \_ macro ListView GetItemSpacing.
ms.assetid: 4e43fb43-468c-4b8a-9e3b-1694e90ffef8
keywords:
- LVM_GETITEMSPACING controles de Windows mensagem
topic_type:
- apiref
api_name:
- LVM_GETITEMSPACING
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 687a1aa75d71b96cebe855bb97ea57f0a9c628ed49b1ef7a51a7557b23b5ce41
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120088886"
---
# <a name="lvm_getitemspacing-message"></a>Mensagem \_ GETITEMSPACING LVM

Determina o espaçamento entre itens em um controle de exibição de lista. Você pode enviar essa mensagem explicitamente ou usando a [**macro \_ ListView GetItemSpacing.**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getitemspacing)

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Exibição para a qual recuperar o espaçamento do item. Esse parâmetro é **TRUE para** exibição de ícone pequeno ou **FALSE para** exibição de ícone.

</dd> <dt>

*lParam* 
</dt> <dd>Deve ser zero.</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna a quantidade de espaçamento entre itens. O espaçamento horizontal está contido no [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) e o espaçamento vertical está contido no [**HIWORD.**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

