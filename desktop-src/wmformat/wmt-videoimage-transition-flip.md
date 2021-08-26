---
title: WMT_VIDEOIMAGE_TRANSITION_FLIP (Wmsdkidl. h)
description: A transição de flip gira a imagem antiga em um eixo y por meio do centro do quadro. A nova imagem é revelada como a parte traseira da imagem antiga.
ms.assetid: ff9990ef-962c-4dbb-b2bc-3bee070d2044
keywords:
- WMT_VIDEOIMAGE_TRANSITION_FLIP o formato Windows Media
topic_type:
- apiref
api_name:
- WMT_VIDEOIMAGE_TRANSITION_FLIP
api_location:
- wmsdkidl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d2a3bfe94e001c6a65256facd5484a015d00f245
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122475752"
---
# <a name="wmt_videoimage_transition_flip"></a>Inverter WMT de \_ \_ transição VIDEOIMAGE \_

A transição de flip gira a imagem antiga em um eixo y por meio do centro do quadro. A nova imagem é revelada como a parte traseira da imagem antiga.

## <a name="parameters"></a>Parâmetros

A tabela a seguir descreve os parâmetros usados por essa transição e lista os membros da estrutura [**WMT \_ VIDEOIMAGE \_ SAMPLE2**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) à qual eles são atribuídos.




| Parâmetro | Membro da estrutura | Descrição | 
|-----------|------------------|-------------|
| Ângulo | <strong>fEffectPara0</strong> | Ângulo da rotação, de 0,0 a 180,0 graus. | 
| Composição | <strong>fEffectPara1</strong> | Defina como um dos seguintes valores:<ul><li>0-especifica a composição normal, na qual a imagem anterior é o plano de fundo e a imagem atual é o primeiro plano.</li><li>1-especifica a composição revertida, na qual a imagem atual é a imagem de plano de fundo e a imagem anterior é o primeiro plano</li></ul> | 




 

## <a name="remarks"></a>Comentários

Você pode visualizar o efeito dessa transição como se ambas as imagens fossem fotos físicas coladas de volta para trás. A transição tem o mesmo efeito que conter duas fotografias no centro da borda inferior e girando-as 180 graus.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Wmsdkidl. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Transições de imagem de vídeo**](video-image-transitions.md)
</dt> </dl>

 

 





