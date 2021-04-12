---
title: Usando avaliadores
description: Usando avaliadores
ms.assetid: a5a99d0a-526e-4492-90c4-a6b9fdbdff16
keywords:
- OpenGL, avaliadores
- avaliadores OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1aef70a7a854e16cf4992d9dd44c4931ad4d044
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104291990"
---
# <a name="using-evaluators"></a>Usando avaliadores

As funções do avaliador OpenGL permitem usar um mapeamento polinomial para produzir vértices, normais, coordenadas de textura e cores. Esses valores calculados são passados para o pipeline de processamento como se tivessem sido especificados diretamente. As funções do avaliador também são a base para as funções NURBS (B não-uniforme racional), que permitem que você defina curvas e superfícies, conforme descrito na [biblioteca do utilitário OpenGL](opengl-utility-library.md).

A primeira etapa no uso de avaliadores é definir o mapeamento polinomial apropriado de uma ou duas dimensões usando [**glMap \***](glmap1.md). Em seguida, você pode especificar e avaliar os valores de domínio para esse mapa de uma das duas maneiras:

-   Defina uma série de valores de domínio com espaçamento uniforme para ser mapeado usando [**glMapGrid**](glmapgrid-functions.md) e, em seguida, avalie um subconjunto retangular dessa grade com [**glEvalMesh**](glevalmesh-functions.md). Um único ponto da grade pode ser avaliado usando [**glEvalPoint**](glevalpoint.md).
-   Especifique explicitamente um valor de domínio desejado como um argumento, que avalia os mapas nesse valor.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência de avaliadores](evaluators-reference.md)
</dt> </dl>

 

 




