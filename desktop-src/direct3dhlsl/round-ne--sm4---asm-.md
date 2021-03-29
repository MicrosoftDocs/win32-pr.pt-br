---
title: round_ne (sm4-ASM)
description: Ponto flutuante redondo para integral float. | round_ne (sm4-ASM)
ms.assetid: 2D1A0786-F7DB-4D69-9F56-82ECD1EE7ABA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f1c6f5e332453318dc0ad1a7806c3506343ff3b6
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104968425"
---
# <a name="round_ne-sm4---asm"></a>Round \_ ne (sm4-ASM)

Ponto flutuante redondo para integral float.



| Round \_ ne \[ \_ \] dest \[ . Mask \] , \[ - \] src0 \[ \_ ABS \] \[ . swizzle\] |
|------------------------------------------------------------------|



 



| Item                                                            | Descrição                                                    |
|-----------------------------------------------------------------|----------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/> | \[no \] endereço dos resultados da operação.<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[nos \] componentes na operação.<br/>             |



 

## <a name="remarks"></a>Comentários

Essa instrução executa uma rodada de ponto flutuante de componente para os valores em *src0*, gravando valores de ponto flutuante integral para *dest*. **Round \_ ne** arredonda para mais próximo mesmo.

A tabela a seguir mostra os resultados obtidos ao executar a instrução com várias classes de números.

F significa número real finito.



|          |          |        |             |        |        |             |        |          |         |
|----------|----------|--------|-------------|--------|--------|-------------|--------|----------|---------|
| **src**  | **-INF** | **-F** | **-desnorma** | **-0** | **+0** | **+ desnormativo** | **+ F** | **+ INF** | **NaN** |
| **dest** | -inf     | -F     | -0          | -0     | +0     | +0          | + F     | +inf     | NaN     |



 

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

 

 





