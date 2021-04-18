---
title: WMT_VIDEOIMAGE_TRANSITION_DIAGONAL (Wmsdkidl. h)
description: A transição diagonal revela a nova imagem ao longo de uma linha diagonal originada em um canto do quadro.
ms.assetid: 1aaaf9e8-bbb8-4289-948e-5d352798e831
keywords:
- WMT_VIDEOIMAGE_TRANSITION_DIAGONAL o formato Windows Media
topic_type:
- apiref
api_name:
- WMT_VIDEOIMAGE_TRANSITION_DIAGONAL
api_location:
- wmsdkidl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b6affa3e0727972e66e1ab6584c94ec233a11655
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105788082"
---
# <a name="wmt_videoimage_transition_diagonal"></a>\_diagonal de \_ transição WMT VIDEOIMAGE \_

A transição diagonal revela a nova imagem ao longo de uma linha diagonal originada em um canto do quadro.

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
<td>Largura da seção diagonal em pixels.</td>
</tr>
<tr class="even">
<td>Altura</td>
<td><strong>fEffectPara1</strong></td>
<td>Altura da seção diagonal em pixels.</td>
</tr>
<tr class="odd">
<td>Direção</td>
<td><strong>fEffectPara2</strong></td>
<td>Determina o canto do qual a transição se origina. Defina como um dos seguintes:<br/>
<ul>
<li>0-superior direito</li>
<li>1-superior esquerdo</li>
<li>2-inferior direito</li>
<li>3-inferior esquerdo</li>
</ul></td>
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

 

 





