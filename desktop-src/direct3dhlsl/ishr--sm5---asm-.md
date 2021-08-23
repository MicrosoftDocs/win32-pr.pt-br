---
title: ishr (sm5 - asm)
description: Deslocamento aritmético para a direita (extensão de sinal). | ishr (sm5 - asm)
ms.assetid: 8124B6C3-4576-4616-85A9-A2DD19EB6BB9
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c7c75d64ded9beb6cdc5660d6157b15fc989863ee9e907e67c00854fe7cfe161
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119488326"
---
# <a name="ishr-sm5---asm"></a>ishr (sm5 - asm)

Deslocamento aritmético para a direita (extensão de sinal).



| ishl dest \[ .mask \] , src0 \[ .swizzle, \] src1 \[ .swizzle\] |
|--------------------------------------------------------|



 



| Item                                                            | Descrição                                          |
|-----------------------------------------------------------------|------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*Dest*<br/> | \[em \] Contém os resultados da mudança.<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[em \] O número de bits a ser deslocado.<br/>       |
| <span id="src1"></span><span id="SRC1"></span>*src1*<br/> | \[em \] Os valores de 32 bits a ser deslocados.<br/>        |



 

## <a name="remarks"></a>Comentários

Essa instrução executa uma mudança aritmética por componente de cada valor de 32 bits em *src0* à direita por uma contagem de bits inteiro sem sinal fornecida pelo LSB de 5 bits (intervalo de 0 a 31) *em src1,* replicando o valor de bit 31. O resultado de 32 bits por componente é colocado *em dest.*

Essa instrução se aplica aos seguintes estágios do sombreador:



| Vértice | Casco | Domínio | Geometry | Pixel | Computação |
|--------|------|--------|----------|-------|---------|
| X      | X    | X      | X        | X     | X       |



 

## <a name="minimum-shader-model"></a>Modelo de sombreador mínimo

Essa instrução tem suporte nos seguintes modelos de sombreador:



| Modelo de Sombreador                                              | Com suporte |
|-----------------------------------------------------------|-----------|
| [Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)        | sim       |
| [Modelo de sombreador 4.1](dx-graphics-hlsl-sm4.md)              | não        |
| [Modelo de sombreador 4](dx-graphics-hlsl-sm4.md)                | não        |
| [Modelo de sombreador 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | não        |
| [Modelo de sombreador 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | não        |
| [Modelo de sombreador 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | não        |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Assembly do modelo de sombreador 5 (DirectX HLSL)](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





