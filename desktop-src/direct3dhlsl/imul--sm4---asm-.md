---
title: imul (sm4-ASM)
description: Número inteiro com sinal multiplicado.
ms.assetid: DB95A38F-54E4-4BB6-81DF-CFFEBB4D425B
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 87eabcc07dc5c6a662494c71a26c5f60e5fa1053265e3740ad3605ed685771a0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118986486"
---
# <a name="imul-sm4---asm"></a>imul (sm4-ASM)

Número inteiro com sinal multiplicado.



| imul destHI \[ . Mask \] , destLO \[ . Mask \] , \[ - \] src0 \[ . swizzle \] , \[ - \] src1 \[ . swizzle\] |
|-------------------------------------------------------------------------------------|



 



| Item                                                                                           | Descrição                                                      |
|------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <span id="destHI"></span><span id="desthi"></span><span id="DESTHI"></span>*destHI*<br/> | \[no \] endereço dos altos 32 bits do resultado.<br/> |
| <span id="destLO"></span><span id="destlo"></span><span id="DESTLO"></span>*destLO*<br/> | \[no \] endereço dos baixos 32 bits do resultado.<br/>  |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/>                                | \[no \] valor para multiplicar com *src1*.<br/>             |
| <span id="src1"></span><span id="SRC1"></span>*src1*<br/>                                | \[no \] valor para multiplicar com *src0*.<br/>             |



 

## <a name="remarks"></a>Comentários

A multiplicação por componente dos operandos de 32 bits *src0* e *src1* (ambos são assinados), produzindo o resultado completo de 64 bits (por componente) correto. Os bits de 32 baixos (por componente) são colocados em *destLO*. Os bits de 32 altos (por componente) são colocados em *destHI*.

*DestHI* ou *destLO* pode ser especificado como NULL em vez de especificar um registro, se os bits de 32 altos ou baixos do resultado de 64 bits não forem necessários.

O modificador opcional Negate nos operandos de origem usa o complemento de 2 antes de executar a operação aritmética.

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

 

 





