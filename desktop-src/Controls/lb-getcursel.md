---
title: Mensagem de LB_GETCURSEL (WinUser. h)
description: Obtém o índice do item selecionado no momento, se houver, em uma caixa de listagem de seleção única.
ms.assetid: 39ab7f77-6c8e-45a4-aad4-47eba0a11a11
keywords:
- Controles de LB_GETCURSEL de mensagens do Windows
topic_type:
- apiref
api_name:
- LB_GETCURSEL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4a6209f1f5b67e059f9a2b8a224e6f96ec671e38
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009713"
---
# <a name="lb_getcursel-message"></a>\_Mensagem GETcurseal de lb

Obtém o índice do item selecionado no momento, se houver, em uma caixa de listagem de seleção única.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Não usado; deve ser zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Não usado; deve ser zero.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Em uma caixa de listagem de seleção única, o valor de retorno é o índice de base zero do item selecionado no momento. Se não houver nenhuma seleção, o valor de retorno será um erro de LB \_ .

## <a name="remarks"></a>Comentários

Para recuperar os índices dos itens selecionados em uma caixa de listagem de seleção múltipla, use a [**mensagem \_ GETSELITEMS de lb**](lb-getselitems.md) . Para determinar se o item que tem o retângulo de foco em uma caixa de listagem de seleção múltipla está selecionado, use a mensagem [**\_ GETSEL de lb**](lb-getsel.md) .

Se for enviado para uma caixa de listagem de seleção múltipla, **lb \_ getcurseal** retornará o índice do item que tem o retângulo de foco. Se nenhum item for selecionado, ele retornará zero.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                                           |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                                     |
| parâmetro<br/>                   | <dl> <dt>WinUser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Referência**
</dt> <dt>

[**\_GETCARETINDEX lb**](lb-getcaretindex.md)
</dt> <dt>

[**\_GETSEL lb**](lb-getsel.md)
</dt> <dt>

[**\_GETSELITEMS lb**](lb-getselitems.md)
</dt> <dt>

[**LB- \_ REcursel**](lb-setcursel.md)
</dt> </dl>

 

 





