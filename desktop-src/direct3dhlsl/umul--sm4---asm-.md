---
title: umul (sm4-ASM)
description: Multiplicação de inteiro sem sinal.
ms.assetid: C84AF349-32E6-40C4-9973-BCFA73EFBF0B
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1ec63b3a95ffbdf1f71142c9fc508e21e718b44d988b725dad5d73775746871c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117721830"
---
# <a name="umul-sm4---asm"></a>umul (sm4-ASM)

Multiplicação de inteiro sem sinal.



| umul destHI \[ . Mask \] , destLO \[ . Mask \] , src0 \[ . swizzle \] , src1 \[ . swizzle\] |
|---------------------------------------------------------------------------|



 



| Item                                                                                           | Descrição                                                      |
|------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <span id="destHI"></span><span id="desthi"></span><span id="DESTHI"></span>*destHI*<br/> | \[nos \] altos 32 bits do resultado, por componente.<br/> |
| <span id="destLO"></span><span id="destlo"></span><span id="DESTLO"></span>*destLO*<br/> | \[nos \] poucos 32 bits do resultado, por componente.<br/>  |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/>                                | \[nos \] componentes pelos quais multiplicar *src1*.<br/>    |
| <span id="src1"></span><span id="SRC1"></span>*src1*<br/>                                | \[nos \] componentes pelos quais multiplicar *src0*.<br/>    |



 

## <a name="remarks"></a>Comentários

Essa instrução executa uma multiplicação por componente de operandos de 32 bits não assinados *src0* e *src1*, produzindo o resultado de 64 de bits completo correto por componente. Os baixos 32 bits por componente são colocados em *destLO*. Os bits de 32 altos por componente são colocados em *destHI*.

Você pode especificar *destHI* ou *destLO* como NULL em vez de especificar um registro se os bits de 32 altos ou baixos do resultado de 64 bits não forem necessários.

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

 

 





