---
title: dcl_outputTopology (sm4 – asm)
description: dcl \_ outputTopology (sm4 – asm)
ms.assetid: a03a6feb-ec34-4655-a68c-a91e31e7140b
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: b9648b1b662cb98bc762a479782e4d3742d4d32056fc9f15f43f58f8f4a89659
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117726936"
---
# <a name="dcl_outputtopology-sm4---asm"></a>dcl \_ outputTopology (sm4 – asm)

Declara os dados de saída do sombreador de geometria do tipo primitivo.



| dcl \_ *outputTopology Type* |
|----------------------------|



 



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Item</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="Type"></span><span id="type"></span><span id="TYPE"></span><em>Tipo</em><br/></td>
<td>[in] Uma topologia primitiva de saída, que é um dos seguintes valores: <br/>
<ul>
<li><em>lista de pontos</em></li>
<li><em>linestrip</em></li>
<li><em>trianglestrip</em></li>
</ul></td>
</tr>
</tbody>
</table>



 

Essa instrução se aplica aos seguintes estágios do sombreador:



| Sombreador de vértice | Sombreador de geometria | Sombreador de pixel |
|---------------|-----------------|--------------|
|               | x               |              |



 

Essa instrução é incluída para auxiliar na depuração de um sombreador no assembly; não é possível autor de um sombreador na linguagem de assembly usando o Modelo de Sombreador 4.

## <a name="example"></a>Exemplo

Veja um exemplo.


```
dcl_outputTopology trianglestrip
```



## <a name="minimum-shader-model"></a>Modelo de sombreador mínimo

Essa função tem suporte nos modelos de sombreador a seguir.



| Modelo de Sombreador                                              | Com suporte |
|-----------------------------------------------------------|-----------|
| [Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)        | sim       |
| [Modelo de sombreador 4.1](dx-graphics-hlsl-sm4.md)              | sim       |
| [Modelo de sombreador 4](dx-graphics-hlsl-sm4.md)                | sim       |
| [Modelo de sombreador 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | não        |
| [Modelo de sombreador 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | não        |
| [Modelo de sombreador 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | não        |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Assembly do modelo de sombreador 4 (DirectX HLSL)](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





