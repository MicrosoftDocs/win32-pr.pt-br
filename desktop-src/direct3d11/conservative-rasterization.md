---
title: Rasterização conservadora do Direct3D 11.3
description: A rasterização conservadora adiciona alguma certeza à renderização de pixel, o que é útil em particular para algoritmos de detecção de colisão.
ms.assetid: 83F223C0-9282-4149-86CF-471B88829F76
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd33b7c7d237fc30adb349f1c1b24ce16c2740ce93fc97445a6e3f69d0949aeb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119408566"
---
# <a name="direct3d-113-conservative-rasterization"></a>Rasterização conservadora do Direct3D 11.3

A rasterização conservadora adiciona alguma certeza à renderização de pixel, o que é útil em particular para algoritmos de detecção de colisão.

-   [Visão geral](#overview)
-   [Interações com o pipeline](#interactions-with-the-pipeline)
-   [Detalhes de implementação](#implementation-details)
-   [Resumo da API](#api-summary)
-   [Tópicos relacionados](#related-topics)

## <a name="overview"></a>Visão geral

A rasterização conservadora significa que todos os pixels que são pelo menos parcialmente cobertos por um primitivo renderizado são rasterizados, o que significa que o sombreador de pixel é invocado. O comportamento normal é a amostragem, que não será usada se a rasterização conservadora estiver habilitada.

A rasterização conservadora é útil em várias situações, incluindo para ter certeza na detecção de colisão, redução de oclusão e detecção de visibilidade.

Por exemplo, a figura a seguir mostra um triângulo verde renderizado usando a rasterização conservadora. A área marrom é conhecida como uma "região de incerteza", uma região em que erros de arredondamento e outros problemas adicionam certa incerteza às dimensões exatas do triângulo. Os triângulos vermelhos em cada vértice mostram como a região de incerteza é calculada. Os quadrados cinza grandes mostram os pixels que serão renderizados. Os quadrados de cor de rosa mostram pixels renderizados usando a "regra superior esquerda", que entra em jogo à medida que a borda do triângulo cruza a borda dos pixels. Pode haver falsos positivos (conjunto de pixels que não deveria ter sido) que o sistema normalmente, mas nem sempre será eliminado.

![mostra a regra superior esquerda](images/conservative-rasterization-0.png)

## <a name="interactions-with-the-pipeline"></a>Interações com o pipeline

Para obter muitos detalhes sobre como a rasterização conservadora interage com o pipeline de gráficos, consulte [D3D12 Rasterização conservadora](/windows/desktop/direct3d12/conservative-rasterization).

## <a name="implementation-details"></a>Detalhes de implementação

Às vezes, o tipo de rasterização com suporte no Direct3D 12 é conhecido como "rasterização conservadora supervalorada". Também há o conceito de "rasterização descaradamente conservadora", o que significa que apenas pixels totalmente cobertos por um primitivo renderizado são rasterizados. As informações de rasterização falsas e conservadoras estão disponíveis por meio do sombreador de pixels por meio do uso de dados de cobertura de entrada e apenas a rasterização conservadora excessiva está disponível como um modo de rasterização.

Se qualquer parte de um primitivo sobrepor um pixel, esse pixel será considerado coberto e, em seguida, será rasterizado. Quando uma borda ou canto de um primitivo se enquadra na borda ou canto de um pixel, a aplicação da "regra superior esquerda" é específica da implementação. No entanto, para implementações que dão suporte a triângulos degenerado, um triângulo degenere ao longo de uma borda ou canto deve abranger pelo menos um pixel.

Implementações de rasterização conservadoras podem variar em diferentes hardwares e produzir falsos positivos, o que significa que eles podem decidir incorretamente que os pixels são cobertos. Isso pode ocorrer devido a detalhes específicos da implementação, como erros primitivos de crescimento ou ajuste inerentes às coordenadas de vértice de ponto fixo usadas na rasterização. O motivo pelo qual os falsos positivos (em relação às coordenadas de vértice de ponto fixo) são válidos é porque uma quantidade de falsos positivos são necessários para permitir que uma implementação faça a avaliação de cobertura em vértices pós-fixados (ou seja, coordenadas de vértice que foram convertidas de ponto flutuante para o ponto fixo 16,8 usado no rasterizador), mas respeitam a cobertura produzida pelas coordenadas de vértice de ponto flutuante originais.

Implementações de rasterização conservadoras não produzem falsos negativos em relação às coordenadas de vértice de ponto flutuante para primitivos pós-snap não degenerões: se qualquer parte de um primitivo sobrepor qualquer parte de um pixel, esse pixel será rasterizado.

Triângulos que são degenerados (índices duplicados em um buffer de índice ou collinear em 3D) ou se tornam degenerados após a conversão de ponto fixo (vértices collinear no rasterizador) podem ou não ser eliminados; ambos são comportamentos válidos. Triângulos degeneração devem ser considerados voltados para trás, portanto, se um comportamento específico for exigido por um aplicativo, ele poderá usar a replicação facial ou o teste para frente. Os triângulos degeneração usam os valores atribuídos ao vértice 0 para todos os valores interpolados.

Há três camadas de suporte de hardware, além da possibilidade de o hardware não dar suporte a esse recurso.

-   A Camada 1 dá suporte a regiões de incerteza de 1/2 pixels e não a nenhum desaparador pós-snap. Isso é bom para renderização lado a lado, um atlas de textura, geração de mapa de luz e mapas de sombra de sub pixel.
-   A Camada 2 adicionageneros pós-snap e 1/256 regiões de incerteza. Ele também adiciona suporte para aceleração de algoritmo baseada em CPU (como voxelization).
-   A Camada 3 adiciona regiões de incerteza de 1/512, cobertura de entrada interna e dá suporte à redução de oclusão. A cobertura de entrada adiciona o novo `SV_InnerCoverage` valor ao HLSL (High Level Shading Language). Este é um inteiro escalar de 32 bits que pode ser especificado na entrada para um sombreador de pixel e representa as informações de rasterização menosprezadas conservadoras (ou seja, se um pixel é garantido para ser totalmente coberto).

## <a name="api-summary"></a>Resumo da API

Os seguintes métodos, estruturas, enums e classes auxiliares referenciam a rasterização conservadora:

-   [**D3D11 \_ RASTERIZER \_ DESC2:**](/windows/desktop/api/D3D11_3/ns-d3d11_3-cd3d11_rasterizer_desc2) estrutura que mantém a descrição do rasterizador, notando a classe auxiliar CD3D12 RASTERIZER DESC2 para criar descrições do \_ \_ rasterizador.
-   [**D3D11 \_ MODO \_ DE RASTERIZAÇÃO \_ CONSERVADORA:**](/windows/desktop/api/D3D11_3/ne-d3d11_3-d3d11_conservative_rasterization_mode) valores de enum para o modo (on ou off).
-   [**D3D11 \_ FEATURE \_ DATA \_ D3D11 \_ OPTIONS2:**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_feature_data_d3d11_options2) estrutura que mantém a camada de suporte.
-   [**D3D11 \_ TIPO \_ DE RASTERIZAÇÃO \_ CONSERVADORA:**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_conservative_rasterization_tier) valores de enum para cada camada de suporte pelo hardware.
-   [**ID3D11Device::CheckFeatureSupport:**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-checkfeaturesupport) método para acessar os recursos com suporte.

## <a name="related-topics"></a>Tópicos relacionados
* [Recursos do Direct3D 11.3](direct3d-11-3-features.md)