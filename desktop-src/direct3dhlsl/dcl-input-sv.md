---
title: dcl_input_sv (sm4-ASM)
description: '\_entrada DCL \_ VA (sm4-ASM)'
ms.assetid: 59270148-e2eb-4525-a888-ad7e843d62a5
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 650196dff224259f48d1471f3005f95ec0de9c8b
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "103638897"
---
# <a name="dcl_input_sv-sm4---asm"></a>\_entrada DCL \_ VA (sm4-ASM)

Declara um registro de entrada de sombreador que espera que um [valor de sistema](dx-graphics-hlsl-semantics.md) seja fornecido de um estágio anterior.



| \_entrada DCL \_ VA v *N \[ . Mask \]* *\[ \] , systemValueName, interpolamode* |
|------------------------------------------------------------------------|



 



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
<td><span id="vN_.mask_"></span><span id="vn_.mask_"></span><span id="VN_.MASK_"></span>v<em>N [. Mask]</em><br/></td>
<td>no Um registro de dados de vértice. <br/>
<ul>
<li><em>N</em> é um inteiro que identifica o número do registro.</li>
<li><em>[. Mask]</em> é uma máscara de componente opcional (. xyzw) que especifica qual dos componentes de registro usar.</li>
</ul></td>
</tr>
<tr class="even">
<td><span id="systemValueName"></span><span id="systemvaluename"></span><span id="SYSTEMVALUENAME"></span><em>systemValueName</em><br/></td>
<td>no O nome do valor do sistema que é uma cadeia de caracteres (consulte a <a href="dx-graphics-hlsl-semantics.md">semântica do valor do sistema</a>) sem o prefixo de &quot; SV_ &quot; .<br/></td>
</tr>
<tr class="odd">
<td><span id="interpolationMode"></span><span id="interpolationmode"></span><span id="INTERPOLATIONMODE"></span><em>interpolação</em><br/></td>
<td>[in] Opcional. O modo de interpolação que afeta como os valores são calculados durante a rasterização; o modo é usado apenas por um sombreador de pixel. Pode ser um dos seguintes valores: <br/>
<ul>
<li>constante-não interpolar entre valores de registro.</li>
<li>interpolar linearmente entre valores de registro.</li>
<li>linearCentroid-o mesmo que linear, mas de centróide clamped quando há multiamostragens.</li>
<li>linearNoperspective-igual à linear, mas sem correção de perspectiva.</li>
<li>linearNoperspectiveCentroid – o mesmo que linear, mas sem correção de perspectiva e centróide clamped quando há multiamostragens.</li>
</ul></td>
</tr>
</tbody>
</table>



 

Uma máscara de componente para uma declaração de valor de sistema pode ser qualquer subconjunto apropriado de \[ xyzw \] ; declarações não podem se sobrepor (cada declaração deve seguir a sequência xyzw). Ao declarar valores de sistema escalares (distância de corte e distância de busca, por exemplo), você pode declarar vários valores de sistema em um único registro. Se você fizer isso, certifique-se de que outros modificadores, como os modos de interpolação coincidam.

Essa instrução se aplica aos seguintes estágios de sombreador:



| Sombreador de vértice | Sombreador de geometria | Sombreador de pixel |
|---------------|-----------------|--------------|
| x             | x               | x            |



 

Essa instrução está incluída para auxiliar na depuração de um sombreador no assembly; Você não pode criar um sombreador na linguagem de assembly usando o modelo de sombreador 4.

## <a name="example"></a>Exemplo

Estes são alguns exemplos:


```
// valid
dcl_input v0.y, linear
dcl_input_sv v0.w, clipDistance
dcl_input_sv v0.z, cullDistance
```




```
// invalid declarations
dcl_input v0.y, linear
dcl_input_sv v0.x, clipDistance  // the y component was previously declared, this declaration must use 
                                 // either the z or w component

dcl_input v0.y, linearNoPerspective                  // the interpolation mode is linear-no-perspective
dcl_input_sv v0.z, renderTargetArrayIndex, constant  // the interpolation modes is constant
                                                     // the interpolation modes must match
```



## <a name="minimum-shader-model"></a>Modelo de sombreamento mínimo

Essa função tem suporte nos seguintes modelos de sombreador.



| Modelo de Sombreador                                              | Com suporte |
|-----------------------------------------------------------|-----------|
| [Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)        | sim       |
| [Modelo do sombreador 4,1](dx-graphics-hlsl-sm4.md)              | sim       |
| [Modelo de sombreador 4](dx-graphics-hlsl-sm4.md)                | sim       |
| [Modelo de sombreador 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | não        |
| [Modelo de sombreador 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | não        |
| [Modelo de sombreador 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | não        |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Assembly do Shader Model 4 (DirectX HLSL)](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





