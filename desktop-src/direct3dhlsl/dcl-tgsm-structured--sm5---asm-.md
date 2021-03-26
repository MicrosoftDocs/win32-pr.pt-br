---
title: dcl_tgsm_structured (SM5-ASM)
description: Declare uma referência a uma região de espaço de memória compartilhada disponível para o grupo de threads do sombreador de computação. A memória é exibida como uma matriz de estruturas.
ms.assetid: C42CD506-58EB-4740-8403-3F9BF29F0CAE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9a639d31c4449a0dfeb152c06b35cfb86c5cc30a
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104988573"
---
# <a name="dcl_tgsm_structured-sm5---asm"></a>DCL \_ tgsm \_ estruturado (SM5-ASM)

Declare uma referência a uma região de espaço de memória compartilhada disponível para o grupo de threads do sombreador de computação. A memória é exibida como uma matriz de estruturas.



| DCL \_ tgsm \_ estruturado g \# , structByteStride, structCount |
|----------------------------------------------------------|



 



| Item                                                                                                                                   | Descrição                                                                                                   |
|----------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span id="g_"></span><span id="G_"></span>*m\#*<br/>                                                                             | \[em \] uma referência a um bloco de memória compartilhada de tamanho *structByteStride* \* *structCount* bytes. <br/> |
| <span id="structByteStride"></span><span id="structbytestride"></span><span id="STRUCTBYTESTRIDE"></span>*structByteStride*<br/> | \[no \] Stride da estrutura. Esse valor é um UINT em bytes e deve ser um múltiplo de 4. <br/>           |
| <span id="structCount"></span><span id="structcount"></span><span id="STRUCTCOUNT"></span>*structCount*<br/>                     | \[no \] número de estruturas.<br/>                                                                   |



 

## <a name="remarks"></a>Comentários

O armazenamento total para todos os g \# deve ser <= a quantidade de memória compartilhada disponível por grupo de threads, que é 32 KB ou escalares de 8192 32 bits.

Em um caso extremo, você pode declarar o total de 8192 g \# s, se cada um tiver um *structByteStride* de 4 e um *structCount* de 1.

No lado oposto, você pode declarar um g único \# com um stride de estrutura de 32 KB e uma contagem de estrutura de 1.

Essa instrução se aplica aos seguintes estágios de sombreador:



| Vértice | Envoltória | Domínio | Geometria | 16x16 | Computação |
|--------|------|--------|----------|-------|---------|
|        |      |        |          |       | X       |



 

## <a name="minimum-shader-model"></a>Modelo de sombreamento mínimo

Essa instrução tem suporte nos seguintes modelos de sombreador:



| Modelo de Sombreador                                              | Com suporte |
|-----------------------------------------------------------|-----------|
| [Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)        | sim       |
| [Modelo do sombreador 4,1](dx-graphics-hlsl-sm4.md)              | não        |
| [Modelo de sombreador 4](dx-graphics-hlsl-sm4.md)                | não        |
| [Modelo de sombreador 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | não        |
| [Modelo de sombreador 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | não        |
| [Modelo de sombreador 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | não        |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Assembly do Shader Model 5 (DirectX HLSL)](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





