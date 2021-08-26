---
title: dcl_output oMask (SM5-ASM)
description: Declare um registro de saída para ser gravado pelo sombreador.
ms.assetid: 23FC5FA3-F550-4CD1-9AA9-86738818686F
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a6860904b557bc21a5202bbfd60105852adc260580457afb02b4fe6d92352b5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120068506"
---
# <a name="dcl_output-omask-sm5---asm"></a>\_oMask de saída DCL (SM5-ASM)

Declare um registro de saída para ser gravado pelo sombreador.



| DCL \_ saída o \# \[ . Mask\] |
|--------------------------|



 



| Item                                                   | Descrição                            |
|--------------------------------------------------------|----------------------------------------|
| <span id="o"></span><span id="O"></span>*minúscula*<br/> | \[no \] registro de saída.<br/> |



 

## <a name="remarks"></a>Comentários


```
Example:
                dcl_output o[3].xyz
```



### <a name="restrictions"></a>Restrições

-   A máscara de componente pode ser qualquer subconjunto de \[ xyzw \] . No entanto, deixar as lacunas entre os componentes desperdiça espaço.
-   É legal declarar um superconjunto da máscara do componente declarado para entrada pelo próximo estágio. No entanto, as máscaras mutuamente exclusivas não são permitidas. O sombreador de vértice gerando O3. XY, significa que o sombreador de pixel inserindo v3. z é inválido, mas inserindo v3. x ou v3. y ou v3. XY é válido.

Essa instrução se aplica aos seguintes estágios de sombreador:



| Vértice | Envoltória | Domínio | Geometry | 16x16 | Computação |
|--------|------|--------|----------|-------|---------|
| X      | X    | X      | X        | X     |         |



 

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

 

 





