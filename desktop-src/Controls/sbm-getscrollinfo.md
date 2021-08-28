---
title: SBM_GETSCROLLINFO mensagem (Winuser.h)
description: A mensagem \_ GETSCROLLINFO do SBM é enviada para recuperar os parâmetros de uma barra de rolagem.
ms.assetid: 3b43430f-b55f-43ec-8558-baf5c953064f
keywords:
- SBM_GETSCROLLINFO controles Windows mensagem
topic_type:
- apiref
api_name:
- SBM_GETSCROLLINFO
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b5fde18fe30e9d944e547305094e7ea69e6745d4e1e112d8697367cd82833588
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119919466"
---
# <a name="sbm_getscrollinfo-message"></a>Mensagem GETSCROLLINFO do SBM \_

A **mensagem \_ GETSCROLLINFO do SBM** é enviada para recuperar os parâmetros de uma barra de rolagem.

Os aplicativos não devem enviar essa mensagem diretamente. Em vez disso, eles devem usar a [**função GetScrollInfo.**](/windows/desktop/api/Winuser/nf-winuser-getscrollinfo) Uma janela recebe essa mensagem por meio de [*sua função WindowProc.*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) Os aplicativos que implementam um controle de barra de rolagem personalizado devem responder a essas mensagens para que a **função GetScrollInfo** funcione corretamente.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Este parâmetro não é usado.

</dd> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma [**estrutura SCROLLINFO.**](/windows/win32/api/winuser/ns-winuser-scrollinfo) Antes de [**chamar GetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-getscrollinfo), de definir o membro **cbSize** da estrutura como **sizeof**(**SCROLLINFO**) e definir o membro **fMask** para especificar os parâmetros da barra de rolagem a recuperar. Antes de retornar, a mensagem copia os parâmetros especificados para os membros apropriados da estrutura.

O **membro fMask** pode ser um ou mais dos valores a seguir.



| Valor                                                                                                                                                      | Significado                                                                             |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <span id="SIF_ALL"></span><span id="sif_all"></span><dl> <dt>**SIF \_ ALL**</dt> </dl>                | Combinação de SIF \_ PAGE, SIF \_ POS, SIF \_ RANGE e SIF \_ TRACKPOS.<br/>       |
| <span id="SIF_PAGE"></span><span id="sif_page"></span><dl> <dt>**PÁGINA \_ SIF**</dt> </dl>             | Copia a página de rolagem para o membro nPage.<br/>                              |
| <span id="SIF_POS"></span><span id="sif_pos"></span><dl> <dt>**POS \_ do SIF**</dt> </dl>                | Copia a posição de rolagem para o membro nPos. <br/>                          |
| <span id="SIF_RANGE"></span><span id="sif_range"></span><dl> <dt>**INTERVALO \_ SIF**</dt> </dl>          | Copia o intervalo de rolagem para os membros nMin e nMax. <br/>                   |
| <span id="SIF_TRACKPOS"></span><span id="sif_trackpos"></span><dl> <dt>**TRACKPOS do SIF \_**</dt> </dl> | Copia a posição de acompanhamento da caixa de rolagem atual para o membro nTrackPos.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se a mensagem tiver recuperado valores, o valor de retorno será **TRUE;** caso contrário, será **FALSE.**

## <a name="remarks"></a>Comentários

As mensagens que indicam a posição da barra de rolagem, [**WM \_ HSCROLL**](wm-hscroll.md) e [**WM \_ VSCROLL**](wm-vscroll.md)fornecem apenas 16 bits de dados de posição. No entanto, a estrutura [**SCROLLINFO**](/windows/win32/api/winuser/ns-winuser-scrollinfo) usada por **SBM \_ GETSCROLLINFO,** [**SBM \_ SETSCROLLINFO,**](sbm-setscrollinfo.md) [**GetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-getscrollinfo)e [**SetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-setscrollinfo) fornece 32 bits de dados de posição da barra de rolagem. Você pode usar essas mensagens e funções ao processar as mensagens **WM \_ HSCROLL** ou **WM \_ VSCROLL** para obter dados de posição da barra de rolagem de 32 bits.

Para obter a posição de 32 bits da caixa de rolagem (thumb) durante um código de solicitação SB THUMBTRACK em uma mensagem \_ [**WM \_ HSCROLL**](wm-hscroll.md) ou [**WM \_ VSCROLL,**](wm-vscroll.md) envie **SBM \_ GETSCROLLINFO** com o valor TRACKPOS SIF no membro \_ **fMask** da estrutura [**SCROLLINFO.**](/windows/win32/api/winuser/ns-winuser-scrollinfo) A mensagem retorna a posição de acompanhamento da caixa de rolagem no **membro nTrackPos** da **estrutura SCROLLINFO.** Isso permite que você receba a posição da caixa de rolagem conforme o usuário a move. Como alternativa, você pode usar a [**função GetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-getscrollinfo) para obter as mesmas informações.

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

[**Getscrollinfo**](/windows/desktop/api/Winuser/nf-winuser-getscrollinfo)
</dt> <dt>

[**SBM \_ SETSCROLLINFO**](sbm-setscrollinfo.md)
</dt> <dt>

[**Scrollinfo**](/windows/win32/api/winuser/ns-winuser-scrollinfo)
</dt> <dt>

[**Setscrollinfo**](/windows/desktop/api/Winuser/nf-winuser-setscrollinfo)
</dt> </dl>

 

