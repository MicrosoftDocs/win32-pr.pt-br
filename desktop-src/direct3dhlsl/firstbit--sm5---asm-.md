---
title: firstbit (SM5-ASM)
description: Localiza o primeiro conjunto de bits em um número, seja de LSB ou MSB.
ms.assetid: E3066676-5218-470A-944A-7B221E1BF64D
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b88fa9291ce64fcc8c94510bd09bed31e7b7f96
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104293595"
---
# <a name="firstbit-sm5---asm"></a>firstbit (SM5-ASM)

Localiza o primeiro conjunto de bits em um número, seja de LSB ou MSB.



| firstbit { \_ Hi \|\_lo|\_Shi} dest \[ . Mask \] , src0 \[ . swizzle\] |
|-------------------------------------------------------------|



 



| Item                                                            | Descrição                                                                                                                           |
|-----------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/> | \[na \] posição de inteiro do primeiro conjunto de bits em *src0* começando do LSB para FIRSTBIT \_ lo ou MSB para firstbit \_ Hi.<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[no \] número inteiro de entrada.<br/>                                                                                                  |



 

## <a name="remarks"></a>Comentários

Essa operação retorna a posição de inteiro do primeiro conjunto de bits na entrada de 32 bits, começando do LSB para firstbit \_ lo ou MSB para firstbit \_ Hi. Por exemplo, firstbit \_ lo em 0x00000001 retorna 0. firstbit \_ Hi em 0x10000000 retorna 3.

firstbit \_ shi (s para assinadas) retornará o primeiro 0 do MSB se o número for negativo; caso contrário, ele retornará o primeiro 1 do MSB.

Todas as variantes da instrução retornam ~ 0 (0xFFFFFFFF no registro de 32 bits) se nenhuma correspondência for encontrada.

Use essa instrução para enumerar rapidamente os bits de conjunto em um campo de campo ou encontrar a maior potência de 2 em um número.

Essa instrução se aplica aos seguintes estágios de sombreador:



| Vértice | Envoltória | Domínio | Geometria | 16x16 | Computação |
|--------|------|--------|----------|-------|---------|
| X      | X    | X      | X        | X     | X       |



 

## <a name="mimimum-shader-model"></a>Modelo de sombreador mínimo

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

 

 





