---
title: ushr (sm4 – asm)
description: Shift para a direita. | ushr (sm4 – asm)
ms.assetid: 3E7CB515-9D0F-44C7-A770-AD0584631BFE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a55343f9c9b4db4fff4b0df7ab4e2a567f25f0eb43e93486fe9c41b89cf68454
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119787816"
---
# <a name="ushr-sm4---asm"></a>ushr (sm4 – asm)

Shift para a direita.



| ushr dest \[ .mask \] , src0 \[ .swizzle \] , src1.select \_ component |
|--------------------------------------------------------------|



 



| Item                                                            | Descrição                                                   |
|-----------------------------------------------------------------|---------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*Dest*<br/> | \[em \] O endereço do resultado da operação.<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[em \] Os componentes a ser deslocados.<br/>                    |
| <span id="src1"></span><span id="SRC1"></span>*src1*<br/> | \[em \] O valor a ser deslocado *src0.*<br/>                 |



 

## <a name="remarks"></a>Comentários

Essa instrução executa uma mudança de componente de cada valor de 32 bits em *src0* à direita por uma contagem de bits inteiro sem sinal fornecida pelo LSB de 5 bits (intervalo de 0 a 31) no componente *\_ src1.select,* inserindo 0. O resultado de 32 bits por componente é colocado *em dest.* A contagem é um valor escalar aplicado a todos os componentes.

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

 

 





