---
title: Mensagem de LB_GETCOUNT (WinUser. h)
description: Obtém o número de itens em uma caixa de listagem.
ms.assetid: 1fbe44fc-8b9d-4bfa-a8bb-06817eecf064
keywords:
- controles de Windows de mensagem de LB_GETCOUNT
topic_type:
- apiref
api_name:
- LB_GETCOUNT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef4f4792bf290343e2868b754f8efb1bfc03d0be1f600c9f7584f051053400b1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119435469"
---
# <a name="lb_getcount-message"></a>\_Mensagem de GETcount de lb

Obtém o número de itens em uma caixa de listagem.

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

O valor de retorno é o número de itens na caixa de listagem, ou \_ erro de lb se ocorrer um erro.

## <a name="remarks"></a>Comentários

A contagem retornada é uma maior que o valor de índice do último item (o índice é baseado em zero).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                                           |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                                     |
| parâmetro<br/>                   | <dl> <dt>Winuser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**NÚMERO de LB \_**](lb-setcount.md)
</dt> </dl>

 

 





