---
title: Mensagem de EM_SCROLL (WinUser. h)
description: Rola o texto verticalmente em um controle de edição de várias linhas. Essa mensagem é equivalente a enviar uma \_ mensagem do WM VSCROLL para o controle de edição. Você pode enviar essa mensagem para um controle de edição ou um controle de edição rico.
ms.assetid: 616b5ac2-d92f-4fc5-9a9e-2c7527fb0d97
keywords:
- Controles de EM_SCROLL de mensagens do Windows
topic_type:
- apiref
api_name:
- EM_SCROLL
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 09eb185fb14ef866ab0e7ea8c8064445193347d1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104086418"
---
# <a name="em_scroll-message"></a>\_Mensagem de rolagem em em

Rola o texto verticalmente em um controle de edição de várias linhas. Essa mensagem é equivalente a enviar uma mensagem do [**WM \_ VSCROLL**](wm-vscroll.md) para o controle de edição. Você pode enviar essa mensagem para um controle de edição ou um controle de edição rico.

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

A ação que a barra de rolagem deve tomar. Esse parâmetro pode usar um dos valores a seguir.



| Valor                                                                                                                                                   | Significado                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------|
| <span id="SB_LINEDOWN"></span><span id="sb_linedown"></span><dl> <dt>**SB \_ LINEDOWN**</dt> </dl> | Rola uma linha para baixo.<br/> |
| <span id="SB_LINEUP"></span><span id="sb_lineup"></span><dl> <dt>**linha de SB \_**</dt> </dl>       | Rola uma linha para cima.<br/>   |
| <span id="SB_PAGEDOWN"></span><span id="sb_pagedown"></span><dl> <dt>**SB \_ PageDown**</dt> </dl> | Rola uma página para baixo.<br/> |
| <span id="SB_PAGEUP"></span><span id="sb_pageup"></span><dl> <dt>**SB \_ PageUp**</dt> </dl>       | Rola uma página para cima.<br/>   |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Este parâmetro não é usado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se a mensagem for bem-sucedida, o [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)) do valor de retorno será **true** e [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) será o número de linhas que o comando rolará. O número retornado pode não ser o mesmo que o número real de linhas roladas se a rolagem for movida para o início ou para o fim do texto. Se o parâmetro *wParam* especificar um valor inválido, o valor de retorno será **false**.

## <a name="remarks"></a>Comentários

Para rolar para uma linha ou posição de caractere específica, use a mensagem em [**\_ LINESCROLL**](em-linescroll.md) . Para rolar o cursor para a exibição, use a mensagem em [**\_ SCROLLCARET**](em-scrollcaret.md) .

**Edição avançada:** Com suporte no Microsoft Rich Edit 1,0 e posterior. Para obter informações sobre a compatibilidade das versões de edição rica com as várias versões do sistema, consulte [sobre controles de edição avançados](about-rich-edit-controls.md).

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

[**em \_ LINESCROLL**](em-linescroll.md)
</dt> <dt>

[**em \_ SCROLLCARET**](em-scrollcaret.md)
</dt> <dt>

[**VSCROLL do WM \_**](wm-vscroll.md)
</dt> </dl>

 

