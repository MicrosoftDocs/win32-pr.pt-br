---
title: Mensagem de HDM_SETITEM (commctrl. h)
description: Define os atributos do item especificado em um controle de cabeçalho. Você pode enviar essa mensagem explicitamente ou usar a \_ macro SetItem do cabeçalho.
ms.assetid: c8f0d526-3ebe-48c5-8aea-ea3703e2d983
keywords:
- controles de Windows de mensagem de HDM_SETITEM
topic_type:
- apiref
api_name:
- HDM_SETITEM
- HDM_SETITEMA
- HDM_SETITEMW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dd0e2709a1b40bd4a564498cd0ae0b5d4e11861066aa9b0951815f92ee1c295f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118171061"
---
# <a name="hdm_setitem-message"></a>\_Mensagem HDM SETITEM

Define os atributos do item especificado em um controle de cabeçalho. Você pode enviar essa mensagem explicitamente ou usar a [**macro \_ SetItem do cabeçalho**](/windows/desktop/api/Commctrl/nf-commctrl-header_setitem) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

O índice atual do item cujos atributos devem ser alterados.

</dd> <dt>

*lParam* 
</dt> <dd>

Um ponteiro para uma estrutura [**HDITEM**](/windows/win32/api/commctrl/ns-commctrl-hditema) que contém informações de item. Quando essa mensagem é enviada, o membro **Mask** da estrutura deve ser definido para indicar quais atributos estão sendo definidos.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna zero após o êxito ou zero caso contrário.

## <a name="remarks"></a>Comentários

A estrutura [**HDITEM**](/windows/win32/api/commctrl/ns-commctrl-hditema) que dá suporte a essa mensagem dá suporte a informações de ordem de item e de lista de imagens. Ao usar esses membros, você pode controlar a ordem na qual os itens são exibidos e especificar imagens para serem exibidos com os itens.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Nomes Unicode e ANSI<br/>   | **HDM \_ SETITEMW** (Unicode) e **HDM \_ setitema** (ANSI)<br/>                   |



 

 





