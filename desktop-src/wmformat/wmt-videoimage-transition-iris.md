---
title: WMT_VIDEOIMAGE_TRANSITION_IRIS (Wmsdkidl. h)
description: A transição íris revela a nova imagem ao longo de um eixo x e um eixo y. O efeito visual dessa transição é que a nova imagem aparece em um alcance cruzado ampliando para todos os lados do quadro.
ms.assetid: 7390d959-a566-43e7-937d-1e617bc98a6e
keywords:
- WMT_VIDEOIMAGE_TRANSITION_IRIS o formato Windows Media
topic_type:
- apiref
api_name:
- WMT_VIDEOIMAGE_TRANSITION_IRIS
api_location:
- wmsdkidl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 919af0b15ef8a7437c9852df3ff12623553cdabf
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122472962"
---
# <a name="wmt_videoimage_transition_iris"></a>\_íris de \_ transição WMT VIDEOIMAGE \_

A transição íris revela a nova imagem ao longo de um eixo x e um eixo y. O efeito visual dessa transição é que a nova imagem aparece em um alcance cruzado ampliando para todos os lados do quadro.

## <a name="parameters"></a>Parâmetros

A tabela a seguir descreve os parâmetros usados por essa transição e lista os membros da estrutura [**WMT \_ VIDEOIMAGE \_ SAMPLE2**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) à qual eles são atribuídos.




| Parâmetro | Membro da estrutura | Descrição | 
|-----------|------------------|-------------|
| X central | <strong>fEffectPara0</strong> | Coordenada X, em relação ao quadro de vídeo, do centro do efeito de íris. | 
| Y central | <strong>fEffectPara1</strong> | Coordenada Y, em relação ao quadro de vídeo, do centro do efeito de íris. | 
| Largura | <strong>fEffectPara2</strong> | Largura da linha vertical que revela a nova imagem, em pixels. | 
| Altura | <strong>fEffectPara3</strong> | Altura da linha horizontal que revela a nova imagem, em pixels. | 
| Composição | <strong>fEffectPara4</strong> | Defina como um dos seguintes valores:<ul><li>0-especifica a composição normal, na qual a imagem anterior é o plano de fundo e a imagem atual é o primeiro plano.</li><li>1-especifica a composição revertida, na qual a imagem atual é a imagem de plano de fundo e a imagem anterior é o primeiro plano</li></ul> | 




 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Wmsdkidl. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Transições de imagem de vídeo**](video-image-transitions.md)
</dt> </dl>

 

 





