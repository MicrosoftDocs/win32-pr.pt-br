---
title: WMT_VIDEOIMAGE_TRANSITION_IRIS (Wmsdkidl.h)
description: A transição de íris revela a nova imagem ao longo de um eixo x e um eixo y. O efeito visual dessa transição é que a nova imagem aparece em um alcance cruzado de ampliação para todos os lados do quadro.
ms.assetid: 7390d959-a566-43e7-937d-1e617bc98a6e
keywords:
- WMT_VIDEOIMAGE_TRANSITION_IRIS formato de mídia do Windows
topic_type:
- apiref
api_name:
- WMT_VIDEOIMAGE_TRANSITION_IRIS
api_location:
- wmsdkidl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 88d935b6f8f049571f89eba4c5f9f72e298dd7b1f0ec52ba30d69e9ca3235655
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118027386"
---
# <a name="wmt_videoimage_transition_iris"></a>IRIS DE TRANSIÇÃO DO WMT \_ VIDEOIMAGE \_ \_

A transição de íris revela a nova imagem ao longo de um eixo x e um eixo y. O efeito visual dessa transição é que a nova imagem aparece em um alcance cruzado de ampliação para todos os lados do quadro.

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
<td>Coordenada X, em relação ao quadro de vídeo, do centro do efeito íris.</td>
</tr>
<tr class="even">
<td>Y central</td>
<td><strong>fEffectPara1</strong></td>
<td>Coordenada Y, em relação ao quadro de vídeo, do centro do efeito íris.</td>
</tr>
<tr class="odd">
<td>Largura</td>
<td><strong>fEffectPara2</strong></td>
<td>Largura da linha vertical revelando a nova imagem, em pixels.</td>
</tr>
<tr class="even">
<td>Altura</td>
<td><strong>fEffectPara3</strong></td>
<td>Altura da linha horizontal revelando a nova imagem, em pixels.</td>
</tr>
<tr class="odd">
<td>Composição</td>
<td><strong>fEffectPara4</strong></td>
<td>De acordo com um dos seguintes valores:
<ul>
<li>0 – Especifica a composição normal, na qual a imagem anterior é a plano de fundo e a imagem atual é o primeiro plano.</li>
<li>1 - Especifica a composição invertida, na qual a imagem atual é a imagem de plano de fundo e a imagem anterior é o primeiro plano</li>
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

 

 





