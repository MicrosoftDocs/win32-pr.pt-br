---
title: O pipeline de transformação do Direct3D
description: Este artigo fornece uma explicação técnica para desenvolvedores de aplicativos Direct3D sobre como definir os parâmetros do pipeline de transformação Direct3D pela manipulação direta de matrizes de Direct3D.
ms.assetid: 48ae49f0-1162-c292-4bd4-34da5aadd2df
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2b97a87293a840ccd9641b1418c2005cf73a855
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/04/2021
ms.locfileid: "103837542"
---
# <a name="the-direct3d-transformation-pipeline"></a>O pipeline de transformação do Direct3D

Este artigo fornece uma explicação técnica para desenvolvedores de aplicativos Direct3D sobre como definir os parâmetros do pipeline de transformação Direct3D pela manipulação direta de matrizes de Direct3D.

-   [Visão geral](#overview)
-   [O pipeline de transformação](#the-transformation-pipeline)
-   [Dicas de uso](#usage-tips)

## <a name="overview"></a>Visão geral

O Direct3D usa três transformações para alterar suas coordenadas de modelo 3D em coordenadas de pixel (espaço da tela). Essas transformações são transformação de mundo, transformação de exibição e transformação de projeção.

A transformação mundial controla como as coordenadas de modelo são transformadas em coordenadas mundiais. A transformação mundial pode incluir traduções, rotações e escalas, mas não se aplica a luzes. Para obter mais informações sobre como trabalhar com transformações mundiais, consulte [World Transform](/windows/desktop/direct3d9/world-transform).

Exibir os controles de transformação a transição do mundo coordena para "espaço da câmera", determinando a posição da câmera no mundo. Para obter um exemplo de como trabalhar com transformações de exibição, consulte [Exibir transformação](/windows/desktop/direct3d9/view-transform).

A transformação projeção altera a geometria do espaço da câmera para o "espaço do clipe" e aplica a distorção de perspectiva. O termo "espaço do clipe" refere-se a como a geometria é recortada para o volume de exibição durante essa transformação. Para obter um exemplo de como trabalhar com transformações de projeção, consulte [projetion Transform](/windows/desktop/direct3d9/projection-transform).

Por fim, a geometria no espaço do clipe é transformada em coordenadas de pixel (espaço na tela). Essa transformação é controlada pelas configurações do visor.

Os vértices de recorte e transformação devem ocorrer no espaço homogêneo (simplesmente put, espaço no qual o sistema de coordenadas inclui um quarto elemento), mas o resultado final para a maioria dos aplicativos precisa ser coordenadas tridimensionais (3D) não homogêneas definidas no "espaço da tela". Isso significa que os vértices de entrada e o volume de recorte devem ser convertidos em espaço homogêneo para executar o recorte e, em seguida, convertidos novamente em espaço não homogêneo para serem exibidos.

As três transformações do Direct3D – mundo, exibição e transformação de projeção – são definidas por matrizes de Direct3D. Uma matriz de Direct3D é uma matriz homogênea 4x4 definida por uma estrutura [**D3DMATRIX**](/windows/desktop/direct3d9/d3dmatrix) . Embora as matrizes de Direct3D não sejam objetos padrão-elas não são representadas por uma interface COM, você pode criá-las e defini-las como faria com qualquer outro objeto do Direct3D. Para obter mais informações sobre matrizes de Direct3D, consulte [transformações](/windows/desktop/direct3d9/transforms).

## <a name="the-transformation-pipeline"></a>O pipeline de transformação

Se um vértice na coordenada de modelo for fornecido por PM = (XM, YM, ZM, 1), as transformações mostradas na figura a seguir serão aplicadas às coordenadas da tela de computação PS = (XS, haves, ZS, WS).

![espaço de modelo para transformação de espaço na tela](images/d3dxfrm61.gif)

Aqui estão as descrições dos estágios mostrados na figura anterior:

1.  O World Matrix Mworld transforma os vértices do espaço do modelo no espaço do mundo. Essa matriz é definida por:

    ``` syntax
        d3dDevice->SetTransform (D3DTRANSFORMSTATE_WORLD, matrix address) 
    ```

    A implementação do Direct3D pressupõe que a última coluna dessa matriz é (0, 0, 0, 1). Nenhum erro será retornado se o usuário especificar uma matriz com uma última coluna diferente, mas a iluminação e a neblina estarão incorretas.

2.  Exibir MVIEW de matriz transforma vértices do espaço do mundo para o espaço da câmera. Essa matriz é definida por:

    ``` syntax
        d3dDevice->SetTransform (D3DTRANSFORMSTATE_VIEW, matrix address) 
    ```

    A implementação do Direct3D pressupõe que a última coluna dessa matriz é (0, 0, 0, 1). Nenhum erro será retornado se o usuário especificar uma matriz com a última coluna diferente, mas a iluminação e a neblina ficarão incorretas.

3.  A matriz de projeção mproj transforma os vértices do espaço da câmera no espaço de projeção. Essa matriz é definida por:

    ``` syntax
        d3dDevice->SetTransform (D3DTRANSFORMSTATE_PROJECTION, matrix address) 
    ```

    A última coluna da matriz de projeção deve ser (0, 0, 1, 0) ou (0, 0, a, 0) para efeitos corretos de neblina e iluminação; o formulário (0, 0, 1, 0) é preferencial.

    O volume de recorte para todos os pontos XP = (XP, YP, ZP, WP) no espaço de projeção é definido como:

    ``` syntax
        -Wp < Xp <= Wp 
        -Wp < Yp <= Wp 
        0 < Zp <= Wp 
    ```

    Todos os pontos que não atenderem a essas equações serão recortados.

    Se um volume de exibição for definido como:

    -   SW-largura da janela de tela no espaço da câmera no plano de recorte próximo
    -   SH-altura da janela de tela no espaço da câmera no plano de recorte próximo
    -   Zn-distância ao próximo plano de recorte ao longo dos eixos Z no espaço da câmera
    -   ZF-distância até o plano de recorte distante ao longo dos eixos Z no espaço da câmera

    em seguida, uma matriz de projeção em perspectiva poderia ser escrita da seguinte maneira:

    ![Mostra uma matriz de projeção em perspectiva.](images/d3dxfrm62.gif)

    em que MIJ são membros de mproj.

    Para a projeção ortogonal, temos:

    ![projeção ortogonal](images/d3dxfrm63.gif)

    O Direct3D pressupõe que a matriz de projeção de perspectiva tem o formato:

    ![matriz de projeção em perspectiva](images/d3dxfrm64.gif)

    Se a matriz de projeção de perspectiva não tiver esse formulário, haverá alguns artefatos. Por exemplo, a sombra da tabela não funcionará.

4.  O Direct3D permite que o usuário altere o volume do clipe da seguinte maneira:

    ![alterar o volume do clipe](images/d3dxfrm65.gif)

    Isso pode ser reescrito como:

    ![alterar o volume do clipe regravado](images/d3dxfrm66.gif)

    onde:

    ``` syntax
        Cx, Cy - dvClipX, dvClipY from D3DVIEWPORT9  
        Cw, Ch - dvClipWidth, dvClipHeight from D3DVIEWPORT9  
        Zmin, Zmax - dvMinZ, dvMaxZ from D3DVIEWPORT9  
    ```

    Essa transformação pode fornecer maior precisão e equivale a dimensionar e deslocar o volume de recorte.

    A matriz Mclip correspondente é:

    ![matriz mclip](images/d3dxfrm67.gif)

    Um vértice é transformado por:

    ``` syntax
        dvClipWidth = 2   
        dvClipHeight = 2   
        dvClipX = -1   
        dvClipY = 1   
        dvMinZ = 0   
        dvMaxZ = 1   
    ```

    Se você não quiser dimensionar o volume do clipe, poderá definir os parâmetros do visor para os valores padrão:

    ``` syntax
        (Xc, Yc, Zc, Wc) = (Xp, Yp, Zp, Wp) * Mclip   
    ```

5.  O estágio de recorte será opcional se o usuário especificar o \_ sinalizador D3DDP DONOTCLIP em uma chamada DrawPrimitive. Nesse caso, todas as matrizes (incluindo MVS) podem ser combinadas.
6.  A matriz de escala do visor MVS dimensiona as coordenadas para estar dentro da janela viewport e inverte o eixo Y de cima para baixo:

    ![MVS da matriz de escala do visor](images/d3dxfrm68.gif)

    onde:

    ``` syntax
        dwX, dwY - viewport offsets in pixels from D3DVIEWPORT9 
        dwWidth, dwHeight - viewport width and height in pixels from D3DVIEWPORT9    
    ```

7.  Por fim, as coordenadas da tela são computadas e passadas para o rasterizador:

    ![coordenadas de tela computadas e passadas para o rasterizador](images/d3dxfrm69.gif)

## <a name="usage-tips"></a>Dicas de uso

Aqui estão algumas dicas sobre como usar o pipeline de transformação do Direct3D:

-   A última coluna do mundo e as matrizes de exibição devem ser (0, 0, 0, 1) ou a iluminação estará incorreta.
-   Defina os parâmetros do visor para criar uma matriz de identidade Mclip, a menos que você entenda exatamente o que é necessário para o.

    ``` syntax
        dvClipWidth = 2 
        dvClipHeight = 2
        dvClipX = -1
        dvClipY = 1
        dvMinZ = 0 
        dvMaxZ = 1
    ```

 

 