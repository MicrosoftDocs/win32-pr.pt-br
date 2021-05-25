---
description: Constantes de filtragem de textura.
ms.assetid: 4434e456-670e-46a9-ba78-affdc195fe1c
title: D3DPTFILTERCAPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46adc4759290691e93ef68a8a4e212eacf5b6451
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/24/2021
ms.locfileid: "110343081"
---
# <a name="d3dptfiltercaps"></a>D3DPTFILTERCAPS

Constantes de filtragem de textura.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>#Definir</td>
<td>Descrição</td>
</tr>
<tr class="even">
<td>D3DPTFILTERCAPS_CONVOLUTIONMONO</td>
<td>O dispositivo dá suporte à filtragem de convolução monocromática. Esse filtro é representado pelo membro D3DTEXF_CONVOLUTIONMONO do tipo enumerado <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE.</strong></a> 
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
<td>D3DPTFILTERCAPS_MAGFPOINT</td>
<td>O dispositivo dá suporte à filtragem de exemplo de ponto por estágio para ampliar texturas. O filtro de ampliação de exemplo de ponto é representado pelo D3DTEXF_POINT membro do tipo enumerado <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE.</strong></a></td>
</tr>
<tr class="even">
<td>D3DPTFILTERCAPS_MAGFLINEAR</td>
<td>O dispositivo dá suporte à filtragem de interpolação bilinear por estágio para ampliar mipmaps. O filtro mipmapping de interpolação bilinear é representado pelo D3DTEXF_LINEAR membro do tipo enumerado <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE.</strong></a></td>
</tr>
<tr class="odd">
<td>D3DPTFILTERCAPS_MAGFANISOTROPIC</td>
<td>O dispositivo dá suporte à filtragem anisoél por estágio para ampliar texturas. O filtro de ampliação anisuária é representado pelo D3DTEXF_ANISOTROPIC membro do tipo enumerado <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE.</strong></a></td>
</tr>
<tr class="even">
<td>D3DPTFILTERCAPS_MAGFPYRAMIDALQUAD</td>
<td>O dispositivo dá suporte à filtragem de amostra piramidal por estágio para ampliar texturas. O filtro de lupa piramidal é representado pelo membro de D3DTEXF_PYRAMIDALQUAD do tipo enumerado <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE</strong></a> .</td>
</tr>
<tr class="odd">
<td>D3DPTFILTERCAPS_MAGFGAUSSIANQUAD</td>
<td>O dispositivo dá suporte a filtragem quádrupla gaussiano por estágio para ampliar texturas.</td>
</tr>
<tr class="even">
<td>D3DPTFILTERCAPS_MINFPOINT</td>
<td>O dispositivo dá suporte à filtragem de amostra de ponto por estágio para texturas minificar. O filtro minificação de exemplo de ponto é representado pelo membro D3DTEXF_POINT do tipo enumerado <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE</strong></a> .</td>
</tr>
<tr class="odd">
<td>D3DPTFILTERCAPS_MINFLINEAR</td>
<td>O dispositivo dá suporte à filtragem linear por estágio para texturas minificar. O filtro minificação linear é representado pelo membro D3DTEXF_LINEAR do tipo enumerado <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE</strong></a> .</td>
</tr>
<tr class="even">
<td>D3DPTFILTERCAPS_MINFANISOTROPIC</td>
<td>O dispositivo dá suporte à filtragem de anisotropic por estágio para texturas minificar. O filtro anisotropic minificação é representado pelo membro D3DTEXF_ANISOTROPIC do tipo enumerado <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE</strong></a> .</td>
</tr>
<tr class="odd">
<td>D3DPTFILTERCAPS_MINFPYRAMIDALQUAD</td>
<td>O dispositivo dá suporte à filtragem de amostra piramidal por estágio para texturas minificar.</td>
</tr>
<tr class="even">
<td>D3DPTFILTERCAPS_MINFGAUSSIANQUAD</td>
<td>O dispositivo dá suporte à filtragem quádrupla gaussiano por etapa para texturas minificars.</td>
</tr>
<tr class="odd">
<td>D3DPTFILTERCAPS_MIPFPOINT</td>
<td>O dispositivo dá suporte à filtragem de amostra de ponto por etapa para mipmaps. O filtro mipmapping de exemplo de ponto é representado pelo membro D3DTEXF_POINT do tipo enumerado <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE</strong></a> .</td>
</tr>
<tr class="even">
<td>D3DPTFILTERCAPS_MIPFLINEAR</td>
<td>O dispositivo dá suporte à filtragem de interpolação bilinear por estágio para mipmaps. O filtro mipmapping de interpolação bilinear é representado pelo D3DTEXF_LINEAR membro do tipo enumerado <a href="/windows/desktop/direct3d9/d3dtexturefiltertype"><strong>D3DTEXTUREFILTERTYPE.</strong></a></td>
</tr>
</tbody>
</table>



 

Essas constantes são usadas pelos membros TextureFilterCaps, CubeTextureFilterCaps, VolumeTextureFilterCaps e VertexTextureFilterCaps [**de D3DCAPS9.**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9)

## <a name="constant-information"></a>Informações constantes



|  Requisito                        | Valor           |
|--------------------------|------------|
| parâmetro                   | d3d9caps.h |
| Sistema operacional mínimo | Windows 98 |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Constantes Direct3D](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 
