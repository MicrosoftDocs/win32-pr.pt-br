---
title: Mensagem de LB_ADDSTRING (WinUser. h)
description: Adiciona uma cadeia de caracteres a uma caixa de listagem. Se a caixa de listagem não tiver o \_ estilo de classificação lbs, a cadeia de caracteres será adicionada ao final da lista. Caso contrário, a cadeia de caracteres será inserida na lista e a lista será classificada.
ms.assetid: 924d9232-6e38-49c3-aa3e-19efd46b01ba
keywords:
- Controles de LB_ADDSTRING de mensagens do Windows
topic_type:
- apiref
api_name:
- LB_ADDSTRING
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 87e1c820b7a4c122012076c82ce20adc0d01e2e9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009301"
---
# <a name="lb_addstring-message"></a>\_Mensagem de ADDSTRING lb

Adiciona uma cadeia de caracteres a uma caixa de listagem. Se a caixa de listagem não tiver o estilo de [**\_ classificação lbs**](list-box-styles.md) , a cadeia de caracteres será adicionada ao final da lista. Caso contrário, a cadeia de caracteres será inserida na lista e a lista será classificada.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Este parâmetro não é usado.

</dd> <dt>

*lParam* 
</dt> <dd>

Um ponteiro para a cadeia de caracteres terminada em nulo que deve ser adicionado.

Se a caixa de listagem tiver um estilo desenhado pelo proprietário, mas não o estilo de [**lbs \_ HASSTRINGS**](list-box-styles.md) , esse parâmetro será armazenado como dados de item em vez de uma cadeia de caracteres. Você pode enviar as **mensagens \_ GETITEMDATA** e **lb \_ SETITEMDATA** para recuperar ou modificar os dados do item.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O valor de retorno é o índice de base zero da cadeia de caracteres na caixa de listagem. Se ocorrer um erro, o valor de retorno será um erro de LB \_ . Se não houver espaço suficiente para armazenar a nova cadeia de caracteres, o valor de retorno será LB \_ ERRSPACE.

## <a name="remarks"></a>Comentários

Se a caixa de listagem tiver um estilo desenhado pelo proprietário e o estilo de [**\_ classificação lbs**](list-box-styles.md) , mas não o estilo [**lbs \_ HASSTRINGS**](list-box-styles.md) , o sistema enviará a mensagem [**\_ COMPAREITEM do WM**](wm-compareitem.md) uma ou mais vezes para o proprietário da caixa de listagem para posicionar o novo item corretamente na caixa de listagem.

A [**mensagem \_ INITSTORAGE de lb**](lb-initstorage.md) ajuda a acelerar a inicialização de caixas de listagem que têm um grande número de itens (mais de 100). Ele reserva a quantidade especificada de memória para que as mensagens de **\_ cadeia de caracteres do lb** subsequentes tenham o menor tempo possível. Você pode usar estimativas para os parâmetros *wParam* e *lParam* . Se você superestimar, a memória extra é alocada; Se você subestimar, a alocação normal será usada para itens que excedem o valor solicitado.

Se a caixa de listagem tiver o estilo [**WS \_ HSCROLL**](/windows/desktop/winmsg/window-styles) e você adicionar uma cadeia de caracteres maior que a caixa de listagem, envie uma mensagem [**\_ SETHORIZONTALEXTENT de lb**](lb-sethorizontalextent.md) para garantir que a barra de rolagem horizontal seja exibida.

Para um aplicativo ANSI, o sistema converte o texto em uma caixa de listagem para Unicode usando CP \_ ACP. Isso pode causar problemas. Por exemplo, caracteres romanos acentuados em uma caixa de listagem não-Unicode no Windows em Japonês ficarão confusos. Para corrigir isso, compile o aplicativo como Unicode ou use uma caixa de listagem desenhada pelo proprietário.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                                           |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                                     |
| parâmetro<br/>                   | <dl> <dt>WinUser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Referência**
</dt> <dt>

[**LB \_ DeleteString**](lb-deletestring.md)
</dt> <dt>

[**KG \_ InsertString**](lb-insertstring.md)
</dt> <dt>

[**seleção de LBstring \_**](lb-selectstring.md)
</dt> <dt>

[**\_SETHORIZONTALEXTENT lb**](lb-sethorizontalextent.md)
</dt> <dt>

[**COMPAREITEM do WM \_**](wm-compareitem.md)
</dt> </dl>

 

