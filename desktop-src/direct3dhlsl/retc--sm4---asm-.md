---
title: retc (sm4-ASM)
description: Retorno condicional.
ms.assetid: D936099D-4A75-4AE2-9FE3-70ED213DF4D9
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d68d65cf64c3c1fb7945f93053f280be3eb3bd9d5fe76e34f30102316b1f1e8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119853736"
---
# <a name="retc-sm4---asm"></a>retc (sm4-ASM)

Retorno condicional.



| retc { \_ z \|\_NZ} src0. Select \_ componente |
|----------------------------------------|



 



| Item                                                            | Descrição                                                   |
|-----------------------------------------------------------------|---------------------------------------------------------------|
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[no \] registro para testar a condição.<br/> |



 

## <a name="remarks"></a>Comentários

Se dentro de uma sub-rotina, essa instrução retorna condicionalmente para a instrução após a chamada. Se não estiver dentro de uma sub-rotina, essa instrução encerrará a execução do programa.

O exemplo a seguir mostra como usar essa instrução.

``` syntax
           ...
           call l3
           ...
           ret
           label l3
               ...
               retc_nz r0.x  // If any bit in r0.x is nonzero, then return
               retc_z  r1.x  // If all bits in r0.x are zero, then return.
               ...
           ret
```

### <a name="restrictions"></a>Restrições

-   **retc** podem aparecer em qualquer lugar em um programa, várias vezes.
-   A última instrução em um programa principal ou uma sub-rotina não pode ser um **\_ NZ** **retc \_ z** ou retc. Em vez disso, a [RET](ret--sm4---asm-.md) incondicional pode ser usada.
-   O registro de 32 bits fornecido pelo *src0* é testado em um nível de bit. Se algum bit for diferente de zero, a **RET \_ NZ** retornará. Se todos os bits forem zero, **retc \_ z** retornará.

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

 

 





