---
title: ishr (sm4 – asm)
description: Deslocamento aritmético para a direita (extensão de sinal). | ishr (sm4 – asm)
ms.assetid: AFE46BBA-A6B2-4691-A3F4-A4141F1578DB
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d2ec191320561b05ba736b7da5630fb50a610e739d0e74f9def3eaa10bb4e17
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118511131"
---
# <a name="ishr-sm4---asm"></a>ishr (sm4 – asm)

Deslocamento aritmético para a direita (extensão de sinal).



| ishr dest \[ \] .mask, src0 \[ .swizzle, \] src1.select \_ component |
|--------------------------------------------------------------|



 



| Item                                                            | Descrição                                             |
|-----------------------------------------------------------------|---------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*Dest*<br/> | \[em \] Contém o resultado da operação.<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[em \] Contém o valor a ser deslocado.<br/>     |
| <span id="src1"></span><span id="SRC1"></span>*src1*<br/> | \[em \] Contém o valor de deslocamento.<br/>            |



 

## <a name="remarks"></a>Comentários

Essa instrução executa uma mudança aritmética por componente de cada valor de 32 bits em *src0* à direita por uma contagem de bits inteiro sem sinal fornecida pelo LSB de 5 bits (intervalo de 0 a 31) no componente *\_ src1.select,* replicando o valor do bit 31. O resultado de 32 bits por componente é colocado *em dest.* A contagem é um valor escalar aplicado a todos os componentes.

Essa instrução se aplica aos seguintes estágios do sombreador:



| Sombreador de vértice | Sombreador de geometria | Sombreador de pixel |
|---------------|-----------------|--------------|
| x             | x               | x            |



 

## <a name="minimum-shader-model"></a>Modelo de sombreador mínimo

Essa função tem suporte nos modelos de sombreador a seguir.



| Modelo de Sombreador                                              | Com suporte |
|-----------------------------------------------------------|-----------|
| [Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)        | sim       |
| [Modelo de sombreador 4.1](dx-graphics-hlsl-sm4.md)              | sim       |
| [Modelo de sombreador 4](dx-graphics-hlsl-sm4.md)                | sim       |
| [Modelo de sombreador 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | não        |
| [Modelo de sombreador 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | não        |
| [Modelo de sombreador 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | não        |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Assembly do modelo de sombreador 4 (DirectX HLSL)](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





