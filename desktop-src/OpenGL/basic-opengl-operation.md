---
title: Operação OpenGL básica
description: Operação OpenGL básica
ms.assetid: ad4c9321-a9e3-40c5-af80-0ad6a8b9f380
keywords:
- OpenGL, operações básicas
- OpenGL, processamento de dados
- OpenGL, estágios de processamento
- OpenGL, listas de exibição
- listas de exibição OpenGL
- OpenGL, avaliadores
- avaliadores OpenGL
- OpenGL, operações por vértice
- Operações por vértice OpenGL
- OpenGL, assembly primitivo
- assembly primitivo OpenGL
- OpenGL, rasterização
- Rasterização OpenGL
- OpenGL, operações por fragmento
- Operações por fragmento OpenGL
- framebuffers, operações básicas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f72f6abed7d06a93985b798e72efbf4d6ec0901e7ad9fb4614f5bf81590cefcf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119554707"
---
# <a name="basic-opengl-operation"></a>Operação OpenGL básica

O diagrama a seguir ilustra como o OpenGL processa dados. Conforme mostrado, os comandos entram da esquerda e passam por um pipeline de processamento. Alguns comandos especificam objetos geométricos a serem desenhados e outros controlam como os objetos são tratados durante vários estágios de processamento.

![Diagrama mostrando os estágios do pipeline de processamento de dados openGL.](images/basic01.png)

Os estágios de processamento na operação básica do OpenGL são os seguintes:

-   **Lista de exibição** Em vez de fazer com que todos os comandos prossigam imediatamente pelo pipeline, você pode optar por acumular alguns deles em uma lista de exibição para processamento posterior.
-   **Avaliador** O estágio de processamento do avaliador fornece uma maneira eficiente de aproximar a geometria da curva e da superfície avaliando comandos polinomiais de valores de entrada.
-   **Operações por vértice e assembly primitivo** O OpenGL processa primitivos geométricos, segmentos de linha e polígonos, que são descritos por vértices. Os vértices são transformados e acesos, e os primitivos são recortados para o viewport em preparação para rasterização.
-   **Rasterização** O estágio de rasterização produz uma série de endereços de buffer de quadros e valores associados usando uma descrição bidimensional de um ponto, segmento de linha ou polígono. Cada fragmento produzido é alimentado no último estágio, operações por fragmento.
-   **Operações por fragmento** Essas são as operações finais executadas nos dados antes que eles sejam armazenados como pixels no framebuffer.

    As operações por fragmento incluem atualizações condicionais no framebuffer com base em valores z de entrada e armazenados anteriormente (para buffer z) e mesclagem de cores de pixel de entrada com cores armazenadas, bem como mascaramento e outras operações lógicas em valores de pixel.

Os dados podem ser entrada na forma de pixels em vez de vértices. Os dados na forma de pixels, como podem descrever uma imagem para uso no mapeamento de textura, ignoram o primeiro estágio de processamento descrito acima e, em vez disso, são processados como pixels, no estágio de operações de pixel. As seguintes operações de pixel, os dados de pixel são:

-   Armazenado como memória de textura, para uso no estágio de rasterização.
-   Rasterizado, com os fragmentos resultantes mesclados no framebuffer, como se fossem gerados de dados geométricos.

 

 




