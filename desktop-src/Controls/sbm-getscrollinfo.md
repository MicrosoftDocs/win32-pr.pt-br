---
title: Mensagem de SBM_GETSCROLLINFO (WinUser. h)
description: A \_ mensagem SBM GETSCROLLINFO é enviada para recuperar os parâmetros de uma barra de rolagem.
ms.assetid: 3b43430f-b55f-43ec-8558-baf5c953064f
keywords:
- Controles de SBM_GETSCROLLINFO de mensagens do Windows
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
ms.openlocfilehash: c4cb05b05ba2686d755c5fa34adcff0016433346
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105753789"
---
# <a name="sbm_getscrollinfo-message"></a>\_Mensagem SBM GETSCROLLINFO

A mensagem **SBM \_ GETSCROLLINFO** é enviada para recuperar os parâmetros de uma barra de rolagem.

Os aplicativos não devem enviar essa mensagem diretamente. Em vez disso, eles devem usar a função [**GetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-getscrollinfo) . Uma janela recebe essa mensagem por meio de sua função [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) . Os aplicativos que implementam um controle de barra de rolagem personalizado devem responder a essas mensagens para que a função **GetScrollInfo** funcione corretamente.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Este parâmetro não é usado.

</dd> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma estrutura [**SCROLLINFO**](/windows/win32/api/winuser/ns-winuser-scrollinfo) . Antes de chamar [**GetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-getscrollinfo), defina o membro **cbSize** da estrutura como **sizeof**(**SCROLLINFO**) e defina o membro **fMask** para especificar os parâmetros da barra de rolagem a serem recuperados. Antes de retornar, a mensagem copia os parâmetros especificados para os membros apropriados da estrutura.

O membro **fMask** pode ser um ou mais dos valores a seguir.



| Valor                                                                                                                                                      | Significado                                                                             |
|------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <span id="SIF_ALL"></span><span id="sif_all"></span><dl> <dt>**SIF \_ todos**</dt> </dl>                | Combinação de \_ Page sif, Sif \_ POS, Sif \_ Range e sif \_ TRACKPOS.<br/>       |
| <span id="SIF_PAGE"></span><span id="sif_page"></span><dl> <dt>**\_página sif**</dt> </dl>             | Copia a página de rolagem para o membro Nconfiguração.<br/>                              |
| <span id="SIF_POS"></span><span id="sif_pos"></span><dl> <dt>**POS do SIF \_**</dt> </dl>                | Copia a posição de rolagem para o membro nPos. <br/>                          |
| <span id="SIF_RANGE"></span><span id="sif_range"></span><dl> <dt>**intervalo do SIF \_**</dt> </dl>          | Copia o intervalo de rolagem para os membros Nmín e Nmáx. <br/>                   |
| <span id="SIF_TRACKPOS"></span><span id="sif_trackpos"></span><dl> <dt>**\_TRACKPOS sif**</dt> </dl> | Copia a posição de controle da caixa de rolagem atual para o membro nTrackPos.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se a mensagem tiver recuperado quaisquer valores, o valor de retorno será **true**; caso contrário, será **false**.

## <a name="remarks"></a>Comentários

As mensagens que indicam a posição da barra de rolagem, o [**WM \_ HSCROLL**](wm-hscroll.md) e o [**WM \_ VSCROLL**](wm-vscroll.md), fornecem apenas 16 bits de dados de posição. No entanto, a estrutura [**SCROLLINFO**](/windows/win32/api/winuser/ns-winuser-scrollinfo) usada por **SBM \_ GETSCROLLINFO**, [**SBM \_ SETSCROLLINFO**](sbm-setscrollinfo.md), [**GETSCROLLINFO**](/windows/desktop/api/Winuser/nf-winuser-getscrollinfo)e [**SETSCROLLINFO**](/windows/desktop/api/Winuser/nf-winuser-setscrollinfo) fornece 32 bits de dados de posição da barra de rolagem. Você pode usar essas mensagens e funções durante o processamento das mensagens do **WM \_ HSCROLL** ou do **WM \_ VSCROLL** para obter dados de posição da barra de rolagem de 32 bits.

Para obter a posição de 32 bits da caixa de rolagem (Thumb) durante um \_ código de solicitação do SB THUMBTRACK em uma mensagem do [**WM \_ HSCROLL**](wm-hscroll.md) ou do [**WM \_ VSCROLL**](wm-vscroll.md) , envie **SBM \_ GETSCROLLINFO** com o valor de TRACKPOS do SIF \_ no membro **fMask** da estrutura [**SCROLLINFO**](/windows/win32/api/winuser/ns-winuser-scrollinfo) . A mensagem retorna a posição de rastreamento da caixa de rolagem no membro **nTrackPos** da estrutura **SCROLLINFO** . Isso permite que você obtenha a posição da caixa de rolagem à medida que o usuário a move. Como alternativa, você pode usar a função [**GetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-getscrollinfo) para obter as mesmas informações.

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

[**GetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-getscrollinfo)
</dt> <dt>

[**SBM \_ SETSCROLLINFO**](sbm-setscrollinfo.md)
</dt> <dt>

[**SCROLLINFO**](/windows/win32/api/winuser/ns-winuser-scrollinfo)
</dt> <dt>

[**SetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-setscrollinfo)
</dt> </dl>

 

