---
title: WMT_VIDEOIMAGE_TRANSITION_INSET (Wmsdkidl.h)
description: A transição de inset revela a nova imagem em um retângulo originado de um canto do quadro.
ms.assetid: fd8bc4b7-0546-4897-ab7b-a320bbd126ef
keywords:
- WMT_VIDEOIMAGE_TRANSITION_INSET formato de mídia do Windows
topic_type:
- apiref
api_name:
- WMT_VIDEOIMAGE_TRANSITION_INSET
api_location:
- wmsdkidl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a47d53de99d3c6f6144755934989ca3958d28a23
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122476773"
---
# <a name="wmt_videoimage_transition_inset"></a>INSET DE TRANSIÇÃO DO WMT \_ VIDEOIMAGE \_ \_

A transição de inset revela a nova imagem em um retângulo originado de um canto do quadro.

## <a name="parameters"></a>Parâmetros

A tabela a seguir descreve os parâmetros usados por essa transição e lista os membros da estrutura [**WMT \_ VIDEOIMAGE \_ SAMPLE2**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) à qual eles são atribuídos.




| Parâmetro | Membro da estrutura | Descrição | 
|-----------|------------------|-------------|
| Largura | <strong>fEffectPara0</strong> | Largura do inset em pixels. | 
| Altura | <strong>fEffectPara1</strong> | Altura do inset em pixels. | 
| Direção | <strong>fEffectPara2</strong> | Canto do qual o inset se origina. De acordo com um dos seguintes valores:<br /><ul><li>0 – Inferior esquerdo</li><li>1 - Inferior direito</li><li>2 – Superior esquerdo</li><li>3 – Canto superior direito</li></ul> | 
| Composição | <strong>fEffectPara3</strong> | De acordo com um dos seguintes valores:<ul><li>0 – Especifica a composição normal, na qual a imagem anterior é a plano de fundo e a imagem atual é o primeiro plano.</li><li>1 - Especifica a composição invertida, na qual a imagem atual é a imagem de plano de fundo e a imagem anterior é o primeiro plano</li></ul> | 




 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Wmsdkidl.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Transições de imagem de vídeo**](video-image-transitions.md)
</dt> </dl>

 

 





