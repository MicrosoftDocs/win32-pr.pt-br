---
title: dcl_inputPrimitive (sm4-ASM)
description: DCL \_ inputPrimitive (sm4-ASM)
ms.assetid: 86672fd3-7955-45ac-a8b2-a9cc8d1e8805
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 0660fe4da14a20f074e4f04de8891fc0848f2597
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122479892"
---
# <a name="dcl_inputprimitive-sm4---asm"></a>DCL \_ inputPrimitive (sm4-ASM)

Declara o tipo primitivo para entradas Geometry-Shader.



| \_ *tipo* de inputPrimitive de DCL |
|----------------------------|



 




| Item | Descrição | 
|------|-------------|
| <span id="type"></span><span id="TYPE"></span><em>Escreva</em><br /> | no Tipo primitivo de dados de entrada, que é um dos seguintes: <br /><ul><li>lista de pontos de <em>extremidade</em></li><li>lista de linhas de <em>linha</em></li><li><em>triângulo</em> – lista de triângulo</li><li>lista de linhas de <em>line_adj</em> com dados de adjacência</li><li>lista de <em>triangle_adj</em> de triângulo com dados de adjacência</li></ul> | 




 

Essa instrução se aplica aos seguintes estágios de sombreador:



| Sombreador de vértice | Sombreador de geometria | Sombreador de pixel |
|---------------|-----------------|--------------|
|               | x               |              |



 

Essa instrução está incluída para auxiliar na depuração de um sombreador no assembly; Você não pode criar um sombreador na linguagem de assembly usando o modelo de sombreador 4.

## <a name="example"></a>Exemplo

Veja um exemplo.


```
dcl_inputPrimitive triangle
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

 

 





