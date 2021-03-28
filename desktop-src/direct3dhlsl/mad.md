---
title: Função mad
description: Executa uma operação aritmética de multiplicar/adicionar em três valores.
ms.assetid: 2e58229d-2387-4319-adc6-2d66eda88bd1
keywords:
- HLSL da função Mad
topic_type:
- apiref
api_name:
- mad
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 208b1bbc87c430ca5a58a70fb3c86f9edae762bf
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104453787"
---
# <a name="mad-function"></a>Função mad

Executa uma operação aritmética de multiplicar/adicionar em três valores.

## <a name="syntax"></a>Sintaxe

``` syntax
numeric mad(
  in numeric mvalue,
  in numeric avalue,
  in numeric bvalue
);
```

## <a name="parameters"></a>Parâmetros

<dl> <dt>

*mvalue* \[ no\]
</dt> <dd>

Tipo: **numérico**

O valor de multiplicação.

</dd> <dt>

*aValue* \[ no\]
</dt> <dd>

Tipo: **numérico**

O primeiro valor de adição.

</dd> <dt>

*bValue* \[ no\]
</dt> <dd>

Tipo: **numérico**

O segundo valor de adição.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Tipo: **numérico**

O resultado de *mvalue* \* *aValue*  +  *bValue*.

## <a name="remarks"></a>Comentários

### <a name="minimum-shader-model"></a>Modelo de sombreamento mínimo

Essa função tem suporte nos seguintes modelos de sombreador.



| Modelo de Sombreador                                                                | Com suporte |
|-----------------------------------------------------------------------------|-----------|
| [Modelo](d3d11-graphics-reference-sm5.md) de sombreador 5 e modelos de sombreador mais altos | sim       |



 

Essa função tem suporte nos seguintes tipos de sombreadores:



| Vértice | Envoltória | Domínio | Geometria | 16x16 | Computação |
|--------|------|--------|----------|-------|---------|
| x      | x    | x      | x        | x     | x       |



 

Os autores de sombreador podem usar o **Mad** instrinsic para direcionar explicitamente a instrução de hardware **Mad** na saída do sombreador compilado, que é particularmente útil com sombreadores que marcam os resultados com a palavra-chave [precisa](dx-graphics-hlsl-appendix-keywords.md) . A instrução **Mad** pode ser implementada no hardware como "fundido", que oferece maior precisão do que a implementação de uma instrução **Mul** seguida por uma instrução **Add** , ou como uma adição de **Mul**  +  .

Se os autores de sombreador usarem o **Mad** instrinsic para calcular um resultado de que o sombreador está marcado como preciso, eles indicarão ao hardware para usar qualquer implementação válida da instrução **Mad** (com fusível ou não), desde que a implementação seja consistente para todos os usos dessa **Mad** intrínseca em qualquer sombreador no hardware. Os sombreadores podem aproveitar as possíveis melhorias de desempenho usando uma instrução **Mad** nativa (versus **Mul**  +  **Add**) em algum hardware. O resultado da execução de uma instrução de hardware **Mad** nativo pode ou não ser diferente de executar um **Mul** seguido por um **Add**. No entanto, seja qual for o resultado, o resultado deve ser consistente para que a mesma operação ocorra em vários sombreadores ou partes diferentes de um sombreador.

## <a name="see-also"></a>Confira também

<dl> <dt>

[Funções intrínsecas](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[Modelo de sombreador 5](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




