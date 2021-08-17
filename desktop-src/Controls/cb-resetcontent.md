---
title: Mensagem de CB_RESETCONTENT (WinUser. h)
description: Remove todos os itens da caixa de listagem e edita o controle de uma caixa de combinação.
ms.assetid: 55203c34-87ca-46e9-a914-a480d43ccadd
keywords:
- controles de Windows de mensagem de CB_RESETCONTENT
topic_type:
- apiref
api_name:
- CB_RESETCONTENT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4918437d7b0d347e071386486b31e5f4b9d948b4ff55b4c6eea6e3afe93fb1c4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117832244"
---
# <a name="cb_resetcontent-message"></a>\_Mensagem de RESETCONTENT CB

Remove todos os itens da caixa de listagem e edita o controle de uma caixa de combinação.

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

Essa mensagem sempre retorna CB \_ OK.

## <a name="remarks"></a>Comentários

Se você criar a caixa de combinação com um estilo desenhado pelo proprietário, mas sem o estilo [**CBS \_ HASSTRINGS**](combo-box-styles.md) , o proprietário da caixa de combinação receberá uma mensagem [**\_ DELETEITEM do WM**](wm-deleteitem.md) para cada item na caixa de combinação.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                                           |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                                     |
| Cabeçalho<br/>                   | <dl> <dt>Winuser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Referência**
</dt> <dt>

[**excluído de CB \_**](cb-deletestring.md)
</dt> <dt>

[**DELETEITEM do WM \_**](wm-deleteitem.md)
</dt> </dl>

 

 





