---
title: bufinfo (SM5-ASM)
description: Consultar a contagem de elementos em um buffer (mas não no buffer de constantes).
ms.assetid: 3A5C28F3-FE59-4C67-92AC-66B10E1D9692
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a107896973e7457b4bf596843ec77934d95675d50a146190a7f9f40e1c2ce3c6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118287579"
---
# <a name="bufinfo-sm5---asm"></a>bufinfo (SM5-ASM)

Consultar a contagem de elementos em um buffer (mas não no buffer de constantes).



| bufinfo dest \[ . Mask \] , srcResource |
|------------------------------------|



 



| Item                                                                                                               | Descrição                                                                           |
|--------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/>                                                    | \[no \] endereço dos resultados.<br/>                                         |
| <span id="srcResource"></span><span id="srcresource"></span><span id="SRCRESOURCE"></span>*srcResource*<br/> | \[no \] buffer, além de um buffer de constantes, em um SRV (t \# ) ou UAV (u \# ).<br/> |



 

## <a name="remarks"></a>Comentários

Todos os componentes no *dest* recebem o número inteiro de elementos na exibição de recursos do sombreador s do buffer. O número de elementos depende dos parâmetros de exibição, como o formato de memória.

Para um buffer tipado SRV ou UAV, o valor de retorno é o número de elementos na exibição (em que um elemento é uma unidade do formato digitado).

Para um buffer bruto SRV ou UAV, o valor de retorno é o número de bytes na exibição.

Para um buffer estruturado SRV ou UAV, o valor de retorno é o número de estruturas na exibição.

Essa instrução se aplica aos seguintes estágios de sombreador:



| Vértice | Envoltória | Domínio | Geometry | 16x16 | Computação |
|--------|------|--------|----------|-------|---------|
| X      | X    | X      | X        | X     | X       |



 

## <a name="minimum-shader-model"></a>Modelo de sombreamento mínimo

Essa instrução tem suporte nos seguintes modelos de sombreador:



| Modelo de Sombreador                                              | Com suporte |
|-----------------------------------------------------------|-----------|
| [Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)        | sim       |
| [Modelo do sombreador 4,1](dx-graphics-hlsl-sm4.md)              | no        |
| [Modelo de sombreador 4](dx-graphics-hlsl-sm4.md)                | no        |
| [Modelo de sombreador 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | no        |
| [Modelo de sombreador 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | no        |
| [Modelo de sombreador 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | no        |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Assembly do Shader Model 5 (DirectX HLSL)](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





