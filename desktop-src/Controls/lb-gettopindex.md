---
title: Mensagem de LB_GETTOPINDEX (WinUser. h)
description: Obtém o índice do primeiro item visível em uma caixa de listagem.
ms.assetid: vs|controls|~\controls\listboxes\listboxreference\listboxmessages\lb_gettopindex.htm
keywords:
- controles de Windows de mensagem de LB_GETTOPINDEX
topic_type:
- apiref
api_name:
- LB_GETTOPINDEX
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e4b23360da45041e5a728f370e54f8250f216507dd439291a2ffce5ed383d80
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120085376"
---
# <a name="lb_gettopindex-message"></a>GETTOPINDEX de mensagens de LB \_

Obtém o índice do primeiro item visível em uma caixa de listagem. Inicialmente, o item com o índice 0 está na parte superior da caixa de listagem, mas se o conteúdo da caixa de listagem tiver sido rolado, outro item poderá estar na parte superior. O primeiro item visível em uma caixa de listagem de várias colunas é o item superior esquerdo.

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

O valor de retorno é o índice do primeiro item visível na caixa de listagem.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                                           |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                                     |
| Cabeçalho<br/>                   | <dl> <dt>Winuser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_SETTOPINDEX lb**](lb-settopindex.md)
</dt> </dl>

 

 





