---
title: Acesso ao pipeline para recursos lado a lado
description: Os recursos do lado do xadrez podem ser usados em modos de exibição de recurso de sombreador (SRV), exibições de destino de renderização (RTV), exibições de estêncil de profundidade (DSV) e exibições de acesso não ordenado (UAV), bem como alguns pontos de ligação em que as exibições não são usadas, como associações de buffer de vértice.
ms.assetid: D0BC0B6C-2325-4EAF-9E80-E748F58045B1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef4a183fcaee90d84985a09c83826a4ad0b6d646
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103641588"
---
# <a name="pipeline-access-to-tiled-resources"></a>Acesso ao pipeline para recursos lado a lado

Os recursos do lado do xadrez podem ser usados em modos de exibição de recurso de sombreador (SRV), exibições de destino de renderização (RTV), exibições de estêncil de profundidade (DSV) e exibições de acesso não ordenado (UAV), bem como alguns pontos de ligação em que as exibições não são usadas, como associações de buffer de vértice. Para obter a lista de associações com suporte, consulte [parâmetros de criação de recursos de lado e xadrez](tiled-resource-creation-parameters.md). \*As operações de cópia também funcionam em recursos de lado.

Se várias coordenadas de bloco em um ou mais modos de exibição estiverem vinculadas ao mesmo local de memória, leituras e gravações de diferentes caminhos para a mesma memória ocorrerão em uma ordem de acesso de memória não determinística e não repetida.

Se todos os blocos por trás de um volume de acesso de memória de um sombreador estiverem mapeados para blocos exclusivos, o comportamento será idêntico em todas as implementações para superfícies com o mesmo conteúdo da memória de maneira sem blocos.

Esta seção fornece mais informações sobre o acesso do pipeline a recursos de lado.

## <a name="in-this-section"></a>Nesta seção



| Tópico                                                                                                              | Descrição                                                                                                                                                               |
|--------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Comportamento de SRV com blocos não mapeados](srv-behavior-with-non-mapped-tiles.md)<br/>                            | O comportamento de leituras de modo de exibição (SRV) de recurso de sombreador que envolve blocos não mapeados depende do nível de suporte de hardware. <br/>                                          |
| [Comportamento de UAV com blocos não mapeados](uav-behavior-with-non-mapped-tiles.md)<br/>                            | O comportamento das leituras e gravações de modo de exibição de acesso não ordenado (UAV) depende do nível de suporte do hardware. <br/>                                                            |
| [Comportamento de rasterizador com blocos não mapeados](rasterizer-behavior-with-non-mapped-tiles.md)<br/>              | Esta seção descreve o comportamento de rasterizador com blocos não mapeados.<br/>                                                                                              |
| [Limitações de acesso de bloco com mapeamentos duplicados](tile-access-limitations-with-duplicate-mappings-.md)<br/> | Esta seção descreve as limitações de acesso de bloco com mapeamentos duplicados.<br/>                                                                                        |
| [Recursos de amostragem de textura de recursos ao lado](tiled-resources-texture-sampling-features.md)<br/>              | Esta seção descreve os recursos de amostragem de textura de recursos com ladrilhos.<br/>                                                                                              |
| [Exposição dos recursos do lado do HLSL](hlsl-tiled-resources-exposure.md)<br/>                                      | A nova sintaxe de HLSL (linguagem de sombreamento de alto nível) da Microsoft é necessária para dar suporte a recursos de lado do [sombreado no modelo de Shader](/windows/desktop/direct3dhlsl/d3d11-graphics-reference-sm5) <br/> |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Recursos em ladrilho](tiled-resources.md)
</dt> </dl>

 

