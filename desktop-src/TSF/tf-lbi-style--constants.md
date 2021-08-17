---
title: TF_LBI_STYLE_ constantes (Ctfutb.h)
description: As constantes TF LBI STYLE \ são usadas no membro dwStyle da estrutura \_ \_ \_ TF LANGBARITEMINFO para especificar o estilo de um item de \_ barra de idiomas.
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
ms.openlocfilehash: 9954c416d9ad28f0ba0b2ddd6853b125039bf4db24adb3b3ff41f8722b2ba494
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117950791"
---
# <a name="tf_lbi_style_-constants"></a>Constantes \_ de ESTILO LBI \_ de \_ \* TF

As **\_ constantes TF LBI STYLE _ são usadas no \_ membro \_ \* *_* dwStyle** da estrutura [TF \_ LANGBARITEMINFO](/windows/desktop/api/Ctfutb/ns-ctfutb-tf_langbariteminfo) para especificar o estilo de um item de barra de idiomas.

Se esse estilo for combinado com tF \_ LBI \_ STYLE \_ BTN BUTTON, uma seta para baixo será exibida para o item além \_ do texto. A seta para baixo funciona como o botão de menu e clicar nele fará com que **ITfLangBarItemButton::InitMenu** seja chamado. Clicar na parte de texto do botão fará com que **ITfLangBarItemButton::OnClick** seja chamado.



| Constante/valor                                                                                                                                                                                                                                                                           | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TF_LBI_STYLE_HIDDENSTATUSCONTROL"></span><span id="tf_lbi_style_hiddenstatuscontrol"></span><dl> <dt>**TF \_ ESTILO LBI \_ \_ HIDDENSTATUSCONTROL**</dt> <dt>0x00000001</dt> </dl> | O item pode ser oculto ou mostrado dinamicamente usando o valor TF LBI STATUS HIDDEN no \_ \_ método \_ [ITfLangBarItem::GetStatus.](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritem-getstatus) Se esse valor não estiver presente, o item não poderá ser ocultado dessa maneira.<br/>                                                                                                                                                                                                                                                                         |
| <span id="TF_LBI_STYLE_SHOWNINTRAY"></span><span id="tf_lbi_style_shownintray"></span><dl> <dt>**TF \_ ESTILO LBI \_ \_ SHOWNINTRAY**</dt> <dt>0x00000002</dt> </dl>                         | O item será exibido na bandeja do ícone de notificação, além da barra de idiomas. Atualmente, não há suporte para esse sinalizador.<br/>                                                                                                                                                                                                                                                                                                                                                                              |
| <span id="TF_LBI_STYLE_HIDEONNOOTHERITEMS"></span><span id="tf_lbi_style_hideonnootheritems"></span><dl> <dt>**TF \_ \_ \_ HIDEONNOOTHERITEMS**</dt> DE ESTILO LBI <dt>0x00000004</dt> </dl>    | A barra de idiomas será oculta se todos os itens na barra de idiomas contêm esse estilo. Se algum item na barra de idiomas não contém esse estilo, a barra de idiomas é exibida.<br/>                                                                                                                                                                                                                                                                                                                                  |
| <span id="TF_LBI_STYLE_SHOWNINTRAYONLY"></span><span id="tf_lbi_style_shownintrayonly"></span><dl> <dt>**TF \_ ESTILO LBI \_ \_ SHOWNINTRAYONLY**</dt> <dt>0X00000008</dt> </dl>             | O item só será exibido na bandeja do ícone de notificação e não na barra de idiomas. Atualmente, não há suporte para esse sinalizador.<br/>                                                                                                                                                                                                                                                                                                                                                                             |
| <span id="TF_LBI_STYLE_HIDDENBYDEFAULT"></span><span id="tf_lbi_style_hiddenbydefault"></span><dl> <dt>**TF \_ ESTILO LBI \_ \_ HIDDENBYDEFAULT**</dt> <dt>0X00000010</dt> </dl>             | O item não é exibido na barra de ferramentas até que ele seja selecionado no menu de opções da barra de idiomas. Esse sinalizador será ignorado se o TF \_ LBI STYLE HIDDENSTATUSCONTROL estiver definido ou se o usuário já tiver alterado o estado oculto/mostrado usando o menu de opções \_ \_ da barra de idiomas.<br/>                                                                                                                                                                                                                                         |
| <span id="TF_LBI_STYLE_TEXTCOLORICON"></span><span id="tf_lbi_style_textcoloricon"></span><dl> <dt>**TF \_ TEXTO DE \_ ESTILO \_ LBICOLORICON**</dt> <dt>0x00000020</dt> </dl>                   | Qualquer pixel preto dentro do ícone será convertido na cor do texto do tema selecionado. O ícone deve ser monocromático.<br/>                                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="TF_LBI_STYLE_BTN_BUTTON"></span><span id="tf_lbi_style_btn_button"></span><dl> <dt>**TF \_ BOTÃO \_ \_ BTN \_ DE ESTILO LBI**</dt> <dt>0X00010000</dt> </dl>                           | O item é um botão de push. [ITfLangBarItemButton::OnClick](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritembutton-onclick) é chamado quando o item é pressionado.<br/>                                                                                                                                                                                                                                                                                                                                                                             |
| <span id="TF_LBI_STYLE_BTN_MENU"></span><span id="tf_lbi_style_btn_menu"></span><dl> <dt>**TF \_ MENU \_ \_ BTN \_ ESTILO LBI**</dt> <dt>0x00020000</dt> </dl>                                 | O item é um menu. [ITfLangBarItemButton::InitMenu](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritembutton-initmenu) é chamado quando o item é pressionado.<br/> Se esse estilo for combinado com tF \_ LBI \_ STYLE \_ BTN BUTTON, uma seta para baixo será exibida para o item além \_ do texto. A seta para baixo funciona como o botão de menu e clicar nele fará com que **ITfLangBarItemButton::InitMenu** seja chamado. Clicar na parte de texto do botão fará com que **ITfLangBarItemButton::OnClick** seja chamado.<br/> |
| <span id="TF_LBI_STYLE_BTN_TOGGLE"></span><span id="tf_lbi_style_btn_toggle"></span><dl> <dt>**TF \_ ALTERNÂNCIA \_ \_ DE ALTERNÂNCIA DE ESTILO \_ LBI BTN**</dt> <dt>0X00040000</dt> </dl>                           | O item é um botão de alternância e opera semelhante a uma caixa de seleção. **ITfLangBarItemButton::OnClick** é chamado quando o item é pressionado.<br/>                                                                                                                                                                                                                                                                                                                                                                       |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 2000 Professional \[somente aplicativos da área de trabalho\]<br/>                            |
| Servidor mínimo com suporte<br/> | Windows 2000 Server \[somente aplicativos da área de trabalho\]<br/>                                  |
| Redistribuível<br/>          | TSF 1.0 no Windows 2000 Professional<br/>                                       |
| Cabeçalho<br/>                   | <dl> <dt>Ctfutb.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Ctfutb.idl</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[TF \_ LANGBARITEMINFO](/windows/desktop/api/Ctfutb/ns-ctfutb-tf_langbariteminfo)
</dt> <dt>

[ITfLangBarItem::GetInfo](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritem-getinfo)
</dt> <dt>

[ITfLangBarItem::GetStatus](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritem-getstatus)
</dt> </dl>

 

 





