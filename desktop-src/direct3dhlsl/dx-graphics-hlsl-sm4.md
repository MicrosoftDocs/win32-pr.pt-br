---
title: Modelo de sombreador 4
description: O Shader Model 4 é um superconjunto dos recursos no Shader Model 3, exceto que o Shader Model 4 não oferece suporte aos recursos no Shader Model 1.
ms.assetid: 76155749-11e9-41ff-881d-8f77f2729364
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 3f1964eaf84e9b0a2669f59357f54d16b1b4cbd3
ms.sourcegitcommit: 927b9c371f75f52b8011483edf3a4ba37d11ebe4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/11/2020
ms.locfileid: "104365475"
---
# <a name="shader-model-4"></a>Modelo de sombreador 4

O Shader Model 4 é um superconjunto dos recursos no [Shader Model 3](dx-graphics-hlsl-sm3.md), exceto que o Shader Model 4 não oferece suporte aos recursos no Shader Model 1. Ele foi projetado usando um núcleo de sombreador comum que fornece um conjunto comum de recursos para todos os sombreadores programáveis, que só podem ser programados usando HLSL.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Recurso</th>
<th>Funcionalidade</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Conjunto de instruções</td>
<td><a href="dx-graphics-hlsl-intrinsic-functions.md"><strong>Funções HLSL</strong></a></td>
</tr>
<tr class="even">
<td>Conjunto de registros</td>
<td>O conjunto de registros é acessível por meio de membros em buffers de textura e constantes usando a semântica HLSL para coisas como empacotamento de componentes.
<ul>
<li>Registros de sombreador de pixel (consulte <a href="dx-graphics-hlsl-sm4-registers-ps-4-0.md">Registers-ps_4_0</a> e <a href="dx-graphics-hlsl-sm4-registers-ps-4-1.md">registers-ps_4_1</a>)</li>
<li>Registros de sombreador de vértice (consulte <a href="dx-graphics-hlsl-sm4-registers-vs-4-0.md">Registers-vs_4_0</a> e <a href="dx-graphics-hlsl-sm4-registers-vs-4-1.md">registers-vs_4_1</a>)</li>
<li>Registros de sombreador de geometria (consulte <a href="dx-graphics-hlsl-sm4-registers-gs-4-0.md">Registers-gs_4_0</a> e <a href="dx-graphics-hlsl-sm4-registers-gs-4-1.md">registers-gs_4_1</a>)</li>
</ul></td>
</tr>
<tr class="odd">
<td>Sombreador máximo do vértice</td>
<td>Nenhuma restrição</td>
</tr>
<tr class="even">
<td>Sombreador máximo de pixel</td>
<td>Nenhuma restrição</td>
</tr>
<tr class="odd">
<td>Novos perfis de sombreador adicionados</td>
<td>gs_4_0, ps_4_0, vs_4_0, gs_4_1 *, ps_4_1*, gs_4_1 *</td>
</tr>
<tr class="even">
<td>Novo perfil de Effect-Framework adicionado</td>
<td>fx_4_0, fx_4_1 *</td>
</tr>
</tbody>
</table>



 

\* -GS \_ 4 \_ 1, PS \_ 4 \_ 1, vs \_ 4 \_ 1 e FX \_ 4 \_ 1 têm suporte no Direct3D 10,1 ou superior.

O Shader Model 4 dá suporte a um novo estágio de pipeline — o estágio Geometry-Shader — que pode ser usado para criar ou modificar a geometria existente. Ele também inclui dois novos tipos de objeto: um objeto Stream-output criado para streaming de dados do estágio Geometry e um objeto de textura modelo que implementa funções de amostragem de textura.

-   [Núcleo de sombreador comum](dx-graphics-hlsl-common-core.md)
-   [Constantes](dx-graphics-hlsl-constants.md)
-   [Objeto Geometry-Shader](dx-graphics-hlsl-geometry-shader.md)
-   [Fluxo-objeto de saída](dx-graphics-hlsl-so-type.md)
-   [Objeto de textura](dx-graphics-hlsl-to-type.md)

O Shader Model 4 dá suporte a regras de empacotamento que determinam quão rigidamente os dados podem ser organizados quando são armazenados. Essas regras são descritas em [regras de empacotamento para variáveis constantes](dx-graphics-hlsl-packing-rules.md)

A seção de [assembly do Shader Model 4](dx-graphics-hlsl-sm4-asm.md) descreve as instruções de assembly que o sombreador modelo 4 e suporte ao modelo do sombreador 4,1.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Modelos de sombreador vs. perfis de sombreador](dx-graphics-hlsl-models.md)
</dt> </dl>

 

 




