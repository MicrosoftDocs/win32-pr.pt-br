---
title: Rasterização de Direct3D 11,3 conservador
description: A rasterização conservadora adiciona alguma certeza à renderização de pixels, que é útil em particular aos algoritmos de detecção de colisão.
ms.assetid: 83F223C0-9282-4149-86CF-471B88829F76
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 003cb7e31c1380943318b34f9308f6b5e72d6e51
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104162379"
---
# <a name="direct3d-113-conservative-rasterization"></a>Rasterização de Direct3D 11,3 conservador

A rasterização conservadora adiciona alguma certeza à renderização de pixels, que é útil em particular aos algoritmos de detecção de colisão.

-   [Visão geral](#overview)
-   [Interações com o pipeline](#interactions-with-the-pipeline)
-   [Detalhes da implementação](#implementation-details)
-   [Resumo da API](#api-summary)
-   [Tópicos relacionados](#related-topics)

## <a name="overview"></a>Visão geral

A rasterização conservadora significa que todos os pixels que estão pelo menos parcialmente cobertos por um primitivo renderizado são rasterizados, o que significa que o sombreador de pixel é invocado. O comportamento normal é a amostragem, que não é usada se a rasterização conservadora estiver habilitada.

A rasterização conservadora é útil em várias situações, incluindo a certeza da detecção de colisão, da remoção de oclusão e da detecção de visibilidade.

Por exemplo, a figura a seguir mostra um triângulo verde renderizado usando a rasterização conservadora. A área Brown é conhecida como "região de incerteza" – uma região em que o arredondamento de erros e outros problemas adicionam algumas incertezas às dimensões exatas do triângulo. Os triângulos vermelhos em cada vértice mostram como a região incerteza é calculada. Os quadrados cinzas grandes mostram os pixels que serão renderizados. Os quadrados rosa mostram pixels renderizados usando a "regra de cima para a esquerda", que entra em cena, pois a borda do triângulo cruza a borda dos pixels. Pode haver falsos positivos (conjunto de pixels que não deveriam ter sido) que o sistema normalmente, mas nem sempre irá fazer a seleção.

![mostra a regra superior esquerda](images/conservative-rasterization-0.png)

## <a name="interactions-with-the-pipeline"></a>Interações com o pipeline

Para muitos detalhes sobre como a rasterização conservadora interage com o pipeline de gráficos, consulte [rasterização D3D12 conservadora](/windows/desktop/direct3d12/conservative-rasterization).

## <a name="implementation-details"></a>Detalhes de implementação

O tipo de rasterização com suporte no Direct3D 12 é às vezes chamado de "rasterização conservadora estimada". Também há o conceito de "rasterização conservadora subestimada", o que significa que apenas os pixels totalmente cobertos por um primitivo renderizado são rasterizados. As informações de rasterização conservadora subestimadas estão disponíveis por meio do sombreador de pixel através do uso de dados de cobertura de entrada e apenas a rasterização conservadora Sobreestimada está disponível como um modo de rasterização.

Se qualquer parte de um primitivo sobrepuser um pixel, esse pixel será considerado coberto e, em seguida, será rasterizado. Quando uma borda ou canto de um primitivo cai ao longo da borda ou do canto de um pixel, o aplicativo da "regra de cima para a esquerda" é específico da implementação. No entanto, para implementações que dão suporte a triângulos de degeneração, um triângulo degenerado ao longo de uma borda ou canto deve abranger pelo menos um pixel.

Implementações de rasterização conservadoras podem variar em hardwares diferentes e produzir falsos positivos, o que significa que eles podem decidir incorretamente que os pixels são cobertos. Isso pode ocorrer devido a detalhes específicos da implementação, como erros primitivos de crescimento ou encaixe inerentes às coordenadas de vértice de ponto fixo usadas na rasterização. O motivo pelo qual falsos positivos (em relação às coordenadas de vértice de ponto fixo) é válido porque alguns falsos positivos são necessários para permitir que uma implementação faça a avaliação de cobertura em vértices de postagem (ou seja, coordenadas de vértice que foram convertidas do ponto flutuante para o ponto fixo 16,8 usado no rasterizador), mas obedeça a cobertura produzida pelas coordenadas originais do vértice do ponto flutuante

Implementações de rasterização conservadoras não produzem falsos negativos em relação às coordenadas de vértice de ponto flutuante para primitivos post-snap não degenerados: se qualquer parte de um primitivo sobrepuser qualquer parte de um pixel, esse pixel será rasterizado.

Triângulos que são degenerados (índices duplicados em um buffer de índice ou colineares em 3D) ou tornam-se degenerados após a conversão de ponto fixo (vértices de colineares no rasterizador), pode ou não ser possível fazer a remoção; Ambos são comportamentos válidos. Os triângulos de degeneração devem ser considerados voltados, portanto, se um comportamento específico for exigido por um aplicativo, ele poderá usar a remoção ou teste de face para frente. Os triângulos de degeneração usam os valores atribuídos ao vértice 0 para todos os valores interpolados.

Há três camadas de suporte a hardware, além da possibilidade de que o hardware não ofereça suporte a esse recurso.

-   A camada 1 dá suporte a regiões de incerteza de 1/2 pixels e nenhum degenerado após o snap. Isso é bom para a renderização de ladrilho, um Atlas de textura, geração de mapa claro e mapas de sombra de subpixel.
-   A camada 2 adiciona degenerações de pós-snap e 1/256 regiões de incerteza. Ele também adiciona suporte para aceleração de algoritmos baseada em CPU (como voxelization).
-   A camada 3 adiciona regiões de incertezas de 1/512, cobertura de entrada interna e dá suporte à remoção de oclusão. A cobertura de entrada adiciona o novo valor `SV_InnerCoverage` à HLSL (linguagem de sombreamento de alto nível). Este é um inteiro escalar de 32 bits que pode ser especificado na entrada para um sombreador de pixel e representa as informações de rasterização conservadora subestimadas (ou seja, se um pixel é garantido para ser totalmente coberto).

## <a name="api-summary"></a>Resumo da API

Os seguintes métodos, estruturas, enumerações e classes auxiliares referenciam a rasterização conservadora:

-   [**D3D11 \_ RASTERIZAdor \_ DESC2**](/windows/desktop/api/D3D11_3/ns-d3d11_3-cd3d11_rasterizer_desc2) : estrutura que mantém a descrição do rasterizador, observando a \_ classe auxiliar do CD3D12 rasterizador \_ DESC2 para criar descrições do rasterizador.
-   [**D3D11 \_ \_ \_ Modo de rasterização conservador**](/windows/desktop/api/D3D11_3/ne-d3d11_3-d3d11_conservative_rasterization_mode) : valores de enumeração para o modo (ativado ou desativado).
-   [**D3D11 \_ Dados de recurso \_ \_ D3D11 \_ OPTIONS2**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options2) : estrutura que mantém a camada de suporte.
-   [**D3D11 \_ \_ \_ Camada de rasterização conservadora**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_conservative_rasterization_tier) : valores de enumeração para cada camada de suporte pelo hardware.
-   [**ID3D11Device:: CheckFeatureSupport**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport) : método para acessar os recursos com suporte.

## <a name="related-topics"></a>Tópicos relacionados
* [Recursos do Direct3D 11,3](direct3d-11-3-features.md)