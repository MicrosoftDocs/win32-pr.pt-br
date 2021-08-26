---
title: Mensagem de SBM_SETSCROLLINFO (WinUser. h)
description: A \_ mensagem SBM SETSCROLLINFO é enviada para definir os parâmetros de uma barra de rolagem.
ms.assetid: e0e42a81-67be-4d40-88c8-77398b068617
keywords:
- controles de Windows de mensagem de SBM_SETSCROLLINFO
topic_type:
- apiref
api_name:
- SBM_SETSCROLLINFO
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5622371abb86301e1450c9fa0d6864e8db76c9837fca48fe8bcf11cb884f6b5c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119914286"
---
# <a name="sbm_setscrollinfo-message"></a>\_Mensagem SBM SETSCROLLINFO

A mensagem **SBM \_ SETSCROLLINFO** é enviada para definir os parâmetros de uma barra de rolagem.

Os aplicativos não devem enviar essa mensagem diretamente. Em vez disso, eles devem usar a função [**SetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-setscrollinfo) . Uma janela recebe essa mensagem por meio de sua função [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) . Os aplicativos que implementam um controle de barra de rolagem personalizado devem responder a essas mensagens para que a função **SetScrollInfo** funcione corretamente.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

Especifica se a barra de rolagem é redesenhada para refletir a nova posição da caixa de rolagem. Se esse parâmetro for **true**, a barra de rolagem será redesenhada. Se for **false**, a barra de rolagem não será redesenhada.

</dd> <dt>

*lParam* 
</dt> <dd>

Ponteiro para uma estrutura [**SCROLLINFO**](/windows/win32/api/winuser/ns-winuser-scrollinfo) . Antes de chamar [**SetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-setscrollinfo), defina o membro **cbSize** da estrutura como **sizeof**(**SCROLLINFO**), defina o membro **fMask** para indicar os parâmetros a serem definidos e especifique os novos valores de parâmetro nos membros apropriados.

O membro **fMask** pode ser um ou mais dos valores a seguir.



| Valor                                                                                                                                                                           | Significado                                                                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| <span id="SIF_DISABLENOSCROLL"></span><span id="sif_disablenoscroll"></span><dl> <dt>**\_DISABLENOSCROLL sif**</dt> </dl> | Desabilita a barra de rolagem em vez de removê-la, se os novos parâmetros da barra de rolagem tornarem a barra de rolagem desnecessária.<br/> |
| <span id="SIF_PAGE"></span><span id="sif_page"></span><dl> <dt>**\_página sif**</dt> </dl>                                  | Define a página de rolagem para o valor especificado no membro **nconfiguração** .<br/>                                                |
| <span id="SIF_POS"></span><span id="sif_pos"></span><dl> <dt>**POS do SIF \_**</dt> </dl>                                     | Define a posição de rolagem para o valor especificado no membro **nPos** . <br/>                                            |
| <span id="SIF_RANGE"></span><span id="sif_range"></span><dl> <dt>**intervalo do SIF \_**</dt> </dl>                               | Define o intervalo de rolagem para o valor especificado nos membros **nmín** e **nmáx** . <br/>                                 |



 

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O valor de retorno é a posição atual da caixa de rolagem.

## <a name="remarks"></a>Comentários

As mensagens que indicam a posição da barra de rolagem, o [**WM \_ HSCROLL**](wm-hscroll.md) e o [**WM \_ VSCROLL**](wm-vscroll.md), fornecem apenas 16 bits de dados de posição. No entanto, a estrutura [**SCROLLINFO**](/windows/win32/api/winuser/ns-winuser-scrollinfo) usada por [**SBM \_ GETSCROLLINFO**](sbm-getscrollinfo.md), **SBM \_ SETSCROLLINFO**, [**GETSCROLLINFO**](/windows/desktop/api/Winuser/nf-winuser-getscrollinfo)e [**SETSCROLLINFO**](/windows/desktop/api/Winuser/nf-winuser-setscrollinfo) fornece 32 bits de dados de posição da barra de rolagem. Você pode usar essas mensagens e funções durante o processamento das mensagens do **WM \_ HSCROLL** ou do **WM \_ VSCROLL** para obter dados de posição da barra de rolagem de 32 bits.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                                           |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2003\]<br/>                                                     |
| Cabeçalho<br/>                   | <dl> <dt>Winuser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

**Referência**
</dt> <dt>

[**GetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-getscrollinfo)
</dt> <dt>

[**SBM \_ GETSCROLLINFO**](sbm-getscrollinfo.md)
</dt> <dt>

[**SCROLLINFO**](/windows/win32/api/winuser/ns-winuser-scrollinfo)
</dt> <dt>

[**SetScrollInfo**](/windows/desktop/api/Winuser/nf-winuser-setscrollinfo)
</dt> </dl>

 

