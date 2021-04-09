---
title: Mensagem de LB_FINDSTRINGEXACT (WinUser. h)
description: Localiza a primeira cadeia de caracteres da caixa de listagem que corresponde exatamente à cadeia de caracteres especificada, exceto que a pesquisa não diferencia maiúsculas de minúsculas.
ms.assetid: 9bfe21af-626d-4416-aa20-65c425bd99af
keywords:
- Controles de LB_FINDSTRINGEXACT de mensagens do Windows
topic_type:
- apiref
api_name:
- LB_FINDSTRINGEXACT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d85b4f817eabae95c6021647b0c47926b2163722
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009716"
---
# <a name="lb_findstringexact-message"></a>FINDSTRINGEXACT de mensagens de LB \_

Localiza a primeira cadeia de caracteres da caixa de listagem que corresponde exatamente à cadeia de caracteres especificada, exceto que a pesquisa não diferencia maiúsculas de minúsculas.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

O índice baseado em zero do item antes do primeiro item a ser pesquisado. Quando a pesquisa atingir a parte inferior da caixa de listagem, ela continuará pesquisando da parte superior da caixa de listagem de volta para o item especificado pelo parâmetro *wParam* . Se *wParam* for-1, a caixa de listagem inteira será pesquisada desde o início.

Windows 95/Windows 98/Windows Millennium Edition (Windows me): o parâmetro *wParam* é limitado a valores de 16 bits. Isso significa que as caixas de listagem não podem conter mais de 32.767 itens. Embora o número de itens seja restrito, o tamanho total em bytes dos itens em uma caixa de listagem é limitado apenas pela memória disponível.

</dd> <dt>

*lParam* 
</dt> <dd>

Um ponteiro para a cadeia de caracteres terminada em nulo para pesquisa. A pesquisa não diferencia maiúsculas de minúsculas, portanto, essa cadeia de caracteres pode conter qualquer combinação de letras maiúsculas e minúsculas.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O valor de retorno será o índice de base zero do item de correspondência ou o \_ erro de lb se a pesquisa não tiver sido bem-sucedida.

## <a name="remarks"></a>Comentários

Essa função só será bem-sucedida se a cadeia de caracteres especificada e um item de caixa de listagem tiverem o mesmo comprimento (exceto para NULL no final da cadeia de caracteres especificada) e tiverem exatamente os mesmos caracteres.

Se a caixa de listagem tiver o estilo desenhado pelo proprietário, mas não o estilo de [**lbs \_ HASSTRINGS**](list-box-styles.md) , a ação executada por **lb \_ FINDSTRINGEXACT** dependerá de o estilo de [**\_ classificação lbs**](list-box-styles.md) ser usado. Se **a \_ classificação de lbs** for usada, o sistema enviará mensagens do [**WM \_ COMPAREITEM**](wm-compareitem.md) para o proprietário da caixa de listagem para determinar qual item corresponde à cadeia de caracteres especificada. Caso contrário, o **lb \_ FINDSTRINGEXACT** tentará localizar um item que tenha um valor longo (fornecido como o parâmetro *lParam* da mensagem de [**\_ inserção**](lb-insertstring.md) [**\_ AddString**](lb-addstring.md) ou lb) do lb que corresponda ao parâmetro *lParam* .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                                           |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                                     |
| parâmetro<br/>                   | <dl> <dt>WinUser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Localizar LBstring \_**](lb-findstring.md)
</dt> </dl>

 

 





