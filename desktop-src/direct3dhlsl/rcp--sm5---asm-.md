---
title: RCP (SM5-ASM)
description: Recíproco de componente.
ms.assetid: 499A14D6-36DB-4860-94D1-887D931E60D4
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: abbaa2ffc29a4c3373009d9dec1b895710186e67
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104498952"
---
# <a name="rcp-sm5---asm"></a>RCP (SM5-ASM)

Recíproco de componente.



| RCP \[ \_ SAT \] dest \[ . Mask \] , \[ - \] src0 \[ \_ ABS \] \[ . swizzle\] |
|------------------------------------------------------------|



 



| Item                                                            | Descrição                                                                         |
|-----------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/> | \[no \] endereço dos resultados<br/> *dest*  =  **1,0 f**  /  *src0*.<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[no \] número para pegar o recíproco de.<br/>                             |



 

## <a name="remarks"></a>Comentários

Use essa instrução para reduzir a precisão recíproca, independentemente dos requisitos estritos para a divisão.

O erro relativo máximo é 2-21. (A tolerância de erro apenas corresponde a RSQ)

A tabela a seguir mostra os resultados obtidos ao executar a instrução com várias classes de números.



|        |          |        |             |        |        |             |        |          |         |
|--------|----------|--------|-------------|--------|--------|-------------|--------|----------|---------|
| *src*  | **-INF** | **-F** | **-desnorma** | **-0** | **+0** | **+ desnormativo** | **+ F** | **+ INF** | **NaN** |
| *dest* | -0       | -F     | -inf        | -inf   | +inf   | +inf        | + F     | +0       | NaN     |



 

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

 

 





