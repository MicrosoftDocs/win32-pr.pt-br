---
title: WMT_VIDEOIMAGE_TRANSITION_FILLED_V (Wmsdkidl.h)
description: A transição V preenchida revela a nova imagem em um triângulo originado de um lado do quadro.
ms.assetid: d256178f-cb1d-4d36-9d30-e6dd6b3b23ec
keywords:
- WMT_VIDEOIMAGE_TRANSITION_FILLED_V formato de mídia do Windows
topic_type:
- apiref
api_name:
- WMT_VIDEOIMAGE_TRANSITION_FILLED_V
api_location:
- wmsdkidl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cfbf032700959dd21a560b879357de2800ac657b
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122466153"
---
# <a name="wmt_videoimage_transition_filled_v"></a>WMT \_ VIDEOIMAGE \_ TRANSITION PREENCHIDO \_ \_ V

A transição V preenchida revela a nova imagem em um triângulo originado de um lado do quadro.

## <a name="parameters"></a>Parâmetros

A tabela a seguir descreve os parâmetros usados por essa transição e lista os membros da estrutura [**WMT \_ VIDEOIMAGE \_ SAMPLE2**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) à qual eles são atribuídos.




| Parâmetro | Membro da estrutura | Descrição | 
|-----------|------------------|-------------|
| Largura | <strong>fEffectPara0</strong> | Largura do V preenchido em pixels. | 
| Altura | <strong>fEffectPara1</strong> | Altura do V preenchido em pixels. | 
| Direção | <strong>fEffectPara2</strong> | Direção da qual o V preenchido se origina. De acordo com um dos seguintes valores:<br /><ul><li>0 – Entra do lado esquerdo do quadro.</li><li>1 - Entra do lado direito do quadro.</li><li>2 – Entra na parte inferior do quadro.</li><li>3 – Entra na parte superior do quadro.</li></ul> | 
| Composição | <strong>fEffectPara3</strong> | De acordo com um dos seguintes valores:<ul><li>0 – Especifica a composição normal, na qual a imagem anterior é a plano de fundo e a imagem atual é o primeiro plano.</li><li>1 - Especifica a composição invertida, na qual a imagem atual é a imagem de plano de fundo e a imagem anterior é o primeiro plano</li></ul> | 




 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Wmsdkidl.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Transições de imagem de vídeo**](video-image-transitions.md)
</dt> </dl>

 

 





