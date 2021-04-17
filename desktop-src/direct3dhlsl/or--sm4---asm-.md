---
title: ou (sm4-ASM)
description: OR-bit.
ms.assetid: BBC06F8C-4C86-4077-A1F9-383D6A8FBED3
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 62064189725b246cc48bbde03a9c094d13f8b9a0
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104988601"
---
# <a name="or-sm4---asm"></a>ou (sm4-ASM)

OR-bit.



| ou dest \[ . Mask \] , src0 \[ . swizzle \] , src1 \[ . swizzle\] |
|------------------------------------------------------|



 



| Item                                                            | Descrição                                         |
|-----------------------------------------------------------------|-----------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/> | \[no \] resultado da operação.<br/>      |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[nos \] componentes para ou com *src1*.<br/> |
| <span id="src1"></span><span id="SRC1"></span>*src1*<br/> | \[nos \] componentes para ou com *src0*.<br/> |



 

## <a name="remarks"></a>Comentários

Essa instrução executa um componente lógico ou de cada par de valores de 32 bits de *src0* e *src1*. Os resultados de 32 bits são colocados no *dest*.

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

 

 





