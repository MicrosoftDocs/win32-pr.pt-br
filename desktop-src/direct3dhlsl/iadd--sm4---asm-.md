---
title: IAdd (sm4-ASM)
description: Adição de inteiro.
ms.assetid: EF78EA65-DC16-469A-9E45-52844FF4BD93
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9226223b5a065714ca17bd63775b8d4e8a3bc9b96de111cec87b879114728bf6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118285785"
---
# <a name="iadd-sm4---asm"></a>IAdd (sm4-ASM)

Adição de inteiro.



| IAdd dest \[ . Mask \] , \[ - \] src0 \[ . swizzle \] , \[ - \] src1 \[ . swizzle\] |
|------------------------------------------------------------------|



 



| Item                                                            | Descrição                                                   |
|-----------------------------------------------------------------|---------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/> | \[no \] endereço do resultado da operação.<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[no \] número a ser adicionado ao *src1*.<br/>           |
| <span id="src1"></span><span id="SRC1"></span>*src1*<br/> | \[no \] número a ser adicionado ao *src0*.<br/>           |



 

## <a name="remarks"></a>Comentários

Adição de componente de operandos de 32 bits *src0* e *src1*, colocando o resultado de 32 bits correto no *dest*. Nenhum transporte ou empréstimo além dos valores de 32 bits de cada componente é executado, portanto, essa instrução não é sensível à qualidade de seus operandos.

O modificador opcional Negate nos operandos de origem usa o complemento de 2 antes de executar a operação.

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
| [Modelo de sombreador 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | no        |
| [Modelo de sombreador 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | no        |
| [Modelo de sombreador 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | no        |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Assembly do Shader Model 4 (DirectX HLSL)](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





