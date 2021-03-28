---
title: ISHR (sm4-ASM)
description: Deslocamento aritmético à direita (extensão de assinatura). | ISHR (sm4-ASM)
ms.assetid: AFE46BBA-A6B2-4691-A3F4-A4141F1578DB
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7516543c5501ed886c5c1fa98d093062e3099a0f
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104989248"
---
# <a name="ishr-sm4---asm"></a>ISHR (sm4-ASM)

Deslocamento aritmético à direita (extensão de assinatura).



| ISHR dest \[ . Mask \] , src0 \[ . swizzle \] , o componente src1. Select \_ |
|--------------------------------------------------------------|



 



| Item                                                            | Descrição                                             |
|-----------------------------------------------------------------|---------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/> | \[in \] contém o resultado da operação.<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[in \] contém o valor a ser deslocado.<br/>     |
| <span id="src1"></span><span id="SRC1"></span>*src1*<br/> | \[in \] contém o valor de deslocamento.<br/>            |



 

## <a name="remarks"></a>Comentários

Essa instrução executa uma mudança aritmética de componente de cada valor de 32 bits em *src0* à direita por um número de bits de inteiro sem sinal fornecido pelo LSB de 5 bits (0-31 intervalo) no *\_ componente src1. Select*, replicando o valor do bit 31. O resultado de 32 bits por componente é colocado no *dest*. A contagem é um valor escalar aplicado a todos os componentes.

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

 

 





