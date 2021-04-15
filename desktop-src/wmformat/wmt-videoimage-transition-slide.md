---
title: WMT_VIDEOIMAGE_TRANSITION_SLIDE (Wmsdkidl. h)
description: A transição de slides revela a nova imagem deslizando a imagem antiga para fora do quadro.
ms.assetid: 925bcf92-5608-48ca-9bdc-dd08bcd8b8d5
keywords:
- WMT_VIDEOIMAGE_TRANSITION_SLIDE o formato Windows Media
topic_type:
- apiref
api_name:
- WMT_VIDEOIMAGE_TRANSITION_SLIDE
api_location:
- wmsdkidl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 26caaadc268e823734c2bcf4a7899e6bb5399192
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105747632"
---
# <a name="wmt_videoimage_transition_slide"></a>SLIDE de transição do WMT \_ VIDEOIMAGE \_ \_

A transição de slides revela a nova imagem deslizando a imagem antiga para fora do quadro.

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
<td>Distância</td>
<td><strong>fEffectPara0</strong></td>
<td>Distância, em pixels, que a imagem antiga desliza para fora do quadro.</td>
</tr>
<tr class="even">
<td>Direção</td>
<td><strong>fEffectPara1</strong></td>
<td>Direção na qual os slides da imagem antiga. Defina como um dos seguintes valores:<br/>
<ul>
<li>0 – deslize para a direita.</li>
<li>1-slide à esquerda.</li>
<li>2-Deslize para cima.</li>
<li>3-deslizar para baixo.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Composição</td>
<td><strong>fEffectPara2</strong></td>
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

 

 





