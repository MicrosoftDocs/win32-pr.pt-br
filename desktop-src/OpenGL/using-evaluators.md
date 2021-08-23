---
title: Usando avaliadores
description: Usando avaliadores
ms.assetid: a5a99d0a-526e-4492-90c4-a6b9fdbdff16
keywords:
- OpenGL, avaliadores
- avaliadores OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a4bb6808ad1898b0c98906a543291c700ee61257a35befa8886789f3f8b7e31
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119553486"
---
# <a name="using-evaluators"></a>Usando avaliadores

As funções do avaliador OpenGL permitem que você use um mapeamento polinomial para produzir vértices, normais, coordenadas de textura e cores. Esses valores calculados são passados para o pipeline de processamento como se eles tivessem sido especificados diretamente. As funções do avaliador também são a base para as funções N LTDS (B-Spline Racional Não Uniforme), que permitem definir curvas e superfícies, conforme descrito em Biblioteca do Utilitário [OpenGL](opengl-utility-library.md).

A primeira etapa no uso de avaliadores é definir o mapeamento polinomial unidimensional ou bidimensional apropriado usando [**glMap \***](glmap1.md). Em seguida, você pode especificar e avaliar os valores de domínio para este mapa de uma das duas maneiras:

-   Defina uma série de valores de domínio espaçados de maneira espaçada para serem mapeados usando [**glMapGrid**](glmapgrid-functions.md) e, em seguida, avalie um subconjunto retangular dessa grade com [**glEvalMesh**](glevalmesh-functions.md). Um único ponto da grade pode ser avaliado usando [**glEvalPoint**](glevalpoint.md).
-   Especifique explicitamente um valor de domínio desejado como um argumento, que avalia os mapas nesse valor.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência de avaliadores](evaluators-reference.md)
</dt> </dl>

 

 




