---
title: Modelo de sombreador 2
description: O Shader Model 2 adicionou funcionalidades adicionais ao Shader Model 1.
ms.assetid: 53c367d2-5b6a-4afa-894a-8ab9927169d5
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 88bd2f6292687c5387fadf65f8f43437904168cc
ms.sourcegitcommit: 927b9c371f75f52b8011483edf3a4ba37d11ebe4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/11/2020
ms.locfileid: "104988647"
---
# <a name="shader-model-2"></a>Modelo de sombreador 2

O Shader Model 2 adicionou funcionalidades adicionais ao [Shader Model 1](dx-graphics-hlsl-sm1.md).



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
<li>Instruções de assembly (consulte <a href="dx9-graphics-reference-asm-vs-instructions-vs-2-0.md">instruções-VS_2_0</a>, <a href="dx9-graphics-reference-asm-vs-instructions-vs-2-x.md">instruções-vs_2_x</a>, <a href="dx9-graphics-reference-asm-ps-instructions-ps-2-0.md">instruções de PS_2_0</a>, instruções de <a href="dx9-graphics-reference-asm-ps-instructions-ps-2-x.md">ps_2_x</a>)</li>
</ul></td>
</tr>
<tr class="odd">
<td>Conjunto de registros</td>
<td><ul>
<li>Registros de sombreador de pixel (consulte <a href="dx9-graphics-reference-asm-ps-registers-ps-2-0.md">registros de PS_2_0</a>, <a href="dx9-graphics-reference-asm-ps-registers-ps-2-x.md">registros de ps_2_x</a>)</li>
<li>Registros de sombreador de vértice (consulte <a href="dx9-graphics-reference-asm-vs-registers-vs-2-0.md">Registers-VS_2_0</a>, <a href="dx9-graphics-reference-asm-vs-registers-vs-2-x.md">registers-vs_2_x</a>)</li>
</ul></td>
</tr>
<tr class="even">
<td>Sombreador máximo de pixel</td>
<td><ul>
<li>ps_2_0-32 Texture + 64 aritmético</li>
<li>ps_2_x-96 mínimo e até o número de Slots em D3DCAPS9. D3DPSHADERCAPS2_0. NumInstructionSlots. Consulte D3DPSHADERCAPS2_0</li>
</ul></td>
</tr>
<tr class="odd">
<td>Sombreador máximo do vértice</td>
<td>256 instruções</td>
</tr>
<tr class="even">
<td>Perfis de sombreador</td>
<td>ps_2_0, ps_2_x, vs_2_0 vs_2_x</td>
</tr>
</tbody>
</table>



 

Para obter mais detalhes sobre o modelo de sombreador 2, consulte:

-   [Sombreador de pixel 2,0](dx9-graphics-reference-asm-ps-2-0.md), [sombreador de pixel 2. x](dx9-graphics-reference-asm-ps-2-x.md)
-   [Sombreador de vértice 2,0](dx9-graphics-reference-asm-vs-2-0.md), [sombreador de vértice 2. x](dx9-graphics-reference-asm-vs-2-x.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Modelos de sombreador vs. perfis de sombreador](dx-graphics-hlsl-models.md)
</dt> </dl>

 

 




