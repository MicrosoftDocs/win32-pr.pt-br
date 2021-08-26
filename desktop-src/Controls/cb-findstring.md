---
title: CB_FINDSTRING mensagem (Winuser.h)
description: Pesquisa na caixa de listagem de uma caixa de combinação um item que começa com os caracteres em uma cadeia de caracteres especificada.
ms.assetid: 872a72d5-4d8e-41c7-ac6b-eeb571403623
keywords:
- CB_FINDSTRING controles de Windows mensagem
topic_type:
- apiref
api_name:
- CB_FINDSTRING
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1af584e04a108c39a76a54c05c311d26e107c132d0c132e7b8fcc99a7cd7321b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120089346"
---
# <a name="cb_findstring-message"></a>Mensagem CB \_ FINDSTRING

Pesquisa na caixa de listagem de uma caixa de combinação um item que começa com os caracteres em uma cadeia de caracteres especificada.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

O índice baseado em zero do item anterior ao primeiro item a ser pesquisado. Quando a pesquisa atinge a parte inferior da caixa de listagem, ela continua da parte superior da caixa de listagem de volta para o item especificado pelo *parâmetro wParam.* Se *wParam* for -1, toda a caixa de listagem será pesquisada desde o início.

</dd> <dt>

*lParam* 
</dt> <dd>

Um ponteiro para a cadeia de caracteres terminada em nulo que contém os caracteres para os quais pesquisar. A pesquisa não é sensível a maiúsculas e minúsculas, portanto, essa cadeia de caracteres pode conter qualquer combinação de letras maiúsculas e minúsculas.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O valor de retorno é o índice baseado em zero do item correspondente. Se a pesquisa não for bem-sucedida, será CB \_ ERR.

## <a name="remarks"></a>Comentários

Se você criar a caixa de combinação com um estilo desenhado pelo proprietário, mas sem o estilo [**\_ CBS HASSTRINGS,**](combo-box-styles.md) o que a mensagem **CB \_ FINDSTRING** faz dependerá de seu aplicativo usar o estilo [**CBS \_ SORT.**](combo-box-styles.md) Se você usar o estilo **CBS \_ SORT,** as mensagens [**WM \_ COMPAREITEM**](wm-compareitem.md) serão enviadas ao proprietário da caixa de combinação para determinar qual item corresponde à cadeia de caracteres especificada. Se você não usar o estilo **CBS \_ SORT,** a mensagem **CB \_ FINDSTRING** pesquisa um item de lista que corresponde ao valor do *parâmetro lParam.*

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

[**CB \_ FINDSTRINGEXACT**](cb-findstringexact.md)
</dt> <dt>

[**CB \_ SELECTSTRING**](cb-selectstring.md)
</dt> <dt>

[**CB \_ SETCURSEL**](cb-setcursel.md)
</dt> <dt>

[**WM \_ COMPAREITEM**](wm-compareitem.md)
</dt> </dl>

 

 





