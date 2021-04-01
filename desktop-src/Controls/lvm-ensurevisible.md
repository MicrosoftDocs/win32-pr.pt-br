---
title: Mensagem de LVM_ENSUREVISIBLE (commctrl. h)
description: Garante que um item de exibição de lista seja totalmente ou parcialmente visível, rolando o controle de exibição de lista, se necessário. Você pode enviar essa mensagem explicitamente ou usando a \_ macro EnsureVisible do ListView.
ms.assetid: 3564b6e6-b8b6-401b-85bc-8bd6261fc054
keywords:
- Controles de LVM_ENSUREVISIBLE de mensagens do Windows
topic_type:
- apiref
api_name:
- LVM_ENSUREVISIBLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3d0ff4009399988f20f3e162114f91e4cff02820
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103917998"
---
# <a name="lvm_ensurevisible-message"></a>\_Mensagem ENSUREVISIBLE LVM

Garante que um item de exibição de lista seja totalmente ou parcialmente visível, rolando o controle de exibição de lista, se necessário. Você pode enviar essa mensagem explicitamente ou usando a macro [**\_ EnsureVisible do ListView**](/windows/desktop/api/Commctrl/nf-commctrl-listview_ensurevisible) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

O índice do item de exibição de lista.

</dd> <dt>

*lParam* 
</dt> <dd>

Um valor que especifica se o item deve estar totalmente visível. Se esse parâmetro for **true**, nenhuma rolagem ocorrerá se o item estiver pelo menos parcialmente visível.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna **verdadeiro** se for bem-sucedido ou **false** caso contrário.

## <a name="remarks"></a>Comentários

A mensagem falhará se o estilo da janela incluir [**LVS \_ NoScroll**](list-view-window-styles.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





