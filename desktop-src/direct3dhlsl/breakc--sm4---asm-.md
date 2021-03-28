---
title: breakc (sm4-ASM)
description: Move condicionalmente o ponto de execução para a instrução após o próximo loop Endou endswitch.
ms.assetid: 5735EF88-1E8C-4142-8442-9328D78999A7
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 019a1c859f7d1e0ee6368f5b9984775ef9bfaba1
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104365243"
---
# <a name="breakc-sm4---asm"></a>breakc (sm4-ASM)

Move condicionalmente o ponto de execução para a instrução após o próximo [loop](endloop--sm4---asm-.md) Endou [endswitch](endswitch--sm4---asm-.md).



| breakc { \_ z \|\_NZ} src0. Select \_ componente |
|------------------------------------------|



 



| Item                                                            | Descrição                                                     |
|-----------------------------------------------------------------|-----------------------------------------------------------------|
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[no \] componente no qual testar a condição.<br/> |



 

## <a name="remarks"></a>Comentários

O formato do token contém o deslocamento da instrução **ENDLOOP** correspondente no sombreador como uma conveniência.

O exemplo a seguir mostra a instrução **breakc** .


```
                loop
                    // example of termination condition
                    breakc_z  r0.x // break if all bits in r0.x are 0
                    breakc_nz r1.x // break if any bit in r1.x is nonzero
                    ...
                endloop

```



Essa instrução deve aparecer em um **loop** / **ENDLOOP** ou **alternar** / **endswitch**.

O registro de 32 bits fornecido pelo *src0* é testado em um nível de bit. Se algum bit for diferente de zero, **breakc \_ NZ** executará a interrupção. Se todos os bits forem zero, o **breakc \_ z** executará a interrupção.

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

 

 





