---
title: Renderização (gráficos do Direct3D 12)
description: Esta seção contém informações sobre a renderização de recursos novos no Direct3D 12 (e no Direct3D 11,3).
ms.assetid: 5BF1440E-E4D8-43C8-BF0E-F02FEFE79C93
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c1abb8e8d1d645149652e5c1cd429fb4e4b2e0b1e079eda13956f5ab8279b3c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119123463"
---
# <a name="rendering-direct3d-12-graphics"></a>Renderização (gráficos do Direct3D 12)

Esta seção contém informações sobre a renderização de recursos novos no Direct3D 12 (e no Direct3D 11,3).

## <a name="in-this-section"></a>Nesta seção



| Tópico                                                                                               | Descrição                                                                                                                                                                                                                                                                                                                                                                                  |
|-----------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Rasterização conservativa](conservative-rasterization.md)<br/>                             | A rasterização conservadora adiciona alguma certeza à renderização de pixels, que é útil em particular aos algoritmos de detecção de colisão.<br/>                                                                                                                                                                                                                                              |
| [Desenho indireto](indirect-drawing.md)<br/>                                                 | O desenho indireto permite que alguns atravessamentos de cena e de seleção sejam movidos da CPU para a GPU, o que pode melhorar o desempenho. O buffer de comando pode ser gerado pela CPU ou GPU.<br/>                                                                                                                                                                                              |
| [Modos de exibição ordenados do rasterizador](rasterizer-order-views.md)<br/>                                   | As exibições ordenadas do rasterizador (ROVs) permitem que o código do sombreador de pixel marque as associações UAV com uma declaração que altera os requisitos normais para a ordem dos resultados do pipeline de gráficos para o UAVs. Isso permite que algoritmos de OIT (transparência independente de ordem) funcionem, o que fornece resultados de renderização muito melhores quando vários objetos transparentes estão em linha entre si em uma exibição. <br/> |
| [Valor de referência de estêncil especificado pelo sombreador](shader-specified-stencil-reference-value.md)<br/> | A habilitação de sombreadores de pixel para produzir o valor de referência do estêncil, em vez de usar o especificado pela API, permite um controle muito refinado sobre as operações de estêncil.<br/>                                                                                                                                                                                                              |
| [Cadeias de troca](swap-chains.md)<br/>                                                           | As cadeias de permuta controlam a rotação do buffer de fundo, formando a base da animação de gráficos.<br/>                                                                                                                                                                                                                                                                                            |



 

Os tópicos a seguir também são novos no Direct3D 12 e no Direct3D 11,3:

-   [Mapeamento de textura padrão](default-texture-mapping.md)
-   [Cargas de exibição de acesso não ordenado digitado](typed-unordered-access-view-loads.md)
-   [Alocação dinâmica de volumes de recursos](volume-tiled-resources.md)

## <a name="high-dynamic-range-and-wide-color-gamut"></a>Ampla gama de cores e intervalos dinâmicos

Consulte o suporte para intervalo dinâmico alto (maior diferença entre os brancos mais brilhantes e os pretos mais escuros) e a gama de cores largos (10 bits, em vez de 8 bits, por cor) descritos em [melhorias de DXGI 1,5](/windows/desktop/direct3ddxgi/dxgi-1-5-improvements).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Guia de programação do Direct3D 12](directx-12-programming-guide.md)
</dt> </dl>

 

