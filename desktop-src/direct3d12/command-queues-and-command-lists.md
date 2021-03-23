---
title: Envio de trabalho no Direct3D 12
description: Para melhorar a eficiência da CPU dos aplicativos do Direct3D, o Direct3D 12 não dá mais suporte a um contexto imediato associado a um dispositivo.
ms.assetid: BE2F46EA-D4A9-47F7-A2D1-6A486DD4DC1A
ms.localizationpriority: high
ms.topic: article
ms.date: 11/15/2018
ms.openlocfilehash: aa852fc82280b14b0270a7c4a4c40cfe441803b7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "74104206"
---
# <a name="work-submission-in-direct3d-12"></a>Envio de trabalho no Direct3D 12

Para melhorar a eficiência da CPU dos aplicativos do Direct3D, a partir da versão 12, o Direct3D não dá mais suporte a um contexto imediato associado a um dispositivo. Em vez disso, seu aplicativo registra e, em seguida, envia as *listas de comandos*, que contêm chamadas de gerenciamento de recursos e de desenho. Você pode enviar essas listas de comandos de vários threads para uma ou mais filas de comando, que gerenciam a execução dos comandos. Essa alteração fundamental aumenta a eficiência de thread único, permitindo que seu aplicativo implante previamente o trabalho de renderização para reutilização posterior e aproveite os sistemas de vários núcleos, distribuindo o trabalho de renderização em vários threads.

## <a name="in-this-section"></a>Nesta seção

| Tópico | Descrição |
|-|-|
| [Design de filosofia de filas de comando e listas de comandos](design-philosophy-of-command-queues-and-command-lists.md) | As metas de habilitar a reutilização do trabalho de renderização e do dimensionamento multithread, exigiam alterações fundamentais em como os aplicativos do Direct3D enviam o trabalho de renderização para a GPU. |
| [Criação e gravação de listas de comandos e pacotes](recording-command-lists-and-bundles.md) | Este tópico descreve a gravação de listas de comandos e pacotes em aplicativos Direct3D 12. As listas de comandos e os pacotes permitem que os aplicativos registrem chamadas de desenho ou alteração de estado para execução posterior na GPU (unidade de processamento gráfico). |
| [Executando e sincronizando listas de comandos](executing-and-synchronizing-command-lists.md) | No Microsoft Direct3D 12, o modo imediato de versões anteriores não está mais presente. Em vez disso, os aplicativos criam listas de comandos e pacotes e, em seguida, registram conjuntos de comandos de GPU. As filas de comando são usadas para enviar listas de comandos a serem executadas. Esse modelo permite que os desenvolvedores tenham mais controle sobre o uso eficiente da GPU e da CPU. |
| [Gerenciando o estado do pipeline de gráficos no Direct3D 12](managing-graphics-pipeline-state-in-direct3d-12.md) | Este tópico descreve como o estado do pipeline de gráficos é definido no Direct3D 12. |
| [Usando barreiras de recursos para sincronizar Estados de recursos no Direct3D 12](using-resource-barriers-to-synchronize-resource-states-in-direct3d-12.md) | Para reduzir o uso geral da CPU e habilitar o pré-processamento e o pós-processamento do driver, o Direct3D 12 move a responsabilidade do gerenciamento de estado por recurso do driver de gráficos para o aplicativo. |
| [Pipelines e sombreadores com o Direct3D 12](pipelines-and-shaders-with-directx-12.md) | O pipeline programável do Direct3D 12 aumenta significativamente o desempenho de renderização em comparação com as interfaces de programação de gráficos de geração anteriores. |
| [Sombreamento de taxa variável (VRS)](vrs.md) | Sombreamento de taxa variável &mdash; ou sombreamento de pixel grosso &mdash; é um mecanismo que permite alocar desempenho de renderização/energia em taxas que variam em sua imagem renderizada. |
| [Passagens de renderização](direct3d-12-render-passes.md) | O recurso render passes ajuda seu renderizador a melhorar a eficiência da GPU, reduzindo o tráfego de memória de/para a memória fora do chip; Ele faz isso habilitando seu aplicativo para identificar melhor os requisitos de ordenação de processamento de recursos e as dependências de dados. |

## <a name="related-topics"></a>Tópicos relacionados

* [Guia de programação do Direct3D 12](directx-12-programming-guide.md)
