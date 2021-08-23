---
title: Mensagem de LB_SELECTSTRING (WinUser. h)
description: Pesquisa uma caixa de listagem para um item que começa com os caracteres em uma cadeia de caracteres especificada. Se um item correspondente for encontrado, o item será selecionado.
ms.assetid: fd443ade-665d-439a-8951-3d9fed50695b
keywords:
- controles de Windows de mensagem de LB_SELECTSTRING
topic_type:
- apiref
api_name:
- LB_SELECTSTRING
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 848a0935a1ca4d3ce717fecae3de76f57e36091ba084041aa9d012d6318a269a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119434076"
---
# <a name="lb_selectstring-message"></a>\_Mensagem SelectString do lb

Pesquisa uma caixa de listagem para um item que começa com os caracteres em uma cadeia de caracteres especificada. Se um item correspondente for encontrado, o item será selecionado.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

O índice baseado em zero do item antes do primeiro item a ser pesquisado. Quando a pesquisa atingir a parte inferior da caixa de listagem, ela continuará na parte superior da caixa de listagem de volta para o item especificado pelo parâmetro *wParam* . Se *wParam* for-1, a caixa de listagem inteira será pesquisada desde o início.

Windows 95/Windows 98/Windows Millennium Edition (Windows Me): o parâmetro *wParam* é limitado a valores de 16 bits. Isso significa que as caixas de listagem não podem conter mais de 32.767 itens. Embora o número de itens seja restrito, o tamanho total em bytes dos itens em uma caixa de listagem é limitado apenas pela memória disponível.

</dd> <dt>

*lParam* 
</dt> <dd>

Um ponteiro para a cadeia de caracteres terminada em nulo que contém o prefixo a ser pesquisado. A pesquisa diferencia maiúsculas de minúsculas, portanto, essa cadeia de caracteres pode conter qualquer combinação de letras maiúsculas e minúsculas.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se a pesquisa for bem-sucedida, o valor de retorno será o índice do item selecionado. Se a pesquisa não for bem-sucedida, o valor de retorno será de \_ erro lb e a seleção atual não será alterada.

## <a name="remarks"></a>Comentários

A caixa de listagem é rolada, se necessário, para colocar o item selecionado em exibição.

Não use essa mensagem com uma caixa de listagem que tenha os estilos de [**lbs \_ MULTIPLESEL**](list-box-styles.md) ou [**lbs \_ EXTENDEDSEL**](list-box-styles.md) .

Um item será selecionado somente se seus caracteres iniciais do ponto de partida corresponderem aos caracteres na cadeia de caracteres especificada pelo parâmetro *lParam* .

Se a caixa de listagem tiver o estilo desenhado pelo proprietário, mas não o estilo de [**lbs \_ HASSTRINGS**](list-box-styles.md) , a ação tomada por **lb \_ SelectString** dependerá de o estilo de [**\_ classificação lbs**](list-box-styles.md) ser usado. Se **a \_ classificação de lbs** for usada, o sistema enviará mensagens do [**WM \_ COMPAREITEM**](wm-compareitem.md) para o proprietário da caixa de listagem para determinar qual item corresponde à cadeia de caracteres especificada. Caso contrário, o **lb \_ SelectString** tentará localizar um item que tem um valor longo (fornecido como o parâmetro *lParam* da mensagem do [**lb \_ AddString**](lb-addstring.md) ou [**lbstring \_**](lb-insertstring.md) ) que corresponde ao parâmetro *lParam* .

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

[**Localizar LBstring \_**](lb-findstring.md)
</dt> <dt>

[**KG \_ InsertString**](lb-insertstring.md)
</dt> </dl>

 

 





