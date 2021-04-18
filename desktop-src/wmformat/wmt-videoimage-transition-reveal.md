---
title: WMT_VIDEOIMAGE_TRANSITION_REVEAL (Wmsdkidl. h)
description: A transição Reveal revela a nova imagem ao longo de uma linha reta originada de um lado do quadro.
ms.assetid: 75ff6155-6b28-474a-b5d1-c3f1b3873b8e
keywords:
- WMT_VIDEOIMAGE_TRANSITION_REVEAL o formato Windows Media
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
ms.openlocfilehash: a9aa385912cf106955dd33e06824d0b3668fcd97
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751304"
---
# <a name="wmt_videoimage_transition_reveal"></a>WMT \_ de \_ transição VIDEOIMAGE \_ revela

A transição Reveal revela a nova imagem ao longo de uma linha reta originada de um lado do quadro.

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
<td>A quantidade da nova imagem revelada, em pixels. Esse valor é relativo ao lado de origem do quadro.</td>
</tr>
<tr class="even">
<td>Direção</td>
<td><strong>fEffectPara1</strong></td>
<td>Direção da revelação. Defina como um dos seguintes valores:<br/>
<ul>
<li>0-revelar à direita; origine do lado esquerdo do quadro.</li>
<li>1-revelar à esquerda; origine do lado direito do quadro.</li>
<li>2-revelar para cima; originar-se da parte inferior do quadro.</li>
<li>3-revelar para baixo; origine da parte superior do quadro.</li>
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

 

 





