---
title: dcl_maxOutputVertexCount (sm4-ASM)
description: DCL \_ maxOutputVertexCount (sm4-ASM)
ms.assetid: 91eb2dfc-f4ff-4f23-9cb4-ec5fdb676157
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ba7783575ac5782c63bc1ec3ca5f56f6ffe9a1bc7483f3f01ccbcf8adac5e23f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120068516"
---
# <a name="dcl_maxoutputvertexcount-sm4---asm"></a>DCL \_ maxOutputVertexCount (sm4-ASM)

Declara o número máximo de vértices que podem ser gerados por um sombreador de geometria.



| \_ *contagem* de maxOutputVertexCount de DCL |
|-----------------------------------|



 



| Item                                                               | Descrição                                                             |
|--------------------------------------------------------------------|-------------------------------------------------------------------------|
| <span id="count"></span><span id="COUNT"></span>*contar*<br/> | \[em \] um inteiro sem sinal de 32 bits entre 1 e n, inclusive.<br/> |



 

Um sombreador Geometry pode gerar um máximo de valores de 1024 32 bits. Esse máximo inclui o tamanho dos dados de entrada e o tamanho dos dados criados pelo sombreador.

Aqui estão algumas limitações:

-   Se o número de vértices for atingido antes de concluir a execução do sombreador de geometria, o sombreador será encerrado.
-   Um sombreador Geometry pode alcançar o final de seu programa antes de gerar qualquer vértice; Isso é perfeitamente legal.
-   Se você estiver depurando um sombreador de geometria, poderá informar o número de vértices gerados contando o número de instruções de emissão geradas.

Essa instrução se aplica aos seguintes estágios de sombreador:



| Sombreador de vértice | Sombreador de geometria | Sombreador de pixel |
|---------------|-----------------|--------------|
|               | x               |              |



 

Essa instrução está incluída para auxiliar na depuração de um sombreador no assembly; Você não pode criar um sombreador na linguagem de assembly usando o modelo de sombreador 4.

## <a name="example"></a>Exemplo

Veja alguns exemplos.

Suponha que os dados de entrada sejam compostos de posição (. xyzw) e cor (. RGB). Cada componente consome um byte; dadas 7 bytes, o número máximo de vértices que o sombreador pode gerar seria 1024/(4 + 3) = 146.


```
dcl_maxOutputVertexCount 146
```



Suponha que o sombreador de geometria crie vetores de componentes 32 4. O número máximo de vértices que o sombreador pode gerar seria 1024/(32 \* 4) = 8.


```
dcl_maxOutputVertexCount 8
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

 

 





