---
title: Gerenciando o estado do pipeline de gráficos no Direct3D 12
description: Este tópico descreve como o estado do pipeline de gráficos é definido no Direct3D 12.
ms.assetid: AAF97BD2-D532-469D-9242-CC94C06727C3
keywords:
- Estado do pipeline
- objeto de estado do pipeline
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7564b5863d3efebdf8a335e2c46945aeebea93e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104548329"
---
# <a name="managing-graphics-pipeline-state-in-direct3d-12"></a>Gerenciando o estado do pipeline de gráficos no Direct3D 12

Este tópico descreve como o estado do pipeline de gráficos é definido no Direct3D 12.

## <a name="pipeline-state-overview"></a>Visão geral do estado do pipeline

Quando a geometria é enviada para a GPU (unidade de processamento gráfico) a ser desenhada, há uma ampla gama de configurações de hardware que determinam como os dados de entrada são interpretados e renderizados. Coletivamente, essas configurações são chamadas de estado de pipeline de gráficos e incluem configurações comuns, como estado do rasterizador, estado de mistura e estado de estêncil de profundidade, bem como o tipo de topologia primitivo da geometria enviada e os sombreadores que serão usados para renderização. No Microsoft Direct3D 12, a maioria dos Estados de pipeline de gráficos é definida usando o PSO (objetos de estado de pipeline). Um aplicativo pode criar um número ilimitado desses objetos, representados pela interface [**ID3D12PipelineState**](/windows/win32/api/d3d12/nn-d3d12-id3d12pipelinestate) , normalmente no momento da inicialização. Em seguida, no momento da renderização, as listas de comandos podem alternar rapidamente várias configurações do estado do pipeline chamando [**ID3D12GraphicsCommandList:: Setpipelinestate**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setpipelinestate) em um pacote ou lista de comandos diretos para definir o PSO ativo.

No Direct3D 11, o estado do pipeline de gráficos foi agrupado em objetos de estado grandes e de alta granularidade, como [**ID3D11BlendState**](/windows/win32/api/d3d11/nn-d3d11-id3d11blendstate) , que poderiam ser criados e definidos no momento do processamento no contexto imediato com métodos como [**ID3D11DeviceContext:: OMSetBlendState**](/windows/win32/api/d3d10/nf-d3d10-id3d10device-omsetblendstate). A ideia por trás disso era que a GPU poderia obter eficiências definindo configurações relacionadas, como as configurações de estado de mesclagem, tudo de uma só vez. No entanto, com o hardware de gráficos atual, há dependências entre as diferentes unidades de hardware. Por exemplo, o estado de mesclagem de hardware pode ter dependências no estado de varredura, bem como no estado de mesclagem. O PSOs no Direct3D 12 foi projetado para permitir que a GPU processe previamente todas as configurações dependentes em cada Estado de pipeline, normalmente durante a inicialização, para fazer a alternância entre os Estados em tempo de processamento o mais eficiente possível.

Observe que, embora a maioria das configurações de estado do pipeline seja definida usando PSOs, há algumas configurações de estado que são definidas separadamente usando as APIs fornecidas pelo [**ID3D12GraphicsCommandList**](/windows/win32/api/d3d12/nn-d3d12-id3d12graphicscommandlist). Essas configurações e as APIs associadas são discutidas em detalhes abaixo. Além disso, há diferenças na forma como o estado do pipeline de gráficos é herdado e persistido de listas de comandos e pacotes diretos. Este tópico fornece detalhes sobre ambos abaixo.

## <a name="graphics-pipeline-states-set-with-pipeline-state-objects"></a>Conjuntos de Estados de pipeline de gráficos definidos com objetos de estado do pipeline

A maneira mais fácil de ver todos os Estados de pipeline diferentes que podem ser definidos usando um objeto de estado de pipeline é examinar o tópico de referência para [**o \_ estado de pipeline de gráficos D3D12 \_ \_ \_ desc**](/windows/win32/api/d3d12/ns-d3d12-d3d12_graphics_pipeline_state_desc) que você passa para [**ID3D12Device:: CreateGraphicsPipelineState**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-creategraphicspipelinestate) quando você inicializa o objeto. Um resumo rápido dos Estados que podem ser definidos inclui:

-   O código de bytes para todos os sombreadores, incluindo vértices, pixel, domínio, envoltória e sombreadores de geometria.
-   O formato de vértice de entrada.
-   O tipo de topologia primitiva. Observe que o tipo de topologia primitiva do assembler de entrada (ponto, linha, triângulo, patch) é definido dentro do PSO usando a enumeração de [**\_ \_ \_ tipo de topologia primitiva D3D12**](/windows/win32/api/d3d12/ne-d3d12-d3d12_primitive_topology_type) . A adjacência e a ordenação primitivas (lista de linhas, faixa de linhas, faixa de linhas com dados de adjacência, etc.) são definidas de dentro de uma lista de comandos usando o método [**ID3D12GraphicsCommandList:: IASetPrimitiveTopology**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-iasetprimitivetopology) .
-   O estado de mesclagem, estado do rasterizador, estado do estêncil de profundidade.
-   O estêncil de profundidade e os formatos de destino de renderização, bem como a contagem de destino de renderização.
-   Parâmetros de várias amostras.
-   Um buffer de saída de streaming.
-   A assinatura raiz. Para obter mais informações, consulte [assinaturas raiz](root-signatures.md).

