---
title: Modelo de sombreador 3
description: O Shader Model 3 adicionou recursos adicionais ao Shader Model 2.
ms.assetid: bd09f86e-946f-4281-bc48-1db5cd32b2ae
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 9c53b8252f617c6ee3b95512a5d930a93f646479
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/08/2020
ms.locfileid: "104366806"
---
# <a name="shader-model-3-hlsl-reference"></a>Modelo de sombreador 3 (referência de HLSL)

O Shader Model 3 adicionou recursos adicionais ao [Shader Model 2](dx-graphics-hlsl-sm2.md).



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
<li>Instruções de assembly (consulte <a href="dx9-graphics-reference-asm-ps-instructions-ps-3-0.md">Ps_3_0 instruções</a>, <a href="dx9-graphics-reference-asm-vs-instructions-vs-3-0.md">instruções-vs_3_0</a>)</li>
</ul></td>
</tr>
<tr class="odd">
<td>Conjunto de registros</td>
<td><ul>
<li>Registros de sombreador de pixel (consulte <a href="dx9-graphics-reference-asm-ps-registers-ps-3-0.md">registros de ps_3_0</a>)</li>
<li>Registros de sombreador de vértice (consulte <a href="dx9-graphics-reference-asm-vs-registers-vs-3-0.md">registradores-vs_3_0</a>)</li>
</ul></td>
</tr>
<tr class="even">
<td>Sombreador máximo de pixel</td>
<td>mínimo de 512 e até o número de Slots em D3DCAPS9. MaxPixelShader30InstructionSlots (consulte <a href="/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dpshadercaps2_0"><strong>D3DPSHADERCAPS2_0</strong></a>).</td>
</tr>
<tr class="odd">
<td>Sombreador máximo do vértice</td>
<td>mínimo de 512 e até o número de Slots em D3DCAPS9. MaxVertexShader30InstructionSlots (consulte <a href="/windows/desktop/api/d3d9caps/ns-d3d9caps-d3dcaps9"><strong>D3DCAPS9</strong></a>).</td>
</tr>
<tr class="even">
<td>Perfis de sombreador</td>
<td>ps_3_0, vs_3_0</td>
</tr>
</tbody>
</table>



 

Para obter mais detalhes sobre os sombreadores do modelo 3, consulte:

-   [Sombreador de pixel 3,0](dx9-graphics-reference-asm-ps-3-0.md)
-   [Sombreador de vértice 3,0](dx9-graphics-reference-asm-vs-3-0.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Modelos de sombreador vs. perfis de sombreador](dx-graphics-hlsl-models.md)
</dt> </dl>

 

 