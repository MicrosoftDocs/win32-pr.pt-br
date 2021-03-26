---
title: bufinfo (SM5-ASM)
description: Consultar a contagem de elementos em um buffer (mas não no buffer de constantes).
ms.assetid: 3A5C28F3-FE59-4C67-92AC-66B10E1D9692
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff8dd33871aa5bd56db6e7375979c6d49f374b74
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104988582"
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



| Vértice | Envoltória | Domínio | Geometria | 16x16 | Computação |
|--------|------|--------|----------|-------|---------|
| X      | X    | X      | X        | X     | X       |



 

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

 

 





