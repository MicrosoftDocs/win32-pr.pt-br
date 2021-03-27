---
title: itof (sm4-ASM)
description: Inteiro assinado para conversão de ponto flutuante.
ms.assetid: 60652168-25FA-4084-8CC1-73F12984ECED
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f9d262f65801cd2caa0e6432b335ce32fff0d4e
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "103823452"
---
# <a name="itof-sm4---asm"></a>itof (sm4-ASM)

Inteiro assinado para conversão de ponto flutuante.



| itof dest \[ . Mask \] , \[ - \] src0 \[ . swizzle\] |
|-------------------------------------------|



 



| Item                                                            | Descrição                                             |
|-----------------------------------------------------------------|---------------------------------------------------------|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/> | \[in \] contém o resultado da operação.<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[in \] contém o valor a ser convertido.<br/>        |



 

## <a name="remarks"></a>Comentários

Essa instrução de conversão de inteiro em float assinada pressupõe que *src0* contém uma tupla de 4 bits de número inteiro de 32-bit assinado. Depois que a instrução for executada, o *dest* conterá um ponto flutuante de 4 tuplas.

A conversão é executada por componente.

Quando um valor de entrada de inteiro é muito grande em magnitude para ser representado exatamente no formato de ponto flutuante, o arredondamento para o modo de par mais próximo é altamente recomendado, mas não obrigatório.

O modificador opcional Negate no operando de origem usa o complemento de 2 antes de executar a operação aritmética.

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

 

 





