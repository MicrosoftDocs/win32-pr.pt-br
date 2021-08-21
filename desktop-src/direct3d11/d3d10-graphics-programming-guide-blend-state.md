---
title: Configurando a funcionalidade do Blending
description: As operações de mesclagem são executadas em cada saída do sombreador de pixel (valor RGBA) antes que o valor de saída seja gravado em um destino de renderização. Se a multisampling estiver habilitada, a combinação será feita em cada multisample; caso contrário, a mesclagem será executada em cada pixel.
ms.assetid: f5c79baf-7bd3-4f58-abe7-8e96cd6be9d3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0de75e092a08a0dae83cd966cd986469cef9a6ea34e51c237800bf96b3a84232
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118808196"
---
# <a name="configuring-blending-functionality"></a>Configurando a funcionalidade do Blending

As operações de mesclagem são executadas em cada saída do sombreador de pixel (valor RGBA) antes que o valor de saída seja gravado em um destino de renderização. Se a multisampling estiver habilitada, a combinação será feita em cada multisample; caso contrário, a mesclagem será executada em cada pixel.

-   [Criar o estado do Blend](#create-the-blend-state)
-   [Vincular o estado do Blend](#bind-the-blend-state)
-   [Tópicos do Advanced Blending](#advanced-blending-topics)
    -   [Alfa para cobertura](#alpha-to-coverage)
    -   [Mesclando saídas de sombreador de pixel](#blending-pixel-shader-outputs)
-   [Tópicos relacionados](#related-topics)

## <a name="create-the-blend-state"></a>Criar o estado do Blend

O estado blend é uma coleção de estados usados para controlar a combinação. Esses estados (definidos em [**D3D11 \_ BLEND \_ DESC1**](/windows/desktop/api/D3D11_1/ns-d3d11_1-cd3d11_blend_desc1)) são usados para criar o objeto de estado blend chamando [**ID3D11Device1::CreateBlendState1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11device1-createblendstate1).

Por exemplo, aqui está um exemplo muito simples de criação de blend-state que desabilita a combinação alfa e não usa nenhuma máscara de pixel por componente.


```
ID3D11BlendState1* g_pBlendStateNoBlend = NULL;

D3D11_BLEND_DESC1 BlendState;
ZeroMemory(&BlendState, sizeof(D3D11_BLEND_DESC1));
BlendState.RenderTarget[0].BlendEnable = FALSE;
BlendState.RenderTarget[0].RenderTargetWriteMask = D3D11_COLOR_WRITE_ENABLE_ALL;
pd3dDevice->CreateBlendState1(&BlendState, &g_pBlendStateNoBlend);
```



Este exemplo é semelhante ao [exemplo HLSLWithoutFX10](https://msdn.microsoft.com/library/Ee416414(v=VS.85).aspx).

## <a name="bind-the-blend-state"></a>Vincular o estado do Blend

Depois de criar o objeto blend-state, a bind o objeto blend-state ao estágio de fusão de saída chamando [**ID3D11DeviceContext::OMSetBlendState**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-omsetblendstate).


```
float blendFactor[4] = { 0.0f, 0.0f, 0.0f, 0.0f };
UINT sampleMask   = 0xffffffff;

pd3dDevice->OMSetBlendState(g_pBlendStateNoBlend, blendFactor, sampleMask);
```



Essa API aceita três parâmetros: o objeto blend-state, um fator de combinação de quatro componentes e uma máscara de exemplo. Você pode passar **NULL para** o objeto blend-state para especificar o estado de mesclagem padrão ou passar um objeto blend-state. Se você criou o objeto blend-state com [**D3D11 \_ BLEND BLEND BLEND \_ \_ FACTOR**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_blend) ou [**D3D11 \_ BLEND \_ INV BLEND \_ \_ FACTOR**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_blend), você pode passar um fator blend para modular valores para o sombreador de pixel, renderizar destino ou ambos. Se você não tiver criado o objeto blend-state com **D3D11 \_ BLEND \_ BLEND \_ FACTOR** ou **D3D11 \_ BLEND \_ INV BLEND \_ \_ FACTOR**, você ainda poderá passar um fator de combinação não NULL, mas o estágio de combinação não usará o fator blend; o runtime armazenará o fator blend e, posteriormente, você poderá chamar [**ID3D11DeviceContext::OMGetBlendState**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-omgetblendstate) para recuperar o fator blend. Se você passar **NULL,** o runtime usará ou armazenará um fator de mesclagem igual a { 1, 1, 1, 1 }. A máscara de exemplo é uma máscara definida pelo usuário que determina como amostrar o destino de renderização existente antes de atualizá-lo. A máscara de amostragem padrão é 0xffffffff que designa a amostragem de ponto.

Em esquemas de buffer mais profundos, o pixel mais próximo da câmera é aquele que é desenhado. Ao [configurar o estado de estêncil](d3d10-graphics-programming-guide-depth-stencil.md)de profundidade , o membro **DepthFunc** da [**D3D11 \_ DEPTH \_ STENCIL \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_depth_stencil_desc) pode ser qualquer [**D3D11 \_ COMPARISON \_ FUNC**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_comparison_func). Normalmente, você deseja **que DepthFunc** seja **D3D11 \_ COMPARISON \_ LESS,** de modo que os pixels mais próximos da câmera substituirão os pixels por trás deles. No entanto, dependendo das necessidades do seu aplicativo, qualquer uma das outras funções de comparação pode ser usada para fazer o teste de profundidade.

## <a name="advanced-blending-topics"></a>Tópicos do Advanced Blending

-   [Alfa para cobertura](#alpha-to-coverage)
-   [Mesclando saídas de sombreador de pixel](#blending-pixel-shader-outputs)

### <a name="alpha-to-coverage"></a>Alfa para cobertura

A alfa para cobertura é uma técnica multisampling que é mais útil para situações como densa, em que há vários polígonos sobrepostos que usam transparência alfa para definir bordas dentro da superfície.

Você pode usar o membro **AlphaToCoverageEnable** de [**D3D11 \_ BLEND \_ DESC1**](/windows/desktop/api/D3D11_1/ns-d3d11_1-cd3d11_blend_desc1) ou [**D3D11 \_ BLEND \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_blend_desc) para alternar se o runtime converte o componente .a (alfa) do registro de saída [SV \_ Target](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-semantics)0 do sombreador de pixel em uma máscara de cobertura de n etapas (considerando um **RenderTarget** de n amostras). O runtime executa uma operação **AND** dessa máscara com a cobertura de exemplo típica para o pixel no primitivo (além da máscara de exemplo) para determinar quais amostras atualizar em todos os **RenderTarget** s ativos.

Se o sombreador de pixels saída cobertura [SV \_ ](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-semantics), o runtime desabilita alfa para cobertura.

> [!Note]  
> Em multisampling, o runtime compartilha apenas uma cobertura para todos os **RenderTarget** s. O fato de que o runtime lê e converte .a da saída [SV \_ Target](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-semantics)0 para cobertura quando **AlphaToCoverageEnable** é TRUE não altera o valor .a que vai para o blender em **RenderTarget** 0 (se um **RenderTarget** estiver definido lá). Em geral, se você habilitar alfa para cobertura, não afetará como todas as saídas [](d3d10-graphics-programming-guide-output-merger-stage.md) de cores de sombreadores de pixel interagem com **RenderTarget** s por meio do estágio de fusão de saída, exceto que o runtime executa uma operação **AND** da máscara de cobertura com a máscara alfa para cobertura. A alfa para cobertura funciona independentemente se o runtime pode combinar **RenderTarget** ou se você usa a mesclagem no **RenderTarget.**

 

O hardware gráfico não especifica exatamente como ele converte o sombreador de pixel [SV \_ Target](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-semantics)0.a (alfa) em uma máscara de cobertura, exceto que o alfa de 0 (ou menos) deve ser mapeado para nenhuma cobertura e o alfa de 1 (ou superior) deve mapear para cobertura completa (antes que o runtime execute uma operação **AND** com cobertura primitiva real). Como alfa vai de 0 a 1, a cobertura resultante geralmente deve aumentar de forma monotônica. No entanto, o hardware pode executar o dithering de área para fornecer uma quantificação melhor dos valores alfa, com o custo da resolução espacial e do ruído. Um valor alfa de NaN (Não um Número) resulta em uma máscara sem cobertura (zero).

A alfa para cobertura também é usada tradicionalmente para transparência da porta da tela ou para definir aslhouettes detalhadas para os sprites opacos.

### <a name="blending-pixel-shader-outputs"></a>Mesclando saídas de sombreador de pixel

Esse recurso permite que a fusão de saída use as duas saídas do sombreador de pixel simultaneamente como fontes de entrada para uma operação de mesclagem com o destino de renderização único no slot 0.

Este exemplo recebe dois resultados e os combina em uma única passagem, combinando um no destino com uma multiplicação e o outro com um adicionar:


```
SrcBlend = D3D11_BLEND_ONE;
DestBlend = D3D11_BLEND_SRC1_COLOR;
```



Este exemplo configura a primeira saída do sombreador de pixel como a cor de origem e a segunda saída como um fator de combinação de componentes por cor.


```
SrcBlend = D3D11_BLEND_SRC1_COLOR;
DestBlend = D3D11_BLEND_INV_SRC1_COLOR;
```



Este exemplo ilustra como os fatores de combinação devem corresponder aos swizzles do sombreador:


```
SrcFactor = D3D11_BLEND_SRC1_ALPHA;
DestFactor = D3D11_BLEND_SRC_COLOR;
OutputWriteMask[0] = .ra; // pseudocode for setting the mask at
                          // RenderTarget slot 0 to .ra
```



Juntos, os fatores blend e o código do sombreador implicam que o sombreador de pixel é necessário para a saída de pelo menos o0.r e o1.a. Componentes de saída extras podem ser produzidos pelo sombreador, mas seriam ignorados, menos componentes produziriam resultados indefinido.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Estágio de fusão de saída](d3d10-graphics-programming-guide-output-merger-stage.md)
</dt> <dt>

[Estágios de pipeline (Direct3D 10)](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-pipeline-stages)
</dt> </dl>

 

 