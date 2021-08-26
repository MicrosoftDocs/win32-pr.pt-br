---
title: udiv (sm4 – asm)
description: Divisão de inteiro sem sinal.
ms.assetid: 87C81418-0F74-4C67-9D4A-DA952EFD008E
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 87b1320d0518034129efe2222a42aa2694df0422db524da0714377cb43a2b9a0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119948976"
---
# <a name="udiv-sm4---asm"></a>udiv (sm4 – asm)

Divisão de inteiro sem sinal.



| udiv destQUOT \[ \] .mask, destREM \[ \] .mask, src0 \[ .swizzle, \] src1 \[ .swizzle\] |
|------------------------------------------------------------------------------|



 



| Item                                                                                                   | Descrição                                                |
|--------------------------------------------------------------------------------------------------------|------------------------------------------------------------|
| <span id="destQUOT"></span><span id="destquot"></span><span id="DESTQUOT"></span>*destQUOT*<br/> | \[em \] O endereço do quociente resultante.<br/>   |
| <span id="destREM"></span><span id="destrem"></span><span id="DESTREM"></span>*destREM*<br/>     | \[em \] O endereço do resto resultante.<br/>  |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/>                                        | \[em \] Os componentes a serem divididos *por src1*.<br/>  |
| <span id="src1"></span><span id="SRC1"></span>*src1*<br/>                                        | \[em \] Os componentes por whch para dividir *src0*.<br/> |



 

## <a name="remarks"></a>Comentários

Essa instrução executa uma divisão sem assinatura por componente do *src0* do operand de 32 bits pelo *src1* do operand de 32 bits. Os resultados das divisãos são os quocientes de 32 bits colocados em *destQUOT* e os restantes de 32 bits colocados *em destREM.*

Dividir por zero retorna 0xffffffff para quociente e resto.

Você pode especificar *destQUOT* ou *destREM* como NULL em vez de especificar um registro, se o quociente ou o restante não for necessário.

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

 

 





