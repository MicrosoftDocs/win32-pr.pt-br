---
title: Funções (referência de HLSL)
description: As funções encapsulam instruções HLSL.
ms.assetid: b6f934e5-eac7-4859-b1d0-698632011e1d
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 59b0bfcb2079329d4d7ad7c02e7e5a326d22c236
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/23/2019
ms.locfileid: "104293604"
---
# <a name="functions-hlsl-reference"></a>Funções (referência de HLSL)

As funções encapsulam instruções HLSL. Isso permite que você depure um conjunto de funções e, em seguida, reutilize-as em sombreadores ou efeitos. Talvez você queira criar uma função que encapsula a funcionalidade de um sombreador de vértice, sombreador de pixel ou sombreador de textura. Em outras ocasiões, convém escrever uma função auxiliar que executa uma tarefa comumente usada e, em seguida, chamar essa função auxiliar a partir de sua função de sombreador. As regras para escrever funções de sombreador para HLSL são muito parecidas com a gravação de funções de C.

-   [Sintaxe](dx-graphics-hlsl-function-syntax.md)
-   [Parâmetros](dx-graphics-hlsl-function-parameters.md)
-   [Instrução Return](dx-graphics-hlsl-return.md)
-   [Assinaturas](dx-graphics-hlsl-signatures.md)

O HLSL também tem várias [**funções intrínsecas internas (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md). Como todas as funções intrínsecas são testadas e otimizadas para desempenho, é recomendável usar uma função intrínseca onde for possível, em vez de criar sua própria função.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sintaxe de linguagem (DirectX HLSL)](dx-graphics-hlsl-language-syntax.md)
</dt> </dl>

 

 




