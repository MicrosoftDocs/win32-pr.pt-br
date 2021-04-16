---
title: WMT_VIDEOIMAGE_TRANSITION_RECTANGLE (Wmsdkidl. h)
description: A transição de retângulo revela a nova imagem em um retângulo dentro do quadro.
ms.assetid: 2e238cd5-1da5-4145-a44d-b2658559fa0f
keywords:
- WMT_VIDEOIMAGE_TRANSITION_RECTANGLE o formato Windows Media
topic_type:
- apiref
api_name:
- WMT_VIDEOIMAGE_TRANSITION_RECTANGLE
api_location:
- wmsdkidl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1cdcc5e5b074a07cee13a9af7f7a0f8c0f629de0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105782511"
---
# <a name="wmt_videoimage_transition_rectangle"></a>\_retângulo de \_ transição WMT VIDEOIMAGE \_

A transição de retângulo revela a nova imagem em um retângulo dentro do quadro.

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
<td>Coordenada X, em relação ao quadro de vídeo, do centro do retângulo.</td>
</tr>
<tr class="even">
<td>Y central</td>
<td><strong>fEffectPara1</strong></td>
<td>Coordenada Y, em relação ao quadro de vídeo, do centro do retângulo.</td>
</tr>
<tr class="odd">
<td>Largura</td>
<td><strong>fEffectPara2</strong></td>
<td>Largura do retângulo em pixels.</td>
</tr>
<tr class="even">
<td>Altura</td>
<td><strong>fEffectPara3</strong></td>
<td>Altura do retângulo em pixels.</td>
</tr>
<tr class="odd">
<td>Composição</td>
<td><strong>fEffectPara4</strong></td>
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

 

 





