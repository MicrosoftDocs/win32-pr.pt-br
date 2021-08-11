---
description: Este tópico descreve o design geral do Microsoft Media Foundation. Para obter informações sobre como usar Media Foundation para tarefas de programação específicas, consulte Media Foundation Guia de programação.
ms.assetid: DEA2B19A-CF15-4BF4-84C3-9A6417C942E2
title: Visão geral da arquitetura de Media Foundation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de953d05c55c96d1affa2213e1a7f11143a71aa319b4671c159f085e65268d05
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118239623"
---
# <a name="overview-of-the-media-foundation-architecture"></a>Visão geral da arquitetura de Media Foundation

Este tópico descreve o design geral do Microsoft Media Foundation. Para obter informações sobre como usar Media Foundation para tarefas de programação específicas, consulte [Media Foundation Guia de programação](media-foundation-programming-guide.md).

O diagrama a seguir mostra uma exibição de alto nível da arquitetura de Media Foundation.

![diagrama mostrando uma exibição de alto nível da arquitetura do Media Foundation.](images/mfarch01.png)

Media Foundation fornece dois modelos de programação distintos. O primeiro modelo, mostrado no lado esquerdo do diagrama, usa um pipeline de ponta a ponta para dados de mídia. O aplicativo Inicializa o pipeline — por exemplo, fornecendo a URL de um arquivo a ser reproduzido — e depois chama métodos para controlar o streaming. No segundo modelo, mostrado no lado direito do diagrama, o aplicativo obtém dados de uma fonte ou envia-os por push para um destino (ou ambos). Esse modelo é particularmente útil se você precisar processar os dados, pois o aplicativo tem acesso direto ao fluxo de dados.

### <a name="primitives-and-platform"></a>Primitivas e plataforma

Começando na parte inferior do diagrama, os *primitivos* são objetos auxiliares usados em toda a API de Media Foundation:

-   Os [atributos](attributes-and-properties.md) são uma maneira genérica de armazenar informações dentro de um objeto, como uma lista de pares de chave/valor.
-   Os [tipos de mídia](media-types.md) descrevem o formato de um fluxo de dados de mídia.
-   Os [buffers de mídia](media-buffers.md) armazenam partes de dados de mídia, como quadros de vídeo e amostras de áudio, e são usados para transportar dados entre objetos.
-   [Exemplos de mídia](media-samples.md) são contêineres para buffers de mídia. Eles também contêm metadados sobre os buffers, como carimbos de data/hora.

As [APIs da plataforma Media Foundation](media-foundation-platform-apis.md) fornecem algumas funcionalidades básicas que são usadas pelo pipeline de Media Foundation, como retornos de chamada e filas de trabalho assíncronos. Alguns aplicativos podem precisar chamar essas APIs diretamente; Além disso, você precisará delas se implementar uma fonte, transformação ou coletor personalizado para Media Foundation.

### <a name="media-pipeline"></a>Pipeline de mídia

O pipeline de mídia contém três tipos de objeto que geram ou processam dados de mídia:

-   As [fontes de mídia](media-sources.md) introduzem dados no pipeline. Uma fonte de mídia pode obter dados de um arquivo local, como um arquivo de vídeo; de um fluxo de rede; ou de um dispositivo de captura de hardware.
-   [Media Foundation transformações](media-foundation-transforms.md) (MFTs) processam dados de um fluxo. Os codificadores e os decodificadores são implementados como MFTs.
-   Os [coletores de mídia](media-sinks.md) consomem os dados; por exemplo, mostrando o vídeo na exibição, reproduzindo áudio ou gravando os dados em um arquivo de mídia.

Terceiros podem implementar suas próprias fontes personalizadas, coletores e MFTs; por exemplo, para dar suporte a novos formatos de arquivo de mídia.

A [sessão de mídia](media-session.md) controla o fluxo de dados por meio do pipeline e manipula tarefas como controle de qualidade, sincronização de áudio/vídeo e resposta a alterações de formato.

### <a name="source-reader-and-sink-writer"></a>Leitor de fonte e gravador de coletor

O [leitor de origem](source-reader.md) e o [gravador do coletor](sink-writer.md) fornecem uma maneira alternativa de usar os componentes básicos do Media Foundation (fontes de mídia, transformações e coletores de mídia). O leitor de origem hospeda uma fonte de mídia e zero ou mais decodificadores, enquanto o gravador de coletor hospeda um coletor de mídia e zero ou mais codificadores. Você pode usar o leitor de origem para obter dados compactados ou descompactados de uma fonte de mídia e usar o gravador de coletor para codificar dados e enviar os dados para um coletor de mídia.

> [!Note]  
> o leitor de fonte e o gravador de coletor estão disponíveis no Windows 7.

 

Esse modelo de programação fornece ao aplicativo mais controle sobre o fluxo de dados e também fornece ao aplicativo acesso direto aos dados da origem.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Media Foundation: conceitos essenciais](media-foundation-programming--essential-concepts.md)
</dt> <dt>

[Arquitetura Media Foundation](media-foundation-architecture.md)
</dt> </dl>

 

 



