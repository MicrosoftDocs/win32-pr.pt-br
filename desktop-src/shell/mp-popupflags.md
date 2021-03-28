---
description: Representam opções disponíveis ao exibir um menu pop-up.
title: Constantes de MP_POPUPFLAGS (shobjidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: cc1d9ff0-a03b-4bd3-b481-9b78d20eb771
api_name:
- MPPF_SETFOCUS
- MPPF_INITIALSELECT
- MPPF_NOANIMATE
- MPPF_KEYBOARD
- MPPF_REPOSITION
- MPPF_FORCEZORDER
- MPPF_FINALSELECT
- MPPF_ALIGN_LEFT
- MPPF_ALIGN_RIGHT
- MPPF_TOP
- MPPF_LEFT
- MPPF_RIGHT
- MPPF_BOTTOM
- MPPF_POS_MASK
api_type:
- HeaderDef
api_location:
- Shobjidl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 5d49f848df7749a732e9f0b849d44a9be56a5c3e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090838"
---
# <a name="mp_popupflags-constants"></a>\_Constantes POPUPFLAGS MP

Representam opções disponíveis ao exibir um menu pop-up.



| Constante/valor                                                                                                                                                                                                                               | Description                                                                                                                                                                                                                                                              |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MPPF_SETFOCUS"></span><span id="mppf_setfocus"></span><dl> <dt>**MPPF \_ SETFOCUS**</dt> <dt>0x00000001</dt> </dl>                | Dê o foco ao menu pop-up.<br/>                                                                                                                                                                                                                               |
| <span id="MPPF_INITIALSELECT"></span><span id="mppf_initialselect"></span><dl> <dt>**MPPF \_ INITIALSELECT**</dt> <dt>0x00000002</dt> </dl> | Selecione o primeiro item no menu pop-up.<br/>                                                                                                                                                                                                                     |
| <span id="MPPF_NOANIMATE"></span><span id="mppf_noanimate"></span><dl> <dt>**MPPF \_ Noanimate**</dt> <dt>0x00000004</dt> </dl>             | Não use as animações padrão do sistema, por exemplo, fade-in, ao exibir o menu.<br/>                                                                                                                                                                     |
| <span id="MPPF_KEYBOARD"></span><span id="mppf_keyboard"></span><dl> <dt>**MPPF \_ TECLADO**</dt> <dt>0x00000010</dt> </dl>                | Ative o menu por um atalho de teclado.<br/>                                                                                                                                                                                                                     |
| <span id="MPPF_REPOSITION"></span><span id="mppf_reposition"></span><dl> <dt>**MPPF \_ Reposicionar**</dt> <dt>0x00000020</dt> </dl>          | Exiba a barra em uma posição diferente, com base nas alterações feitas no menu.<br/>                                                                                                                                                                                        |
| <span id="MPPF_FORCEZORDER"></span><span id="mppf_forcezorder"></span><dl> <dt>**MPPF \_ FORCEZORDER**</dt> <dt>0x00000040</dt> </dl>       | Reservado. Não use.<br/>                                                                                                                                                                                                                                         |
| <span id="MPPF_FINALSELECT"></span><span id="mppf_finalselect"></span><dl> <dt>**MPPF \_ FINALSELECT**</dt> <dt>0x00000080</dt> </dl>       | Selecione o último item no menu.<br/>                                                                                                                                                                                                                             |
| <span id="MPPF_ALIGN_LEFT"></span><span id="mppf_align_left"></span><dl> <dt>**MPPF \_ ALINHAr 0x02000000 \_ à esquerda**</dt> <dt></dt> </dl>         | **Windows Vista ou posterior**: Alinhe o menu pop-up à esquerda da área especificada no parâmetro *prcExclude* de [**ITrackShellMenu::P opup**](/windows/desktop/api/Shdeprecated/nf-shdeprecated-itrackshellmenu-popup) ou [**IMenuPopup::P opup**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-imenupopup-popup). Esse é o alinhamento padrão.<br/> |
| <span id="MPPF_ALIGN_RIGHT"></span><span id="mppf_align_right"></span><dl> <dt>**MPPF \_ ALINHAr 0x04000000 \_ à direita**</dt> <dt></dt> </dl>      | **Windows Vista ou posterior**: Alinhe o menu pop-up à direita da área especificada no parâmetro *prcExclude* de [**ITrackShellMenu::P opup**](/windows/desktop/api/Shdeprecated/nf-shdeprecated-itrackshellmenu-popup) ou [**IMenuPopup::P opup**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-imenupopup-popup).<br/>                               |
| <span id="MPPF_TOP"></span><span id="mppf_top"></span><dl> <dt>**MPPF \_**</dt> <dt>0x20000000</dt> superior </dl>                               | Posicione o menu pop-up acima do ponto inicial especificado no parâmetro *ppt* de [**ITrackShellMenu::P opup**](/windows/desktop/api/Shdeprecated/nf-shdeprecated-itrackshellmenu-popup) ou [**IMenuPopup::P opup**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-imenupopup-popup).<br/>                                                                |
| <span id="MPPF_LEFT"></span><span id="mppf_left"></span><dl> <dt>**MPPF \_**</dt> <dt>0x40000000</dt> esquerdo </dl>                            | Posicione o menu pop-up à esquerda do ponto inicial.<br/>                                                                                                                                                                                                    |
| <span id="MPPF_RIGHT"></span><span id="mppf_right"></span><dl> <dt>**MPPF \_ 0x60000000 à direita**</dt> <dt></dt> </dl>                         | Posicione o menu pop-up à direita do ponto inicial.<br/>                                                                                                                                                                                                   |
| <span id="MPPF_BOTTOM"></span><span id="mppf_bottom"></span><dl> <dt>**MPPF \_ INFERIOR**</dt> <dt>(int) 0x80000000</dt> </dl>                 | Posicione o menu pop-up abaixo do ponto inicial.<br/>                                                                                                                                                                                                             |
| <span id="MPPF_POS_MASK"></span><span id="mppf_pos_mask"></span><dl> <dt>**MPPF \_ \_Máscara do PDV**</dt> <dt>(int) 0xE0000000</dt> </dl>          | A máscara de posição do menu.<br/>                                                                                                                                                                                                                                       |



## <a name="remarks"></a>Comentários

Essas constantes são definidas no arquivo ShObjIdl. h a partir do Windows XP Service Pack 1 (SP1) e do Windows Server 2003

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows XP com SP1\]<br/>                                    |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                    |
| parâmetro<br/>                   | <dl> <dt>ShObjIdl. h</dt> </dl>   |
| INSERI<br/>                      | <dl> <dt>ShObjIdl. idl</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**IMenuPopup::P opup**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-imenupopup-popup)
</dt> <dt>

[**ITrackShellMenu::P opup**](/windows/desktop/api/Shdeprecated/nf-shdeprecated-itrackshellmenu-popup)
</dt> </dl>

 

 




