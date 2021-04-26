---
title: Sincos (sm4-ASM)
description: Meio do componente (teta) e cos (teta) para teta em radianos.
ms.assetid: 81FDEC8F-2C1C-4C60-A6DA-699C798F8316
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c03118ff9a1fc2d958eaa6eb1a550a6dbf672a2
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107997013"
---
# <a name="sincos-sm4---asm"></a>Sincos (sm4-ASM)

Meio do componente (teta) e cos (teta) para teta em radianos.



| Sincos \[ \_ SAT \] destSIN \[ . Mask \] , destCOS \[ . Mask \] , \[ - \] src0 \[ \_ ABS \] \[ . swizzle\] |
|------------------------------------------------------------------------------------|



 



| Item                                                                                               | Descrição                                                           |
|----------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| <span id="destSIN"></span><span id="destsin"></span><span id="DESTSIN"></span>*destSIN*<br/> | \[no \] endereço do sin (*src0*), calculado por componente.<br/> |
| <span id="destCOS"></span><span id="destcos"></span><span id="DESTCOS"></span>*destCOS*<br/> | \[no \] endereço de cos (*src0*), calculado por componente.<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/>                                    | \[nos \] componentes para os quais computar Sin e cos.<br/>    |



 

## <a name="remarks"></a>Comentários

Se o resultado não for necessário, você poderá especificar *destSIN* e *destCOS* como NULL em vez de especificar um registro.

Os valores de teta podem ser quaisquer valores de ponto flutuante de IEEE 32 bits.

O erro absoluto máximo é 0, 8 no intervalo de-100 \* PI a + 100 \* PI.

A tabela a seguir mostra os resultados obtidos ao executar a instrução com várias classes de números.

F significa número real finito.



| **src**     | **-INF** | **-F**       | **-desnorma** | **-0** | **+0** | **+ desnormativo** | **+ F**       | **+ INF** | **NaN** |
|-------------|----------|--------------|-------------|--------|--------|-------------|--------------|----------|---------|
| **destSIN** | NaN      | \[-1 a + 1\] | -0          | -0     | +0     | +0          | \[-1 a + 1\] | NaN      | NaN     |
| **destCOS** | NaN      | \[-1 a + 1\] | +1          | +1     | +1     | +1          | \[-1 a + 1\] | NaN      | NaN     |



 

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

 

 





