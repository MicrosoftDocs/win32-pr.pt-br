---
title: WMT_VIDEOIMAGE_TRANSITION_WHEEL (Wmsdkidl.h)
description: A transição de roda revela a nova imagem girando quatro linhas em torno de um ponto de pivô comum, como os spokes de uma roda.
ms.assetid: 426217be-789b-4b78-b0ea-de9629ecd46c
keywords:
- WMT_VIDEOIMAGE_TRANSITION_WHEEL formato de mídia do Windows
topic_type:
- apiref
api_name:
- WMT_VIDEOIMAGE_TRANSITION_WHEEL
api_location:
- wmsdkidl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8b77e8640f21bd06194b2fe6b1e7048d85b323e
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122469263"
---
# <a name="wmt_videoimage_transition_wheel"></a>RODA DE TRANSIÇÃO DO WMT \_ VIDEOIMAGE \_ \_

A transição de roda revela a nova imagem girando quatro linhas em torno de um ponto de pivô comum, como os spokes de uma roda.

## <a name="parameters"></a>Parâmetros

A tabela a seguir descreve os parâmetros usados por essa transição e lista os membros da estrutura [**WMT \_ VIDEOIMAGE \_ SAMPLE2**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) à qual eles são atribuídos.




| Parâmetro | Membro da estrutura | Descrição | 
|-----------|------------------|-------------|
| X central | <strong>fEffectPara0</strong> | Coordenada X, relativa ao quadro de vídeo, do centro do efeito de roda. | 
| Y central | <strong>fEffectPara1</strong> | Coordenada Y, em relação ao quadro de vídeo, do centro do efeito da roda. | 
| Ângulo | <strong>fEffectPara2</strong> | Ângulo de rotação, em graus, dos spokes do efeito de roda. Um valor de 0,0 indica a imagem antiga sem nenhuma das novas imagens reveladas. Um valor de 90,0 indica que a nova imagem foi totalmente revelada. A movimentação de 0,0 para 90,0 aparece como rotação no sentido horário dos spokes.<br /> | 
| Composição | <strong>fEffectPara3</strong> | De acordo com um dos seguintes valores:<ul><li>0 – Especifica a composição normal, na qual a imagem anterior é a plano de fundo e a imagem atual é o primeiro plano.</li><li>1 - Especifica a composição invertida, na qual a imagem atual é a imagem de plano de fundo e a imagem anterior é o primeiro plano</li></ul> | 




 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Wmsdkidl.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Transições de imagem de vídeo**](video-image-transitions.md)
</dt> </dl>

 

 





