---
title: Mensagem de LVM_FINDITEM (commctrl. h)
description: Procura um item de exibição de lista com as características especificadas. Você pode enviar essa mensagem explicitamente ou usando a \_ macro FindItem do ListView.
ms.assetid: 3b18c8ad-97e6-4f4d-bf89-afb95f925ed1
keywords:
- Controles de LVM_FINDITEM de mensagens do Windows
topic_type:
- apiref
api_name:
- LVM_FINDITEM
- LVM_FINDITEMA
- LVM_FINDITEMW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f1f7dfc19e263a6ab7ad29b5e514fa4e52c1a9ba
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104454636"
---
# <a name="lvm_finditem-message"></a>\_Mensagem FINDITEM LVM

Procura um item de exibição de lista com as características especificadas. Você pode enviar essa mensagem explicitamente ou usando a macro [**\_ FindItem do ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_finditem) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

O índice do item para iniciar a pesquisa com ou-1 para iniciar desde o início. O item especificado é excluído da pesquisa.

</dd> <dt>

*lParam* 
</dt> <dd>

Um ponteiro para uma estrutura [**LVFINDINFO**](/windows/win32/api/commctrl/ns-commctrl-lvfindinfoa) que contém informações sobre o que Pesquisar.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna o índice do item se for bem-sucedido ou-1 caso contrário.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Nomes Unicode e ANSI<br/>   | **LVM \_ FINDITEMW** (Unicode) e **LVM \_ FINDITEMA** (ANSI)<br/>                 |



 

 





