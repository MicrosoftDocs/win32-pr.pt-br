---
title: CB_SETCURSEL mensagem (Winuser.h)
description: Um aplicativo envia uma mensagem CB SETCURSEL para selecionar uma cadeia de \_ caracteres na lista de uma caixa de combinação.
ms.assetid: d4ce3811-6e0a-4952-97cf-ba6efde0de0d
keywords:
- CB_SETCURSEL controles Windows mensagem
topic_type:
- apiref
api_name:
- CB_SETCURSEL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e154d5c75dd2e26a8015414cac783e610411ccd1bb63b0c3f85f6e3327f725c1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118171557"
---
# <a name="cb_setcursel-message"></a>Mensagem CB \_ SETCURSEL

Um aplicativo envia uma **mensagem CB \_ SETCURSEL** para selecionar uma cadeia de caracteres na lista de uma caixa de combinação. Se necessário, a lista rolará a cadeia de caracteres para a exibição. O texto no controle de edição da caixa de combinação muda para refletir a nova seleção e qualquer seleção anterior na lista é removida.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Especifica o índice baseado em zero da cadeia de caracteres a ser selecionada. Se esse parâmetro for -1, qualquer seleção atual na lista será removida e o controle de edição será limpo.

</dd> <dt>

*lParam* 
</dt> <dd>

Este parâmetro não é usado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se a mensagem for bem-sucedida, o valor de retorno será o índice do item selecionado. Se *wParam* for maior que o número de itens na lista ou se *wParam* for -1, o valor de retorno será CB ERR e a \_ seleção será limpa.

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

[**CB \_ FINDSTRING**](cb-findstring.md)
</dt> <dt>

[**CB \_ GETCURSEL**](cb-getcursel.md)
</dt> <dt>

[**CB \_ SELECTSTRING**](cb-selectstring.md)
</dt> </dl>

 

 





