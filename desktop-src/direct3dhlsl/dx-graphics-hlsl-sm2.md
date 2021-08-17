---
title: Modelo de sombreador 2
description: O Modelo de Sombreador 2 adicionou recursos adicionais ao modelo de sombreador 1.
ms.assetid: 53c367d2-5b6a-4afa-894a-8ab9927169d5
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 23b4caa0e4da92e992eb0486f5a998ad7d21016dc691563f29589c5fc9ab5310
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119119970"
---
# <a name="shader-model-2"></a>Modelo de sombreador 2

O Modelo de Sombreador 2 adicionou recursos adicionais ao [modelo de sombreador 1.](dx-graphics-hlsl-sm1.md)



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Recurso</td>
<td>Funcionalidade</td>
</tr>
<tr class="even">
<td>Conjunto de instruções</td>
<td><ul>
<li><a href="dx-graphics-hlsl-intrinsic-functions.md"><strong>Funções HLSL</strong></a></li>
<li>Instruções de assembly (consulte <a href="dx9-graphics-reference-asm-vs-instructions-vs-2-0.md">Instruções - vs_2_0</a>, Instruções - <a href="dx9-graphics-reference-asm-vs-instructions-vs-2-x.md">vs_2_x</a>, <a href="dx9-graphics-reference-asm-ps-instructions-ps-2-0.md">ps_2_0 instruções</a>, ps_2_x <a href="dx9-graphics-reference-asm-ps-instructions-ps-2-x.md">Instruções</a>)</li>
</ul></td>
</tr>
<tr class="odd">
<td>Conjunto de registros</td>
<td><ul>
<li>Registros de sombreador de pixel <a href="dx9-graphics-reference-asm-ps-registers-ps-2-0.md">(consulte ps_2_0 registros,</a> <a href="dx9-graphics-reference-asm-ps-registers-ps-2-x.md">ps_2_x registros</a>)</li>
<li>Registros de sombreador de vértice (consulte <a href="dx9-graphics-reference-asm-vs-registers-vs-2-0.md">Registros - vs_2_0</a>, Registros - <a href="dx9-graphics-reference-asm-vs-registers-vs-2-x.md">vs_2_x</a>)</li>
</ul></td>
</tr>
<tr class="even">
<td>Pixel Shader Max</td>
<td><ul>
<li>ps_2_0 - 32 textura + 64 aritmética</li>
<li>ps_2_x mínimo de 96 e até o número de slots em D3DCAPS9. D3DPSHADERCAPS2_0.NumInstructionSlots. Consulte D3DPSHADERCAPS2_0</li>
</ul></td>
</tr>
<tr class="odd">
<td>Máx. de sombreador de vértice</td>
<td>256 instruções</td>
</tr>
<tr class="even">
<td>Perfis do sombreador</td>
<td>ps_2_0, ps_2_x, vs_2_0, vs_2_x</td>
</tr>
</tbody>
</table>



 

Para obter mais detalhes sobre o modelo de sombreador 2, consulte:

-   [Sombreador de Pixel 2.0,](dx9-graphics-reference-asm-ps-2-0.md) [Sombreador de Pixel 2.x](dx9-graphics-reference-asm-ps-2-x.md)
-   [Sombreador de vértice 2.0,](dx9-graphics-reference-asm-vs-2-0.md)Sombreador de [vértice 2.x](dx9-graphics-reference-asm-vs-2-x.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Modelos de sombreador versus perfis de sombreador](dx-graphics-hlsl-models.md)
</dt> </dl>

 

 




