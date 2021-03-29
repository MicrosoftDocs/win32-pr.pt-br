---
title: ushr (SM5-ASM)
description: Deslocar para a direita. | ushr (SM5-ASM)
ms.assetid: C695CB6C-A6C9-4DC8-8EBE-70A0CFFC4981
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f33c627ec4aa985b5ac8a27cf0babd6219c9247c
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104968434"
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

 

 





