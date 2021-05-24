---
description: No Direct3D 10, o estado do dispositivo é agrupado em objetos de estado, o que reduz consideravelmente o custo das alterações de estado.
ms.assetid: b2839da9-60ed-4f6c-9cc7-eac53647cca7
title: Objetos de estado (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a51c05e3e220e510c462265941549f91e6368a9
ms.sourcegitcommit: ca37395fd832e798375e81142b97cffcffabf184
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/24/2021
ms.locfileid: "110335420"
---
# <a name="state-objects-direct3d-10"></a>Objetos de estado (Direct3D 10)

No Direct3D 10, o estado do dispositivo é agrupado em objetos de estado, o que reduz consideravelmente o custo das alterações de estado. Há vários objetos de estado, e cada um deles é projetado para inicializar um conjunto de estado para um estágio de pipeline específico. Você pode criar até 4096 de cada tipo de objeto de estado.

-   [Estado de layout de entrada](#input-layout-state)
-   [Estado do rasterizador](#rasterizer-state)
-   [Estado de estêncil de profundidade](#depth-stencil-state)
-   [Estado do Blend](#blend-state)
-   [Estado do sampler](#sampler-state)
-   [Considerações sobre desempenho](#performance-considerations)
-   [Tópicos relacionados](#related-topics)

## <a name="input-layout-state"></a>Estado de layout de entrada

Esse grupo de estado (consulte [**D3D10 \_ INPUT \_ ELEMENT \_ DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_input_element_desc)) determina como o estágio de [assembler](../direct3d11/d3d10-graphics-programming-guide-input-assembler-stage.md) de entrada lê dados dos buffers de entrada e os monta para uso pelo sombreador de vértice. Isso inclui o estado, como o número de elementos no buffer de entrada e a assinatura dos dados de entrada. O estágio do assembler de entrada é um novo estágio no pipeline cujo trabalho é transmitir primitivos da memória para o pipeline.

Para criar um objeto de estado de layout de entrada, [**consulte CreateInputLayout**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createinputlayout).

## <a name="rasterizer-state"></a>Estado do rasterizador

Esse grupo de estado (consulte [**D3D10 \_ RASTERIZER \_ DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_rasterizer_desc)) inicializa o [estágio do rasterizador](../direct3d11/d3d10-graphics-programming-guide-rasterizer-stage.md). Esse objeto inclui o estado como modos preenchimento ou eliminação, permitindo o recorte de um retângulo de corte e a configuração de parâmetros de várias amostras. Este estágio rasteriza os primitivos em pixels, realizando operações como recorte e mapeamento de primitivos no visor.

Para criar um objeto rasterizer-state, consulte [**CreateRasterizerState**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createrasterizerstate).

## <a name="depth-stencil-state"></a>Estado do estêncil de profundidade

Esse grupo de estado (consulte [**D3D10 \_ DEPTH \_ STENCIL \_ DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_depth_stencil_desc)) inicializa a parte de estêncil de profundidade do estágio de fusão [de saída.](../direct3d11/d3d10-graphics-programming-guide-output-merger-stage.md) Mais especificamente, esse objeto inicializa os testes de estêncil e profundidade.

Para criar um objeto depth-stencil-state, consulte [**CreateDepthStencilState**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createdepthstencilstate).

## <a name="blend-state"></a>Estado de mesclagem

Esse grupo de estado (consulte [**D3D10 \_ BLEND \_ DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_blend_desc)) inicializa a parte de mesclagem do estágio [de fusão de saída.](../direct3d11/d3d10-graphics-programming-guide-output-merger-stage.md)

Para criar um objeto blend-state, consulte [**CreateBlendState**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createblendstate).

## <a name="sampler-state"></a>Estado do sampler

Esse grupo de estado (consulte [**a \_ amostra \_ de d3d10 desc**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_sampler_desc)) Inicializa um objeto de amostra. Um objeto de amostra é usado pelos estágios de sombreador para filtrar texturas na memória.



Diferenças entre o Direct3D 9 e o Direct3D 10:

- No Direct3D 10, o objeto de amostra não está mais ligado a uma textura específica; ele apenas descreve como fazer a filtragem de acordo com qualquer recurso anexado.



 

Para criar um objeto de estado de amostra, consulte [**Createsamplestate**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createsamplerstate).

## <a name="performance-considerations"></a>Considerações sobre desempenho

Projetar a API para usar objetos de estado cria várias vantagens de desempenho. Isso inclui validação de estado no momento da criação de objeto, habilitação do cache de objetos de estado no hardware e redução considerável da quantidade de estado que é passada durante uma chamada de API de configuração de estado (passando um manipulador para o objeto de estado em vez do estado).

Para obter essas melhorias de desempenho, é necessário criar os objetos de estado quando seu aplicativo for inicializado, logo antes do seu loop de renderização. Os objetos de estado são imutáveis, ou seja, depois que são criados, não podem ser alterados. Em vez disso, você deve destruí-los ou recriá-los. Para lidar com essa restrição, você pode criar até 4096 de cada tipo de objetos de estado. Por exemplo, você pode criar vários objetos de amostra com várias combinações de estado de amostra. A alteração do estado de amostra é então realizada chamando a API Set apropriada que passa um identificador para o objeto (em oposição ao estado de amostra). Isso reduz significativamente a quantidade de sobrecarga durante cada quadro de renderização para alterar o estado, uma vez que o número de chamadas e a quantidade de dados são consideravelmente reduzidos.

Como alternativa, você pode optar por usar o sistema de efeito que gerenciará automaticamente a criação e destruição eficientes de objetos de estado para seu aplicativo.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Recursos de API (Direct3D 10)](d3d10-graphics-programming-guide-api-features.md)
</dt> </dl>

 

 
