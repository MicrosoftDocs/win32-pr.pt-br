---
title: Valor absoluto
description: Pegue o valor absoluto de um operando de origem usado em uma operação aritmética.
ms.assetid: FD2ACE91-0AF6-43E8-80C5-849488E39BEF
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 27ceefa2c4b4ee2eb890b0692a33266e89a18cfb
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104293593"
---
# <a name="absolute-value"></a>Valor absoluto

Pegue o valor absoluto de um operando de origem usado em uma operação aritmética.



| \_ABS |
|-------|



 

Esse modificador é usado somente para ponto flutuante de precisão simples e dupla. O modificador **\_ ABS** força o sinal dos números no operando de origem positivo, incluindo os valores inf.

A aplicação de **\_ ABS** em Nan preserva Nan, embora o padrão de bit Nan específico que resulte não esteja definido.

Quando \_ ABS é combinado com o modificador de [negação](negate.md) , a combinação força o sinal a ser negativo, como se o modificador de **\_ ABS** for aplicado primeiro, em seguida, o **negará**.

## <a name="minimum-shader-model"></a>Modelo de sombreamento mínimo

Esse modificador tem suporte nos seguintes modelos de sombreador.



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

[Modificadores de instrução](instruction-modifiers.md)
</dt> </dl>

 

 




