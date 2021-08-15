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
ms.openlocfilehash: b916a5142f09628852a016754f9fb3ad691882731466d802b8367e03837b9699
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119083730"
---
# <a name="wmt_videoimage_transition_reveal"></a>REVELAÇÃO DA TRANSIÇÃO DO WMT \_ \_ \_ VIDEOIMAGE

A transição de revelação revela a nova imagem ao longo de uma linha reta originada de um lado do quadro.

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
<td>Quantidade da nova imagem revelada, em pixels. Esse valor é relativo ao lado de origem do quadro.</td>
</tr>
<tr class="even">
<td>Direção</td>
<td><strong>fEffectPara1</strong></td>
<td>Direção da revelação. De acordo com um dos seguintes valores:<br/>
<ul>
<li>0 – Revelar à direita; originam-se do lado esquerdo do quadro.</li>
<li>1 - Revelar à esquerda; originam-se do lado direito do quadro.</li>
<li>2 - Revelar para cima; originam-se da parte inferior do quadro.</li>
<li>3 - Revelar para baixo; originam-se da parte superior do quadro.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Composição</td>
<td><strong>fEffectPara2</strong></td>
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

 

 





