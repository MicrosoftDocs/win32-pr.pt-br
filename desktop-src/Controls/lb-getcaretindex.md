---
title: Mensagem de LB_GETCARETINDEX (WinUser. h)
description: Recupera o índice do item que tem o foco em uma caixa de listagem de seleção múltipla. O item pode ou não ser selecionado.
ms.assetid: vs|controls|~\controls\listboxes\listboxreference\listboxmessages\lb_getcaretindex.htm
keywords:
- Controles de LB_GETCARETINDEX de mensagens do Windows
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
ms.openlocfilehash: 4b9e4b8b2c75d72cdec606942991e957d8109ac7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009714"
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

## <a name="return-value"></a>Retornar valor

O valor de retorno é o índice de base zero do item da caixa de listagem focada ou 0 se nenhum item tiver o foco.

## <a name="remarks"></a>Comentários

Essa mensagem também pode ser usada para obter o índice do item selecionado atualmente em uma caixa de listagem de seleção única.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                                           |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                                     |
| parâmetro<br/>                   | <dl> <dt>WinUser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_SETCARETINDEX lb**](lb-setcaretindex.md)
</dt> </dl>

 

 





