---
title: udiv (sm4-ASM)
description: Divisão de inteiro sem sinal.
ms.assetid: 87C81418-0F74-4C67-9D4A-DA952EFD008E
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 07a3dd2f4170a3c8fe522af12d412cfae49396da
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104365229"
---
# <a name="udiv-sm4---asm"></a>udiv (sm4-ASM)

Divisão de inteiro sem sinal.



| udiv destQUOT \[ . Mask \] , destREM \[ . Mask \] , src0 \[ . swizzle \] , src1 \[ . swizzle\] |
|------------------------------------------------------------------------------|



 



| Item                                                                                                   | Descrição                                                |
|--------------------------------------------------------------------------------------------------------|------------------------------------------------------------|
| <span id="destQUOT"></span><span id="destquot"></span><span id="DESTQUOT"></span>*destQUOT*<br/> | \[no \] endereço do quociente resultante.<br/>   |
| <span id="destREM"></span><span id="destrem"></span><span id="DESTREM"></span>*destREM*<br/>     | \[no \] endereço do restante resultante.<br/>  |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/>                                        | \[nos \] componentes a serem divididos por *src1*.<br/>  |
| <span id="src1"></span><span id="SRC1"></span>*src1*<br/>                                        | \[nos \] componentes de qual para dividir *src0*.<br/> |



 

## <a name="remarks"></a>Comentários

Essa instrução executa uma divisão não assinada por componente do operando de 32 bits *src0* pelo operando de 32 bits *src1*. Os resultados das divisões são os quocientes de 32 bits colocados em *destQUOT* e os restantes de 32 bits colocados em *destREM*.

A divisão por zero retorna 0xFFFFFFFF para o quociente e o resto.

Você pode especificar *destQUOT* ou *destREM* como NULL em vez de especificar um registro, se o quociente ou o resto não forem necessários.

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

 

 





