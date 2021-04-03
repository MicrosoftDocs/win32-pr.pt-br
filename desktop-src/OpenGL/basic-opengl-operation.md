---
title: Operação OpenGL básica
description: Operação OpenGL básica
ms.assetid: ad4c9321-a9e3-40c5-af80-0ad6a8b9f380
keywords:
- OpenGL, operações básicas
- OpenGL, processamento de dados
- OpenGL, estágios de processamento
- OpenGL, exibir listas
- Exibir listas OpenGL
- OpenGL, avaliadores
- avaliadores OpenGL
- OpenGL, operações por vértice
- operações por vértice OpenGL
- OpenGL, assembly primitivo
- assembly primitivo OpenGL
- OpenGL, rasterização
- OpenGL de rasterização
- OpenGL, operações por fragmento
- operações por fragmento OpenGL
- framebuffers, operações básicas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77f6b9fb8c8ca4efb05d9050e0de3da807b213e7
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/10/2021
ms.locfileid: "103930064"
---
# <a name="basic-opengl-operation"></a>Operação OpenGL básica

O diagrama a seguir ilustra como o OpenGL processa os dados. Conforme mostrado, os comandos entram da esquerda e passam por um pipeline de processamento. Alguns comandos especificam objetos geométricos a serem desenhados e outros controlam como os objetos são tratados durante vários estágios de processamento.

![Diagrama mostrando os estágios do pipeline de processamento de dados OpenGL.](images/basic01.png)

Os estágios de processamento na operação OpenGL básica são os seguintes:

-   **Lista de exibição** Em vez de fazer com que todos os comandos continuem imediatamente por meio do pipeline, você pode optar por acumular alguns deles em uma lista de exibição para processamento posterior.
-   **Avaliador** O estágio de processamento do avaliador fornece uma maneira eficiente de aproximar a curva e a geometria da superfície avaliando comandos polinomiais de valores de entrada.
-   **Operações por vértice e assembly primitivo** O OpenGL processa primitivespointss geométricos, segmentos de linha e polygonsall dos quais são descritos por vértices. Os vértices são transformados e acesos e os primitivos são recortados para o visor na preparação para a rasterização.
-   **Rasterização** O estágio de rasterização produz uma série de endereços de buffer de quadros e valores associados usando uma descrição bidimensional de um ponto, segmento de linha ou polígono. Cada fragmento produzido é colocado no último estágio por operações por fragmento.
-   **Operações por fragmento** Essas são as operações finais executadas nos dados antes de serem armazenadas como pixels no framebuffer.

    As operações por fragmento incluem atualizações condicionais para o framebuffer com base em valores z de entrada e armazenados anteriormente (para armazenamento em buffer z) e mesclagem de cores de pixel de entrada com cores armazenadas, bem como mascaramento e outras operações lógicas em valores de pixel.

Os dados podem ser inseridos na forma de pixels em vez de vértices. Dados na forma de pixels, como podem descrever uma imagem para uso no mapeamento de textura, ignora o primeiro estágio de processamento descrito acima e, em vez disso, é processado como pixels, no estágio de operações de pixel. Após as operações de pixel, os dados de pixel são:

-   Armazenado como memória de textura, para uso no estágio de rasterização.
-   Rasterizado, com os fragmentos resultantes mesclados no framebuffer como se fossem gerados a partir de dados geométricos.

 

 




