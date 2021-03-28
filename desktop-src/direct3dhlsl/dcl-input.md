---
title: dcl_input (sm4-ASM)
description: '\_entrada DCL (sm4-ASM)'
ms.assetid: 13456f2a-ee6c-42da-a9fe-670ab0fcbddf
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 400a1d47b6e0f9d82ec662553c36629deb4b1f0b
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104988620"
---
# <a name="dcl_input-sm4---asm"></a>\_entrada DCL (sm4-ASM)

Declara um inregistrador de entrada de sombreador.



| \_entrada DCL v *N \[ . Mask \] \[ , interpolação \]* |
|-------------------------------------------------|



 



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
<td><span id="interpolationMode"></span><span id="interpolationmode"></span><span id="INTERPOLATIONMODE"></span><em>interpolação</em><br/></td>
<td>[in] Opcional. O modo de interpolação, que é respeitado apenas em registros de entrada do sombreador de pixel. Pode ser um dos seguintes valores: <br/>
<ul>
<li>constante-não interpolar entre valores de registro.</li>
<li>interpolar linearmente entre valores de registro.</li>
<li>linearCentroid-o mesmo que linear, mas de centróide clamped quando há multiamostragens.</li>
<li>linearNoperspective-igual à linear, mas sem correção de perspectiva.</li>
<li>linearNoperspectiveCentroid-igual à linear, centróide clamped quando há multiamostragens, sem correção de perspectiva.</li>
</ul></td>
</tr>
</tbody>
</table>



 

### <a name="interpolation-notes"></a>Notas de interpolação

Por padrão, os atributos de vértice são interpolados de um centro de pixels ao executar a suavização de multiamostras. Se um pixel Center não for coberto, um atributo será extrapolado para um pixel Center antes da interpolação.

Para um pixel que não está totalmente coberto ou um atributo que não cobre um pixel Center, você pode especificar a amostragem de centróide que força a amostragem a ocorrer em algum lugar dentro da área coberta do pixel. Como uma máscara de exemplo (se usada) é aplicada antes de o centróide ser computado, qualquer local de exemplo mascarado pela máscara de exemplo não pode ser escolhido como um local de centróide.

Essa instrução se aplica aos seguintes estágios de sombreador:



| Sombreador de vértice | Sombreador de geometria | Sombreador de pixel |
|---------------|-----------------|--------------|
| x             | x               | x            |



 

Para identificar a entrada como um valor do sistema, [use \_ a entrada DCL \_ VA (sm4-ASM)](dcl-input-sv.md).

Essa instrução está incluída para auxiliar na depuração de um sombreador no assembly; Você não pode criar um sombreador na linguagem de assembly usando o modelo de sombreador 4.

## <a name="example"></a>Exemplo

Aqui estão alguns exemplos.


```
dcl_input v3.xyz

dcl_input v0.x, linearCentroid
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

 

 





