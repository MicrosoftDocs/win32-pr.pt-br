---
title: Introdução com o estágio rasterizador
description: Esta seção descreve como definir o visor, o retângulo de tesoura, o estado do rasterizador e a várias amostras.
ms.assetid: d78c3845-76fd-4bd7-a603-bb1d8c66ac49
keywords:
- multiamostrando, estado do rasterizador (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e819dd92dd9c07a71f3830d3b67e371bc3d0e0c98f62fa36fdcf8ee3550ecd3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117913997"
---
# <a name="getting-started-with-the-rasterizer-stage"></a>Introdução com o estágio rasterizador

Esta seção descreve como definir o visor, o retângulo de tesoura, o estado do rasterizador e a várias amostras.

## <a name="set-the-viewport"></a>Definir o visor

Um visor mapeia as posições de vértice (no espaço de clipe) para processar posições de destino. Esta etapa dimensiona as posições 3D em espaço 2D. Um destino de renderização é orientado com os eixos Y apontando para baixo; Isso requer que as coordenadas Y sejam invertidas durante a escala do visor. Além disso, as extensões x e y (intervalo dos valores x e y) são dimensionadas para se ajustarem ao tamanho do visor de acordo com as fórmulas a seguir:


```
X = (X + 1) * Viewport.Width * 0.5 + Viewport.TopLeftX
Y = (1 - Y) * Viewport.Height * 0.5 + Viewport.TopLeftY
Z = Viewport.MinDepth + Z * (Viewport.MaxDepth - Viewport.MinDepth) 
```



O tutorial 1 cria um visor 640 × 480 usando o [**\_ visor D3D11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_viewport) e chamando [**ID3D11DeviceContext:: RSSetViewports**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-rssetviewports).


```
    D3D11_VIEWPORT vp[1];
    vp[0].Width = 640.0f;
    vp[0].Height = 480.0f;
    vp[0].MinDepth = 0;
    vp[0].MaxDepth = 1;
    vp[0].TopLeftX = 0;
    vp[0].TopLeftY = 0;
    g_pd3dDevice->RSSetViewports( 1, vp );
```



A descrição do visor especifica o tamanho do visor, o intervalo para mapear profundidade (usando *MinDepth* e *MaxDepth*) e o posicionamento da parte superior esquerda do visor. *MinDepth* deve ser menor ou igual a *MaxDepth*; o intervalo para *MinDepth* e *MaxDepth* está entre 0,0 e 1,0, inclusive. É comum que o visor mapeie para um destino de renderização, mas não é necessário; Além disso, o visor não precisa ter o mesmo tamanho ou posição que o destino de renderização.

Você pode criar uma matriz de visores, mas apenas um pode ser aplicado a uma saída primitiva do sombreador de geometria. Somente um visor pode ser definido de modo ativo por vez. O pipeline usa um visor padrão (e um retângulo de mola, discutido na próxima seção) durante a rasterização. O padrão é sempre o primeiro visor (ou retângulo de mola) na matriz. Para executar uma seleção por primitiva do visor no sombreador Geometry, especifique a semântica ViewportArrayIndex no componente de saída GS apropriado na declaração de assinatura de saída GS.

O número máximo de visores (e retângulos de recorte) que podem ser vinculados ao estágio de rasterizador a qualquer momento é 16 (especificado pelo **\_ visor D3D11 \_ e \_ contagem de \_ objetos SCISSORRECT \_ \_ por \_ pipeline**).

## <a name="set-the-scissor-rectangle"></a>Definir o retângulo da mola

Um retângulo de recorte dá a você outra oportunidade de reduzir o número de pixels que serão enviados para o estágio de fusão de saída. Os pixels fora do retângulo da mola são descartados. O tamanho do retângulo da mola é especificado em inteiros. Somente um retângulo de recorte (baseado em *ViewportArrayIndex* na [semântica de valor do sistema](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-semantics)) pode ser aplicado a um triângulo durante a rasterização.

Para habilitar o retângulo de mola, use o membro *ScissorEnable* (no [**D3D11 \_ rasterizador \_ DESC1**](/windows/desktop/api/D3D11_1/ns-d3d11_1-cd3d11_rasterizer_desc1)). O retângulo de tesoura padrão é um retângulo vazio; ou seja, todos os valores de RECT são 0. Em outras palavras, se você não configurar o retângulo de corte e a tesoura estiver habilitada, você não enviará nenhum pixel para o estágio de mesclagem de saída. A configuração mais comum é inicializar o retângulo de mola até o tamanho do visor.

Para definir uma matriz de retângulos de mola para o dispositivo, chame [**ID3D11DeviceContext:: RSSetScissorRects**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-rssetscissorrects) com [**D3D11 \_ Rect**](d3d11-rect.md).


```
D3D11_RECT rects[1];
  rects[0].left = 0;
  rects[0].right = 640;
  rects[0].top = 0;
  rects[0].bottom = 480;

  D3DDevice->RSSetScissorRects( 1, rects );
```



Esse método usa dois parâmetros: (1) o número de retângulos na matriz e (2) uma matriz de retângulos.

O pipeline usa um índice de retângulo de tesoura padrão durante a rasterização (o padrão é um retângulo de tamanho zero com recorte desabilitado). Para substituir isso, especifique a \_ semântica ViewportArrayIndex de VA para um componente de saída GS na declaração de assinatura de saída GS. Isso fará com que o estágio GS marque esse componente de saída GS como um componente gerado pelo sistema com essa semântica. O estágio rasterizador reconhece essa semântica e usará o parâmetro ao qual ele está anexado como o índice de retângulo de mola para acessar a matriz de retângulos de recorte. Não se esqueça de instruir o estágio de rasterizador a usar o retângulo de recorte definido por meio da habilitação do valor *ScissorEnable* na descrição do rasterizador antes de criar o objeto rasterizador.

## <a name="set-rasterizer-state"></a>Definir estado do rasterizador

Começando com o Direct3D 10, o estado do rasterizador é encapsulado em um objeto de estado do rasterizador. Você pode criar até 4096 objetos de estado do rasterizador que podem ser definidos para o dispositivo passando um identificador para o objeto de estado.

Use [**ID3D11Device1:: CreateRasterizerState1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11device1-createrasterizerstate1) para criar um objeto de estado do rasterizador a partir de uma descrição do rasterizador (consulte [**D3D11 do \_ rasterizador \_ DESC1**](/windows/desktop/api/D3D11_1/ns-d3d11_1-cd3d11_rasterizer_desc1)).


```
    ID3D11RasterizerState1 * g_pRasterState;

    D3D11_RASTERIZER_DESC1 rasterizerState;
    rasterizerState.FillMode = D3D11_FILL_SOLID;
    rasterizerState.CullMode = D3D11_CULL_FRONT;
    rasterizerState.FrontCounterClockwise = true;
    rasterizerState.DepthBias = false;
    rasterizerState.DepthBiasClamp = 0;
    rasterizerState.SlopeScaledDepthBias = 0;
    rasterizerState.DepthClipEnable = true;
    rasterizerState.ScissorEnable = true;
    rasterizerState.MultisampleEnable = false;
    rasterizerState.AntialiasedLineEnable = false;
    rasterizerState.ForcedSampleCount = 0;
    pd3dDevice->CreateRasterizerState1( &rasterizerState, &g_pRasterState );
```



Esse conjunto de exemplo de estado realiza talvez a configuração mais básica do rasterizador:

-   Modo de preenchimento sólido
-   Excluir ou remover faces traseiras; assumir a ordem de enrolamento no sentido anti-horário para primitivos
-   Desativar a tendência de profundidade, mas habilitar o buffer de profundidade e habilitar o retângulo de mola
-   Desligar a multiamostra e a suavização de linha

Além disso, as operações básicas do rasterizador, sempre incluem o seguinte: recorte (para a exibição frustum), divisão em perspectiva e escala do visor. Depois de criar com êxito o objeto de estado do rasterizador, defina-o para o dispositivo da seguinte maneira:


```
    pd3dDevice->RSSetState(g_pRasterState);
```



### <a name="multisampling"></a>Amostragem múltipla

As amostras de multiamostragem são alguns ou todos os componentes de uma imagem em uma resolução mais alta (seguida pela redução da resolução original) para reduzir a forma mais visível de alias causada pelo desenho de bordas do polígono. Embora a multiamostração exija amostras de sub-pixel, a GPU moderna implementa multiamostrar para que um sombreador de pixel seja executado uma vez por pixel. Isso fornece uma compensação aceitável entre o desempenho (especialmente em um aplicativo vinculado à GPU) e a suavização da imagem final.

Para usar a multiamostragem, defina o campo habilitar na [**Descrição da rasterização**](/windows/desktop/api/D3D11_1/ns-d3d11_1-cd3d11_rasterizer_desc1), crie um destino de renderização com uma amostra e leia o destino de renderização com um sombreador para resolver os exemplos em uma única cor de pixel ou chame [**ID3D11DeviceContext:: ResolveSubresource**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-resolvesubresource) para resolver os exemplos usando a placa de vídeo. O cenário mais comum é desenhar para um ou mais destinos de renderização multiamostrados.

A multiamostragem é independente de ser usada ou não por uma máscara de exemplo, o [alfa-to-Coverage](d3d10-graphics-programming-guide-blend-state.md) é habilitado ou as operações de estêncil (que são sempre executadas por amostra).

O teste de profundidade é afetado por multiamostragem:

-   Quando a multiamostragem está habilitada, a profundidade é interpolada por amostra e o teste de profundidade/estêncil é feito por amostra; a cor de saída do sombreador de pixel é duplicada para todos os exemplos de passagem. Se o sombreador de pixel gerar profundidade, o valor de profundidade será duplicado para todos os exemplos (embora esse cenário perca o benefício de uma multiamostragem).
-   Quando a multiamostração está desabilitada, o teste de profundidade/estêncil ainda é feito por amostra, mas a profundidade não é interpolada por amostra.

Não há restrições para misturar renderização de multiamostra e sem amostra em um único destino de renderização. Se você habilitar a multiamostrar e desenhar para um destino de renderização não multiamostrado, produzirá o mesmo resultado que se a multiamostragem não estivesse habilitada; a amostragem é feita com um único exemplo por pixel.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Estágio de rasterizador](d3d10-graphics-programming-guide-rasterizer-stage.md)
</dt> </dl>

 

 