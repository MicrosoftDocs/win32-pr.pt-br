---
title: LB_FINDSTRING mensagem (Winuser.h)
description: Localiza a primeira cadeia de caracteres em uma caixa de listagem que começa com a cadeia de caracteres especificada.
ms.assetid: 1b7f25a7-0892-4d12-b3e3-21180d9ddfb1
keywords:
- LB_FINDSTRING controles Windows mensagem
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
ms.openlocfilehash: c0a4eb2abbff27c6bde6a4bb44d0faa192ca75229be657bd787aa437b243cd59
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118671299"
---
# <a name="lb_findstring-message"></a>Mensagem \_ DE LB FINDSTRING

Localiza a primeira cadeia de caracteres em uma caixa de listagem que começa com a cadeia de caracteres especificada.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

O índice baseado em zero do item antes do primeiro item a ser pesquisado. Quando a pesquisa atinge a parte inferior da caixa de listagem, ela continua pesquisando da parte superior da caixa de listagem de volta para o item especificado pelo *parâmetro wParam.* Se *wParam* for -1, toda a caixa de listagem será pesquisada desde o início.

Windows 95/Windows 98/Windows Millennium Edition (Windows Me) : o parâmetro *wParam* é limitado a valores de 16 bits. Isso significa que as caixas de listagem não podem conter mais de 32.767 itens. Embora o número de itens seja restrito, o tamanho total em bytes dos itens em uma caixa de listagem é limitado apenas pela memória disponível.

</dd> <dt>

*lParam* 
</dt> <dd>

Um ponteiro para a cadeia de caracteres terminada em nulo que contém a cadeia de caracteres para a qual pesquisar. A pesquisa é independente de maiúsculas e minúsculas, portanto, essa cadeia de caracteres pode conter qualquer combinação de letras maiúsculas e minúsculas.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O valor de retorno é o índice do item correspondente ou LB \_ ERR se a pesquisa não foi bem-sucedida.

## <a name="remarks"></a>Comentários

Se a caixa de listagem tiver o estilo desenhado pelo proprietário, mas não o estilo [**\_ HASSTRINGS do LBS,**](list-box-styles.md) a ação tomada por **LB \_ FINDSTRING** dependerá de se o estilo [**SORT \_ do LBS**](list-box-styles.md) será usado. Se **LBS \_ SORT** for usado, o sistema enviará mensagens [**WM \_ COMPAREITEM**](wm-compareitem.md) ao proprietário da caixa de listagem para determinar qual item corresponde à cadeia de caracteres especificada. Caso contrário, **LB \_ FINDSTRING** tenta encontrar um item que tenha um valor longo (fornecido como o parâmetro *lParam* da mensagem [**LB \_ ADDSTRING**](lb-addstring.md) ou [**LB \_ INSERTSTRING)**](lb-insertstring.md) que corresponde ao parâmetro *lParam.*

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                                           |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                                     |
| parâmetro<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**LB \_ FINDSTRINGEXACT**](lb-findstringexact.md)
</dt> </dl>

 

 





