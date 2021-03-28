---
title: Recursos do Direct3D 11,3
description: As seções a seguir descrevem a funcionalidade que foi adicionada no Direct3D 11,3. Esses recursos também estão disponíveis no Direct3D 12.
ms.assetid: CA79A315-22C4-4141-8E66-89C0DCF29191
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc256b9b85dd807e2e6c923affdec496fe92e075
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/04/2020
ms.locfileid: "104368961"
---
# <a name="direct3d-113-features"></a>Recursos do Direct3D 11,3

As seções a seguir descrevem a funcionalidade que foi adicionada no Direct3D 11,3. Esses recursos também estão disponíveis no Direct3D 12.


## <a name="in-this-section"></a>Nesta seção



| Tópico                                                                                               | Descrição                                                                                                                                                                                                                                                                                                                                                                                  |
|-----------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Rasterização conservativa](conservative-rasterization.md)<br/>                             | A rasterização conservadora adiciona alguma certeza à renderização de pixels, que é útil em particular aos algoritmos de detecção de colisão.<br/>                                                                                                                                                                                                                                              |
| [Mapeamento de textura padrão](default-texture-mapping.md)<br/>                                   | O uso de mapeamento de textura padrão reduz a cópia e o uso de memória ao compartilhar dados de imagem entre a GPU e a CPU. No entanto, ele só deve ser usado em situações específicas. O layout swizzle padrão evita copiar ou swizzling dados em vários layouts.<br/>                                                                                                               |
| [Exibições de ordem do rasterizador](rasterizer-order-views.md)<br/>                                     | As exibições ordenadas do rasterizador (ROVs) permitem que o código do sombreador de pixel marque as associações UAV com uma declaração que altera os requisitos normais para a ordem dos resultados do pipeline de gráficos para o UAVs. Isso permite que algoritmos de OIT (transparência independente de ordem) funcionem, o que fornece resultados de renderização muito melhores quando vários objetos transparentes estão em linha entre si em uma exibição. <br/> |
| [Valor de referência de estêncil especificado pelo sombreador](shader-specified-stencil-reference-value.md)<br/> | A habilitação de sombreadores de pixel para produzir o valor de referência do estêncil, em vez de usar o especificado pela API, permite um controle muito refinado sobre as operações de estêncil.<br/>                                                                                                                                                                                                              |
| [Cargas de exibição de acesso não ordenado digitado](typed-unordered-access-view-loads.md)<br/>               | A carga digitada UAV (exibição de acesso não ordenada) é a capacidade de um sombreador de ler de um UAV com um formato DXGI específico \_ .<br/>                                                                                                                                                                                                                                                               |
| [Arquitetura de memória unificada](unified-memory-architecture.md)<br/>                           | Consultar se há suporte para a uma (arquitetura de memória unificada) pode ajudar a determinar como lidar com alguns recursos.<br/>                                                                                                                                                                                                                                                              |
| [Alocação dinâmica de volumes de recursos](volume-tiled-resources.md)<br/>                                     | Texturas de volume (3D) podem ser usadas como recursos ao lado, observando que a resolução do bloco é tridimensional.<br/>                                                                                                                                                                                                                                                                            |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[O que há de novo no Direct3D 11](dx-graphics-overviews-introduction.md)
</dt> </dl>

 

 





