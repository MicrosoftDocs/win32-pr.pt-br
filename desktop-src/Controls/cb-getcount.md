---
title: Mensagem de CB_GETCOUNT (WinUser. h)
description: Obtém o número de itens na caixa de listagem de uma caixa de combinação.
ms.assetid: 69667724-5452-4fcc-afc3-0d98d3beedc8
keywords:
- controles de Windows de mensagem de CB_GETCOUNT
topic_type:
- apiref
api_name:
- CB_GETCOUNT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8215046ae9558fd03388b2b0637233c2f69832ea07a7f20fd24ddc0a5eb3c177
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117832274"
---
# <a name="cb_getcount-message"></a>\_Mensagem de GETCOUNT CB

Obtém o número de itens na caixa de listagem de uma caixa de combinação.

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

O valor de retorno é o número de itens na caixa de listagem. Se ocorrer um erro, será CB \_ Err.

## <a name="remarks"></a>Comentários

O índice é baseado em zero, portanto, a contagem retornada é maior que o valor de índice do último item.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                                           |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                                     |
| Cabeçalho<br/>                   | <dl> <dt>Winuser. h (incluir Windows. h)</dt> </dl> |



 

 





