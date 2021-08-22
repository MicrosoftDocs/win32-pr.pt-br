---
title: Nomes de função OpenGL
description: Muitas funções OpenGL são variações umas das outras, diferindo principalmente nos tipos de dados de seus argumentos.
ms.assetid: 2d30e2e4-9671-4e57-962d-0328b13159f3
keywords:
- OpenGL, nomes de função
- nomes de função OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7729ca1f8a092c261a2ae87a835b51ea253ff2d09de710a830458c0825642bb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118936876"
---
# <a name="opengl-function-names"></a>Nomes de função OpenGL

Muitas funções OpenGL são variações umas das outras, diferindo principalmente nos tipos de dados de seus argumentos. Algumas funções diferem no número de argumentos relacionados e se esses argumentos podem ser especificados como um vetor ou devem ser especificados separadamente em uma lista. Por exemplo, se você usar a **função glVertex2f,** precisará fornecer coordenadas x e y como números de ponto flutuante de 32 bits; com **glVertex3sv**, você deve fornecer uma matriz de três valores inteiros curtos (16 bits) para x, y e z. Somente o nome base da função é usado nos tópicos a seguir. Um asterisco indica que pode haver mais para o nome real da função do que é mostrado. Por exemplo, [glVertex \*](glvertex-functions.md) significa todas as variações da função usada para especificar vértices: **glVertex2d,** **glVertex2f,** **glVertex2i** e assim por diante.

O efeito de uma função OpenGL pode variar dependendo se determinados modos estão habilitados. Por exemplo, você precisará habilitar a iluminação se as funções relacionadas à iluminação produzirem um objeto devidamente acessado. Para habilitar um modo específico, use a [**função glEnable**](glenable.md) e forneça a constante apropriada para identificar o modo (por exemplo, GL \_ LIGHTING). Para desabilitar um modo, use [**glDisable.**](gldisable.md) Consulte **glEnable** para ver uma lista completa dos modos que podem ser habilitados.

 

 




