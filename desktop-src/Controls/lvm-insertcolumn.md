---
title: Mensagem de LVM_INSERTCOLUMN (commctrl. h)
description: Insere uma nova coluna em um controle de exibição de lista. Você pode enviar essa mensagem explicitamente ou usando a \_ macro InsertColumn do ListView.
ms.assetid: 1326e38e-bb45-4d0d-b5bc-ec684b3b92ef
keywords:
- Controles de LVM_INSERTCOLUMN de mensagens do Windows
topic_type:
- apiref
api_name:
- LVM_INSERTCOLUMN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8be89ff0b4ef417a715085582544112cb90cb6b1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499664"
---
# <a name="lvm_insertcolumn-message"></a>\_Mensagem INSERTCOLUMN LVM

Insere uma nova coluna em um controle de exibição de lista. Você pode enviar essa mensagem explicitamente ou usando a macro [**\_ InsertColumn do ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_insertcolumn) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Índice da nova coluna.

</dd> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma estrutura [**LVCOLUMN**](/windows/win32/api/commctrl/ns-commctrl-lvcolumna) que contém os atributos da nova coluna.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna o índice da nova coluna se for bem-sucedido ou-1 caso contrário.

## <a name="remarks"></a>Comentários

As colunas são visíveis somente na exibição de relatório (detalhes).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





