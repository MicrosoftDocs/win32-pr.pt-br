---
title: dcl_outputTopology (sm4-ASM)
description: DCL \_ outputTopology (sm4-ASM)
ms.assetid: a03a6feb-ec34-4655-a68c-a91e31e7140b
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: f6a3b46dc226a85593a17b02118ed52088ed75d6
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122471992"
---
# <a name="dcl_outputtopology-sm4---asm"></a>DCL \_ outputTopology (sm4-ASM)

Declara os dados de saída do tipo primitivo Geometry-Shader.



| \_ *tipo* de outputTopology de DCL |
|----------------------------|



 




| Item | Descrição | 
|------|-------------|
| <span id="Type"></span><span id="type"></span><span id="TYPE"></span><em>Escreva</em><br /> | no Uma topologia primitiva de saída, que é um dos seguintes valores: <br /><ul><li><em>ponto da</em></li><li><em>linestrip</em></li><li><em>trianglestrip</em></li></ul> | 




 

Essa instrução se aplica aos seguintes estágios de sombreador:



| Sombreador de vértice | Sombreador de geometria | Sombreador de pixel |
|---------------|-----------------|--------------|
|               | x               |              |



 

Essa instrução está incluída para auxiliar na depuração de um sombreador no assembly; Você não pode criar um sombreador na linguagem de assembly usando o modelo de sombreador 4.

## <a name="example"></a>Exemplo

Veja um exemplo.


```
dcl_outputTopology trianglestrip
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

 

 





