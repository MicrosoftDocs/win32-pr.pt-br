---
description: Sinalizadores de capacidade do driver.
ms.assetid: d9cd7388-3413-472d-aacb-0b8c9c60031a
title: D3DCAPS3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a165ff1d550612ba302c94a0b8181affe040921
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105802082"
---
# <a name="d3dcaps3"></a>D3DCAPS3

Sinalizadores de capacidade do driver.



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<tbody>
<tr class="odd">
<td>#definir</td>
<td>Valor</td>
<td>Descrição</td>
</tr>
<tr class="even">
<td>D3DCAPS3_ALPHA_FULLSCREEN_FLIP_OR_DISCARD</td>
<td>0x00000020L</td>
<td>Indica que o dispositivo pode respeitar o estado de renderização de D3DRS_ALPHABLENDENABLE no modo de tela inteira ao usar o efeito de permuta inverter ou descartar. Isso só se aplica quando os Estados D3DRS_SRCBLEND ou D3DRS_DESTBLEND são definidos como um dos seguintes:
<ul>
<li>D3DBLEND_DESTALPHA</li>
<li>D3DBLEND_INVDESTALPHA</li>
<li>D3DBLEND_DESTCOLOR</li>
<li>D3DBLEND_INVDESTCOLOR</li>
</ul></td>
</tr>
<tr class="odd">
<td>D3DCAPS3_COPY_TO_VIDMEM</td>
<td>0x00000100L</td>
<td>O dispositivo pode acelerar uma cópia de memória da memória do sistema para a memória de vídeo local. Esse limite garante que as chamadas <a href="/windows/desktop/api"><strong>UpdateSurface</strong></a> e <a href="/windows/desktop/api"><strong>UpdateTexture</strong></a> serão aceleradas por hardware. Se esse limite estiver ausente, essas chamadas terão sucesso, mas serão mais lentas.</td>
</tr>
<tr class="even">
<td>D3DCAPS3_COPY_TO_SYSTEMMEM</td>
<td>0x00000200L</td>
<td>O dispositivo pode acelerar uma cópia de memória da memória de vídeo local para a memória do sistema. Esse limite garante que as chamadas de <a href="/windows/desktop/api"><strong>GetRenderTargetData</strong></a> serão aceleradas por hardware. Se esse limite estiver ausente, essa chamada terá sucesso, mas será mais lenta.</td>
</tr>
<tr class="odd">
<td>D3DCAPS3_DXVAHD</td>
<td>0x00000400L</td>
<td>O driver de vídeo dá suporte à DDI DXVA-HD. Para obter mais informações sobre a DDI DXVA-HD, consulte <a href="https://msdn.microsoft.com/library/dd835176.aspx">processamento High-Definition vídeo</a>.<br/> 
<table>
<tbody>
<tr class="odd">
<td>Diferenças entre o Direct3D 9 e o Direct3D 9Ex:<br/> Esse sinalizador está disponível somente no Direct3D 9Ex.<br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td>D3DCAPS3_LINEAR_TO_SRGB_PRESENTATION</td>
<td>0x00000080L</td>
<td>Indica que o dispositivo pode executar a correção gama de um buffer de fundo em janela (que contém conteúdo linear) para uma área de trabalho sRGB.</td>
</tr>
<tr class="odd">
<td>D3DCAPS3_RESERVED</td>
<td>0x8000001fL</td>
<td>Reservado Não usado.</td>
</tr>
</tbody>
</table>



 

Essas constantes são usadas pelo membro D3CAPS3 de [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).

## <a name="constant-information"></a>Informações constantes



|                          |            |
|--------------------------|------------|
| parâmetro                   | d3d9caps. h |
| Sistema operacional mínimo | Windows 98 |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Constantes do Direct3D](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 




