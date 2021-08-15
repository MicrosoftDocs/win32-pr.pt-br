---
title: O pipeline de transformação Direct3D
description: Este artigo fornece uma explicação técnica para desenvolvedores de aplicativos Direct3D sobre como definir os parâmetros do Pipeline de Transformação Direct3D pela manipulação direta de matrizes Direct3D.
ms.assetid: 48ae49f0-1162-c292-4bd4-34da5aadd2df
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6377e3b17cfb4ceb6eda1f4cf59a93c12fd3e6b2f7e43f29f622ed6ee12c271
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118152288"
---
# <a name="the-direct3d-transformation-pipeline"></a>O pipeline de transformação Direct3D

Este artigo fornece uma explicação técnica para desenvolvedores de aplicativos Direct3D sobre como definir os parâmetros do Pipeline de Transformação Direct3D pela manipulação direta de matrizes Direct3D.

-   [Visão geral](#overview)
-   [O pipeline de transformação](#the-transformation-pipeline)
-   [Uso Dicas](#usage-tips)

## <a name="overview"></a>Visão geral

O Direct3D usa três transformações para alterar suas coordenadas de modelo 3D em coordenadas de pixel (espaço da tela). Essas transformações são transformação de mundo, transformação de exibição e transformação de projeção.

A transformação mundial controla como as coordenadas do modelo são transformadas em coordenadas do mundo. A transformação mundial pode incluir traduções, rotações e dimensionamentos, mas não se aplica a luzes. Para obter mais informações sobre como trabalhar com as transformação do mundo, consulte [World Transform](/windows/desktop/direct3d9/world-transform).

A transformação de exibição controla a transição das coordenadas do mundo para o "espaço da câmera", determinando a posição da câmera no mundo. Para ver um exemplo de como trabalhar com as transformação de exibição, consulte [Exibir Transformar](/windows/desktop/direct3d9/view-transform).

A transformação de projeção altera a geometria do espaço da câmera para "espaço de clipe" e aplica distorção de perspectiva. O termo "espaço de clipe" refere-se a como a geometria é recortada para o volume de exibição durante essa transformação. Para ver um exemplo de como trabalhar com as transformação de projeção, consulte [Transformação de projeção.](/windows/desktop/direct3d9/projection-transform)

Por fim, a geometria no espaço de clipe é transformada em coordenadas de pixel (espaço na tela). Essa transformação é controlada pelas configurações do viewport.

O recorte e a transformação de vértices devem ocorrer no espaço homogêneo (simplesmente colocado, espaço no qual o sistema de coordenadas inclui um quarto elemento), mas o resultado final para a maioria dos aplicativos precisa ser coordenadas 3D (não homogêneas tridimensionais) definidas em "espaço na tela". Isso significa que os vértices de entrada e o volume de recorte devem ser convertidos em espaço homogêneo para executar o recorte e, em seguida, convertidos novamente em espaço não homogêneo a ser exibido.

As três transformações direct3D– mundo, exibição e transformação de projeção são definidas por matrizes Direct3D. Uma matriz Direct3D é uma matriz homogênea 4x4 definida por uma [**estrutura D3DMATRIX.**](/windows/desktop/direct3d9/d3dmatrix) Embora as matrizes direct3D não sejam objetos padrão, elas não são representadas por uma interface COM– você pode criar e defini-las da mesma forma que faria com qualquer outro objeto Direct3D. Para obter mais informações sobre matrizes direct3D, consulte [Transforms](/windows/desktop/direct3d9/transforms).

## <a name="the-transformation-pipeline"></a>O pipeline de transformação

Se um vértice na coordenada do modelo for dado por Pm = (Xm, Ym, Zm, 1), as transformações mostradas na figura a seguir serão aplicadas às coordenadas de tela de computação Ps = (Xs, Ys, Zs, Ws).

![espaço do modelo para a transformação de espaço na tela](images/d3dxfrm61.gif)

Aqui estão as descrições dos estágios mostrados na figura anterior:

1.  A matriz mundial Mworld transforma vértices do espaço do modelo para o espaço do mundo. Essa matriz é definida por:

    ``` syntax
        d3dDevice->SetTransform (D3DTRANSFORMSTATE_WORLD, matrix address) 
    ```

    A implementação do Direct3D supõe que a última coluna dessa matriz seja (0, 0, 0, 1). Nenhum erro será retornado se o usuário especificar uma matriz com uma última coluna diferente, mas a iluminação e a luz estarão incorretas.

2.  A matriz de exibição Mview transforma vértices do espaço do mundo para o espaço da câmera. Essa matriz é definida por:

    ``` syntax
        d3dDevice->SetTransform (D3DTRANSFORMSTATE_VIEW, matrix address) 
    ```

    A implementação do Direct3D supõe que a última coluna dessa matriz seja (0, 0, 0, 1). Nenhum erro será retornado se o usuário especificar uma matriz com a última coluna diferente, mas a iluminação e a luz estarão incorretas.

3.  A matriz de projeção Mproj transforma vértices do espaço da câmera para o espaço de projeção. Essa matriz é definida por:

    ``` syntax
        d3dDevice->SetTransform (D3DTRANSFORMSTATE_PROJECTION, matrix address) 
    ```

    A última coluna da matriz de projeção deve ser (0, 0, 1, 0) ou (0, 0, a, 0) para efeitos corretos de luminosidade e luminosidade; (0, 0, 1, 0) é preferencial.

    O volume de recorte para todos os pontos Xp = (Xp, Yp, Zp, Wp) no espaço de projeção é definido como:

    ``` syntax
        -Wp < Xp <= Wp 
        -Wp < Yp <= Wp 
        0 < Zp <= Wp 
    ```

    Todos os pontos que não atenderem a essas equações serão recortados.

    Se um volume de exibição for definido como:

    -   Largura da janela de tela de sw no espaço da câmera no plano de recorte próximo
    -   Altura da janela sh-screen no espaço da câmera no plano de recorte próximo
    -   Distância Zn para o plano de recorte próximo ao longo dos eixos Z no espaço da câmera
    -   Distância Zf para o plano de recorte distante ao longo dos eixos Z no espaço da câmera

    em seguida, uma matriz de projeção de perspectiva pode ser escrita da seguinte forma:

    ![Mostra uma matriz de projeção de perspectiva.](images/d3dxfrm62.gif)

    em que Mij são membros de Mproj.

    Para a projeção ortogonal, temos:

    ![projeção ortogonal](images/d3dxfrm63.gif)

    O Direct3D pressupo que a matriz de projeção de perspectiva tem o formato:

    ![matriz de projeção de perspectiva](images/d3dxfrm64.gif)

    Se a matriz de projeção de perspectiva não tiver esse formulário, haverá alguns artefatos. Por exemplo, a tabela não funcionará.

4.  O Direct3D permite que o usuário altere o volume do clipe da seguinte forma:

    ![alterar o volume do clipe](images/d3dxfrm65.gif)

    Isso pode ser reescrito como:

    ![alterar o volume de clipe reescrito](images/d3dxfrm66.gif)

    em que:

    ``` syntax
        Cx, Cy - dvClipX, dvClipY from D3DVIEWPORT9  
        Cw, Ch - dvClipWidth, dvClipHeight from D3DVIEWPORT9  
        Zmin, Zmax - dvMinZ, dvMaxZ from D3DVIEWPORT9  
    ```

    Essa transformação pode fornecer maior precisão e é equivalente a dimensionar e deslocar o volume de recorte.

    A matriz Mclip correspondente é:

    ![Matriz mclip](images/d3dxfrm67.gif)

    Um vértice é transformado por:

    ``` syntax
        dvClipWidth = 2   
        dvClipHeight = 2   
        dvClipX = -1   
        dvClipY = 1   
        dvMinZ = 0   
        dvMaxZ = 1   
    ```

    Se você não quiser dimensionar o volume do clipe, poderá definir parâmetros do viewport como valores padrão:

    ``` syntax
        (Xc, Yc, Zc, Wc) = (Xp, Yp, Zp, Wp) * Mclip   
    ```

5.  O estágio de recorte será opcional se o usuário especificar o sinalizador D3DDP \_ DONOTCLIP em uma chamada DrawPrimitive. Nesse caso, todas as matrizes (incluindo Mvs) podem ser combinadas.
6.  A matriz de escala do viewport Mvs dimensiona coordenadas para estar dentro da janela do viewport e inverte o eixo Y de cima para baixo:

    ![viewport scale matrix mvs](images/d3dxfrm68.gif)

    em que:

    ``` syntax
        dwX, dwY - viewport offsets in pixels from D3DVIEWPORT9 
        dwWidth, dwHeight - viewport width and height in pixels from D3DVIEWPORT9    
    ```

7.  Por fim, as coordenadas de tela são computadas e passadas para o rasterizador:

    ![coordenadas de tela computadas e passadas para o rasterizador](images/d3dxfrm69.gif)

## <a name="usage-tips"></a>Uso Dicas

Aqui estão algumas dicas de como usar o Pipeline de Transformação Direct3D:

-   A última coluna do mundo e as matrizes de exibição devem ser (0, 0, 0, 1) ou a iluminação estará incorreta.
-   De definir os parâmetros do viewport para criar uma matriz de Mclip de identidade, a menos que você entenda exatamente para que ela é necessária.

    ``` syntax
        dvClipWidth = 2 
        dvClipHeight = 2
        dvClipX = -1
        dvClipY = 1
        dvMinZ = 0 
        dvMaxZ = 1
    ```

 

 