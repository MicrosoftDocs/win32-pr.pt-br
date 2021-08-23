---
title: breakc (sm4 – asm)
description: Move condicionalmente o ponto de execução para a instrução após o próximo endloop ou endswitch.
ms.assetid: 5735EF88-1E8C-4142-8442-9328D78999A7
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1eff9be2428db0d0df24879f50964ce14f6831e235c54655958d9401224d7225
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119626466"
---
# <a name="breakc-sm4---asm"></a>breakc (sm4 – asm)

Move condicionalmente o ponto de execução para a instrução após o próximo [endloop](endloop--sm4---asm-.md) ou [endswitch](endswitch--sm4---asm-.md).



| breakc{ \_ z\|\_Componente nz} src0.select \_ |
|------------------------------------------|



 



| Item                                                            | Descrição                                                     |
|-----------------------------------------------------------------|-----------------------------------------------------------------|
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[no \] componente no qual testar a condição.<br/> |



 

## <a name="remarks"></a>Comentários

O formato de token contém o deslocamento da instrução **endloop** correspondente no Sombreador como uma conveniência.

O exemplo a seguir mostra a **instrução breakc.**


```
                loop
                    // example of termination condition
                    breakc_z  r0.x // break if all bits in r0.x are 0
                    breakc_nz r1.x // break if any bit in r1.x is nonzero
                    ...
                endloop

```



Essa instrução deve aparecer dentro de **um endloop de loop** ou de /   / **terminações de com alternação**.

O registro de 32 bits fornecido pelo *src0* é testado em um nível de bit. Se algum bit for diferente de zero, **breakc \_ nz** executará a quebra. Se todos os bits são zero, **breakc \_ z** executará a quebra.

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

 

 





