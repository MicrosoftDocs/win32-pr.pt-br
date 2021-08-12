---
title: ushr (SM5-ASM)
description: Deslocar para a direita. | ushr (SM5-ASM)
ms.assetid: C695CB6C-A6C9-4DC8-8EBE-70A0CFFC4981
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b4f0cacaa785b34eb8910f12ecfe3578bd47781e41110adc71f4a7a7d52858a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118283042"
---
# <a name="ushr-sm5---asm"></a>ushr (SM5-ASM)

Deslocar para a direita.



| ubfe dest \[ . Mask \] , src0 \[ . swizzle \] , src1 \[ . swizzle\] |
|--------------------------------------------------------|



 



| Item                                                            | Descrição                                                                  |
|-----------------------------------------------------------------|------------------------------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/> | \[in \] contém os resultados da instrução.<br/>                   |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[nos \] valores de 32 bits para Shift.<br/>                                |
| <span id="src1"></span><span id="SRC1"></span>*src1*<br/> | \[nos \] bits LSB 5, forneça o número de bits a serem deslocados (0-31).<br/> |



 

Essa instrução executa uma mudança de componente de cada valor de 32 bits em *src0* à direita por um número de bits de inteiro sem sinal fornecido pelo LSB de 5 bits (0-31 intervalo) em *src1*, inserindo 0. Os resultados de 32 bits por componente são colocados no *dest*.

Essa instrução se aplica aos seguintes estágios de sombreador:



| Vértice | Envoltória | Domínio | Geometry | 16x16 | Computação |
|--------|------|--------|----------|-------|---------|
| X      | X    | X      | X        | X     | X       |



 

## <a name="minimum-shader-model"></a>Modelo de sombreamento mínimo

Essa instrução tem suporte nos seguintes modelos de sombreador:



| Modelo de Sombreador                                              | Com suporte |
|-----------------------------------------------------------|-----------|
| [Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)        | sim       |
| [Modelo do sombreador 4,1](dx-graphics-hlsl-sm4.md)              | no        |
| [Modelo de sombreador 4](dx-graphics-hlsl-sm4.md)                | no        |
| [Modelo de sombreador 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | no        |
| [Modelo de sombreador 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | no        |
| [Modelo de sombreador 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | no        |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Assembly do Shader Model 5 (DirectX HLSL)](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





