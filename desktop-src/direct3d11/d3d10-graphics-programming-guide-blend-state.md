---
title: Configurando a funcionalidade de mesclagem
description: As operações de mesclagem são executadas em cada saída de sombreador de pixel (valor RGBA) antes que o valor de saída seja gravado em um destino de renderização. Se a multiamostragem estiver habilitada, a mesclagem será feita em cada multiamostra; caso contrário, a mesclagem será executada em cada pixel.
ms.assetid: f5c79baf-7bd3-4f58-abe7-8e96cd6be9d3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08acf1ea286b29a1cb96873bbfe170c6f38699f7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104988661"
---
# <a name="configuring-blending-functionality"></a>Configurando a funcionalidade de mesclagem

As operações de mesclagem são executadas em cada saída de sombreador de pixel (valor RGBA) antes que o valor de saída seja gravado em um destino de renderização. Se a multiamostragem estiver habilitada, a mesclagem será feita em cada multiamostra; caso contrário, a mesclagem será executada em cada pixel.

-   [Criar o estado de mesclagem](#create-the-blend-state)
-   [Associar o estado de mesclagem](#bind-the-blend-state)
-   [Tópicos de mesclagem avançada](#advanced-blending-topics)
    -   [De alfa para cobertura](#alpha-to-coverage)
    -   [Mesclagem de saídas de sombreador de pixel](#blending-pixel-shader-outputs)
-   [Tópicos relacionados](#related-topics)

## <a name="create-the-blend-state"></a>Criar o estado de mesclagem

O estado de mesclagem é uma coleção de Estados usados para controlar a mesclagem. Esses Estados (definidos no [**D3D11 \_ Blend \_ DESC1**](/windows/desktop/api/D3D11_1/ns-d3d11_1-cd3d11_blend_desc1)) são usados para criar o objeto de estado de mistura chamando [**ID3D11Device1:: CreateBlendState1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11device1-createblendstate1).

Por exemplo, aqui está um exemplo muito simples de criação de estado de mesclagem que desabilita a mistura alfa e não usa mascaramento de pixel por componente.


```
ID3D11BlendState1* g_pBlendStateNoBlend = NULL;

D3D11_BLEND_DESC1 BlendState;
ZeroMemory(&BlendState, sizeof(D3D11_BLEND_DESC1));
BlendState.RenderTarget[0].BlendEnable = FALSE;
BlendState.RenderTarget[0].RenderTargetWriteMask = D3D11_COLOR_WRITE_ENABLE_ALL;
pd3dDevice->CreateBlendState1(&BlendState, &g_pBlendStateNoBlend);
```



Este exemplo é semelhante ao [exemplo de HLSLWithoutFX10](https://msdn.microsoft.com/library/Ee416414(v=VS.85).aspx).

## <a name="bind-the-blend-state"></a>Associar o estado de mesclagem

Depois de criar o objeto de estado de mesclagem, associe o objeto de estado de mesclagem ao estágio de mesclagem de saída chamando [**ID3D11DeviceContext:: OMSetBlendState**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-omsetblendstate).


```
float blendFactor[4] = { 0.0f, 0.0f, 0.0f, 0.0f };
UINT sampleMask   = 0xffffffff;

pd3dDevice->OMSetBlendState(g_pBlendStateNoBlend, blendFactor, sampleMask);
```



Essa API usa três parâmetros: o objeto de estado de mesclagem, um fator de mistura de quatro componentes e uma máscara de exemplo. Você pode passar **NULL** para o objeto de estado de mesclagem para especificar o estado de mesclagem padrão ou passar um objeto de estado de mesclagem. Se você criou o objeto de estado de mesclagem com o fator de mesclagem do [**D3D11 \_ Blend \_ \_**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_blend) ou o [**fator de mistura do D3D11 \_ Blend \_ inv \_ \_**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_blend), você pode passar um fator de mistura para valores modulares para o sombreador de pixel, o destino de renderização ou ambos. Se você não criou o objeto Blend-State com o fator de mistura do **D3D11 \_ Blend \_ \_** ou o **fator de mistura do D3D11 \_ Blend \_ inv \_ \_**, ainda é possível passar um fator de mistura não nulo, mas o estágio de mesclagem não usa o fator de mistura; o tempo de execução armazena o fator de mistura e, posteriormente, você pode chamar [**ID3D11DeviceContext:: OMGetBlendState**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-omgetblendstate) para recuperar o fator de mistura. Se você passar **NULL**, o tempo de execução usará ou armazenará um fator de mistura igual a {1, 1, 1, 1}. A máscara de exemplo é uma máscara definida pelo usuário que determina como obter uma amostra do destino de renderização existente antes de atualizá-lo. A máscara de amostragem padrão é 0xFFFFFFFF, que designa a amostragem de ponto.

Na maioria dos esquemas de buffer mais detalhados, o pixel mais próximo da câmera é aquele que é desenhado. Ao [Configurar o estado de estêncil de profundidade](d3d10-graphics-programming-guide-depth-stencil.md), o membro **DepthFunc** do [**estêncil de profundidade D3D11 \_ \_ \_ desc**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_depth_stencil_desc) pode ser qualquer [**D3D11 de \_ comparação \_ Func**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_comparison_func). Normalmente, você desejaria que **DepthFunc** fosse **D3D11 de \_ comparação \_**, para que os pixels mais próximos da câmera substituam os pixels por trás deles. No entanto, dependendo das necessidades do seu aplicativo, qualquer uma das outras funções de comparação pode ser usada para fazer o teste de profundidade.

## <a name="advanced-blending-topics"></a>Tópicos de mesclagem avançada

-   [De alfa para cobertura](#alpha-to-coverage)
-   [Mesclagem de saídas de sombreador de pixel](#blending-pixel-shader-outputs)

### <a name="alpha-to-coverage"></a>De alfa para cobertura

Alfa-to-Coverage é uma técnica de várias amostras que é mais útil para situações como folhagem densas em que há vários polígonos sobrepostos que usam transparência alfa para definir bordas dentro da superfície.

Você pode usar o membro **AlphaToCoverageEnable** do [**D3D11 \_ Blend \_ DESC1**](/windows/desktop/api/D3D11_1/ns-d3d11_1-cd3d11_blend_desc1) ou [**D3D11 \_ Blend \_ desc**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_blend_desc) para alternar se o tempo de execução converte o. um componente (alfa) do registro de saída [VA de \_ destino](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-semantics)0 do sombreador de pixel para uma máscara de cobertura de n etapas (dada um **renderTarget** de n amostras). O tempo de execução executa uma operação **and** dessa máscara com a cobertura de exemplo típica para o pixel na primitiva (além da máscara de exemplo) para determinar quais amostras atualizar em todos os **renderTarget** s ativos.

Se o sombreador de pixel gerar a [ \_ cobertura da VA](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-semantics), o tempo de execução desabilitará alfa para cobertura.

> [!Note]  
> Em multiamostragens, o tempo de execução compartilha apenas uma cobertura para todos os **renderTarget** s. O fato de que o tempo de execução lê e converte. a da saída [VA de \_ destino](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-semantics)0 para cobertura quando **AlphaToCoverageEnable** é true não altera o. um valor que vai para o Blender em **renderTarget** 0 (se um **renderTarget** for definido aqui). Em geral, se você habilitar a Alpha-to-Coverage, não afetará como todas as saídas de cores de sombreadores de pixel interagem com **renderTarget** s por meio do [estágio de mesclagem de saída](d3d10-graphics-programming-guide-output-merger-stage.md) , exceto que o tempo de execução executa uma operação **and** da máscara de cobertura com a máscara de alfa para cobertura. Alfa-to-Coverage funciona de forma independente se o tempo de execução pode misturar **renderTarget** ou se você usa a mesclagem em **renderTarget**.

 

O hardware de gráficos não especifica precisamente exatamente como converte o pixel shader [VA \_ target](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-semantics)0. a (Alpha) em uma máscara de cobertura, exceto que alfa de 0 (ou menos) deve mapear para sem cobertura e alfa de 1 (ou superior) deve mapear para cobertura completa (antes de o tempo de execução executar uma operação **and** com cobertura primitiva real). Como Alfa vai de 0 a 1, a cobertura resultante geralmente aumenta de forma monotônico. No entanto, o hardware pode executar o pontilhamento de área para fornecer uma melhor quantificação de valores Alfa ao custo da resolução espacial e do ruído. Um valor alfa de NaN (não um número) resulta em uma máscara sem cobertura (zero).

A Alpha-to-Coverage também é tradicionalmente usada para transparência da porta de tela ou definindo silhuetas detalhadas para sprites opacos de outra forma.

### <a name="blending-pixel-shader-outputs"></a>Mesclagem de saídas de sombreador de pixel

Esse recurso permite que a mesclagem de saída use as saídas do sombreador de pixel simultaneamente como fontes de entrada para uma operação de mesclagem com o destino de renderização único no slot 0.

Este exemplo usa dois resultados e os combina em uma única passagem, combinando um no destino com uma multiplicação e o outro com um add:


```
SrcBlend = D3D11_BLEND_ONE;
DestBlend = D3D11_BLEND_SRC1_COLOR;
```



Este exemplo configura a primeira saída do sombreador de pixel como a cor de origem e a segunda saída como um fator de mistura de componente por cor.


```
SrcBlend = D3D11_BLEND_SRC1_COLOR;
DestBlend = D3D11_BLEND_INV_SRC1_COLOR;
```



Este exemplo ilustra como os fatores de mistura devem corresponder ao sombreador swizzles:


```
SrcFactor = D3D11_BLEND_SRC1_ALPHA;
DestFactor = D3D11_BLEND_SRC_COLOR;
OutputWriteMask[0] = .ra; // pseudocode for setting the mask at
                          // RenderTarget slot 0 to .ra
```



Juntos, os fatores de mistura e o código do sombreador sugerem que o sombreador de pixel é necessário para produzir pelo menos o0. r e o1. a. Os componentes de saída extra podem ser gerados pelo sombreador, mas seriam ignorados, menos componentes produzirão resultados indefinidos.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Estágio de fusão de saída](d3d10-graphics-programming-guide-output-merger-stage.md)
</dt> <dt>

[Estágios de pipeline (Direct3D 10)](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-pipeline-stages)
</dt> </dl>

 

 