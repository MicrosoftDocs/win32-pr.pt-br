---
title: DP4 (sm4-ASM)
description: quatro pontos de vetor dimensional-produto dos componentes RGBA, POS-swizzle.
ms.assetid: A41EC054-0060-49CA-90FB-A096E63DD27D
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 57a91a253d4e8b53bc044e658c3fe75d8f7547da
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "103916875"
---
# <a name="dp4-sm4---asm"></a>DP4 (sm4-ASM)

quatro pontos de vetor dimensional-produto dos componentes RGBA, POS-swizzle.



| DP4 \[ \_ SAT \] dest \[ . Mask \] , \[ - \] src0 \[ \_ ABS \] \[ . swizzle \] , \[ - \] src1 \[ \_ ABS \] \[ . swizzle \] , |
|---------------------------------------------------------------------------------------------|



 



| Item                                                            | Descrição                                                                                                                                                  |
|-----------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/> | \[no \] resultado da operação. <br/> *dest*  =  *src0. r* \* *src1. r*  +  *src0. g* \* *src1. g* src0. b src1. b  +   \*  +  *src0. a* \* *src1. a*<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[nos \] componentes do operação.<br/>                                                                                                          |
| <span id="src1"></span><span id="SRC1"></span>*src1*<br/> | \[nos \] componentes do operação.<br/>                                                                                                          |



 

## <a name="remarks"></a>Comentários

Resultado escalar replicado para componentes na máscara de gravação.

Essa instrução se aplica aos seguintes estágios de sombreador:



| Sombreador de vértice | Sombreador de geometria | Sombreador de pixel |
|---------------|-----------------|--------------|
| x             | x               | x            |



 

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

 

 





