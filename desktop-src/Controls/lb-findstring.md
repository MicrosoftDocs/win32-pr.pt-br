---
title: Mensagem de LB_FINDSTRING (WinUser. h)
description: Localiza a primeira cadeia de caracteres em uma caixa de listagem que começa com a cadeia de caracteres especificada.
ms.assetid: 1b7f25a7-0892-4d12-b3e3-21180d9ddfb1
keywords:
- Controles de LB_FINDSTRING de mensagens do Windows
topic_type:
- apiref
api_name:
- LB_FINDSTRING
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b528dbafbc386af05a091f24c8c28327739f5d40
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455896"
---
# <a name="lb_findstring-message"></a>\_Mensagem de localização lb

Localiza a primeira cadeia de caracteres em uma caixa de listagem que começa com a cadeia de caracteres especificada.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

O índice baseado em zero do item antes do primeiro item a ser pesquisado. Quando a pesquisa atingir a parte inferior da caixa de listagem, ela continuará pesquisando da parte superior da caixa de listagem de volta para o item especificado pelo parâmetro *wParam* . Se *wParam* for-1, a caixa de listagem inteira será pesquisada desde o início.

Windows 95/Windows 98/Windows Millennium Edition (Windows me): o parâmetro *wParam* é limitado a valores de 16 bits. Isso significa que as caixas de listagem não podem conter mais de 32.767 itens. Embora o número de itens seja restrito, o tamanho total em bytes dos itens em uma caixa de listagem é limitado apenas pela memória disponível.

</dd> <dt>

*lParam* 
</dt> <dd>

Um ponteiro para a cadeia de caracteres terminada em nulo que contém a cadeia de caracteres a ser pesquisada. A pesquisa diferencia maiúsculas de minúsculas, portanto, essa cadeia de caracteres pode conter qualquer combinação de letras maiúsculas e minúsculas.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O valor de retorno será o índice do item correspondente ou o \_ erro de lb se a pesquisa não tiver sido bem-sucedida.

## <a name="remarks"></a>Comentários

Se a caixa de listagem tiver o estilo desenhado pelo proprietário, mas não o estilo de [**lbs \_ HASSTRINGS**](list-box-styles.md) , a ação executada pela **\_ localização do lb** dependerá se o estilo de [**\_ classificação lbs**](list-box-styles.md) for usado. Se **a \_ classificação de lbs** for usada, o sistema enviará mensagens do [**WM \_ COMPAREITEM**](wm-compareitem.md) para o proprietário da caixa de listagem para determinar qual item corresponde à cadeia de caracteres especificada. Caso contrário, o **lb \_ FindString** tentará localizar um item que tem um valor longo (fornecido como o parâmetro *lParam* da mensagem do [**lb \_ AddString**](lb-addstring.md) ou [**lbstring \_**](lb-insertstring.md) ) que corresponde ao parâmetro *lParam* .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                                           |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                                     |
| parâmetro<br/>                   | <dl> <dt>WinUser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_FINDSTRINGEXACT lb**](lb-findstringexact.md)
</dt> </dl>

 

 





