---
title: Dicas de exatidão do OpenGL
description: Dicas de exatidão do OpenGL
ms.assetid: 48397fbf-823d-4ea0-adfd-2c639e20e38f
keywords:
- OpenGL, dicas de correção
- OpenGL, práticas recomendadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5294d2e989591216ea8cf66aa380933718776f2d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104363862"
---
# <a name="opengl-correctness-tips"></a>Dicas de exatidão do OpenGL

Siga estas diretrizes para criar aplicativos OpenGL que são executados como você pretende:

-   Suponha que o comportamento do erro na parte de uma implementação do OpenGL possa ser alterado em uma versão futura do OpenGL. A semântica de erro OpenGL pode mudar em revisões futuras.
-   Use a matriz de projeção para recolher todas as geometrias em um único plano. Se a matriz modelview for usada, os recursos OpenGL que operam em coordenadas de olho (como a iluminação e os planos de recorte definidos pelo aplicativo) podem falhar.
-   Não faça alterações extensivas em uma única matriz. Por exemplo, não anime uma rotação chamando continuamente [**glRotate**](glrotate.md) com um ângulo incremental. Em vez disso, use [**glLoadIdentity**](glloadidentity.md) para inicializar a matriz determinada para cada quadro e, em seguida, chame **glRotate** com o ângulo completo desejado para esse quadro.
-   Espere que várias passagens passem por um banco de dados de renderização para gerar os mesmos fragmentos de pixel somente se esse comportamento for garantido pelas regras de invariação estabelecidas para uma implementação de OpenGL em conformidade. Caso contrário, várias passagens podem gerar conjuntos variados de fragmentos.
-   Não espere erros a serem relatados enquanto uma lista de exibição está sendo definida. Os comandos em uma lista de exibição geram erros somente quando a lista é executada.
-   Para otimizar a operação do buffer de profundidade, coloque o plano próximo de frustum no ponto de vista máximo possível.
-   Chame [**glFlush**](glflush.md) para forçar a execução de todos os comandos OpenGL anteriores. Não conte em [**glGet**](glgetbooleanv--glgetdoublev--glgetfloatv--glgetintegerv.md) ou [**glIsEnabled**](glisenabled.md) para liberar o fluxo de renderização. Os comandos de consulta liberam a maior parte do fluxo conforme necessário para retornar dados válidos, mas não necessariamente concluem todos os comandos de renderização pendentes.
-   Desative o pontilhamento ao renderizar imagens com pontilhado (por exemplo, quando [**glCopyPixels**](glcopypixels.md) é chamado).
-   Faça uso do intervalo completo do buffer de acumulação. Por exemplo, se estiver acumulando quatro imagens, dimensione cada uma em um quarto de acordo com sua acumulação.
-   Para obter a rasterização de duas dimensões exata, especifique cuidadosamente a projeção ortográfica e os vértices dos primitivos que devem ser rasterizados. Especifique a projeção ortográfica com coordenadas de inteiro, conforme mostrado no exemplo a seguir.

    ``` syntax
    gluOrtho2D(0, width, 0, height); 
    ```

    A *largura* e a *altura* dos parâmetros são as dimensões do visor. Dada essa matriz de projeção, coloque os vértices do polígono e as posições de imagem em pixel em coordenadas de inteiros para rasterizar previsíveis. Por exemplo, [glRecti](glrect-functions.md)(0, 0, 1, 1) preenche de forma confiável o pixel inferior esquerdo do visor e [glRasterPos2i](glrasterpos-functions.md)(0, 0) posiciona de forma confiável uma imagem sem zoom no pixel inferior esquerdo do visor. No entanto, os vértices de ponto, os vértices de linha e as posições de bitmap devem ser colocados em locais de meio inteiro. Por exemplo, uma linha desenhada de (*x* (1), 0,5) para (*x* (2), 0,5) será processada de maneira confiável na linha inferior de pixels no visor e um ponto desenhado em (0,5, 0,5) preencherá de forma confiável o mesmo pixel que glRecti (0, 0, 1, 1).

    Um comprometimento ideal que permite que todos os primitivos sejam especificados em posições de inteiros, enquanto ainda garante a rasterização previsível, é converter *x* e *y* por 0,375, conforme mostrado no exemplo de código a seguir. Tal tradução mantém as bordas do polígono e da imagem de pixel com segurança, longe dos centros de pixels, ao mesmo tempo em que os vértices de linha são fechados o suficiente para os centros de pixel.

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

-   Evite usar coordenadas *de vértices* negativas em negativo e coordenadas de textura de *q* negativas. O OpenGL pode não cortar essas coordenadas corretamente e pode fazer erros de interpolação ao sombrear primitivos definidos por tais coordenadas.

 

 




