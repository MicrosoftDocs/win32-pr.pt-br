---
title: CB_INSERTSTRING mensagem (Winuser.h)
description: Insere uma cadeia de caracteres ou dados de item na lista de uma caixa de combinação. Ao contrário da mensagem CB ADDSTRING, a mensagem CB INSERTSTRING não faz com que uma lista com o \_ \_ estilo \_ CBS SORT seja classificação.
ms.assetid: b9067b4e-afca-4c78-9ca2-c717b99c7459
keywords:
- CB_INSERTSTRING controles de Windows mensagem
topic_type:
- apiref
api_name:
- CB_INSERTSTRING
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bcebd3ed5c52a40f3ca5d49031948f76edfa9d6d98974cec104c4b8e283c101a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120089066"
---
# <a name="cb_insertstring-message"></a>Mensagem CB \_ INSERTSTRING

Insere uma cadeia de caracteres ou dados de item na lista de uma caixa de combinação. Ao contrário [**da \_ mensagem CB ADDSTRING,**](cb-addstring.md) a mensagem **CB \_ INSERTSTRING** não faz com que uma lista com o [**estilo \_ CBS SORT**](combo-box-styles.md) seja classificação.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

O índice baseado em zero da posição na qual inserir a cadeia de caracteres. Se esse parâmetro for -1, a cadeia de caracteres será adicionada ao final da lista.

</dd> <dt>

*lParam* 
</dt> <dd>

Um ponteiro para a cadeia de caracteres terminada em nulo a ser inserida. Se você criar a caixa de combinação com um estilo desenhado pelo proprietário, mas sem o estilo [**\_ CBS HASSTRINGS,**](combo-box-styles.md) o valor do parâmetro *lParam* será armazenado em vez da cadeia de caracteres para a qual ele apontaria de outra forma.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O valor de retorno é o índice da posição na qual a cadeia de caracteres foi inserida. Se ocorrer um erro, o valor de retorno será CB \_ ERR. Se não houver espaço suficiente disponível para armazenar a nova cadeia de caracteres, será CB \_ ERRSPACE.

Se a caixa de combinação tiver o estilo [**\_ HSCROLL**](/windows/desktop/winmsg/window-styles) do WS e você inserir uma cadeia de caracteres maior do que a caixa de combinação, você deverá enviar uma mensagem [**LB \_ LBORIZONTALEXTENT**](lb-sethorizontalextent.md) para garantir que a barra de rolagem horizontal seja exibida.

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

[**CB \_ ADDSTRING**](cb-addstring.md)
</dt> <dt>

[**LB \_ LB LBORIZONTALEXTENT**](lb-sethorizontalextent.md)
</dt> <dt>

[**CB \_ DIR**](cb-dir.md)
</dt> </dl>

 

