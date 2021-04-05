---
title: Mensagem de LB_GETTEXTLEN (WinUser. h)
description: Obtém o comprimento de uma cadeia de caracteres em uma caixa de listagem.
ms.assetid: 866730bc-ffd4-42fd-9cea-5d326e129189
keywords:
- Controles de LB_GETTEXTLEN de mensagens do Windows
topic_type:
- apiref
api_name:
- LB_GETTEXTLEN
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b1f76bf3574b09b76d5f1010dcb59c8245555dc3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104085465"
---
# <a name="lb_gettextlen-message"></a>GETTEXTLEN de mensagens de LB \_

Obtém o comprimento de uma cadeia de caracteres em uma caixa de listagem.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

O índice de base zero da cadeia de caracteres.

Windows 95/Windows 98/Windows Millennium Edition (Windows me): o parâmetro *wParam* é limitado a valores de 16 bits. Isso significa que as caixas de listagem não podem conter mais de 32.767 itens. Embora o número de itens seja restrito, o tamanho total em bytes dos itens em uma caixa de listagem é limitado apenas pela memória disponível.

</dd> <dt>

*lParam* 
</dt> <dd>

Este parâmetro não é usado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

O valor de retorno é o comprimento da cadeia de caracteres, em **TCHAR** s, excluindo o caractere nulo de terminação. Em determinadas condições, esse valor pode ser, na verdade, maior que o comprimento do texto. Para obter mais informações, consulte a seção Comentários a seguir.

Se o parâmetro *wParam* não especificar um índice válido, o valor de retorno será um \_ erro de lb.

## <a name="remarks"></a>Comentários

Em determinadas condições, o valor de retorno é maior do que o comprimento real do texto. Isso ocorre com determinadas misturas de ANSI e Unicode e é devido ao sistema operacional permitir a possível existência de caracteres de conjunto de caracteres de dois bytes (DBCS) dentro do texto. O valor de retorno, no entanto, sempre será pelo menos tão grande quanto o comprimento real do texto; Portanto, você pode usá-lo sempre para orientar a alocação do buffer. Esse comportamento pode ocorrer quando um aplicativo usa funções ANSI e caixas de diálogo comuns, que usam Unicode.

Para obter o comprimento exato do texto, use as mensagens [**do \_ WM gettext**](/windows/desktop/winmsg/wm-gettext), [**lb \_ gettext**](lb-gettext.md)ou [**CB \_ GETLBTEXT**](cb-getlbtext.md) ou a função [**GetWindowText**](/windows/desktop/api/winuser/nf-winuser-getwindowtexta) .

Se a caixa de listagem tiver um estilo desenhado pelo proprietário, mas não o estilo de [**lbs \_ HASSTRINGS**](list-box-styles.md) , o valor de retorno será sempre o tamanho, em bytes, de um **DWORD**.

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

[**\_GETLBTEXT CB**](cb-getlbtext.md)
</dt> <dt>

[**LB \_ GETtext**](lb-gettext.md)
</dt> <dt>

**Outros recursos**
</dt> <dt>

[**GetWindowText**](/windows/desktop/api/winuser/nf-winuser-getwindowtexta)
</dt> <dt>

[**WM \_ GETtext**](/windows/desktop/winmsg/wm-gettext)
</dt> </dl>

 

