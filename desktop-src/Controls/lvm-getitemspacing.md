---
title: Mensagem de LVM_GETITEMSPACING (commctrl. h)
description: Determina o espaçamento entre os itens em um controle de exibição de lista. Você pode enviar essa mensagem explicitamente ou usando a \_ macro GetItemSpacing do ListView.
ms.assetid: 4e43fb43-468c-4b8a-9e3b-1694e90ffef8
keywords:
- Controles de LVM_GETITEMSPACING de mensagens do Windows
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
ms.openlocfilehash: 5ea08a7fc1004ffb46d710da6d1c2a8b0fb18e57
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918971"
---
# <a name="lvm_getitemspacing-message"></a>\_Mensagem GETITEMSPACING LVM

Determina o espaçamento entre os itens em um controle de exibição de lista. Você pode enviar essa mensagem explicitamente ou usando a macro [**\_ GetItemSpacing do ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getitemspacing) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Exibição para a qual recuperar o espaçamento do item. Esse parâmetro é **verdadeiro** para exibição de ícone pequeno ou **falso** para exibição de ícone.

</dd> <dt>

*lParam* 
</dt> <dd>Deve ser zero.</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna a quantidade de espaçamento entre os itens. O espaçamento horizontal está contido no [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) e o espaçamento vertical está contido no [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

