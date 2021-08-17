---
title: dcl_thread_group (SM5-ASM)
description: Declare o tamanho do grupo de threads.
ms.assetid: CB8192C4-100D-49B6-94E7-6CD3AEC28149
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5402e53e2252d8019ba553c6a8ff449200625b1469ee923f3c26234f1faa292e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118515474"
---
# <a name="dcl_thread_group-sm5---asm"></a>\_grupo de threads DCL \_ (SM5-ASM)

Declare o tamanho do grupo de threads.



| \_grupo de threads DCL \_ x, y, z |
|----------------------------|



 



| Item                                                   | Descrição                                                        |
|--------------------------------------------------------|--------------------------------------------------------------------|
| <span id="x"></span><span id="X"></span>*w.x.y.*<br/> | \[em \] um número inteiro de usigned de 32 bits. 1 <= x <= 1024 <br/> |
| <span id="y"></span><span id="Y"></span>*Iar*<br/> | \[em \] um número inteiro de usigned de 32 bits. 1 <= y <= 1024<br/>  |
| <span id="z"></span><span id="Z"></span>*z*<br/> | \[em \] um número inteiro de usigned de 32 bits. 1 <= z <= 64<br/>    |



 

## <a name="remarks"></a>Comentários

x \* y \* z <= 1024

Essa declaração de grupo de threads deve aparecer uma vez em um sombreador de computação.

Essa instrução se aplica aos seguintes estágios de sombreador:



| Vértice | Envoltória | Domínio | Geometry | 16x16 | Computação |
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

 

 





