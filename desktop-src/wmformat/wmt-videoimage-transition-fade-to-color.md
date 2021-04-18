---
title: WMT_VIDEOIMAGE_TRANSITION_FADE_TO_COLOR (Wmsdkidl. h)
description: A transição de fade-to-Color elimina da imagem até um quadro de cor sólida.
ms.assetid: 4ec52682-1ca2-436d-b7ce-2a9d407ff50e
keywords:
- WMT_VIDEOIMAGE_TRANSITION_FADE_TO_COLOR o formato Windows Media
topic_type:
- apiref
api_name:
- WMT_VIDEOIMAGE_TRANSITION_FADE_TO_COLOR
api_location:
- wmsdkidl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a3873a24cee74e8cad3f6cd91d39f20a72ffa8b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105761140"
---
# <a name="wmt_videoimage_transition_fade_to_color"></a>WMT \_ \_ transição \_ de VIDEOIMAGE esmaecer \_ para \_ cor

A transição de fade-to-Color elimina da imagem até um quadro de cor sólida.

## <a name="parameters"></a>Parâmetros

A tabela a seguir descreve os parâmetros usados por essa transição e lista os membros da estrutura [**WMT \_ VIDEOIMAGE \_ SAMPLE2**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) à qual eles são atribuídos.



| Parâmetro         | Membro da estrutura | Descrição                                                                                                                                                                                                               |
|-------------------|------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Vermelho               | **fEffectPara0** | Valor vermelho da cor do plano de fundo. Defina como um número entre 0 e 255.                                                                                                                                                     |
| Verde             | **fEffectPara1** | Valor verde da cor do plano de fundo. Defina como um número entre 0 e 255.                                                                                                                                                   |
| Azul              | **fEffectPara2** | Valor azul da cor do plano de fundo. Defina como um número entre 0 e 255.                                                                                                                                                    |
| Peso do plano de fundo | **fEffectPara3** | Peso da cor do plano de fundo. Esse parâmetro expressa a porcentagem da cor do plano de fundo na combinação como um decimal. Por exemplo, para misturar a cor do plano de fundo em 30%, tornando a imagem 70% da combinação, defina como 0,30. |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Wmsdkidl. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Transições de imagem de vídeo**](video-image-transitions.md)
</dt> </dl>

 

 





