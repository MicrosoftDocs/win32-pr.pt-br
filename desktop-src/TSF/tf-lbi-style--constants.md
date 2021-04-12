---
title: Constantes de TF_LBI_STYLE_ (Ctfutb. h)
description: As \_ constantes TF bin \_ Style \_ \ são usadas no membro DWSTYLE da estrutura TF \_ LANGBARITEMINFO para especificar o estilo de um item da barra de idiomas.
ms.assetid: 9180a666-774f-401b-bea3-68d5396fab30
topic_type:
- apiref
api_name:
- TF_LBI_STYLE_HIDDENSTATUSCONTROL
- TF_LBI_STYLE_SHOWNINTRAY
- TF_LBI_STYLE_HIDEONNOOTHERITEMS
- TF_LBI_STYLE_SHOWNINTRAYONLY
- TF_LBI_STYLE_HIDDENBYDEFAULT
- TF_LBI_STYLE_TEXTCOLORICON
- TF_LBI_STYLE_BTN_BUTTON
- TF_LBI_STYLE_BTN_MENU
- TF_LBI_STYLE_BTN_TOGGLE
api_location:
- Ctfutb.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3b43ef805161afce6cb73bfaa26060308bc0aa5d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455097"
---
# <a name="tf_lbi_style_-constants"></a>Constantes de estilo de TF \_ bin \_ \_ \*

As **\_ constantes TF bin \_ Style \_ \* *_ são usadas no membro _* dwStyle** da estrutura [TF \_ LANGBARITEMINFO](/windows/desktop/api/Ctfutb/ns-ctfutb-tf_langbariteminfo) para especificar o estilo de um item da barra de idiomas.

Se esse estilo for combinado com o \_ botão TF bin \_ Style \_ BTN \_ , uma seta suspensa será exibida para o item além do texto. A seta suspensa funcionará como o botão de menu e clicar nele fará com que **ITfLangBarItemButton:: InitMenu** seja chamado. Clicar na parte de texto do botão fará com que **ITfLangBarItemButton:: OnClick** seja chamado.



