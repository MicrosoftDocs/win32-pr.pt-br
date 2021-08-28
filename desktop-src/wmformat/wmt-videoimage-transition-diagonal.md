---
title: WMT_VIDEOIMAGE_TRANSITION_DIAGONAL (Wmsdkidl.h)
description: A transição diagonal revela a nova imagem ao longo de uma linha diagonal originada em um canto do quadro.
ms.assetid: 1aaaf9e8-bbb8-4289-948e-5d352798e831
keywords:
- WMT_VIDEOIMAGE_TRANSITION_DIAGONAL formato de mídia do Windows
topic_type:
- apiref
api_name:
- WMT_VIDEOIMAGE_TRANSITION_DIAGONAL
api_location:
- wmsdkidl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ea028777580f7414a834a0aa3e73e18db607eccd
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122471982"
---
# <a name="wmt_videoimage_transition_diagonal"></a>WMT \_ VIDEOIMAGE \_ TRANSITION \_ DIAGONAL

A transição diagonal revela a nova imagem ao longo de uma linha diagonal originada em um canto do quadro.

## <a name="parameters"></a>Parâmetros

A tabela a seguir descreve os parâmetros usados por essa transição e lista os membros da estrutura [**WMT \_ VIDEOIMAGE \_ SAMPLE2**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) à qual eles são atribuídos.




| Parâmetro | Membro da estrutura | Descrição | 
|-----------|------------------|-------------|
| Largura | <strong>fEffectPara0</strong> | Largura da seção diagonal em pixels. | 
| Altura | <strong>fEffectPara1</strong> | Altura da seção diagonal em pixels. | 
| Direção | <strong>fEffectPara2</strong> | Determina o canto do qual a transição se origina. De definido como um dos seguintes:<br /><ul><li>0 – Canto superior direito</li><li>1 – Superior esquerdo</li><li>2 – Inferior direito</li><li>3 – Inferior esquerdo</li></ul> | 
| Composição | <strong>fEffectPara3</strong> | De acordo com um dos seguintes valores:<ul><li>0 – Especifica a composição normal, na qual a imagem anterior é a plano de fundo e a imagem atual é o primeiro plano.</li><li>1 - Especifica a composição invertida, na qual a imagem atual é a imagem de plano de fundo e a imagem anterior é o primeiro plano.</li></ul> | 




 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Wmsdkidl.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Transições de imagem de vídeo**](video-image-transitions.md)
</dt> </dl>

 

 





