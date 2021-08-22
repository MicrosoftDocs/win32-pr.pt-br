---
title: Correção do OpenGL Dicas
description: Correção do OpenGL Dicas
ms.assetid: 48397fbf-823d-4ea0-adfd-2c639e20e38f
keywords:
- OpenGL, dicas de correção
- OpenGL, práticas recomendadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 588cb53ca9e096eb768c4ce448c0bb7badae6f01e7b8d7e16c31a631ebcafb47
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119486396"
---
# <a name="opengl-correctness-tips"></a>Correção do OpenGL Dicas

Siga estas diretrizes para criar aplicativos OpenGL que executam como você pretende:

-   Suponha que o comportamento de erro por parte de uma implementação do OpenGL possa mudar em uma versão futura do OpenGL. A semântica de erro openGL pode mudar em revisões futuras.
-   Use a matriz de projeção para fechar toda a geometria em um único plano. Se a matriz modelview for usada, os recursos do OpenGL que operam em coordenadas de olho (como iluminação e planos de recorte definidos pelo aplicativo) poderão falhar.
-   Não faça alterações abrangentes em uma única matriz. Por exemplo, não animar uma rotação chamando [**glRotate**](glrotate.md) continuamente com um ângulo incremental. Em vez disso, [**use glLoadIdentity**](glloadidentity.md) para inicializar a matriz determinada para cada quadro e, em seguida, chame **glRotate** com o ângulo completo desejado para esse quadro.
-   Espere várias passagens por um banco de dados de renderização para gerar os mesmos fragmentos de pixel somente se esse comportamento for garantido pelas regras de invariância estabelecidas para uma implementação do OpenGL em conformidade. Caso contrário, várias passagens podem gerar conjuntos variados de fragmentos.
-   Não espere que os erros sejam relatados enquanto uma lista de exibição estiver sendo definida. Os comandos em uma lista de exibição geram erros somente quando a lista é executada.
-   Para otimizar a operação do buffer de profundidade, coloque o plano mais próximo possível do ponto de vista.
-   Chame [**glFlush para**](glflush.md) forçar a execução de todos os comandos OpenGL anteriores. Não conte com [**glGet ou**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) [**glIsEnabled**](glisenabled.md) para liberar o fluxo de renderização. Os comandos de consulta liberam tanto do fluxo quanto é necessário para retornar dados válidos, mas não necessariamente concluem todos os comandos de renderização pendentes.
-   Desligue a dithering ao renderizar imagens prediteradas (por exemplo, quando [**glCopyPixels**](glcopypixels.md) é chamado).
-   Use o intervalo completo do buffer de acúmulo. Por exemplo, se estiver acumulando quatro imagens, dimensione cada uma em um trimestre conforme ela é acumulada.
-   Para obter a rasterização bidimensional exata, especifique cuidadosamente a projeção ortográfica e os vértices dos primitivos que devem ser rasterizados. Especifique a projeção ortográfica com coordenadas de inteiro, conforme mostrado no exemplo a seguir.

    ``` syntax
    gluOrtho2D(0, width, 0, height); 
    ```

    A largura *e a altura dos* parâmetros são as dimensões do viewport.  Dada essa matriz de projeção, coloque vértices de polígono e posições de imagem de pixel em coordenadas de inteiro para rasterizar de forma previsível. Por exemplo, [glRecti](glrect-functions.md)( 0, 0, 1, 1 ) preenche de forma confiável o pixel inferior esquerdo do viewport e [glRasterPos2i](glrasterpos-functions.md)( 0, 0 ) posiciona de forma confiável uma imagem nãozoomada no pixel inferior esquerdo do viewport. No entanto, vértices de ponto, vértices de linha e posições de bitmap devem ser colocados em locais de meio inteiro. Por exemplo, uma linha desenhada de (*x* (1) , 0,5) para (*x* (2) , 0,5) será renderizada de forma confiável ao longo da linha inferior de pixels no viewport e um ponto desenhado em (0,5, 0,5) preencherá de forma confiável o mesmo pixel que glRecti( 0, 0, 1, 1 ).

    Um comprometimento ideal que permite que todos os primitivos sejam especificados em posições de inteiro, embora ainda garanta a rasterização previsível, é converter *x* e *y* em 0,375, conforme mostrado no exemplo de código a seguir. Essa tradução mantém as bordas de imagem de polígono e pixel com segurança dos centros de pixels, enquanto move os vértices de linha perto o suficiente dos centros de pixel.

    ``` syntax
    glViewport(0, 0, width, height);
    glMatrixMode(GL_PROJECTION);
    glLoadIdentity( );
    gluOrtho2D(0, width, 0, height);
    glMatrixMode(GL_MODELVIEW);
    glLoadIdentity( );
    glTranslatef(0.375, 0.375, 0.0);
    /* render all primitives at integer positions */
    ```

-   Evite usar coordenadas *de vértice* w negativas e coordenadas de textura *q* negativas. O OpenGL pode não cortar essas coordenadas corretamente e pode fazer erros de interpolação ao sombrear primitivos definidos por essas coordenadas.

 

 




