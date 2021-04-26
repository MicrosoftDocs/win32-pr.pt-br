---
title: round_pi (sm4-ASM)
description: Ponto flutuante redondo para integral float. | round_pi (sm4-ASM)
ms.assetid: AA4E4C2E-A4B0-4892-8660-1EF57767F4C4
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b61282078b3639681eed756e2899d06744f0369e
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107997103"
---
# <a name="round_pi-sm4---asm"></a>arredondar \_ PI (sm4-ASM)

Ponto flutuante redondo para integral float.



| arredondar \_ PI \[ \_ SAT \] dest \[ . Mask \] , \[ - \] src0 \[ \_ ABS \] \[ . swizzle\] |
|------------------------------------------------------------------|



 



| Item                                                            | Descrição                                                    |
|-----------------------------------------------------------------|----------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/> | \[no \] endereço dos resultados da operação.<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[nos \] componentes na operação.<br/>             |



 

## <a name="remarks"></a>Comentários

Essa instrução executa uma rodada de ponto flutuante de componente para os valores em *src0*, gravando valores de ponto flutuante integral para *dest*.

**o \_ PI redondo** Arredonda em direção a + infinito, normalmente conhecido como ceil ().

A tabela a seguir mostra os resultados obtidos ao executar a instrução com várias classes de números.

F significa número real finito.



| **src**  | **-INF** | **-F** | **-desnorma** | **-0** | **+0** | **+ desnormativo** | **+ F** | **+ INF** | **NaN** |
|----------|----------|--------|-------------|--------|--------|-------------|--------|----------|---------|
| **dest** | -inf     | -F     | -0          | -0     | +0     | +0          | + F     | +inf     | NaN     |



 

Essa instrução se aplica aos seguintes estágios de sombreador:



| Sombreador de vértice | Sombreador de geometria | Sombreador de pixel |
|---------------|-----------------|--------------|
| x             | x               | x            |



 

## <a name="minimum-shader-model"></a>Modelo de sombreamento mínimo

Essa função tem suporte nos seguintes modelos de sombreador.



| Modelo de Sombreador                                              | Suportado |
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

 

 





