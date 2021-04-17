---
title: Mensagem de WM_MENUSELECT (WinUser. h)
description: Enviado para a janela do proprietário de um menu quando o usuário seleciona um item de menu.
ms.assetid: 57684a19-dfaa-4e0c-a8ff-010533322cb0
keywords:
- WM_MENUSELECT menus de mensagens e outros recursos
topic_type:
- apiref
api_name:
- WM_MENUSELECT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bdee9187ba2074944b3611fee10f5a22c2cc25ca
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105811964"
---
# <a name="wm_menuselect-message"></a>Mensagem do WM \_ MENUSELECT

Enviado para a janela do proprietário de um menu quando o usuário seleciona um item de menu.


```C++
#define WM_MENUSELECT                   0x011F
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*wParam* 
</dt> <dd>

A palavra de ordem inferior Especifica o item de menu ou o índice de submenu. Se o item selecionado for um item de comando, esse parâmetro conterá o identificador do item de menu. Se o item selecionado abrir um menu suspenso ou submenu, esse parâmetro conterá o índice do menu suspenso ou submenu no menu principal, e o parâmetro *lParam* conterá o identificador para o menu principal (clicado); Use a função [**GetSubMenu**](/windows/desktop/api/Winuser/nf-winuser-getsubmenu) para obter o identificador de menu para o menu suspenso ou o submenu.

A palavra de ordem superior especifica um ou mais sinalizadores de menu. Esse parâmetro pode ser um ou mais dos valores a seguir.



| Valor                                                                                                                                                                                                                             | Significado                                                                                                                            |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MF_BITMAP"></span><span id="mf_bitmap"></span><dl> <dt>**MF \_**</dt> <dt>0X00000004L</dt> de bitmap </dl>                | Item exibe um bitmap.<br/>                                                                                                 |
| <span id="MF_CHECKED"></span><span id="mf_checked"></span><dl> <dt>**MF \_ 0x00000008L VERIFICAda**</dt> <dt></dt> </dl>             | O item está marcado.<br/>                                                                                                        |
| <span id="MF_DISABLED"></span><span id="mf_disabled"></span><dl> <dt>**MF \_ 0x00000002L DESABILITAdo**</dt> <dt></dt> </dl>          | O item está desabilitado.<br/>                                                                                                       |
| <span id="MF_GRAYED"></span><span id="mf_grayed"></span><dl> <dt>**MF \_ Em cinza**</dt> - <dt>0x00000001</dt> </dl>                | O item está acinzentado.<br/>                                                                                                         |
| <span id="MF_HILITE"></span><span id="mf_hilite"></span><dl> <dt>**MF \_ HILITE**</dt> <dt>0x00000080L</dt> </dl>                | O item está realçado.<br/>                                                                                                    |
| <span id="MF_MOUSESELECT"></span><span id="mf_mouseselect"></span><dl> <dt>**MF \_ MOUSESELECT**</dt> <dt>0x00008000L</dt> </dl> | Item selecionado com o mouse.<br/>                                                                                        |
| <span id="MF_OWNERDRAW"></span><span id="mf_ownerdraw"></span><dl> <dt>**MF \_ OWNERDRAW**</dt> <dt>0x00000100L</dt> </dl>       | Item é um item desenhado pelo proprietário.<br/>                                                                                            |
| <span id="MF_POPUP"></span><span id="mf_popup"></span><dl> <dt>**MF \_ 0x00000010L pop-up**</dt> <dt></dt> </dl>                   | Item abre um menu suspenso ou submenu.<br/>                                                                                 |
| <span id="MF_SYSMENU"></span><span id="mf_sysmenu"></span><dl> <dt>**MF \_ SYSMENU**</dt> <dt>0x00002000L</dt> </dl>             | O item está contido no menu janela. O parâmetro *lParam* contém um identificador para o menu associado à mensagem.<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Um identificador para o menu que foi clicado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se um aplicativo processar essa mensagem, ele deverá retornar zero.

## <a name="remarks"></a>Comentários

Se a palavra de ordem superior de *wParam* contiver 0xFFFF e o parâmetro *lParam* contiver **NULL**, o sistema fechará o menu.

Não use o valor 1 para a palavra de ordem superior de *wParam*, pois esse valor é especificado como (**uint**) [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))(*wParam*). Se o valor for 0xFFFF, ele será interpretado como 0x0000FFFF, e não 1, devido à conversão para um **uint**.

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

[**GetSubMenu**](/windows/desktop/api/Winuser/nf-winuser-getsubmenu)
</dt> <dt>

[**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85))
</dt> <dt>

[**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85))
</dt> <dt>

**Conceitua**
</dt> <dt>

[Aceleradores de teclado](keyboard-accelerators.md)
</dt> </dl>

 

