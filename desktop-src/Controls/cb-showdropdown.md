---
title: CB_SHOWDROPDOWN mensagem (Winuser.h)
description: Um aplicativo envia uma mensagem CB SHOWDROPDOWN para mostrar ou ocultar a caixa de listagem de uma caixa de combinação que tem o estilo \_ CBS DROPDOWN ou \_ CBS \_ DROPDOWNLIST.
ms.assetid: 32b995d7-eed6-4173-8525-0d356dea39b3
keywords:
- CB_SHOWDROPDOWN controles de Windows mensagem
topic_type:
- apiref
api_name:
- CB_SHOWDROPDOWN
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c820c65c053f7acbcffb379228ea5f7720476b6d2165ac4988ce8789e912cdd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117832234"
---
# <a name="cb_showdropdown-message"></a>Mensagem CB \_ SHOWDROPDOWN

Um aplicativo envia uma **mensagem CB \_ SHOWDROPDOWN** para mostrar ou ocultar a caixa de listagem de uma caixa de combinação que tem o estilo [**CBS \_ DROPDOWN**](combo-box-styles.md) ou [**CBS \_ DROPDOWNLIST.**](combo-box-styles.md)

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Um **BOOL** que especifica se a caixa de listagem listada deve ser mostrada ou oculta. Um valor true **mostra** a caixa de listagem; um valor **false** o oculta.

</dd> <dt>

*lParam* 
</dt> <dd>

Este parâmetro não é usado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O valor de retorno é sempre **TRUE.**

## <a name="remarks"></a>Comentários

Essa mensagem não tem nenhum efeito em uma caixa de combinação criada com o [**estilo CBS \_ SIMPLE.**](combo-box-styles.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                                           |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                                     |
| Cabeçalho<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**CB \_ GETDROPPEDSTATE**](cb-getdroppedstate.md)
</dt> </dl>

 

 





