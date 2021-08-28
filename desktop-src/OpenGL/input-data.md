---
title: Dados de entrada
description: O pipeline OpenGL exige que você insira vários tipos de dados
ms.assetid: e820d093-3e39-4feb-ab2a-0c28e298bde4
keywords:
- Pipeline de processamento OpenGL, dados de entrada
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a588e60991ad068653890659e236f8a7a96e62cad524b13ea72bfd38fb5bba4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118937423"
---
# <a name="input-data"></a>Dados de entrada

O pipeline OpenGL exige que você insira vários tipos de dados:

-   **Vértices**. Os vértices descrevem a forma do objeto geométrico desejado. Para especificar vértices, use as funções [ * *\* glVertex* _](glvertex-functions.md) em conjunto com [_ *glBegin* *](glbegin.md) e [**glEnd**](glend.md) para criar um ponto, uma linha ou um polígono. Você também pode usar [**glRect**](glrect-functions.md) para descrever um retângulo inteiro ao mesmo tempo.
-   **Sinalizador de borda**. Por padrão, todas as bordas de polígonos são bordas de limite. Use [**glEdgeFlag \***](gledgeflag-functions.md) para definir explicitamente o sinalizador de borda.
-   **Posição atual da rasterização**. Especificado com [**glRasterPos \***](glrasterpos-functions.md), a posição de varredura atual é usada para determinar as coordenadas rasterizadas para operações de desenho de bitmap e pixel.
-   **Normal atual**. Um vetor normal associado a um vértice específico determina como uma superfície nesse vértice é orientada em espaço tridimensional; isso, por sua vez, afeta a quantidade de luz que um vértice específico recebe. Use [**glNormal \***](glnormal-functions.md) para especificar um vetor normal.
-   **Cor atual**. A cor de um vértice, junto com as condições de iluminação, determinam a cor final e definitiva. A cor é especificada com [ * *glColor \** _](glcolor-functions.md) If no modo RGBA ou com [_ *glIndex \** *](glindex-functions.md) se estiver no modo de índice de cor.
-   **Coordenadas de textura atuais**. Especificado com [**glTexCoord \***](gltexcoord-functions.md), as coordenadas de textura determinam o local em um mapa de textura para associar a um vértice de um objeto.

> [!Note]  
> Quando **glVertex \* *_ é chamado, o vértice resultante herda o sinalizador de borda atual, as coordenadas normal, Color e Texture. Portanto, _* glEdgeFlag \* *_, _* glNormal \* *_, _* glColor \* *_ e _* glTexCoord \* *_ deve ser chamado antes de _* glVertex \***, se eles forem afetar o vértice resultante.

 

 

 




