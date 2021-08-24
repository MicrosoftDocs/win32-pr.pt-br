---
description: Determina o comprimento, em caracteres, do texto associado a uma janela.
ms.assetid: 9e185435-a624-4380-adfd-be4f3645ee5d
title: Mensagem de WM_GETTEXTLENGTH (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1bc01f6f7a2b74df41e97a84bb4d7e17d9c3e21966215fcbcca04222d1d5537f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119710386"
---
# <a name="wm_gettextlength-message"></a>Mensagem do WM \_ GETTEXTLENGTH

Determina o comprimento, em caracteres, do texto associado a uma janela.


```C++
#define WM_GETTEXTLENGTH                0x000E
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Esse parâmetro não é usado e deve ser zero.

</dd> <dt>

*lParam* 
</dt> <dd>

Esse parâmetro não é usado e deve ser zero.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **LRESULT**

O valor de retorno é o comprimento do texto em caracteres, não incluindo o caractere nulo de terminação.

## <a name="remarks"></a>Comentários

Para um controle de edição, o texto a ser copiado é o conteúdo do controle de edição. Para uma caixa de combinação, o texto é o conteúdo da parte do controle de edição (ou texto estático) da caixa de combinação. Para um botão, o texto é o nome do botão. Para outras janelas, o texto é o título da janela. Para determinar o comprimento de um item em uma caixa de listagem, um aplicativo pode usar a mensagem [**\_ GETTEXTLEN de lb**](../controls/lb-gettextlen.md) .

Quando a **mensagem \_ GETTEXTLENGTH do WM** é enviada, a função [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) retorna o comprimento, em caracteres, do texto. Em determinadas condições, a função **DefWindowProc** retorna um valor maior que o comprimento real do texto. Isso ocorre com determinadas misturas de ANSI e Unicode e é devido ao sistema permitir a possível existência de caracteres de conjunto de caracteres de dois bytes (DBCS) dentro do texto. O valor de retorno, no entanto, sempre será pelo menos tão grande quanto o comprimento real do texto; Portanto, você pode usá-lo sempre para orientar a alocação do buffer. Esse comportamento pode ocorrer quando um aplicativo usa funções ANSI e caixas de diálogo comuns, que usam Unicode.

Para obter o comprimento exato do texto, use as mensagens [**do \_ WM gettext**](wm-gettext.md), [**lb \_ gettext**](../controls/lb-gettext.md)ou [**CB \_ GETLBTEXT**](../controls/cb-getlbtext.md) ou a função [**GetWindowText**](/windows/win32/api/winuser/nf-winuser-getwindowtexta) .

Enviar uma mensagem do **WM \_ GETTEXTLENGTH** para um controle estático de não texto, como um bitmap estático ou um ícone estático ControlC, não retorna um valor de cadeia de caracteres. Em vez disso, retorna zero.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                               |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                     |
| Cabeçalho<br/>                   | <dl> <dt>Winuser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Referência**
</dt> <dt>

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[**GetWindowText**](/windows/win32/api/winuser/nf-winuser-getwindowtexta)
</dt> <dt>

[**GetWindowTextLength**](/windows/win32/api/winuser/nf-winuser-getwindowtextlengtha)
</dt> <dt>

[**WM \_ GETtext**](wm-gettext.md)
</dt> <dt>

**Conceitua**
</dt> <dt>

[Windows](windows.md)
</dt> <dt>

**Outros recursos**
</dt> <dt>

[**\_GETLBTEXT CB**](../controls/cb-getlbtext.md)
</dt> <dt>

[**LB \_ GETtext**](../controls/lb-gettext.md)
</dt> <dt>

[**\_GETTEXTLEN lb**](../controls/lb-gettextlen.md)
</dt> </dl>

 

 
