---
title: Estágio de rasterizador
description: O estágio de rasterização converte as informações de vetor (compostas de formas ou primitivas) em uma imagem de rasterizador (composta de pixels) para fins de exibição de gráficos 3D em tempo real.
ms.assetid: efd3f819-7c63-4e1a-9923-8e7198354ec6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e746c5ace3512f36f9b9ad34d34a3ea578e1de36
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/04/2020
ms.locfileid: "103917811"
---
# <a name="rasterizer-stage"></a>Estágio de rasterizador

O estágio de rasterização converte as informações de vetor (compostas de formas ou primitivas) em uma imagem de rasterizador (composta de pixels) para fins de exibição de gráficos 3D em tempo real.

Durante a rasterização, cada primitiva é convertida em pixels, enquanto interpola valores por vértice entre cada primitiva. A rasterização inclui o recorte de vértices para o tronco de exibição, execução de uma divisão por z para fornecer perspectiva, mapeamento de primitivas para um visor 2D e determinação de como invocar o sombreador de pixel. Embora o uso de um sombreador de pixel seja opcional, o estágio do rasterizador sempre realiza recorte, uma divisão de perspectiva para transformar os pontos em espaço homogêneo e mapeia os vértices para o visor.

Os vértices (x, y, z, w), que entram no estágio do rasterizador, são considerados no espaço de clipe homogêneo. Nesse espaço de coordenadas, o eixo X aponta para a direita, Y aponta para cima, Z aponta para longe da câmera.

Você pode desabilitar a rasterização informando ao pipeline que não há um sombreador de pixel (defina o estágio do sombreador de pixel como **nulo** com [**ID3D11DeviceContext::P ssetshader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-pssetshader)) e desabilitando o teste de profundidade e de estêncil (defina **DepthEnable** e **StencilEnable** como **false** no [**estêncil de \_ profundidade D3D11 \_ \_ desc**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_depth_stencil_desc)). Enquanto estão desabilitados, os contadores do pipeline relacionados à rasterização não serão atualizados. Também há uma descrição completa das regras de [rasterização](d3d10-graphics-programming-guide-rasterizer-stage-rules.md).

Em hardware que implementa otimizações hierárquicas de buffer Z, você pode habilitar o pré-carregamento do buffer z definindo o estágio do sombreador de pixel como **nulo** ao habilitar o teste de profundidade e de estêncil.


## <a name="in-this-section"></a>Nesta seção



| Tópico                                                                                                                         | Descrição                                                                                                                                                                                                                                                                                                              |
|-------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Introdução com o estágio rasterizador](d3d10-graphics-programming-guide-rasterizer-stage-getting-started.md)<br/> | Esta seção descreve como definir o visor, o retângulo de tesoura, o estado do rasterizador e a várias amostras.<br/>                                                                                                                                                                                                |
| [Regras de rasterização](d3d10-graphics-programming-guide-rasterizer-stage-rules.md)<br/>                                 | As regras de rasterização definem como os dados de vetor são mapeados nos dados de rasterização. Os dados de rasterização são ajustados para locais de inteiro que são, em seguida, removidos e recortados (para desenhar o número mínimo de pixels) e atributos de por pixel são interpolados (de atributos de vértice) antes de serem passados para um sombreador de pixel.<br/> |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Pipeline de gráficos](overviews-direct3d-11-graphics-pipeline.md)
</dt> <dt>

[Estágios de pipeline (Direct3D 10)](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-pipeline-stages)
</dt> </dl>

 

