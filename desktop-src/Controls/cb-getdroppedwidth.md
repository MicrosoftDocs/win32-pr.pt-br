---
title: Mensagem de CB_GETDROPPEDWIDTH (WinUser. h)
description: Obtém a largura mínima permitida, em pixels, da caixa de listagem de uma caixa de combinação com o estilo de lista \_ suspensa CBS ou CBS \_ .
ms.assetid: d7f37a6c-a623-4b15-8ef7-4b64d85c15fa
keywords:
- controles de Windows de mensagem de CB_GETDROPPEDWIDTH
topic_type:
- apiref
api_name:
- CB_GETDROPPEDWIDTH
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fa814803943bcf306b8a057b160acb2b8b3410e0ef08c7e2fb9c4ac8c3856afe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119079110"
---
# <a name="cb_getdroppedwidth-message"></a>\_Mensagem de GETDROPPEDWIDTH CB

Obtém a largura mínima permitida, em pixels, da caixa de listagem de uma caixa de combinação com o estilo de lista [**\_ suspensa CBS**](combo-box-styles.md) ou [**CBS \_**](combo-box-styles.md) .

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

Se a mensagem tiver sucesso, o valor de retorno será a largura, em pixels.

Se a mensagem falhar, o valor de retorno será CB \_ Err.

## <a name="remarks"></a>Comentários

Por padrão, a largura mínima permitida da caixa de listagem suspensa é zero. A largura da caixa de listagem é a largura mínima permitida ou a largura da caixa de combinação, o que for maior.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                                           |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                                     |
| Cabeçalho<br/>                   | <dl> <dt>Winuser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_SETDROPPEDWIDTH CB**](cb-setdroppedwidth.md)
</dt> </dl>

 

 





