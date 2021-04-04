---
description: Copia o texto que corresponde a uma janela em um buffer fornecido pelo chamador.
ms.assetid: 117c3d6d-24cd-462f-bdb0-b65d8914273a
title: Mensagem de WM_GETTEXT (WinUser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 47f8e2268c1d0ec043e24a001f16abae357bdbdc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103662596"
---
# <a name="wm_gettext-message"></a>\_Mensagem de GETtext do WM

Copia o texto que corresponde a uma janela em um buffer fornecido pelo chamador.


```C++
#define WM_GETTEXT                      0x000D
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

O número máximo de caracteres a serem copiados, incluindo o caractere nulo de terminação.

Os aplicativos ANSI podem ter a cadeia de caracteres no buffer reduzida em tamanho (até um mínimo de metade do valor *wParam* ) devido à conversão de ANSI para Unicode.

</dd> <dt>

*lParam* 
</dt> <dd>

Um ponteiro para o buffer que deve receber o texto.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **LRESULT**

O valor de retorno é o número de caracteres copiados, não incluindo o caractere nulo de terminação.

## <a name="remarks"></a>Comentários

A função [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) copia o texto associado à janela no buffer especificado e retorna o número de caracteres copiados. Observe que, para controles estáticos que não são de texto, isso lhe dá o texto com o qual o controle foi originalmente criado, ou seja, o número de ID. No entanto, ele fornece a ID do controle estático de não texto como criado originalmente. Ou seja, se você usou subseqüentemente um **STM \_ SetImage** para alterá-lo, a ID original ainda seria retornada.

Para um controle de edição, o texto a ser copiado é o conteúdo do controle de edição. Para uma caixa de combinação, o texto é o conteúdo da parte do controle de edição (ou texto estático) da caixa de combinação. Para um botão, o texto é o nome do botão. Para outras janelas, o texto é o título da janela. Para copiar o texto de um item em uma caixa de listagem, um aplicativo pode usar a mensagem [**\_ gettext do lb**](../controls/lb-gettext.md) .

Quando a mensagem do **WM \_ gettext** é enviada a um controle estático com o estilo de **\_ ícone SS** , um identificador para o ícone será retornado nos primeiros quatro bytes do buffer apontado por *lParam*. Isso será verdadeiro somente se a [**mensagem \_ SetText do WM**](wm-settext.md) tiver sido usada para definir o ícone.

**Edição avançada:** Se o texto a ser copiado exceder 64K, use a mensagem em [**\_ StreamOut**](../controls/em-streamout.md) ou em [**\_ GETSELTEXT**](../controls/em-getseltext.md) .

Enviar uma mensagem de **\_ gettext do WM** para um controle estático de não texto, como um bitmap estático ou um controle de ícone estático, não retorna um valor de cadeia de caracteres. Em vez disso, retorna zero. Além disso, nas versões anteriores do Windows, os aplicativos podiam enviar uma mensagem de **\_ gettext do WM** a um controle estático não texto para recuperar a ID do controle. Para recuperar a ID de um controle, os aplicativos podem usar [**GetWindowLong**](/windows/win32/api/winuser/nf-winuser-getwindowlonga) passando a **\_ ID GWL** como o valor de índice ou [**GetWindowLongPtr**](/windows/win32/api/winuser/nf-winuser-getwindowlongptra) usando a **\_ ID de GWLP**.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                                               |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                                     |
| Cabeçalho<br/>                   | <dl> <dt>WinUser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Referência**
</dt> <dt>

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[**GetWindowLong**](/windows/win32/api/winuser/nf-winuser-getwindowlonga)
</dt> <dt>

[**GetWindowLongPtr**](/windows/win32/api/winuser/nf-winuser-getwindowlongptra)
</dt> <dt>

[**GetWindowText**](/windows/win32/api/winuser/nf-winuser-getwindowtexta)
</dt> <dt>

[**GetWindowTextLength**](/windows/win32/api/winuser/nf-winuser-getwindowtextlengtha)
</dt> <dt>

[**GETTEXTLENGTH do WM \_**](wm-gettextlength.md)
</dt> <dt>

[**SetText do WM \_**](wm-settext.md)
</dt> <dt>

**Conceitua**
</dt> <dt>

[Windows](windows.md)
</dt> <dt>

**Outros recursos**
</dt> <dt>

[**em \_ GETSELTEXT**](../controls/em-getseltext.md)
</dt> <dt>

[**em \_ fluxo contínuo**](../controls/em-streamout.md)
</dt> <dt>

[**LB \_ GETtext**](../controls/lb-gettext.md)
</dt> </dl>

 

 
