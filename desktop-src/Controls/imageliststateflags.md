---
title: IMAGELISTSTATEFLAGS (commctrl. h)
description: Os sinalizadores a seguir são passados para o método de desenho IImageList no membro fState de IMAGELISTDRAWPARAMS.
ms.assetid: a22b4acf-c290-44b2-9216-b006d0326236
topic_type:
- apiref
api_name:
- ILS_NORMAL
- ILS_GLOW
- ILS_SHADOW
- ILS_SATURATE
- ILS_ALPHA
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fea580294f54b6e2fc5c3e5b6aee1119811c22e8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009203"
---
# <a name="imageliststateflags"></a>IMAGELISTSTATEFLAGS

Os sinalizadores a seguir são passados para o método [**bruto IImageList::D**](/windows/desktop/api/CommonControls/nf-commoncontrols-iimagelist-draw) no membro **fState** de [**IMAGELISTDRAWPARAMS**](/windows/win32/api/commctrl/ns-commctrl-imagelistdrawparams).



| Constante/valor                                                                                                                                                                                                             | Descrição                                                                                                                                                                                                                                                                                                                                                                                   |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="ILS_NORMAL"></span><span id="ils_normal"></span><dl> <dt>**ILS \_ NORMAL**</dt> <dt>0x00000000</dt> </dl>       | O estado da imagem não é modificado.<br/>                                                                                                                                                                                                                                                                                                                                                   |
| <span id="ILS_GLOW"></span><span id="ils_glow"></span><dl> <dt>**ILS \_ BRILHO**</dt> <dt>0x00000001</dt> </dl>             | Não há suporte. <br/>                                                                                                                                                                                                                                                                                                                                                                    |
| <span id="ILS_SHADOW"></span><span id="ils_shadow"></span><dl> <dt>**ILS \_ SOMBRA**</dt> <dt>0x00000002</dt> </dl>       | Não há suporte. <br/>                                                                                                                                                                                                                                                                                                                                                                    |
| <span id="ILS_SATURATE"></span><span id="ils_saturate"></span><dl> <dt>**ILS \_ Saturação**</dt> <dt>0x00000004</dt> </dl> | Reduz a saturação de cor do ícone para escala de cinza. Isso afeta apenas as imagens 32 bpp. <br/>                                                                                                                                                                                                                                                                                            |
| <span id="ILS_ALPHA"></span><span id="ils_alpha"></span><dl> <dt>**ILS \_**</dt> <dt>0x00000008</dt> alfa </dl>          | Alfa mistura o ícone. A mesclagem alfa controla o nível de transparência de um ícone, de acordo com o valor de seu canal alfa. O valor do canal alfa é indicado pelo membro de **quadro** no método [**IMAGELISTDRAWPARAMS**](/windows/win32/api/commctrl/ns-commctrl-imagelistdrawparams) . O canal alfa pode ser de 0 a 255, sendo que 0 é completamente transparente e 255 sendo completamente opaco.<br/> |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2003\]<br/>                                  |
| parâmetro<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

