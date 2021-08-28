---
title: WMT_VIDEOIMAGE_TRANSITION_PAGE_ROLL (Wmsdkidl.h)
description: A transição de rolagem de página transforma a imagem antiga com um efeito de invertência de página, revelando a nova imagem abaixo.
ms.assetid: 50efa4e9-0d3a-4b85-96b0-6d5cd637ca98
keywords:
- WMT_VIDEOIMAGE_TRANSITION_PAGE_ROLL formato de mídia do Windows
topic_type:
- apiref
api_name:
- WMT_VIDEOIMAGE_TRANSITION_PAGE_ROLL
api_location:
- wmsdkidl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0bfa69988f5b5414eac3e27b3371bca0e0a28810
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122474972"
---
# <a name="wmt_videoimage_transition_page_roll"></a>ROLL DE PÁGINA DE TRANSIÇÃO DO WMT \_ VIDEOIMAGE \_ \_ \_

A transição de rolagem de página transforma a imagem antiga com um efeito de invertência de página, revelando a nova imagem abaixo.

## <a name="parameters"></a>Parâmetros

A tabela a seguir descreve os parâmetros usados por essa transição e lista os membros da estrutura [**WMT \_ VIDEOIMAGE \_ SAMPLE2**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) à qual eles são atribuídos.




| Parâmetro | Membro da estrutura | Descrição | 
|-----------|------------------|-------------|
| Raio | <strong>fEffectPara0</strong> | Raio do roll no efeito de rolagem de página. | 
| Distância | <strong>fEffectPara1</strong> | Quantidade da nova imagem que é revelada pelo efeito de rolagem de página, em pixels. | 
| Direção | <strong>fEffectPara2</strong> | Canto ou lado do quadro de vídeo, do qual o roll de página se origina. De acordo com um dos seguintes valores:<br /><ul><li>0 – Lado esquerdo</li><li>1 – Lado direito</li><li>2 – Inferior</li><li>3 – Superior</li><li>4 – Canto inferior esquerdo</li><li>5 – Canto inferior direito</li><li>6 – Canto superior esquerdo</li><li>7 – Canto superior direito</li></ul> | 
| Composição | <strong>fEffectPara3</strong> | De acordo com um dos seguintes valores:<ul><li>0 – Especifica a composição normal, na qual a imagem anterior é a plano de fundo e a imagem atual é o primeiro plano.</li><li>1 - Especifica a composição invertida, na qual a imagem atual é a imagem de plano de fundo e a imagem anterior é o primeiro plano</li></ul> | 




 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Wmsdkidl.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Transições de imagem de vídeo**](video-image-transitions.md)
</dt> </dl>

 

 





