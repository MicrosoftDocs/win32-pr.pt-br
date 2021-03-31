---
title: Mensagem de LVM_SETHOTITEM (commctrl. h)
description: Define o item ativo para um controle de exibição de lista. Você pode enviar essa mensagem explicitamente ou usar a \_ macro SetHotItem do ListView.
ms.assetid: 0aa2b15d-4983-4234-9863-f1fdee09f913
keywords:
- Controles de LVM_SETHOTITEM de mensagens do Windows
topic_type:
- apiref
api_name:
- LVM_SETHOTITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 82c17bc67c530581b79a87030b31b655f856dd0e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103644260"
---
# <a name="lvm_sethotitem-message"></a>\_Mensagem SETHOTITEM LVM

Define o item ativo para um controle de exibição de lista. Você pode enviar essa mensagem explicitamente ou usar a [**macro \_ SetHotItem do ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_sethotitem) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Índice de base zero do item a ser definido como o item ativo.

</dd> <dt>

*lParam* 
</dt> <dd>Deve ser zero.</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna o índice do item que estava anteriormente quente.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





