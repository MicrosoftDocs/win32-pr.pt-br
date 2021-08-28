---
title: WMT_VIDEOIMAGE_TRANSITION_REVEAL (Wmsdkidl.h)
description: A transição de revelação revela a nova imagem ao longo de uma linha reta originada de um lado do quadro.
ms.assetid: 75ff6155-6b28-474a-b5d1-c3f1b3873b8e
keywords:
- WMT_VIDEOIMAGE_TRANSITION_REVEAL formato de mídia do Windows
topic_type:
- apiref
api_name:
- WMT_VIDEOIMAGE_TRANSITION_REVEAL
api_location:
- wmsdkidl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 140271d365d9673c948c4ff6f540e9bef33e8006
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122469313"
---
# <a name="wmt_videoimage_transition_reveal"></a>REVELAÇÃO DA TRANSIÇÃO DO WMT \_ \_ \_ VIDEOIMAGE

A transição de revelação revela a nova imagem ao longo de uma linha reta originada de um lado do quadro.

## <a name="parameters"></a>Parâmetros

A tabela a seguir descreve os parâmetros usados por essa transição e lista os membros da estrutura [**WMT \_ VIDEOIMAGE \_ SAMPLE2**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) à qual eles são atribuídos.




| Parâmetro | Membro da estrutura | Descrição | 
|-----------|------------------|-------------|
| Distância | <strong>fEffectPara0</strong> | Quantidade da nova imagem revelada, em pixels. Esse valor é relativo ao lado de origem do quadro. | 
| Direção | <strong>fEffectPara1</strong> | Direção da revelação. De acordo com um dos seguintes valores:<br /><ul><li>0 – Revelar à direita; originam-se do lado esquerdo do quadro.</li><li>1 - Revelar à esquerda; originam-se do lado direito do quadro.</li><li>2 - Revelar para cima; originam-se da parte inferior do quadro.</li><li>3 - Revelar para baixo; originam-se da parte superior do quadro.</li></ul> | 
| Composição | <strong>fEffectPara2</strong> | De acordo com um dos seguintes valores:<ul><li>0 – Especifica a composição normal, na qual a imagem anterior é a plano de fundo e a imagem atual é o primeiro plano.</li><li>1 - Especifica a composição invertida, na qual a imagem atual é a imagem de plano de fundo e a imagem anterior é o primeiro plano</li></ul> | 




 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Wmsdkidl.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Transições de imagem de vídeo**](video-image-transitions.md)
</dt> </dl>

 

 





