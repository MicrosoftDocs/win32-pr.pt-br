---
title: WMT_VIDEOIMAGE_TRANSITION_PAGE_ROLL (Wmsdkidl. h)
description: A transição de rolagem de página transforma a imagem antiga com um efeito de inversão de página, revelando a nova imagem abaixo.
ms.assetid: 50efa4e9-0d3a-4b85-96b0-6d5cd637ca98
keywords:
- WMT_VIDEOIMAGE_TRANSITION_PAGE_ROLL o formato Windows Media
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
ms.openlocfilehash: b4167395dbe00242af42f30713438f33e88f2dda
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105748041"
---
# <a name="wmt_videoimage_transition_page_roll"></a>Roll WMT de \_ \_ página de transição VIDEOIMAGE \_ \_

A transição de rolagem de página transforma a imagem antiga com um efeito de inversão de página, revelando a nova imagem abaixo.

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
<td>Raio</td>
<td><strong>fEffectPara0</strong></td>
<td>Raio do rolo no efeito de acúmulo de página.</td>
</tr>
<tr class="even">
<td>Distância</td>
<td><strong>fEffectPara1</strong></td>
<td>A quantidade da nova imagem que é revelada pelo efeito de acúmulo de página, em pixels.</td>
</tr>
<tr class="odd">
<td>Direção</td>
<td><strong>fEffectPara2</strong></td>
<td>Canto ou lado do quadro de vídeo, do qual o rolo de página se origina. Defina como um dos seguintes valores:<br/>
<ul>
<li>0-lado esquerdo</li>
<li>1-lado direito</li>
<li>2-inferior</li>
<li>3-superior</li>
<li>4-canto inferior esquerdo</li>
<li>5-canto inferior direito</li>
<li>6-canto superior esquerdo</li>
<li>7-canto superior direito</li>
</ul></td>
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

 

 





