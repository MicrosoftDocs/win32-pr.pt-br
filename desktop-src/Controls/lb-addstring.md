---
title: LB_ADDSTRING mensagem (Winuser.h)
description: Adiciona uma cadeia de caracteres a uma caixa de listagem. Se a caixa de listagem não tiver o estilo SORT do LBS, a cadeia de caracteres será adicionada \_ ao final da lista. Caso contrário, a cadeia de caracteres será inserida na lista e a lista será classificação.
ms.assetid: 924d9232-6e38-49c3-aa3e-19efd46b01ba
keywords:
- LB_ADDSTRING controles de Windows mensagem
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
ms.openlocfilehash: 552e3c344a730ad1fc00337cafa71a19a6586b9a4c95f2ed1ebce352d9d909aa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118671682"
---
# <a name="lb_addstring-message"></a>Mensagem \_ ADDSTRING de LB

Adiciona uma cadeia de caracteres a uma caixa de listagem. Se a caixa de listagem não tiver o estilo [**SORT \_ do LBS,**](list-box-styles.md) a cadeia de caracteres será adicionada ao final da lista. Caso contrário, a cadeia de caracteres será inserida na lista e a lista será classificação.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Este parâmetro não é usado.

</dd> <dt>

*lParam* 
</dt> <dd>

Um ponteiro para a cadeia de caracteres terminada em nulo que deve ser adicionada.

Se a caixa de listagem tiver um estilo desenhado pelo proprietário, mas não o estilo [**\_ HASSTRINGS do LBS,**](list-box-styles.md) esse parâmetro será armazenado como dados de item em vez de uma cadeia de caracteres. Você pode enviar as **mensagens LB \_ GETITEMDATA** e **LB \_ SETITEMDATA** para recuperar ou modificar os dados do item.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O valor de retorno é o índice baseado em zero da cadeia de caracteres na caixa de listagem. Se ocorrer um erro, o valor de retorno será LB \_ ERR. Se não houver espaço suficiente para armazenar a nova cadeia de caracteres, o valor de retorno será LB \_ ERRSPACE.

## <a name="remarks"></a>Comentários

Se a caixa de listagem tiver um estilo desenhado pelo proprietário e o estilo [**SORT do \_ LBS,**](list-box-styles.md) mas não o estilo [**\_ HASSTRINGS do LBS,**](list-box-styles.md) o sistema enviará a mensagem WM [**\_ COMPAREITEM**](wm-compareitem.md) uma ou mais vezes ao proprietário da caixa de listagem para colocar o novo item corretamente na caixa de listagem.

A [**mensagem LB \_ INITSTORAGE**](lb-initstorage.md) ajuda a acelerar a inicialização de caixas de listagem que têm um grande número de itens (mais de 100). Ele reserva a quantidade especificada de memória para que as mensagens **\_ ADDSTRING** de LB subsequentes reservem o menor tempo possível. Você pode usar estimativas para os *parâmetros wParam* e *lParam.* Se você sobrestimar, a memória extra será alocada; se você menosprezá-la, a alocação normal será usada para itens que excedem o valor solicitado.

Se a caixa de listagem tiver o estilo [**\_ HSCROLL**](/windows/desktop/winmsg/window-styles) do WS e você adicionar uma cadeia de caracteres maior do que a caixa de listagem, envie uma mensagem [**LB \_ LBORIZONTALEXTENT**](lb-sethorizontalextent.md) para garantir que a barra de rolagem horizontal seja exibida.

Para um aplicativo ANSI, o sistema converte o texto em uma caixa de listagem em Unicode usando CP \_ ACP. Isso pode causar problemas. Por exemplo, caracteres romes acentos em uma caixa de listagem não Unicode em japonês Windows sairão de forma desinteressada. Para corrigir isso, compile o aplicativo como Unicode ou use uma caixa de listagem desenhada pelo proprietário.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                                           |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                                     |
| parâmetro<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Referência**
</dt> <dt>

[**LB \_ DELETESTRING**](lb-deletestring.md)
</dt> <dt>

[**LB \_ INSERTSTRING**](lb-insertstring.md)
</dt> <dt>

[**LB \_ SELECTSTRING**](lb-selectstring.md)
</dt> <dt>

[**LB \_ LB LBORIZONTALEXTENT**](lb-sethorizontalextent.md)
</dt> <dt>

[**WM \_ COMPAREITEM**](wm-compareitem.md)
</dt> </dl>

 