| Constante/valor                                                                                                                                                                                                                                                                           | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TF_LBI_STYLE_HIDDENSTATUSCONTROL"></span><span id="tf_lbi_style_hiddenstatuscontrol"></span><dl> <dt>**TF \_ \_Estilo bin \_ HIDDENSTATUSCONTROL**</dt> <dt>0x00000001</dt> </dl> | O item pode ser ocultado ou exibido dinamicamente usando o \_ valor oculto de status do TF bin \_ \_ no método [ITfLangBarItem:: GetStatus](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritem-getstatus) . Se esse valor não estiver presente, o item não poderá ser ocultado dessa maneira.<br/>                                                                                                                                                                                                                                                                         |
| <span id="TF_LBI_STYLE_SHOWNINTRAY"></span><span id="tf_lbi_style_shownintray"></span><dl> <dt>**TF \_ \_Estilo bin \_ SHOWNINTRAY**</dt> <dt>0x00000002</dt> </dl>                         | O item será exibido na bandeja de ícones de notificação, além da barra de idiomas. Não há suporte para esse sinalizador no momento.<br/>                                                                                                                                                                                                                                                                                                                                                                              |
| <span id="TF_LBI_STYLE_HIDEONNOOTHERITEMS"></span><span id="tf_lbi_style_hideonnootheritems"></span><dl> <dt>**TF \_ \_Estilo bin \_ HIDEONNOOTHERITEMS**</dt> <dt>0x00000004</dt> </dl>    | A barra de idiomas ficará oculta se todos os itens na barra de idiomas contiverem esse estilo. Se qualquer item na barra de idiomas não contiver esse estilo, a barra de idiomas será exibida.<br/>                                                                                                                                                                                                                                                                                                                                  |
| <span id="TF_LBI_STYLE_SHOWNINTRAYONLY"></span><span id="tf_lbi_style_shownintrayonly"></span><dl> <dt>**TF \_ \_Estilo bin \_ SHOWNINTRAYONLY**</dt> <dt>0x00000008</dt> </dl>             | O item só será exibido na bandeja do ícone de notificação e não na barra de idiomas. Não há suporte para esse sinalizador no momento.<br/>                                                                                                                                                                                                                                                                                                                                                                             |
| <span id="TF_LBI_STYLE_HIDDENBYDEFAULT"></span><span id="tf_lbi_style_hiddenbydefault"></span><dl> <dt>**TF \_ \_Estilo bin \_ HIDDENBYDEFAULT**</dt> <dt>0x00000010</dt> </dl>             | O item não é exibido na barra de ferramentas até que seja selecionado no menu de opções da barra de idiomas. Esse sinalizador será ignorado se o HIDDENSTATUSCONTROL do estilo do TF \_ bin \_ \_ estiver definido ou se o usuário já tiver alterado o estado oculto/mostrado usando o menu de opções da barra de idiomas.<br/>                                                                                                                                                                                                                                         |
| <span id="TF_LBI_STYLE_TEXTCOLORICON"></span><span id="tf_lbi_style_textcoloricon"></span><dl> <dt>**TF \_ \_Estilo bin \_ TEXTCOLORICON**</dt> <dt>0x00000020</dt> </dl>                   | Qualquer pixel preto dentro do ícone será convertido na cor do texto do tema selecionado. O ícone deve ser monocromático.<br/>                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="TF_LBI_STYLE_BTN_BUTTON"></span><span id="tf_lbi_style_btn_button"></span><dl> <dt>**TF \_ \_Botão de \_ BTN \_ estilo bin**</dt> <dt>0x00010000</dt> </dl>                           | O item é um botão de ação. [ITfLangBarItemButton:: OnClick](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritembutton-onclick) é chamado quando o item é pressionado.<br/>                                                                                                                                                                                                                                                                                                                                                                             |
| <span id="TF_LBI_STYLE_BTN_MENU"></span><span id="tf_lbi_style_btn_menu"></span><dl> <dt>**TF \_ \_ \_ \_ Menu BTN estilo bin**</dt> <dt>0x00020000</dt> </dl>                                 | O item é um menu. [ITfLangBarItemButton:: InitMenu](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritembutton-initmenu) é chamado quando o item é pressionado.<br/> Se esse estilo for combinado com o \_ botão TF bin \_ Style \_ BTN \_ , uma seta suspensa será exibida para o item além do texto. A seta suspensa funcionará como o botão de menu e clicar nele fará com que **ITfLangBarItemButton:: InitMenu** seja chamado. Clicar na parte de texto do botão fará com que **ITfLangBarItemButton:: OnClick** seja chamado.<br/> |
| <span id="TF_LBI_STYLE_BTN_TOGGLE"></span><span id="tf_lbi_style_btn_toggle"></span><dl> <dt>**TF \_ \_BTN estilo \_ bin \_ alternar**</dt> <dt>0x00040000</dt> </dl>                           | O item é um botão de alternância e opera de forma semelhante a uma caixa de seleção. **ITfLangBarItemButton:: OnClick** é chamado quando o item é pressionado.<br/>                                                                                                                                                                                                                                                                                                                                                                       |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                            |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                  |
| Redistribuível<br/>          | TSF 1,0 no Windows 2000 Professional<br/>                                       |
| parâmetro<br/>                   | <dl> <dt>Ctfutb. h</dt> </dl>   |
| INSERI<br/>                      | <dl> <dt>Ctfutb. idl</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[TF \_ LANGBARITEMINFO](/windows/desktop/api/Ctfutb/ns-ctfutb-tf_langbariteminfo)
</dt> <dt>

[ITfLangBarItem:: GetInfo](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritem-getinfo)
</dt> <dt>

[ITfLangBarItem:: GetStatus](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritem-getstatus)
</dt> </dl>

 

 