## <a name="graphics-pipeline-states-set-outside-of-the-pipeline-state-object"></a>Os Estados de pipeline de gráficos são definidos fora do objeto de estado do pipeline

A maioria dos Estados de pipeline de gráficos é definida usando PSOs. No entanto, há um conjunto de parâmetros de estado de pipeline que são definidos pela chamada de métodos da interface [**ID3D12GraphicsCommandList**](/windows/win32/api/d3d12/nn-d3d12-id3d12graphicscommandlist) de dentro de uma lista de comandos. A tabela a seguir mostra os Estados que são definidos dessa forma e os métodos correspondentes.

|Estado|Método|
|-|-|
|Associações de recursos|[**IASetIndexBuffer**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-iasetindexbuffer)<br/>[**IASetVertexBuffers**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-iasetvertexbuffers)<br/>[**SOSetTargets**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-sosettargets)<br/>[**OMSetRenderTargets**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-omsetrendertargets)<br/>[**SetDescriptorHeaps**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setdescriptorheaps)<br/>Todos os métodos **SetGraphicsRoot..** .<br/>Todos os métodos **SetComputeRoot..** .<br/>
|Visores|<a href="/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-rssetviewports">**RSSetViewports**</a>|
|Retângulos de tesoura|<a href="/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-rssetscissorrects">**RSSetScissorRects**</a>|
|Fator de mistura|<a href="/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-omsetblendfactor">**OMSetBlendFactor**</a>|
|O valor de referência do estêncil de profundidade|<a href="/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-omsetstencilref">**OMSetStencilRef**</a>|
|A ordem de topologia primitiva de Assembler de entrada e o tipo de adjacência|<a href="/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-iasetprimitivetopology">**IASetPrimitiveTopology**</a>|

## <a name="graphics-pipeline-state-inheritance"></a>Herança de estado de pipeline de gráficos

Como as listas de comandos diretas geralmente são destinadas a um uso por vez e os grupos devem ser usados várias vezes simultaneamente, há regras diferentes sobre como elas herdam o estado do pipeline de gráficos definido por listas de comandos ou pacotes anteriores.

Para os Estados de pipeline de gráficos que são definidos usando PSOs, nenhum desses Estados é herdado por listas de comandos ou grupos diretos. O estado inicial do pipeline de gráficos para as listas de comandos diretos e os pacotes é definido no momento da criação com o parâmetro [**ID3D12PipelineState**](/windows/win32/api/d3d12/nn-d3d12-id3d12pipelinestate) como [**ID3D12Device:: createcommandlist**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createcommandlist). Se nenhum PSO for especificado na chamada, um estado inicial padrão será usado. Você pode alterar o PSO atual em uma lista de comandos chamando [**ID3D12GraphicsCommandList:: Setpipelinestate**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-setpipelinestate).

As listas de comandos diretos também não herdam o estado definido com métodos de lista de comandos como [**RSSetViewports**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-rssetviewports). Para obter detalhes sobre os valores iniciais padrão para os Estados não PSO, consulte [**ID3D12GraphicsCommandList:: clearstate**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-clearstate).

Os grupos herdam todos os Estados de pipeline de gráficos que não estão definidos com PSOs, exceto para o tipo de topologia primitiva. A topologia primitiva sempre é definida como [**\_ tipo de \_ topologia primitivo D3D12 \_ \_ indefinido**](/windows/win32/api/d3d12/ne-d3d12-d3d12_primitive_topology_type) quando um pacote começa a ser executado. Qualquer estado definido em um pacote (o próprio PSO, estado não baseado em PSO e associações de recursos) afeta o estado de sua lista de comandos diretos pai. Por exemplo, se um [**RSSetViewports**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-rssetviewports) for chamado de dentro de um pacote, os viewports especificados continuarão a ser definidos na lista de comandos diretos pai para chamadas subsequentes para a chamada [**ExecuteBundle**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-executebundle) que definem as visores.

As associações de recursos que são definidas em uma lista de comandos ou pacote persistem. Portanto, as associações de recursos modificadas em uma lista de comandos diretas ainda serão definidas na execução subsequente do pacote filho. E as associações de recursos modificadas de dentro de um pacote ainda serão definidas para chamadas subsequentes na lista de comandos diretas pai.

Para obter mais informações sobre associações, consulte a seção **semântica do pacote** de [usando uma assinatura raiz](using-a-root-signature.md).

## <a name="related-topics"></a>Tópicos relacionados

* [Envio de trabalho no Direct3D 12](command-queues-and-command-lists.md)