---
title: CB_DELETESTRING mensagem (Winuser.h)
description: Exclui uma cadeia de caracteres na caixa de listagem de uma caixa de combinação.
ms.assetid: 8d526796-04ef-4c01-94d6-fb50e6fef27b
keywords:
- CB_DELETESTRING controles Windows mensagem
topic_type:
- apiref
api_name:
- CB_DELETESTRING
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0bed1d654b86ffeb4a02c780678822e1999847ef0e163e35ecba081af099f66
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120063576"
---
# <a name="cb_deletestring-message"></a>Mensagem CB \_ DELETESTRING

Exclui uma cadeia de caracteres na caixa de listagem de uma caixa de combinação.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

O índice baseado em zero da cadeia de caracteres a ser excluído.

</dd> <dt>

*lParam* 
</dt> <dd>

Este parâmetro não é usado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O valor de retorno é uma contagem das cadeias de caracteres restantes na lista. Se o *parâmetro wParam* especificar um índice maior que o número de itens na lista, o valor de retorno será CB \_ ERR.

## <a name="remarks"></a>Comentários

Se você criar a caixa de combinação com um estilo desenhado pelo proprietário, mas sem o estilo [**\_ CBS HASSTRINGS,**](combo-box-styles.md) o sistema enviará uma mensagem [**WM \_ DELETEITEM**](wm-deleteitem.md) ao proprietário da caixa de combinação para que o aplicativo possa liberar quaisquer dados adicionais associados ao item.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                                           |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                                     |
| Cabeçalho<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Referência**
</dt> <dt>

[**CB \_ RESETCONTENT**](cb-resetcontent.md)
</dt> <dt>

[**WM \_ DELETEITEM**](wm-deleteitem.md)
</dt> </dl>

 

 





