---
title: Subalocação em buffers
description: Os buffers têm todos os recursos necessários no D3D12 para que os aplicativos transfiram uma grande variedade de dados transitórios da CPU para a GPU. Esta seção aborda quatro cenários comuns para o uso e o gerenciamento de recursos e buffers.
ms.assetid: 359E377A-8E16-4BB5-9055-09617335AB57
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d64944cb11507b8dc437d075938fad419f333433
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "74104680"
---
# <a name="suballocation-within-buffers"></a>Subalocação em buffers

Os buffers têm todos os recursos necessários no D3D12 para que os aplicativos transfiram uma grande variedade de dados transitórios da CPU para a GPU. Esta seção aborda quatro cenários comuns para o uso e o gerenciamento de recursos e buffers.

Semelhante ao D3D11, os aplicativos no D3D12 ainda precisam declarar o uso da memória ao alocar buffers em D3D12 em comparação com os recursos dinâmicos/de preparo no D3D11, mas, em D3D12, os desenvolvedores têm mais flexibilidade e controle mais rígido sobre o uso de memória. Os buffers, por meio da subalocação, têm todos os recursos necessários para o gerenciamento de memória de nível baixo.

## <a name="in-this-section"></a>Nesta seção



| Tópico                                                                                        | Descrição                                                                                                                                                                                                                                                                                                                                                                                                             |
|----------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Carregando diferentes tipos de recursos](uploading-resources.md)<br/>                 | Mostra como usar um buffer para carregar dados de buffer constante e dados de buffer de vértice para a GPU e como subalocar e posicionar corretamente os dados nos buffers. O uso de um único buffer aumenta a flexibilidade do uso de memória e fornece aos aplicativos um controle mais rígido do uso de memória. Também mostra as diferenças entre os modelos D3D11 e D3D12 para carregar diferentes tipos de recursos.<br/> |
| [Carregando dados de textura por meio de buffers](upload-and-readback-of-texture-data.md)<br/> | Carregar dados de textura 2D ou 3D é semelhante a carregar dados 1D, exceto que os aplicativos precisam prestar mais atenção ao alinhamento de dados relacionado à densidade da linha. Os buffers podem ser usados de forma ortogonal e simultânea de várias partes do pipeline de gráficos e são muito flexíveis. <br/>                                                                                                                       |
| [Ler dados por meio de um buffer](readback-data-using-heaps.md)<br/>                    | Ler dados de volta da GPU, como capturar uma captura de tela, envolve o uso do heap readback. <br/>                                                                                                                                                                                                                                                                                                     |
| [Gerenciamento de recursos baseado em isolamento](fence-based-resource-management.md)<br/>            | Mostra como gerenciar o tempo de vida de dados de recursos rastreando o progresso da GPU por meio de limites. A memória pode ser efetivamente reutilizada com limites que gerenciam cuidadosamente a disponibilidade de espaço livre na memória, como em uma implementação de buffer de anéis para um heap de carregamento. <br/>                                                                                                                                                     |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Gerenciamento de memória](memory-management.md)
</dt> </dl>

 

 





