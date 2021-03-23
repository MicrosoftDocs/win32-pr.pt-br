---
title: Guia de programação do Direct3D 12
description: O Direct3D 12 fornece uma API e uma plataforma que permite que os aplicativos tirem proveito dos recursos de computação e elementos gráficos de PCs equipados com uma ou mais GPUs compatíveis com o Direct3D 12.
ms.assetid: 16F78A6B-74C4-4ED1-809F-FE6DE157F368
ms.custom: 19H1
ms.localizationpriority: high
ms.topic: article
ms.date: 04/19/2019
ms.openlocfilehash: 94afd9125a2e73665e3783419651f34fd72285ca
ms.sourcegitcommit: bf6a52b91604d8a9432bf646097e3f31e44967d7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/06/2019
ms.locfileid: "104548300"
---
# <a name="direct3d-12-programming-guide"></a>Guia de programação do Direct3D 12

O Direct3D 12 fornece uma API e uma plataforma que permite que os aplicativos tirem proveito dos recursos de computação e elementos gráficos de PCs equipados com uma ou mais GPUs compatíveis com o Direct3D 12.

## <a name="in-this-section"></a>Nesta seção

| Tópico | Descrição |
|-|-|
| [O que é Direct3D 12?](what-is-directx-12-.md) | O DirectX 12 apresenta a próxima versão do Direct3D, a API gráfica 3D no coração do DirectX. Esta versão do Direct3D é mais rápida e mais eficiente do que qualquer versão anterior. O Direct3D 12 permite cenas mais avançadas, mais objetos, efeitos mais complexos e a utilização total do hardware de GPU moderno.  |
| [O que há de novo no Direct3D 12](new-releases.md) | Descreve a nova documentação mais significativa disponível com a versão mais recente do SDK. |
| [Entendendo o Direct3D 12](directx-12-getting-started.md) | Para escrever jogos e aplicativos 3D para Windows 10 e Windows 10 Mobile, você deve compreender os conceitos básicos da tecnologia do Direct3D 12 e como se preparar para usá-lo em seus jogos e aplicativos. |
| [Envio de trabalho no Direct3D 12](command-queues-and-command-lists.md) | Para melhorar a eficiência da CPU dos aplicativos do Direct3D, o Direct3D 12 não dá mais suporte a um contexto imediato associado a um dispositivo. Em vez disso, os aplicativos registram e enviam *listas de comandos*, que contêm chamadas de gerenciamento de recursos e de desenho. Essas listas de comandos podem ser enviadas de vários threads para uma ou mais filas de comando, que gerenciam a execução dos comandos. Essa alteração fundamental aumenta a eficiência de thread único, permitindo que os aplicativos implantem previamente o trabalho de renderização para reutilização posterior e aproveitem os sistemas de vários núcleos, distribuindo o trabalho de renderização em vários threads.  |
| [Associação de recursos no Direct3D 12](resource-binding.md) | Binding é o processo de vinculação de objetos de recursos aos sombreadores do pipeline de gráficos.  |
| [Gerenciamento de memória no Direct3D 12](memory-management.md) | A mudança para o D3D12 envolve a sincronização adequada e o gerenciamento da residência de memória. O gerenciamento de residência de memória significa que ainda mais sincronização deve ser feita. Esta seção aborda as estratégias de gerenciamento de memória e a subalocação dentro de heaps e buffers.  |
| [Sistemas com vários adaptadores](multi-engine.md) | Descreve o suporte no Direct3D 12 para sistemas que têm vários adaptadores instalados, abrangendo cenários em que seu aplicativo se destina explicitamente a vários adaptadores de GPU e cenários em que os drivers usam implicitamente vários adaptadores de GPU em nome do seu aplicativo. |
| [Sincronização de vários mecanismos](user-mode-heap-synchronization.md) | Este tópico discute a sincronização de acesso a vários mecanismos independentes encontrados na maioria das GPUs modernas. |
| [Renderização](rendering.md) | Esta seção contém informações sobre a renderização de recursos novos no Direct3D 12 (e no Direct3D 11,3). |
| [Contadores, consultas e medição de desempenho](performance-measurement.md) | As seções a seguir descrevem os recursos para uso em testes e melhorias de desempenho, como consultas, contadores, tempo e predicação. |
| [Trabalhando com o Direct3D 11, o Direct3D 10 e o Direct2D](direct3d-12-interop.md) | Esta seção aborda técnicas de interoperabilidade com versões anteriores do Direct3D e Direct2D, a API do Direct3D 11on12 e diretrizes de portabilidade do Direct3D 11 para o Direct3D 12. |
| [Exemplos de trabalho](working-samples.md) | Os exemplos de trabalho estão disponíveis para download, mostrando o uso de vários recursos do Direct3D 12. |
| [Instruções passo a passo de código do D3D12](d3d12-code-walk-throughs.md) | Esta seção fornece código para cenários de exemplo. Muitos dos passo-a-passo fornecem detalhes sobre qual codificação deve ser adicionada a um exemplo básico, para evitar a repetição do código de componente básico para cada cenário. |
| [Depuração e diagnóstico com o Direct3D 12](understanding-the-d3d12-debug-layer.md) | Inclui tópicos que descrevem como fazer melhor uso da camada de depuração do Direct3D 12 com a validação baseada em GPU (GBV) e como usar os dados estendidos removidos do dispositivo (DRED com). |

## <a name="related-topics"></a>Tópicos relacionados

* [Elementos gráficos do Direct3D 12](direct3d-12-graphics.md)
* [Referência do Direct3D 12](direct3d-12-reference.md)
* [Tutoriais de vídeo do DirectX Advanced Learning](https://www.youtube.com/channel/UCiaX2B8XiXR70jaN7NK-FpA)
