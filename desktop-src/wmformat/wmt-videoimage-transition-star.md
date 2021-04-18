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
ms.openlocfilehash: af064682c4488153823164433bd432a9080336fd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105811678"
---
# <a name="wmt_videoimage_transition_star"></a>\_estrela de \_ transição WMT VIDEOIMAGE \_

A transição de estrela revela a nova imagem em uma estrela de cinco pontas dentro do quadro.

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
<td>Coordenada X, em relação ao quadro de vídeo, do centro da estrela.</td>
</tr>
<tr class="even">
<td>Y central</td>
<td><strong>fEffectPara1</strong></td>
<td>Coordenada Y, em relação ao quadro de vídeo, do centro da estrela.</td>
</tr>
<tr class="odd">
<td>Raio</td>
<td><strong>fEffectPara2</strong></td>
<td>Raio, em pixels, do círculo definido pelos pontos da estrela.</td>
</tr>
<tr class="even">
<td>Composição</td>
<td><strong>fEffectPara3</strong></td>
<td>Defina como um dos seguintes valores:
<ul>
<li>0-especifica a composição normal, na qual a imagem anterior é o plano de fundo e a imagem atual é o primeiro plano.</li>
<li>1-especifica a composição invertida, na qual a imagem atual é a imagem de plano de fundo, e a imagem anterior é o primeiro plano.</li>
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

 

 





