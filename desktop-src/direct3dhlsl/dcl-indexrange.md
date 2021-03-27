---
title: dcl_indexRange (sm4-ASM)
description: DCL \_ indexRange (sm4-ASM)
ms.assetid: 88af30f3-dbf9-4556-b170-a7371680f9b9
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 5b0e2c250afd4ce52729a4c4bffeee0f33e4be6b
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104967137"
---
# <a name="dcl_indexrange-sm4---asm"></a>DCL \_ indexRange (sm4-ASM)

Declara um intervalo de registros que serão acessados pelo índice (um inteiro calculado no sombreador).



| DCL \_ IndexRange *minRegisterM*, *maxRegisterN* |
|------------------------------------------------|



 



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
<td><span id="minRegisterM"></span><span id="minregisterm"></span><span id="MINREGISTERM"></span><em>minRegisterM</em><br/></td>
<td>no O primeiro registro a ser acessado pelo índice. <br/>
<ul>
<li><em>minRegister</em> é <strong>v</strong> para um vértice ou registro de entrada de sombreador de pixel ou <strong>o</strong> para um registro de saída de sombreador de vértice.</li>
<li><em>M</em> é um inteiro que denota o número do registro.</li>
</ul></td>
</tr>
<tr class="even">
<td><span id="maxRegisterN"></span><span id="maxregistern"></span><span id="MAXREGISTERN"></span><em>maxRegisterN</em><br/></td>
<td>no O último registro a ser acessado por índice. A mesma forma que <em>minRegister</em> , exceto <em>N</em> é o número de registrador.<br/></td>
</tr>
</tbody>
</table>



 

As seguintes restrições se aplicam a todos os registros:

-   Os registros mínimo e máximo devem ser do mesmo tipo e ter as mesmas máscaras de componente (se as máscaras forem declaradas).
-   Um registro pode ter vários intervalos de índice, desde que não haja sobreposição.
-   O número de registro mínimo deve ser menor que o número de registro máximo.
-   Um registro de índice não pode conter um [valor de sistema](dx-graphics-hlsl-semantics.md).
-   A indexação de um registro fora da declaração de índice máximo produz resultados indefinidos.

Os registros de entrada do sombreador de pixel devem usar o mesmo modo de interpolação; os registros de saída do sombreador de pixel não podem ser indexados.

Um registro de entrada do sombreador de geometria tem duas dimensões (eixo de vértice, eixo de atributo); o intervalo de índice aplica-se somente ao eixo de atributo porque o eixo de vértice é sempre totalmente indexável.

Essa instrução se aplica aos seguintes estágios de sombreador:



| Sombreador de vértice | Sombreador de geometria | Sombreador de pixel |
|---------------|-----------------|--------------|
| x             | x               | x            |



 

Essa instrução está incluída para auxiliar na depuração de um sombreador no assembly; Você não pode criar um sombreador na linguagem de assembly usando o modelo de sombreador 4.

## <a name="example"></a>Exemplo

Veja um exemplo.


```
dcl_indexRange v1, v3
dcl_indexRange v4, v9
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

 

 





