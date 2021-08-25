---
title: WMT_VIDEOIMAGE_TRANSITION_STAR (Wmsdkidl. h)
description: A transição de estrela revela a nova imagem em uma estrela de cinco pontas dentro do quadro.
ms.assetid: d16f73ce-0fa8-47b4-8146-32f276e6d16c
keywords:
- WMT_VIDEOIMAGE_TRANSITION_STAR o formato Windows Media
topic_type:
- apiref
api_name:
- WMT_VIDEOIMAGE_TRANSITION_STAR
api_location:
- wmsdkidl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7524e51908f7d941aa04b138cc67ba6c4ab6a2a8
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122479492"
---
# <a name="wmt_videoimage_transition_star"></a>\_estrela de \_ transição WMT VIDEOIMAGE \_

A transição de estrela revela a nova imagem em uma estrela de cinco pontas dentro do quadro.

## <a name="parameters"></a>Parâmetros

A tabela a seguir descreve os parâmetros usados por essa transição e lista os membros da estrutura [**WMT \_ VIDEOIMAGE \_ SAMPLE2**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) à qual eles são atribuídos.




| Parâmetro | Membro da estrutura | Descrição | 
|-----------|------------------|-------------|
| X central | <strong>fEffectPara0</strong> | Coordenada X, em relação ao quadro de vídeo, do centro da estrela. | 
| Y central | <strong>fEffectPara1</strong> | Coordenada Y, em relação ao quadro de vídeo, do centro da estrela. | 
| Raio | <strong>fEffectPara2</strong> | Raio, em pixels, do círculo definido pelos pontos da estrela. | 
| Composição | <strong>fEffectPara3</strong> | Defina como um dos seguintes valores:<ul><li>0-especifica a composição normal, na qual a imagem anterior é o plano de fundo e a imagem atual é o primeiro plano.</li><li>1-especifica a composição invertida, na qual a imagem atual é a imagem de plano de fundo, e a imagem anterior é o primeiro plano.</li></ul> | 




 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Wmsdkidl. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Transições de imagem de vídeo**](video-image-transitions.md)
</dt> </dl>

 

 





