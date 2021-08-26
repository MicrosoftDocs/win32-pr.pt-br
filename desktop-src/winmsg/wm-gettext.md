---
description: Copia o texto que corresponde a uma janela em um buffer fornecido pelo chamador.
ms.assetid: 117c3d6d-24cd-462f-bdb0-b65d8914273a
title: WM_GETTEXT mensagem (Winuser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e3e1bc6a8a77c51b3ab5b84f5cce700e65b180b357c932b4044a2b65cb49fc8e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120089886"
---
# <a name="wm_gettext-message"></a>Mensagem \_ WM GETTEXT

Copia o texto que corresponde a uma janela em um buffer fornecido pelo chamador.


```C++
#define WM_GETTEXT                      0x000D
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

O número máximo de caracteres a serem copiados, incluindo o caractere nulo de terminação.

Aplicativos ANSI podem ter a cadeia de caracteres no buffer reduzida em tamanho (para um mínimo de metade do valor *wParam)* devido à conversão de ANSI para Unicode.

</dd> <dt>

*lParam* 
</dt> <dd>

Um ponteiro para o buffer que deve receber o texto.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Tipo: **LRESULT**

O valor de retorno é o número de caracteres copiados, não incluindo o caractere nulo de terminação.

## <a name="remarks"></a>Comentários

A [**função DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) copia o texto associado à janela para o buffer especificado e retorna o número de caracteres copiados. Observe que, para controles estáticos que não são de texto, isso fornece o texto com o qual o controle foi originalmente criado, ou seja, o número da ID. No entanto, ele fornece a ID do controle estático sem texto como criado originalmente. Ou seja, se você usou posteriormente um **\_ STM SETIMAGE** para alterá-lo, a ID original ainda será retornada.

Para um controle de edição, o texto a ser copiado é o conteúdo do controle de edição. Para uma caixa de combinação, o texto é o conteúdo da parte do controle de edição (ou texto estático) da caixa de combinação. Para um botão, o texto é o nome do botão. Para outras janelas, o texto é o título da janela. Para copiar o texto de um item em uma caixa de listagem, um aplicativo pode usar a [**mensagem \_ LB GETTEXT.**](../controls/lb-gettext.md)

Quando a **mensagem WM \_ GETTEXT** é enviada para um controle estático com o estilo **SS \_ ICON,** um alça para o ícone será retornado nos primeiros quatro bytes do buffer apontado por *lParam*. Isso só será verdadeiro se a [**mensagem WM \_ SETTEXT**](wm-settext.md) tiver sido usada para definir o ícone.

**Edição rica:** Se o texto a ser copiado exceder 64K, use a mensagem [**EM \_ STREAMOUT**](../controls/em-streamout.md) [**ou EM \_ GETSELTEXT.**](../controls/em-getseltext.md)

Enviar uma **mensagem WM \_ GETTEXT** para um controle estático sem texto, como um bitmap estático ou controle de ícone estático, não retorna um valor de cadeia de caracteres. Em vez disso, ele retorna zero. Além disso, nas versões anteriores do Windows, os aplicativos podiam enviar uma mensagem **WM \_ GETTEXT** para um controle estático sem texto para recuperar a ID do controle. Para recuperar a ID de um controle, os aplicativos podem usar [**GetWindowLong**](/windows/win32/api/winuser/nf-winuser-getwindowlonga) passando **\_ a ID gwL** como o valor de índice ou [**GetWindowLongPtr**](/windows/win32/api/winuser/nf-winuser-getwindowlongptra) usando a **\_ ID gwlp**.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                               |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                     |
| Cabeçalho<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Referência**
</dt> <dt>

[**Defwindowproc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[**Getwindowlong**](/windows/win32/api/winuser/nf-winuser-getwindowlonga)
</dt> <dt>

[**GetWindowLongPtr**](/windows/win32/api/winuser/nf-winuser-getwindowlongptra)
</dt> <dt>

[**Getwindowtext**](/windows/win32/api/winuser/nf-winuser-getwindowtexta)
</dt> <dt>

[**GetWindowTextLength**](/windows/win32/api/winuser/nf-winuser-getwindowtextlengtha)
</dt> <dt>

[**WM \_ GETTEXTLENGTH**](wm-gettextlength.md)
</dt> <dt>

[**WM \_ SETTEXT**](wm-settext.md)
</dt> <dt>

**Conceitual**
</dt> <dt>

[Windows](windows.md)
</dt> <dt>

**Outros recursos**
</dt> <dt>

[**EM \_ GETSELTEXT**](../controls/em-getseltext.md)
</dt> <dt>

[**EM \_ STREAMOUT**](../controls/em-streamout.md)
</dt> <dt>

[**LB \_ GETTEXT**](../controls/lb-gettext.md)
</dt> </dl>

 

 
