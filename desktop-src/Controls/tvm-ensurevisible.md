---
title: Mensagem de TVM_ENSUREVISIBLE (commctrl. h)
description: Garante que um item de exibição de árvore esteja visível, expandindo o item pai ou rolando o controle de exibição de árvore, se necessário. Você pode enviar essa mensagem explicitamente ou usando a macro TreeView \_ EnsureVisible.
ms.assetid: 7053438a-f9ca-4c4c-9da6-46b99fe1e4f8
keywords:
- controles de Windows de mensagem de TVM_ENSUREVISIBLE
topic_type:
- apiref
api_name:
- TVM_ENSUREVISIBLE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c1072c7213eb2172896980662bcd7a22a3c41fccf34eea2f7a107ab7ff894b32
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119797246"
---
# <a name="tvm_ensurevisible-message"></a>\_Mensagem TVM ENSUREVISIBLE

Garante que um item de exibição de árvore esteja visível, expandindo o item pai ou rolando o controle de exibição de árvore, se necessário. Você pode enviar essa mensagem explicitamente ou usando a macro [**TreeView \_ EnsureVisible**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_ensurevisible) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>Deve ser zero.</dd> <dt>

*lParam* 
</dt> <dd>

Identificador para o item.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retornará zero se o sistema tiver rolado os itens no controle de exibição em árvore e nenhum item tiver sido expandido. Caso contrário, a mensagem retornará zero.

## <a name="remarks"></a>Comentários

Se a \_ mensagem TVM ENSUREVISIBLE expandir o item pai, a janela pai receberá os códigos de notificação de [TVN de \_ ](tvn-itemexpanded.md) TVN e itens de isexpanding. [ \_ ](tvn-itemexpanding.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





