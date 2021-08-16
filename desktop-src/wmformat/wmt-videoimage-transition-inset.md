---
title: WMT_VIDEOIMAGE_TRANSITION_INSET (Wmsdkidl.h)
description: A transição de inset revela a nova imagem em um retângulo originado de um canto do quadro.
ms.assetid: fd8bc4b7-0546-4897-ab7b-a320bbd126ef
keywords:
- WMT_VIDEOIMAGE_TRANSITION_INSET formato de mídia do Windows
topic_type:
- apiref
api_name:
- WMT_VIDEOIMAGE_TRANSITION_INSET
api_location:
- wmsdkidl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2f815e0bb1fc7e8e1cba277f68b7950af2b20395092b69b2c07ebb7ac51367da
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117843785"
---
# <a name="wmt_videoimage_transition_inset"></a>INSET DE TRANSIÇÃO DO WMT \_ VIDEOIMAGE \_ \_

A transição de inset revela a nova imagem em um retângulo originado de um canto do quadro.

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
<td>Largura do inset em pixels.</td>
</tr>
<tr class="even">
<td>Altura</td>
<td><strong>fEffectPara1</strong></td>
<td>Altura do inset em pixels.</td>
</tr>
<tr class="odd">
<td>Direção</td>
<td><strong>fEffectPara2</strong></td>
<td>Canto do qual o inset se origina. De acordo com um dos seguintes valores:<br/>
<ul>
<li>0 – Inferior esquerdo</li>
<li>1 - Inferior direito</li>
<li>2 – Superior esquerdo</li>
<li>3 – Canto superior direito</li>
</ul></td>
</tr>
<tr class="even">
<td>Composição</td>
<td><strong>fEffectPara3</strong></td>
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

 

 





