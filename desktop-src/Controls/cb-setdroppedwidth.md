---
title: Mensagem de CB_SETDROPPEDWIDTH (WinUser. h)
description: Um aplicativo envia a \_ mensagem CB SETDROPPEDWIDTH para definir a largura mínima permitida, em pixels, da caixa de listagem de uma caixa de combinação com o estilo de lista \_ suspensa CBS ou CBS \_ .
ms.assetid: 89f44733-aebe-44ea-b62d-8bd988f1bd6f
keywords:
- controles de Windows de mensagem de CB_SETDROPPEDWIDTH
topic_type:
- apiref
api_name:
- CB_SETDROPPEDWIDTH
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 05d59aee89c4be18ba8e5013fa1a1e685a56b727d293c833c7f99140b683efeb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120089046"
---
# <a name="cb_setdroppedwidth-message"></a>\_Mensagem de SETDROPPEDWIDTH CB

Um aplicativo envia a mensagem **CB \_ SETDROPPEDWIDTH** para definir a largura mínima permitida, em pixels, da caixa de listagem de uma caixa de combinação com o estilo de lista [**\_ suspensa CBS**](combo-box-styles.md) ou [**CBS \_**](combo-box-styles.md) .

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

A largura mínima permitida da caixa de listagem, em pixels.

</dd> <dt>

*lParam* 
</dt> <dd>

Este parâmetro não é usado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se a mensagem for bem-sucedida, o valor de retorno será a nova largura da caixa de listagem.

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

[**\_GETDROPPEDWIDTH CB**](cb-getdroppedwidth.md)
</dt> </dl>

 

 





