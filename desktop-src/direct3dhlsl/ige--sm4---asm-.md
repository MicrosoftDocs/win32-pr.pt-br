---
title: ige (sm4 – asm)
description: Comparação de inteiro de vetor maior ou igual a componente.
ms.assetid: 3A3225D1-9A3D-4928-9041-38CB6DE16E2A
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 15de044678d61adea52607166c622e6fb5dc20211499de4c11066e6688216910
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119982416"
---
# <a name="ige-sm4---asm"></a>ige (sm4 – asm)

Comparação de inteiro de vetor maior ou igual a componente.



| ige dest \[ \] .mask, src0 \[ .swizzle, \] src1 \[ .swizzle\] |
|-------------------------------------------------------|



 



| Item                                                            | Descrição                                           |
|-----------------------------------------------------------------|-------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*Dest*<br/> | \[em \] O resultado da operação.<br/>        |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[em \] O componente a ser comparado com *src1*.<br/> |
| <span id="src1"></span><span id="SRC1"></span>*src1*<br/> | \[em \] O componente a ser comparado com *src0*.<br/> |



 

## <a name="remarks"></a>Comentários

Executa a comparação de inteiros (*src0*  >=  *src1*) para cada componente e grava o resultado *em dest*.

Se a comparação for verdadeira, 0xFFFFFFFF será retornado para esse componente. Caso contrário 0x0000000 será retornado.

Essa instrução se aplica aos seguintes estágios do sombreador:



| Sombreador de vértice | Sombreador de geometria | Sombreador de pixel |
|---------------|-----------------|--------------|
| x             | x               | x            |



 

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

 

 





