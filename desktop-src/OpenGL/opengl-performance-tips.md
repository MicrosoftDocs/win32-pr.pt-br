---
title: Dicas de desempenho do OpenGL
description: Dicas de desempenho do OpenGL
ms.assetid: f85bf725-1361-49b9-894c-c803b2dead60
keywords:
- OpenGL, dicas de desempenho
- OpenGL, práticas recomendadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0fe91602d4a30767ed1e66e62d33445bf37152ede2cf9f8450e056f577cb3045
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118936826"
---
# <a name="opengl-performance-tips"></a>Dicas de desempenho do OpenGL

Essas práticas de programação otimizam o desempenho do seu aplicativo:

-   Use [**glColorMaterial**](glcolormaterial.md) quando apenas uma única propriedade material estiver sendo divariada rapidamente (em cada vértice, por exemplo). Use [**glMaterial**](glmaterial-functions.md) para alterações frequentes ou quando mais de uma única propriedade de material estiver sendo variada rapidamente.
-   Use [**glLoadIdentity**](glloadidentity.md) para inicializar uma matriz, em vez de carregar sua própria cópia da matriz de identidade.
-   Use chamadas de matriz específicas, como [**glRotate**](glrotate.md), [**glTranslate**](gltranslate.md)e [**glScale**](glscale.md), em vez de redigir suas próprias matrizes de rotação, tradução e escala e chamar [**glMultMatrix**](glmultmatrix.md).
-   Use [**glPushAttrib**](glpushattrib.md) e [**glPopAttrib**](glpopattrib.md) para salvar e restaurar valores de estado. Use as funções de consulta somente quando seu aplicativo exigir os valores de estado para seus próprios cálculos.
-   Use listas de exibição para encapsular alterações de estado potencialmente intensivas de memória. Por exemplo, Coloque todas as chamadas [**glTexImage**](glteximage1d.md) necessárias para especificar completamente uma textura (e talvez as chamadas [**glTexParameter**](gltexparameter-functions.md), [**glPixelStore**](glpixelstore-functions.md)e [**glPixelTransfer**](glpixeltransfer.md) associadas também) em uma única lista de exibição. Chame essa lista de exibição para selecionar a textura.
-   Use listas de exibição para encapsular as chamadas de renderização de objetos rígidos que serão desenhados repetidamente.
-   Para minimizar a largura de banda de rede em ambientes de cliente/servidor, use avaliadores mesmo para mosaicos de superfície simples.
-   Se possível, para evitar a sobrecarga do GL \_ NORMALIZE, forneça Normals de comprimento de unidade. Como [**glScale**](glscale.md) quase sempre requer a habilitação \_ de NORMALIZE GL, evite usar o **glScale** ao fazer a iluminação.
-   Se o sombreamento suave não for necessário, defina [**glShadeModel**](glshademodel.md) como GL \_ simples.
-   Use uma única chamada [**glClear**](glclear.md) por quadro, se possível. Não use **glClear** para limpar subregiãos pequenas dos buffers; Use-o apenas para limpar o buffer completamente ou quase completamente.
-   Para desenhar vários triângulos independentes, use uma única chamada em vez de várias chamadas para [**glBegin**](glbegin.md) ( \_ triângulos GL) ou uma chamada para **glBegin** ( \_ polígono GL). Da

    Para desenhar um único triângulo, use \_ TRIângulos GL em vez de \_ polígono GL.

    Use uma única chamada para [**glBegin**](glbegin.md) (GL \_ quads) em vez de chamar **glBegin** ( \_ polígono GL) repetidamente.

    Use uma única chamada para [**glBegin**](glbegin.md) ( \_ linhas GL) para desenhar vários segmentos de linha independentes, em vez de chamar **glBegin** ( \_ linhas GL) várias vezes.

-   Em geral, use as formas de vetor de comandos para passar dados de computação e use as formas escalares de comandos para passar valores que são computados perto do tempo de chamada.
-   Evite fazer alterações no modo redundante, como definir a cor com o mesmo valor entre cada vértice de um polígono com sombreamento simples.
-   Ao desenhar ou copiar imagens, desabilite as operações de rasterização e por fragmento para otimizar os recursos. O OpenGL pode aplicar texturas a imagens de pixel.

 

 




