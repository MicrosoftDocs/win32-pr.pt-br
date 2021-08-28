---
title: WMT_VIDEOIMAGE_TRANSITION_SLIDE (Wmsdkidl.h)
description: A transição de slides revela a nova imagem deslizando a imagem antiga para fora do quadro.
ms.assetid: 925bcf92-5608-48ca-9bdc-dd08bcd8b8d5
keywords:
- WMT_VIDEOIMAGE_TRANSITION_SLIDE formato de mídia do Windows
topic_type:
- apiref
api_name:
- WMT_VIDEOIMAGE_TRANSITION_SLIDE
api_location:
- wmsdkidl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9866706528cab038042adc8d098743ce6588c805
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122476332"
---
# <a name="wmt_videoimage_transition_slide"></a>SLIDE DE TRANSIÇÃO DO WMT \_ VIDEOIMAGE \_ \_

A transição de slides revela a nova imagem deslizando a imagem antiga para fora do quadro.

## <a name="parameters"></a>Parâmetros

A tabela a seguir descreve os parâmetros usados por essa transição e lista os membros da estrutura [**WMT \_ VIDEOIMAGE \_ SAMPLE2**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) à qual eles são atribuídos.




| Parâmetro | Membro da estrutura | Descrição | 
|-----------|------------------|-------------|
| Distância | <strong>fEffectPara0</strong> | Distância, em pixels, que a imagem antiga desliza para fora do quadro. | 
| Direção | <strong>fEffectPara1</strong> | Direção na qual a imagem antiga desliza. De acordo com um dos seguintes valores:<br /><ul><li>0 – Deslize para a direita.</li><li>1 – Deslize para a esquerda.</li><li>2 – Deslizar para cima.</li><li>3 – Deslizar para baixo.</li></ul> | 
| Composição | <strong>fEffectPara2</strong> | De acordo com um dos seguintes valores:<ul><li>0 – Especifica a composição normal, na qual a imagem anterior é a plano de fundo e a imagem atual é o primeiro plano.</li><li>1 - Especifica a composição invertida, na qual a imagem atual é a imagem de plano de fundo e a imagem anterior é o primeiro plano</li></ul> | 




 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Wmsdkidl.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Transições de imagem de vídeo**](video-image-transitions.md)
</dt> </dl>

 

 





