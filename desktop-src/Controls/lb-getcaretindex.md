---
title: Mensagem de LB_GETCARETINDEX (WinUser. h)
description: Recupera o índice do item que tem o foco em uma caixa de listagem de seleção múltipla. O item pode ou não ser selecionado.
ms.assetid: vs|controls|~\controls\listboxes\listboxreference\listboxmessages\lb_getcaretindex.htm
keywords:
- controles de Windows de mensagem de LB_GETCARETINDEX
topic_type:
- apiref
api_name:
- LB_GETCARETINDEX
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 74732bae571cdcba0cfe8096437bf681e7a339c5c0edb3f18d378ea610bdf8c2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120085536"
---
# <a name="lb_getcaretindex-message"></a>GETCARETINDEX de mensagens de LB \_

Recupera o índice do item que tem o foco em uma caixa de listagem de seleção múltipla. O item pode ou não ser selecionado.

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

## <a name="return-value"></a>Valor retornado

O valor de retorno é o índice de base zero do item da caixa de listagem focada ou 0 se nenhum item tiver o foco.

## <a name="remarks"></a>Comentários

Essa mensagem também pode ser usada para obter o índice do item selecionado atualmente em uma caixa de listagem de seleção única.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                                           |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                                     |
| Cabeçalho<br/>                   | <dl> <dt>Winuser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_SETCARETINDEX lb**](lb-setcaretindex.md)
</dt> </dl>

 

 





