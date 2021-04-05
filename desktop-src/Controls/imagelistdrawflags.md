---
title: IMAGELISTDRAWFLAGS (commctrl. h)
description: Passado para o método de desenho IImageList no membro fStyle de IMAGELISTDRAWPARAMS.
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
ms.openlocfilehash: 0743fc2778b3ef693646327fe8206ebedcb89e81
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103918274"
---
# <a name="imagelistdrawflags"></a>IMAGELISTDRAWFLAGS

Passado para o método [**bruto IImageList::D**](/windows/desktop/api/CommonControls/nf-commoncontrols-iimagelist-draw) no membro **fStyle** de [**IMAGELISTDRAWPARAMS**](/windows/win32/api/commctrl/ns-commctrl-imagelistdrawparams).



| Constante/valor                                                                                                                                                                                                                            | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="ILD_NORMAL"></span><span id="ild_normal"></span><dl> <dt>**Ilação \_ NORMAL**</dt> <dt>0x00000000</dt> </dl>                      | Desenha a imagem usando a cor do plano de fundo da lista de imagens. Se a cor do plano de fundo for o \_ valor CLR None, a imagem será desenhada de forma transparente usando a máscara.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span id="ILD_TRANSPARENT"></span><span id="ild_transparent"></span><dl> <dt>**Ilação \_**</dt> <dt>0x00000001</dt> transparente </dl>       | Desenha a imagem de forma transparente usando a máscara, independentemente da cor do plano de fundo. Esse valor não tem efeito se a lista de imagens não contiver uma máscara.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span id="ILD_BLEND25"></span><span id="ild_blend25"></span><dl> <dt>**Ilação \_ BLEND25**</dt> <dt>0x00000002</dt> </dl>                   | Desenha a imagem, combinando 25 por cento com a cor de mesclagem especificada por **rgbFg**. Esse valor não tem efeito se a lista de imagens não contiver uma máscara.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span id="ILD_FOCUS"></span><span id="ild_focus"></span><dl> <dt>**Ilação \_ FOCO**</dt> em <dt>0x00000002</dt> </dl>                         | O mesmo que **ilação \_ BLEND25**.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="ILD_BLEND50"></span><span id="ild_blend50"></span><dl> <dt>**Ilação \_ BLEND50**</dt> <dt>0x00000004</dt> </dl>                   | Desenha a imagem, combinando 50 por cento com a cor de mistura especificada por **rgbFg**. Esse valor não tem efeito se a lista de imagens não contiver uma máscara.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span id="ILD_SELECTED"></span><span id="ild_selected"></span><dl> <dt>**Ilação \_**</dt> <dt>0x00000004</dt> selecionado </dl>                | O mesmo que **ilação \_ BLEND50**.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="ILD_BLEND"></span><span id="ild_blend"></span><dl> <dt>**Ilação \_ MISTURAR**</dt> <dt>0x00000004</dt> </dl>                         | O mesmo que **ilação \_ BLEND50**.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="ILD_MASK"></span><span id="ild_mask"></span><dl> <dt>**Ilação \_ MÁSCARA**</dt> <dt>0x00000010</dt> </dl>                            | Desenha a máscara.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span id="ILD_IMAGE"></span><span id="ild_image"></span><dl> <dt>**Ilação \_ IMAGEM**</dt> <dt>0x00000020</dt> </dl>                         | Se a sobreposição não exigir que uma máscara seja desenhada, defina esse sinalizador.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span id="ILD_ROP"></span><span id="ild_rop"></span><dl> <dt>**Ilação \_**</dt> <dt>0X00000040</dt> de ROP </dl>                               | Desenha a imagem usando o código de operação de varredura especificado pelo membro **dwRop** .<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span id="ILD_OVERLAYMASK"></span><span id="ild_overlaymask"></span><dl> <dt>**Ilação \_ OVERLAYMASK**</dt> <dt>0x00000F00</dt> </dl>       | Para extrair a imagem de sobreposição do membro **fStyle** , use a lógica e para combinar **fStyle** com o valor **ilação \_ OVERLAYMASK** .<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span id="ILD_PRESERVEALPHA"></span><span id="ild_preservealpha"></span><dl> <dt>**Ilação \_ PRESERVEALPHA**</dt> <dt>0x00001000</dt> </dl> | Preserva o canal alfa no destino.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span id="ILD_SCALE"></span><span id="ild_scale"></span><dl> <dt>**Ilação \_ DIMENSIONAR**</dt> <dt>0x00002000</dt> </dl>                         | Faz com que a imagem seja dimensionada para CX, Cy em vez de ser recortada.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| <span id="ILD_DPISCALE"></span><span id="ild_dpiscale"></span><dl> <dt>**Ilação \_ DPISCALE**</dt> <dt>0x00004000</dt> </dl>                | Dimensiona a imagem para o DPI atual da exibição.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| <span id="ILD_ASYNC"></span><span id="ild_async"></span><dl> <dt>**Ilação \_ 0x00008000 assíncrona**</dt> <dt></dt> </dl>                         | **Windows Vista e posterior.** Desenhe a imagem se ela estiver disponível no cache. Não a Extraia automaticamente. O método Draw chamado retorna E \_ pendente para o componente de chamada, que deve executar uma ação alternativa, como fornecer outra imagem e enfileirar uma tarefa em segundo plano para forçar a imagem a ser carregada via [**ForceImagePresent**](/windows/desktop/api/Commoncontrols/nf-commoncontrols-iimagelist2-forceimagepresent) usando o \_ sinalizador ILFIP Always. O \_ sinalizador assíncrono ilação impede que a operação de extração bloqueie o thread atual e seja especialmente importante se um método Draw for chamado a partir do thread da interface do usuário.<br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

