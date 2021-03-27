---
title: 'ftoi (sm4 – asm) '
description: Ponto flutuante para conversão de inteiro assinado.
ms.assetid: 580AB4A6-0C1C-409B-B2B9-BA1D37772F46
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c02ce1b506d112a59d3087f59d219557575b8def
ms.sourcegitcommit: 8c658e9872a2173e3dcec94195f9067fbcd85d3d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/17/2020
ms.locfileid: "104294571"
---
# <a name="ftoi-sm4---asm"></a>ftoi (sm4 – asm) 

Ponto flutuante para conversão de inteiro assinado.

| ftoi dest \[ . Mask \] , \[ - \] src0 \[ \_ ABS \] \[ . swizzle\] |
|-|

| Item | Descrição |
|-|-|
| <span id="dest"></span><span id="DEST"></span>*dest*<br/> | \[no \] endereço do resultado da operação.<br/> *dest*  =  [arredondar \_ z](round-z--sm4---asm-.md)(*src0*)<br/> |
| <span id="src0"></span><span id="SRC0"></span>*src0*<br/> | \[no \] componente a ser convertido.<br/> |

## <a name="remarks"></a>Comentários

A conversão é executada por componente. O arredondamento é sempre executado em direção a zero, seguindo a Convenção C para conversões de float para int. Os aplicativos que exigem uma semântica de arredondamento diferente podem invocar as instruções de **arredondamento** antes da conversão para o número inteiro.

As entradas são clamped para o intervalo \[ -2147483648.999 f... 2147483647.999 f \] antes da conversão, e os valores Nan de entrada produzem um resultado zero.

Os modificadores de valor negado e absoluto opcionais são aplicados aos valores de origem antes da conversão.

Essa instrução se aplica aos seguintes estágios de sombreador:

| Sombreador de vértice | Sombreador de geometria | Sombreador de pixel |
|-|-|-|
| x | x | x |

## <a name="minimum-shader-model"></a>Modelo de sombreamento mínimo

Essa função tem suporte nos seguintes modelos de sombreador.

| Modelo de Sombreador | Com suporte |
|-|-|
| [Modelo de sombreador 5](d3d11-graphics-reference-sm5.md) | sim |
| [Modelo do sombreador 4,1](dx-graphics-hlsl-sm4.md) | sim |
| [Modelo de sombreador 4](dx-graphics-hlsl-sm4.md) | sim |
| [Modelo de sombreador 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) | não |
| [Modelo de sombreador 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) | não |
| [Modelo de sombreador 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) | não |

## <a name="related-topics"></a>Tópicos relacionados

[Assembly do Shader Model 4 (DirectX HLSL)](dx-graphics-hlsl-sm4-asm.md)
