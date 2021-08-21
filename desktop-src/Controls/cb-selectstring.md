---
title: CB_SELECTSTRING mensagem (Winuser.h)
description: Pesquisa a lista de uma caixa de combinação para um item que começa com os caracteres em uma cadeia de caracteres especificada. Se um item correspondente for encontrado, ele será selecionado e copiado para o controle de edição.
ms.assetid: c08dff72-7e44-40ed-8b64-513359292829
keywords:
- CB_SELECTSTRING controles de Windows mensagem
topic_type:
- apiref
api_name:
- CB_SELECTSTRING
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4bedef20646664e37405c97a97f9e49147cad8acc08c05e33172e44a34298f5f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119019963"
---
# <a name="cb_selectstring-message"></a>Mensagem CB \_ SELECTSTRING

Pesquisa a lista de uma caixa de combinação para um item que começa com os caracteres em uma cadeia de caracteres especificada. Se um item correspondente for encontrado, ele será selecionado e copiado para o controle de edição.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

O índice baseado em zero do item anterior ao primeiro item a ser pesquisado. Quando a pesquisa atinge a parte inferior da lista, ela continua da parte superior da lista de volta para o item especificado pelo *parâmetro wParam.* Se *wParam* for -1, a lista inteira será pesquisada desde o início.

</dd> <dt>

*lParam* 
</dt> <dd>

Um ponteiro para a cadeia de caracteres terminada em nulo que contém os caracteres para os quais pesquisar. A pesquisa não é sensível a maiúsculas e minúsculas, portanto, essa cadeia de caracteres pode conter qualquer combinação de letras maiúsculas e minúsculas.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se a cadeia de caracteres for encontrada, o valor de retorno será o índice do item selecionado. Se a pesquisa não for bem-sucedida, o valor de retorno será CB \_ ERR e a seleção atual não será alterada.

## <a name="remarks"></a>Comentários

Uma cadeia de caracteres será selecionada somente se os caracteres do ponto de partida corresponderem aos caracteres na cadeia de caracteres de prefixo.

Se você criar a caixa de combinação com um estilo desenhado pelo proprietário, mas sem o estilo [**\_ CBS HASSTRINGS,**](combo-box-styles.md) o que a mensagem **CB \_ SELECTSTRING** faz dependerá de você usar o estilo [**CBS \_ SORT.**](combo-box-styles.md) Se o **estilo CBS \_ SORT** for usado, o sistema enviará mensagens [**WM \_ COMPAREITEM**](wm-compareitem.md) ao proprietário da caixa de combinação para determinar qual item corresponde à cadeia de caracteres especificada. Se você não usar o estilo **CBS \_ SORT,** **CB \_ SELECTSTRING** tentará corresponder o valor **DWORD** ao valor do *parâmetro lParam.*

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

[**CB \_ FINDSTRINGEXACT**](cb-findstringexact.md)
</dt> <dt>

[**CB \_ SETCURSEL**](cb-setcursel.md)
</dt> <dt>

[**WM \_ COMPAREITEM**](wm-compareitem.md)
</dt> </dl>

 

 





