---
title: WMT_VIDEOIMAGE_TRANSITION_BOW_TIE (Wmsdkidl.h)
description: A transição de vínculo de arco revela a nova imagem em um conjunto de triângulos em lados opostos do quadro.
ms.assetid: d98da767-eea7-460c-ae5f-6bef9d93ad9d
keywords:
- WMT_VIDEOIMAGE_TRANSITION_BOW_TIE formato de mídia do Windows
topic_type:
- apiref
api_name:
- WMT_VIDEOIMAGE_TRANSITION_BOW_TIE
api_location:
- wmsdkidl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6f77cd2782bad6e4f83b5a4d1e719b0c21d704fefd2d4cccacfc0690a4fb0fa4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117843947"
---
# <a name="wmt_videoimage_transition_bow_tie"></a>WMT \_ VIDEOIMAGE \_ TRANSITION \_ BOW \_ TIE

A transição de vínculo de arco revela a nova imagem em um conjunto de triângulos em lados opostos do quadro.

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
<td>Largura</td>
<td><strong>fEffectPara0</strong></td>
<td>Largura de cada lado triangular da faixa de arco.</td>
</tr>
<tr class="even">
<td>Altura</td>
<td><strong>fEffectPara1</strong></td>
<td>Altura de cada lado triangular da extremidade do arco.</td>
</tr>
<tr class="odd">
<td>Direção</td>
<td><strong>fEffectPara2</strong></td>
<td>De acordo com um dos seguintes valores:
<ul>
<li>0 – especifica o efeito de arco-remos horizontal, no qual os triângulos entram dos lados direito e esquerdo do quadro.</li>
<li>1 - Especifica o efeito de vínculo de arco vertical, no qual os triângulos entram da parte superior e inferior do quadro.</li>
</ul></td>
</tr>
<tr class="even">
<td>Composição</td>
<td><strong>fEffectPara3</strong></td>
<td>De acordo com um dos seguintes valores:
<ul>
<li>0 – Especifica a composição normal, na qual a imagem anterior é a plano de fundo e a imagem atual é o primeiro plano.</li>
<li>1 - Especifica a composição invertida, na qual a imagem atual é a imagem de plano de fundo e a imagem anterior é o primeiro plano.</li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|---------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Wmsdkidl.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Transições de imagem de vídeo**](video-image-transitions.md)
</dt> </dl>

 

 





