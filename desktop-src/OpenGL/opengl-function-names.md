---
title: Nomes de função OpenGL
description: Muitas funções OpenGL são variações umas das outras, diferentes principalmente nos tipos de dados de seus argumentos.
ms.assetid: 2d30e2e4-9671-4e57-962d-0328b13159f3
keywords:
- OpenGL, nomes de função
- nomes de função OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e06d04d1acde3ddf9baebd4c5ab44b4f55cb126
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103635937"
---
# <a name="opengl-function-names"></a>Nomes de função OpenGL

Muitas funções OpenGL são variações umas das outras, diferentes principalmente nos tipos de dados de seus argumentos. Algumas funções diferem no número de argumentos relacionados e se esses argumentos podem ser especificados como um vetor ou devem ser especificados separadamente em uma lista. Por exemplo, se você usar a função **glVertex2f** , será necessário fornecer coordenadas x e y como números de ponto flutuante de 32 bits; com o **glVertex3sv**, você deve fornecer uma matriz de três valores inteiros curtos (16 bits) para x, y e z. Somente o nome base da função é usado nos tópicos a seguir. Um asterisco indica que pode haver mais para o nome da função real do que é mostrado. Por exemplo, [glVertex \*](glvertex-functions.md) significa todas as variações da função que você usa para especificar vértices: **glVertex2d**, **glVertex2f**, **glVertex2i** e assim por diante.

O efeito de uma função OpenGL pode variar dependendo se determinados modos estão habilitados. Por exemplo, você precisa habilitar a iluminação se as funções relacionadas à iluminação forem produzir um objeto aceso adequadamente. Para habilitar um modo específico, use a função [**glEnable**](glenable.md) e forneça a constante apropriada para identificar o modo (por exemplo, \_ iluminação GL). Para desabilitar um modo, use [**glDisable**](gldisable.md). Consulte **glEnable** para obter uma lista completa dos modos que podem ser habilitados.

 

 




