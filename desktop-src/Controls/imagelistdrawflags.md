---
title: IMAGELISTDRAWFLAGS (Commctrl.h)
description: Passado para o método IImageList Draw no membro fStyle de IMAGELISTDRAWPARAMS.
ms.assetid: 99fd2cb2-0cb0-40c2-b184-b6d8e54397b4
topic_type:
- apiref
api_name:
- ILD_NORMAL
- ILD_TRANSPARENT
- ILD_BLEND25
- ILD_FOCUS
- ILD_BLEND50
- ILD_SELECTED
- ILD_BLEND
- ILD_MASK
- ILD_IMAGE
- ILD_ROP
- ILD_OVERLAYMASK
- ILD_PRESERVEALPHA
- ILD_SCALE
- ILD_DPISCALE
- ILD_ASYNC
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e44d863e82cf126c62262a564e5bf8366fbe71dbb75cc6d47bd16634d798cfcd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119544536"
---
# <a name="imagelistdrawflags"></a>IMAGELISTDRAWFLAGS

Passado para [**o método IImageList::D raw**](/windows/desktop/api/CommonControls/nf-commoncontrols-iimagelist-draw) no membro **fStyle** de [**IMAGELISTDRAWPARAMS**](/windows/win32/api/commctrl/ns-commctrl-imagelistdrawparams).



| Constante/valor                                                                                                                                                                                                                            | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="ILD_NORMAL"></span><span id="ild_normal"></span><dl> <dt>**ILD \_ NORMAL**</dt> <dt>0x00000000</dt> </dl>                      | Desenha a imagem usando a cor da tela de fundo para a lista de imagens. Se a cor da tela de fundo for o valor CLR \_ NONE, a imagem será desenhada de forma transparente usando a máscara.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span id="ILD_TRANSPARENT"></span><span id="ild_transparent"></span><dl> <dt>**ILD \_ TRANSPARENT**</dt> <dt>0x00000001</dt> </dl>       | Desenha a imagem de forma transparente usando a máscara, independentemente da cor da tela de fundo. Esse valor não terá efeito se a lista de imagens não contém uma máscara.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span id="ILD_BLEND25"></span><span id="ild_blend25"></span><dl> <dt>**ILD \_ BLEND25**</dt> <dt>0x00000002</dt> </dl>                   | Desenha a imagem, combinando 25% com a cor da combinação especificada por **rgbFg.** Esse valor não terá efeito se a lista de imagens não contém uma máscara.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span id="ILD_FOCUS"></span><span id="ild_focus"></span><dl> <dt>**ILD \_ FOCO**</dt> <dt>0x00000002</dt> </dl>                         | O mesmo que **ILD \_ BLEND25**.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="ILD_BLEND50"></span><span id="ild_blend50"></span><dl> <dt>**ILD \_ BLEND50**</dt> <dt>0x00000004</dt> </dl>                   | Desenha a imagem, combinando 50% com a cor da combinação especificada por **rgbFg.** Esse valor não terá efeito se a lista de imagens não contém uma máscara.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span id="ILD_SELECTED"></span><span id="ild_selected"></span><dl> <dt>**ILD \_ SELECTED**</dt> <dt>0x00000004</dt> </dl>                | O mesmo que **ILD \_ BLEND50**.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="ILD_BLEND"></span><span id="ild_blend"></span><dl> <dt>**ILD \_ BLEND**</dt> <dt>0x00000004</dt> </dl>                         | O mesmo que **ILD \_ BLEND50**.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="ILD_MASK"></span><span id="ild_mask"></span><dl> <dt>**ILD \_ MÁSCARA**</dt> <dt>0x00000010</dt> </dl>                            | Desenha a máscara.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span id="ILD_IMAGE"></span><span id="ild_image"></span><dl> <dt>**ILD \_ Imagem**</dt> <dt>0x00000020</dt> </dl>                         | Se a sobreposição não exigir que uma máscara seja desenhada, de definir esse sinalizador.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span id="ILD_ROP"></span><span id="ild_rop"></span><dl> <dt>**ILD \_ RoP**</dt> <dt>0x00000040</dt> </dl>                               | Desenha a imagem usando o código de operação de raster especificado pelo **membro dwRop.**<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span id="ILD_OVERLAYMASK"></span><span id="ild_overlaymask"></span><dl> <dt>**ILD \_ OVERLAYMASK**</dt> <dt>0x00000F00</dt> </dl>       | Para extrair a imagem de sobreposição do membro **fStyle,** use o AND lógico para combinar **fStyle** com o **valor \_ ILD OVERLAYMASK.**<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span id="ILD_PRESERVEALPHA"></span><span id="ild_preservealpha"></span><dl> <dt>**ILD \_ PRESERVEALPHA**</dt> <dt>0x00001000</dt> </dl> | Preserva o canal alfa no destino.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span id="ILD_SCALE"></span><span id="ild_scale"></span><dl> <dt>**ILD \_ DIMENSIONAR**</dt> <dt>0x00002000</dt> </dl>                         | Faz com que a imagem seja dimensionada para cx, cy em vez de ser recortada.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| <span id="ILD_DPISCALE"></span><span id="ild_dpiscale"></span><dl> <dt>**ILD \_ DPISCALE**</dt> <dt>0x00004000</dt> </dl>                | Dimensiona a imagem para o dpi atual da exibição.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| <span id="ILD_ASYNC"></span><span id="ild_async"></span><dl> <dt>**ILD \_ AsYNC**</dt> <dt>0x00008000</dt> </dl>                         | **Windows Vista e posterior.** Desenhe a imagem se ela estiver disponível no cache. Não extraia-o automaticamente. O método draw chamado retorna E PENDING para o componente de chamada, que deve então tomar uma ação alternativa, como fornecer outra imagem e enfilar uma tarefa em segundo plano para forçar a imagem a ser carregada por meio de \_ [**ForceImagePresent**](/windows/desktop/api/Commoncontrols/nf-commoncontrols-iimagelist2-forceimagepresent) usando o sinalizador ILFIP \_ ALWAYS. O sinalizador ASYNC ILD impede que a operação de extração bloquee o thread atual e é especialmente importante se um método de desenho é chamado do thread da interface do \_ usuário.<br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

