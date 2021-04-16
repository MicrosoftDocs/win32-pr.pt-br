---
title: WMT_VIDEOIMAGE_TRANSITION_WHEEL (Wmsdkidl. h)
description: A transição da roda revela a nova imagem girando quatro linhas em um ponto dinâmico comum, como os spokes de uma roda.
ms.assetid: 426217be-789b-4b78-b0ea-de9629ecd46c
keywords:
- WMT_VIDEOIMAGE_TRANSITION_WHEEL o formato Windows Media
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
ms.openlocfilehash: 42f39d3355cfce3397c379bf7edafaae77ccfafe
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105747666"
---
# <a name="wmt_videoimage_transition_wheel"></a>\_roda de \_ transição WMT VIDEOIMAGE \_

A transição da roda revela a nova imagem girando quatro linhas em um ponto dinâmico comum, como os spokes de uma roda.

## <a name="parameters"></a>Parâmetros

A tabela a seguir descreve os parâmetros usados por essa transição e lista os membros da estrutura [**WMT \_ VIDEOIMAGE \_ SAMPLE2**](/previous-versions/windows/desktop/api/Wmsdkidl/ns-wmsdkidl-wmt_videoimage_sample2) à qual eles são atribuídos.



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Parâmetro</th>
<th>Membro da estrutura</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>X central</td>
<td><strong>fEffectPara0</strong></td>
<td>Coordenada X, em relação ao quadro de vídeo, do centro do efeito de roda.</td>
</tr>
<tr class="even">
<td>Y central</td>
<td><strong>fEffectPara1</strong></td>
<td>Coordenada Y, em relação ao quadro de vídeo, do centro do efeito de roda.</td>
</tr>
<tr class="odd">
<td>Ângulo</td>
<td><strong>fEffectPara2</strong></td>
<td>Ângulo de rotação, em graus, dos spokes do efeito de roda. Um valor de 0,0 indica a imagem antiga sem qualquer uma das novas imagens reveladas. Um valor de 90,0 indica a nova imagem totalmente revelada. A movimentação de 0,0 para 90,0 aparece como rotação horária dos spokes.<br/></td>
</tr>
<tr class="even">
<td>Composição</td>
<td><strong>fEffectPara3</strong></td>
<td>Defina como um dos seguintes valores:
<ul>
<li>0-especifica a composição normal, na qual a imagem anterior é o plano de fundo e a imagem atual é o primeiro plano.</li>
<li>1-especifica a composição revertida, na qual a imagem atual é a imagem de plano de fundo e a imagem anterior é o primeiro plano</li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Wmsdkidl. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Transições de imagem de vídeo**](video-image-transitions.md)
</dt> </dl>

 

 





