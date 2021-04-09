---
title: Mensagem de CB_SELECTSTRING (WinUser. h)
description: Pesquisa a lista de uma caixa de combinação de um item que começa com os caracteres em uma cadeia de caracteres especificada. Se um item correspondente for encontrado, ele será selecionado e copiado para o controle de edição.
ms.assetid: c08dff72-7e44-40ed-8b64-513359292829
keywords:
- Controles de CB_SELECTSTRING de mensagens do Windows
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
ms.openlocfilehash: 2913b95c02cdfd3c7a9c96a8652038a04d8fde8f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009353"
---
# <a name="cb_selectstring-message"></a>\_Mensagem SelectString do CB

Pesquisa a lista de uma caixa de combinação de um item que começa com os caracteres em uma cadeia de caracteres especificada. Se um item correspondente for encontrado, ele será selecionado e copiado para o controle de edição.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

O índice de base zero do item que antecede o primeiro item a ser pesquisado. Quando a pesquisa atingir a parte inferior da lista, ela continuará na parte superior da lista de volta para o item especificado pelo parâmetro *wParam* . Se *wParam* for-1, a lista inteira será pesquisada desde o início.

</dd> <dt>

*lParam* 
</dt> <dd>

Um ponteiro para a cadeia de caracteres terminada em nulo que contém os caracteres para pesquisa. A pesquisa não diferencia maiúsculas de minúsculas, portanto, essa cadeia de caracteres pode conter qualquer combinação de letras maiúsculas e minúsculas.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se a cadeia de caracteres for encontrada, o valor de retorno será o índice do item selecionado. Se a pesquisa não for bem-sucedida, o valor de retorno será CB \_ Err e a seleção atual não será alterada.

## <a name="remarks"></a>Comentários

Uma cadeia de caracteres será selecionada somente se os caracteres do ponto inicial corresponderem aos caracteres na cadeia de caracteres do prefixo.

Se você criar a caixa de combinação com um estilo desenhado pelo proprietário, mas sem o estilo [**CBS \_ HASSTRINGS**](combo-box-styles.md) , o que a mensagem **\_ SelectString do CB** dependerá se você usar o estilo de [**\_ classificação CBS**](combo-box-styles.md) . Se o estilo de **\_ classificação CBS** for usado, o sistema enviará mensagens do [**WM \_ COMPAREITEM**](wm-compareitem.md) para o proprietário da caixa de combinação para determinar qual item corresponde à cadeia de caracteres especificada. Se você não usar o estilo **de \_ classificação CBS** , o **CB \_ SelectString** tentará corresponder o valor **DWORD** em relação ao valor do parâmetro *lParam* .

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

[**localização da CB \_**](cb-findstring.md)
</dt> <dt>

[**\_FINDSTRINGEXACT CB**](cb-findstringexact.md)
</dt> <dt>

[**CB \_ SETcurseal**](cb-setcursel.md)
</dt> <dt>

[**COMPAREITEM do WM \_**](wm-compareitem.md)
</dt> </dl>

 

 





