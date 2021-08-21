---
title: Negar
description: Inverte o sinal do valor de um operando de origem usado em uma operação aritmética.
ms.assetid: 83ef3f61-7b0b-4033-8f7b-5345b205c441
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a1f220cb0a5becf823ecc547e29c9d4c7363aa8b885355bb76f1182fae333f84
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118089147"
---
# <a name="negate"></a>Negar

Inverte o sinal do valor de um operando de origem usado em uma operação aritmética.



| \-  |
|-----|



 

Para ponto flutuante e instruções de precisão simples e dupla, o modificador de negação inverte o sinal dos números no operando de origem, incluindo os valores INF. A aplicação de **negação** em NaN preserva Nan, embora o padrão de bit Nan específico que resulte não esteja definido.

Para instruções de inteiro, o modificador de **negação** usa o complemento de 2 do número (s) no operando de origem.

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

 

 




