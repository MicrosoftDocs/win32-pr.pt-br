---
description: Sinalizadores de funcionalidade primitiva de driver diversos.
ms.assetid: 7912c682-c179-453b-8a34-e87958217500
title: D3DPMISCCAPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee88ba03b3c0a6d51c0100b20768df4cbf632d46
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2021
ms.locfileid: "122624532"
---
# <a name="d3dpmisccaps"></a>D3DPMISCCAPS

Sinalizadores de funcionalidade primitiva de driver diversos.



<table>
<colgroup>
<col  />
<col  />
<col  />
</colgroup>
<tbody>
<tr class="odd">
<td>#Definir</td>
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
<td>O driver não executa a ressarção de triângulo. Isso corresponde ao D3DCULL_NONE do tipo enumerado <a href="/windows/desktop/direct3d9/d3dcull"><strong>D3DCULL.</strong></a></td>
</tr>
<tr class="even">
<td>D3DPMISCCAPS_CULLCW</td>
<td>0x00000020L</td>
<td>O driver dá suporte à ressarção de triângulo no sentido horário por meio do estado D3DRS_CULLMODE sistema. (Isso se aplica somente a primitivos de triângulo.) Esse sinalizador corresponde ao D3DCULL_CW membro do tipo enumerado <a href="/windows/desktop/direct3d9/d3dcull"><strong>D3DCULL.</strong></a></td>
</tr>
<tr class="odd">
<td>D3DPMISCCAPS_CULLCCW</td>
<td>0x00000040L</td>
<td>O driver dá suporte à respeção no sentido anti-horário por meio do estado D3DRS_CULLMODE trabalho. (Isso se aplica somente a primitivos de triângulo.) Esse sinalizador corresponde ao D3DCULL_CCW do tipo enumerado <a href="/windows/desktop/direct3d9/d3dcull"><strong>D3DCULL.</strong></a></td>
</tr>
<tr class="even">
<td>D3DPMISCCAPS_COLORWRITEENABLE</td>
<td>0x00000100L</td>
<td>O dispositivo dá suporte a gravações por canal para o buffer de cores de destino de renderização por meio do estado D3DRS_COLORWRITEENABLE sistema.</td>
</tr>
<tr class="odd">
<td>D3DPMISCCAPS_CLIPPLANESCALEDPOINTS</td>
<td>0x00000200L</td>
<td>O dispositivo corta corretamente pontos dimensionados de tamanho maior que 1,0 para planos de recorte definidos pelo usuário.</td>
</tr>
<tr class="even">
<td>D3DPMISCCAPS_CLIPTLVERTS</td>
<td>0x00000200L</td>
<td>Os clipes de dispositivo pós-transformados são primitivos de vértice. Especifique D3DUSAGE_DONOTCLIP quando o pipeline não deve fazer nenhum recorte. Nesse caso, o recorte de software adicional pode precisar ser executado em tempo de desenho, exigindo que o buffer de vértice seja na memória do sistema.<br/></td>
</tr>
<tr class="odd">
<td>D3DPMISCCAPS_TSSARGTEMP</td>
<td>0x00000400L</td>
<td>O dispositivo dá <a href="d3dta.md">suporte a D3DTA</a> para registro temporário.</td>
</tr>
<tr class="even">
<td>D3DPMISCCAPS_BLENDOP</td>
<td>0x00000800L</td>
<td>O dispositivo dá suporte a operações de combinação alfa além D3DBLENDOP_ADD.</td>
</tr>
<tr class="odd">
<td>D3DPMISCCAPS_NULLREFERENCE</td>
<td>0x00000100L</td>
<td>Um dispositivo de referência que não renderiza.</td>
</tr>
<tr class="even">
<td>D3DPMISCCAPS_INDEPENDENTWRITEMASKS</td>
<td>0x00004000L</td>
<td>O dispositivo dá suporte a máscaras de gravação independentes para várias texturas de elemento ou vários destinos de renderização.</td>
</tr>
<tr class="odd">
<td>D3DPMISCCAPS_PERSTAGECONSTANT</td>
<td>0x00008000L</td>
<td>O dispositivo dá suporte a constantes por estágio. Consulte D3DTSS_CONSTANT em <a href="/windows/desktop/direct3d9/d3dtexturestagestatetype"><strong>D3DTEXTURESTAGESTATETYPE</strong></a>.</td>
</tr>
<tr class="even">
<td>D3DPMISCCAPS_POSTBLENDSRGBCONVERT</td>
<td>0x00200000L</td>
<td>O dispositivo dá suporte à conversão em sRGB após a mesclagem. 
<table>
<tbody>
<tr class="odd">
<td>Diferenças entre o Direct3D 9 e o Direct3D 9Ex:<br/> Esse sinalizador está disponível apenas no Direct3D 9Ex.<br/></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td>D3DPMISCCAPS_FOGANDSPECULARALPHA</td>
<td>0x00010000L</td>
<td>O dispositivo dá suporte a alfa especular e separado. Muitos dispositivos usam o canal alfa especular para armazenar o fator de cão.</td>
</tr>
<tr class="even">
<td>D3DPMISCCAPS_SEPARATEALPHABLEND</td>
<td>0x00020000L</td>
<td>O dispositivo dá suporte a configurações de combinação separadas para o canal alfa.</td>
</tr>
<tr class="odd">
<td>D3DPMISCCAPS_MRTINDEPENDENTBITDEPTHS</td>
<td>0x00040000L</td>
<td>O dispositivo dá suporte a profundidades de bits diferentes para vários destinos de renderização.</td>
</tr>
<tr class="even">
<td>D3DPMISCCAPS_MRTPOSTPIXELSHADERBLENDING</td>
<td>0x00080000L</td>
<td>O dispositivo dá suporte a operações de sombreador pós-pixel para vários destinos de renderização.</td>
</tr>
<tr class="odd">
<td>D3DPMISCCAPS_FOGVERTEXCLAMPED</td>
<td>0x00100000L</td>
<td>O dispositivo fixa o fator blend blend por vértice.</td>
</tr>
</tbody>
</table>



 

Essas constantes são usadas pelo membro PrimitiveMiscCaps [**de D3DCAPS9.**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)

## <a name="constant-information"></a>Informações constantes



| Requisito                         |  Valor          |
|--------------------------|------------|
| parâmetro                   | d3d9caps.h |
| Sistema operacional mínimo | Windows 98 |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Constantes Direct3D](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 
