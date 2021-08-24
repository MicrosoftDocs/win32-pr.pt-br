---
title: dcl_tgsm_structured (sm5 – asm)
description: Declare uma referência a uma região de espaço de memória compartilhada disponível para o grupo de threads do sombreador de computação. A memória é exibida como uma matriz de estruturas.
ms.assetid: C42CD506-58EB-4740-8403-3F9BF29F0CAE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cc5bf6a6782c455a9bb51ad941a8b6cb42bd70806512a2eef2ed5bd301e57c77
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119673896"
---
# <a name="dcl_tgsm_structured-sm5---asm"></a>dcl \_ tgsm \_ structured (sm5 - asm)

Declare uma referência a uma região de espaço de memória compartilhada disponível para o grupo de threads do sombreador de computação. A memória é exibida como uma matriz de estruturas.



| dcl \_ tgsm \_ structured g , \# structByteStride, structCount |
|----------------------------------------------------------|



 



| Item                                                                                                                                   | Descrição                                                                                                   |
|----------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span id="g_"></span><span id="G_"></span>*G\#*<br/>                                                                             | \[em \] Uma referência a um bloco de memória compartilhada de tamanho *structByteStride* \* *structCount* bytes. <br/> |
| <span id="structByteStride"></span><span id="structbytestride"></span><span id="STRUCTBYTESTRIDE"></span>*structByteStride*<br/> | \[em \] O passo da estrutura. Esse valor é um uint em bytes e deve ser um múltiplo de 4. <br/>           |
| <span id="structCount"></span><span id="structcount"></span><span id="STRUCTCOUNT"></span>*structCount*<br/>                     | \[em \] O número de estruturas.<br/>                                                                   |



 

## <a name="remarks"></a>Comentários

O armazenamento total para todos os g deve ser <= a quantidade de memória compartilhada disponível por grupo de threads, que é de 32kB ou escalares de 32 bits de \# 8192.

Em um caso extremo, você pode declarar 8192 g totais, se cada um tiver um \# *structByteStride* de 4 e um *structCount* de 1.

No extremo oposto, você pode declarar um único g com uma estrutura de \# 32kB e uma contagem de estrutura de 1.

Essa instrução se aplica aos seguintes estágios do sombreador:



| Vértice | Casco | Domínio | Geometry | Pixel | Computação |
|--------|------|--------|----------|-------|---------|
|        |      |        |          |       | X       |



 

## <a name="minimum-shader-model"></a>Modelo de sombreador mínimo

Essa instrução tem suporte nos seguintes modelos de sombreador:



| Modelo de Sombreador                                              | Com suporte |
|-----------------------------------------------------------|-----------|
| [Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)        | sim       |
| [Modelo de sombreador 4.1](dx-graphics-hlsl-sm4.md)              | não        |
| [Modelo de sombreador 4](dx-graphics-hlsl-sm4.md)                | não        |
| [Modelo de sombreador 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | não        |
| [Modelo de sombreador 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | não        |
| [Modelo de sombreador 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | não        |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Assembly do modelo de sombreador 5 (DirectX HLSL)](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





