---
title: Constantes de TF_LBI_ (Ctfutb. h)
description: As \_ constantes TF bin \_ \ são usadas com o método OnUpdate ITfLangBarItemSink para indicar quais itens da barra de idiomas foram alterados.
ms.assetid: ed84012f-19ba-43b3-bbb5-7373ed174c33
topic_type:
- apiref
api_name:
- TF_LBI_ICON
- TF_LBI_TEXT
- TF_LBI_TOOLTIP
- TF_LBI_BITMAP
- TF_LBI_BALLOON
- TF_LBI_STATUS
- TF_LBI_BMPALL
- TF_LBI_BMPBTNALL
- TF_LBI_BTNALL
api_location:
- Ctfutb.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d72b69f1cb5a5b4a24e78a2bdc1ca0e7a9d79cbf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105760348"
---
# <a name="tf_lbi_-constants"></a>Constantes de TF \_ ICB \_ \*

As constantes ** \_ TF \_ \* bin* _ são usadas com o método [ITfLangBarItemSink:: OnUpdate](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritemsink-onupdate) para indicar quais itens da barra de idiomas foram alterados.



| Constante/valor                                                                                                                                                                                                                                                                  | Descrição                                                                                                                                                                                                                                                                                                         |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TF_LBI_ICON"></span><span id="tf_lbi_icon"></span><dl> <dt>_ * TF \_ Ícone de ICB \_ * *</dt> <dt>0x00000001</dt> </dl>                                                        | O ícone do item foi alterado. A barra de idiomas chama [ITfLangBarItemButton:: GetIcon](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritembutton-geticon) em resposta a essa notificação.<br/>                                                                                                                                             |
| <span id="TF_LBI_TEXT"></span><span id="tf_lbi_text"></span><dl> <dt>**TF \_ \_Texto de ICB**</dt> <dt>0x00000002</dt> </dl>                                                        | O texto de um botão ou item de botão de bitmap foi alterado. A barra de idiomas chama [ITfLangBarItemButton:: gettext](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritembutton-gettext) ou [ITfLangBarItemBitmapButton:: gettext](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritembitmapbutton-gettext), o que for apropriado, em resposta a essa notificação.<br/>           |
| <span id="TF_LBI_TOOLTIP"></span><span id="tf_lbi_tooltip"></span><dl> <dt>**TF \_ \_Dica de ferramenta bin**</dt> <dt>0x00000004</dt> </dl>                                               | O texto da dica de ferramenta do item alterado. A barra de idiomas chama [ITfLangBarItem:: Gettooltipstring](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritem-gettooltipstring) em resposta a esta notificação.<br/>                                                                                                                                   |
| <span id="TF_LBI_BITMAP"></span><span id="tf_lbi_bitmap"></span><dl> <dt>**TF \_ 0x00000008 de \_ bitmap bin**</dt> <dt></dt> </dl>                                                  | O bitmap de um item de botão bitmap ou bitmap foi alterado. A barra de idiomas chama [ITfLangBarItemBitmap::D rawbitmap](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritembitmap-drawbitmap) ou [ITfLangBarItemBitmapButton::D rawbitmap](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritembitmapbutton-drawbitmap), o que for apropriado, em resposta a essa notificação.<br/> |
| <span id="TF_LBI_BALLOON"></span><span id="tf_lbi_balloon"></span><dl> <dt>**TF \_ \_Balão de bin**</dt> <dt>0x00000010</dt> </dl>                                               | As informações de um item de balão foram alteradas. A barra de idiomas chama [ITfLangBarItemBalloon:: GetBalloonInfo](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritemballoon-getballooninfo) em resposta a essa notificação.<br/>                                                                                                                   |
| <span id="TF_LBI_STATUS"></span><span id="tf_lbi_status"></span><dl> <dt>**TF \_ 0x00010000 de \_ status bin**</dt> <dt></dt> </dl>                                                  | O status do item foi alterado. A barra de idiomas chama [ITfLangBarItem:: GetStatus](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritem-getstatus) em resposta a esta notificação.<br/>                                                                                                                                                              |
| <span id="TF_LBI_BMPALL"></span><span id="tf_lbi_bmpall"></span><dl> <dt>**TF \_ \_BMPALL**</dt> de <dt> \_ \_ \| \_ \_ ferramentas de mapa de bitmap</dt> do ICB de TF ICB </dl>                          | Combina o \_ bitmap do TF bin \_ e a \_ dica de ferramenta TF bin \_ .<br/>                                                                                                                                                                                                                                                           |
| <span id="TF_LBI_BMPBTNALL"></span><span id="tf_lbi_bmpbtnall"></span><dl> <dt>**TF \_ BIN \_ BMPBTNALL**</dt> <dt>TF \_ bin \_ bitmap \| TF \_ bin \_ texto \| TF \_ bin \_ dica de ferramenta</dt> </dl> | Combina o \_ bitmap do TF bin \_ , o tf \_ bin \_ Text e o tf \_ bin \_ TOOLTIP.<br/>                                                                                                                                                                                                                                            |
| <span id="TF_LBI_BTNALL"></span><span id="tf_lbi_btnall"></span><dl> <dt>**TF \_ BIN \_ BTNALL**</dt> <dt>TF \_ \_ Icon ícone \| TF \_ bin \_ texto \| TF \_ bin \_ dica de ferramenta</dt> </dl>            | Combina o \_ ícone TF bin \_ , TF \_ bin \_ Text e TF \_ bin \_ TOOLTIP.<br/>                                                                                                                                                                                                                                              |



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

[ITfLangBarItemSink:: OnUpdate](/windows/desktop/api/Ctfutb/nf-ctfutb-itflangbaritemsink-onupdate)
</dt> </dl>

 

 





