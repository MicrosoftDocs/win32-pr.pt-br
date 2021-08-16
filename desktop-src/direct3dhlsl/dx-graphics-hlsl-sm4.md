---
title: Modelo de sombreador 4
description: O Modelo de Sombreador 4 é um superconjunto dos recursos no Modelo de Sombreador 3, exceto que o Modelo de Sombreador 4 não dá suporte aos recursos no Modelo de Sombreador 1.
ms.assetid: 76155749-11e9-41ff-881d-8f77f2729364
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: d90444aff674ce876f19f02f21104dd7e42143de5926ba068bbe2c49f427fdde
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117725883"
---
# <a name="shader-model-4"></a>Modelo de sombreador 4

O Modelo de Sombreador 4 é um superconjunto dos recursos no Modelo de Sombreador [3,](dx-graphics-hlsl-sm3.md)exceto pelo fato de que o Modelo de Sombreador 4 não dá suporte aos recursos no Modelo de Sombreador 1. Ele foi projetado usando um núcleo de sombreador comum que fornece um conjunto comum de recursos para todos os sombreadores programáveis, que só são programáveis usando HLSL.



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
<td>O conjunto de registros é acessível por meio de membros em buffers constantes e de textura usando semântica HLSL para coisas como empacotamento de componentes.
<ul>
<li>Registros de sombreador de pixel (consulte <a href="dx-graphics-hlsl-sm4-registers-ps-4-0.md">Registros ps_4_0</a> e Registros <a href="dx-graphics-hlsl-sm4-registers-ps-4-1.md">– ps_4_1</a>)</li>
<li>Registros de sombreador de vértice (consulte <a href="dx-graphics-hlsl-sm4-registers-vs-4-0.md">Registros - vs_4_0</a> e Registros - <a href="dx-graphics-hlsl-sm4-registers-vs-4-1.md">vs_4_1</a>)</li>
<li>Registros de sombreador geometry (consulte <a href="dx-graphics-hlsl-sm4-registers-gs-4-0.md">Registros - gs_4_0</a> e Registros - <a href="dx-graphics-hlsl-sm4-registers-gs-4-1.md">gs_4_1</a>)</li>
</ul></td>
</tr>
<tr class="odd">
<td>Máx. de sombreador de vértice</td>
<td>Nenhuma restrição</td>
</tr>
<tr class="even">
<td>Pixel Shader Max</td>
<td>Nenhuma restrição</td>
</tr>
<tr class="odd">
<td>Novos perfis de sombreador adicionados</td>
<td>gs_4_0, ps_4_0, vs_4_0,*gs_4_1, ps_4_1,* gs_4_1*</td>
</tr>
<tr class="even">
<td>Novo perfil Effect-Framework adicionado</td>
<td>fx_4_0, fx_4_1*</td>
</tr>
</tbody>
</table>



 

\* - gs \_ 4 \_ 1, ps \_ 4 \_ 1, vs 4 1 e fx 4 1 têm suporte no \_ \_ \_ \_ Direct3D 10.1 ou superior.

O Modelo de Sombreador 4 dá suporte a um novo estágio de pipeline , o estágio de sombreador de geometria, que pode ser usado para criar ou modificar a geometria existente. Ele também inclui dois novos tipos de objeto: um objeto de saída de fluxo projetado para transmitir dados fora do estágio de geometria e um objeto de textura modelo que implementa funções de amostragem de textura.

-   [Common-Shader Core](dx-graphics-hlsl-common-core.md)
-   [Constantes](dx-graphics-hlsl-constants.md)
-   [Objeto Geometry-Shader](dx-graphics-hlsl-geometry-shader.md)
-   [Objeto Stream-Output](dx-graphics-hlsl-so-type.md)
-   [Objeto texture](dx-graphics-hlsl-to-type.md)

O Modelo de Sombreador 4 dá suporte a regras de empacotamento que determinam como os dados podem ser organizados quando são armazenados. Essas regras são descritas em [Regras de empacotamento para variáveis constantes](dx-graphics-hlsl-packing-rules.md)

A [seção Assembly do Modelo de Sombreador 4](dx-graphics-hlsl-sm4-asm.md) descreve as instruções de assembly que o Modelo de Sombreador 4 e o Modelo de Sombreador 4.1 suportam.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Modelos de sombreador versus perfis de sombreador](dx-graphics-hlsl-models.md)
</dt> </dl>

 

 




