---
description: Sinalizadores de recurso primitivos de driver diversos.
ms.assetid: 7912c682-c179-453b-8a34-e87958217500
title: D3DPMISCCAPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76af50a1e7f78f6441af9e985f55e42ee2298b46
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104164115"
---
# <a name="d3dpmisccaps"></a>D3DPMISCCAPS

Sinalizadores de recurso primitivos de driver diversos.



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
<td>D3DPMISCCAPS_MASKZ</td>
<td>0x00000002L</td>
<td>O dispositivo pode habilitar e desabilitar a modificação do buffer de profundidade em operações de pixel.</td>
</tr>
<tr class="odd">
<td>D3DPMISCCAPS_CULLNONE</td>
<td>0x00000010L</td>
<td>O driver não executa a remoção de triângulo. Isso corresponde ao membro de D3DCULL_NONE do tipo enumerado <a href="/windows/desktop/direct3d9/d3dcull"><strong>D3DCULL</strong></a> .</td>
</tr>
<tr class="even">
<td>D3DPMISCCAPS_CULLCW</td>
<td>0x00000020L</td>
<td>O driver dá suporte à seleção de triângulo no sentido horário por meio do estado de D3DRS_CULLMODE. (Isso se aplica somente a primitivas de triângulo.) Esse sinalizador corresponde ao membro de D3DCULL_CW do tipo enumerado <a href="/windows/desktop/direct3d9/d3dcull"><strong>D3DCULL</strong></a> .</td>
</tr>
<tr class="odd">
<td>D3DPMISCCAPS_CULLCCW</td>
<td>0x00000040L</td>
<td>O driver dá suporte à seleção no sentido anti-horário por meio do estado de D3DRS_CULLMODE. (Isso se aplica somente a primitivas de triângulo.) Esse sinalizador corresponde ao membro de D3DCULL_CCW do tipo enumerado <a href="/windows/desktop/direct3d9/d3dcull"><strong>D3DCULL</strong></a> .</td>
</tr>
<tr class="even">
<td>D3DPMISCCAPS_COLORWRITEENABLE</td>
<td>0x00000100L</td>
<td>O dispositivo dá suporte a gravações por canal para o buffer de cores de destino de renderização por meio do estado de D3DRS_COLORWRITEENABLE.</td>
</tr>
<tr class="odd">
<td>D3DPMISCCAPS_CLIPPLANESCALEDPOINTS</td>
<td>0x00000200L</td>
<td>O dispositivo corta corretamente os pontos dimensionados de tamanho maior que 1,0 para os planos de recorte definidos pelo usuário.</td>
</tr>
<tr class="even">
<td>D3DPMISCCAPS_CLIPTLVERTS</td>
<td>0x00000200L</td>
<td>Os clipes de dispositivo transformam primitivas de vértice. Especifique D3DUSAGE_DONOTCLIP quando o pipeline não deve fazer recorte. Nesse caso, pode ser necessário recortar o software adicional no momento do desenho, exigindo que o buffer de vértice esteja na memória do sistema.<br/></td>
</tr>
<tr class="odd">
<td>D3DPMISCCAPS_TSSARGTEMP</td>
<td>0x00000400L</td>
<td>O dispositivo dá suporte a <a href="d3dta.md">D3DTA</a> para registro temporário.</td>
</tr>
<tr class="even">
<td>D3DPMISCCAPS_BLENDOP</td>
<td>0x00000800L</td>
<td>O dispositivo dá suporte a operações de mesclagem alfa diferentes de D3DBLENDOP_ADD.</td>
</tr>
<tr class="odd">
<td>D3DPMISCCAPS_NULLREFERENCE</td>
<td>0x00000100L</td>
<td>Um dispositivo de referência que não é renderizado.</td>
</tr>
<tr class="even">
<td>D3DPMISCCAPS_INDEPENDENTWRITEMASKS</td>
<td>0x00004000L</td>
<td>O dispositivo dá suporte a máscaras de gravação independentes para várias texturas de elementos ou vários destinos de renderização.</td>
</tr>
<tr class="odd">
<td>D3DPMISCCAPS_PERSTAGECONSTANT</td>
<td>0x00008000L</td>
<td>O dispositivo dá suporte a constantes por estágio. Consulte D3DTSS_CONSTANT em <a href="/windows/desktop/direct3d9/d3dtexturestagestatetype"><strong>D3DTEXTURESTAGESTATETYPE</strong></a>.</td>
</tr>
<tr class="even">
<td>D3DPMISCCAPS_POSTBLENDSRGBCONVERT</td>
<td>0x00200000L</td>
<td>O dispositivo dá suporte à conversão para sRGB após a mesclagem. 
<table>
<tbody>
<tr class="odd">
<td>Diferenças entre o Direct3D 9 e o Direct3D 9Ex:<br/> Esse sinalizador está disponível somente no Direct3D 9Ex.<br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td>D3DPMISCCAPS_FOGANDSPECULARALPHA</td>
<td>0x00010000L</td>
<td>O dispositivo dá suporte a sombra separada e alfa especular Alpha. Muitos dispositivos usam o canal alfa especular para armazenar o fator de neblina.</td>
</tr>
<tr class="even">
<td>D3DPMISCCAPS_SEPARATEALPHABLEND</td>
<td>0x00020000L</td>
<td>O dispositivo dá suporte a configurações de mesclagem separadas para o canal alfa.</td>
</tr>
<tr class="odd">
<td>D3DPMISCCAPS_MRTINDEPENDENTBITDEPTHS</td>
<td>0x00040000L</td>
<td>O dispositivo dá suporte a diferentes profundidades de bits para vários destinos de renderização.</td>
</tr>
<tr class="even">
<td>D3DPMISCCAPS_MRTPOSTPIXELSHADERBLENDING</td>
<td>0x00080000L</td>
<td>O dispositivo dá suporte a operações de sombreador pós-pixel para vários destinos de renderização.</td>
</tr>
<tr class="odd">
<td>D3DPMISCCAPS_FOGVERTEXCLAMPED</td>
<td>0x00100000L</td>
<td>Fator de mistura de dispositivo coloca de neblina por vértice.</td>
</tr>
</tbody>
</table>



 

Essas constantes são usadas pelo membro PrimitiveMiscCaps de [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).

## <a name="constant-information"></a>Informações constantes



|                          |            |
|--------------------------|------------|
| parâmetro                   | d3d9caps. h |
| Sistema operacional mínimo | Windows 98 |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Constantes do Direct3D](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 
