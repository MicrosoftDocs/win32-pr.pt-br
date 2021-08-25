---
title: Mensagem de LB_INSERTSTRING (WinUser. h)
description: Insere uma cadeia de caracteres ou dados de item em uma caixa de listagem. Ao contrário da \_ mensagem de AddString do lb, a mensagem de inserção de lb não faz com \_ que uma lista com o \_ estilo de classificação lbs seja classificada.
ms.assetid: dfaa742d-2f42-4485-aed5-cda8ca9ba66c
keywords:
- controles de Windows de mensagem de LB_INSERTSTRING
topic_type:
- apiref
api_name:
- LB_INSERTSTRING
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dd47d08ef78c590ecb3b5900143b29bc49676b86d8facdcc91b05bb34c8f4aa1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120085386"
---
# <a name="lb_insertstring-message"></a>Mensagem de inserção de LB \_

Insere uma cadeia de caracteres ou dados de item em uma caixa de listagem. Ao contrário da mensagem de [**\_ AddString do lb**](lb-addstring.md) , a mensagem de **\_ inserção de lb** não faz com que uma lista com o estilo de [**\_ classificação lbs**](list-box-styles.md) seja classificada.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

O índice de base zero da posição na qual inserir a cadeia de caracteres. Se esse parâmetro for-1, a cadeia de caracteres será adicionada ao final da lista.

</dd> <dt>

*lParam* 
</dt> <dd>

Um ponteiro para a cadeia de caracteres terminada em nulo a ser inserida. Se a caixa de listagem tiver um estilo desenhado pelo proprietário, mas não o estilo de [**lbs \_ HASSTRINGS**](list-box-styles.md) , esse parâmetro será armazenado como dados de item em vez de uma cadeia de caracteres. Você pode enviar as [**mensagens \_ GETITEMDATA**](lb-getitemdata.md) e [**lb \_ SETITEMDATA**](lb-setitemdata.md) para recuperar ou modificar os dados do item.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O valor de retorno é o índice da posição na qual a cadeia de caracteres foi inserida. Se ocorrer um erro, o valor de retorno será um erro de LB \_ . Se não houver espaço suficiente para armazenar a nova cadeia de caracteres, o valor de retorno será LB \_ ERRSPACE.

## <a name="remarks"></a>Comentários

A [**mensagem \_ INITSTORAGE de lb**](lb-initstorage.md) ajuda a acelerar a inicialização de caixas de listagem que têm um grande número de itens (mais de 100). Ele reserva a quantidade especificada de memória para que as mensagens de **\_ inserção de lb** subsequentes tenham o menor tempo possível. Você pode usar estimativas para os parâmetros *wParam* e *lParam* . Se você superestimar, a memória extra é alocada; Se você subestimar, a alocação normal será usada para itens que excedem o valor solicitado.

Se a caixa de listagem tiver o estilo [**WS \_ HSCROLL**](/windows/desktop/winmsg/window-styles) e você inserir uma cadeia de caracteres maior que a caixa de listagem, envie uma mensagem [**\_ SETHORIZONTALEXTENT de lb**](lb-sethorizontalextent.md) para garantir que a barra de rolagem horizontal seja exibida.

Para um aplicativo ANSI, o sistema converte o texto em uma caixa de listagem para Unicode usando CP \_ ACP. Isso pode causar problemas. por exemplo, caracteres romanos acentuados em uma caixa de listagem não-Unicode em japonês Windows ficarão confusos. Para corrigir isso, compile o aplicativo como Unicode ou use uma caixa de listagem desenhada pelo proprietário.

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

[**seqüência de caracteres de LB \_**](lb-addstring.md)
</dt> <dt>

[**seleção de LBstring \_**](lb-selectstring.md)
</dt> <dt>

[**\_SETHORIZONTALEXTENT lb**](lb-sethorizontalextent.md)
</dt> </dl>

 

