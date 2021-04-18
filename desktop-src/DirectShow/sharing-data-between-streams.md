---
description: Compartilhando dados entre fluxos
ms.assetid: e18eecf8-9475-420a-9a60-4b1b5f8fd43a
title: Compartilhando dados entre fluxos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee0b2f53fe1952bbc16711f7c7e39c3182ba94a7
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104456688"
---
# <a name="sharing-data-between-streams"></a>Compartilhando dados entre fluxos

> [!Note]  
> Essas APIs são preteridas. Os aplicativos devem usar o filtro de [**apoio de exemplo**](sample-grabber-filter.md) ou implementar um filtro personalizado para obter dados de um grafo de filtro do DirectShow.

 

O processamento de dados de multimídia geralmente requer uma grande quantidade de recursos do sistema; Portanto, você deve evitar copiar dados sempre que possível. A arquitetura de streaming dá suporte a exemplos de fluxo compartilhados, um mecanismo que move dados de um fluxo para outro sem copiá-los. Esse buffer permite o transporte eficiente de dados entre dois fluxos, mesmo que o fluxo de destino não ofereça suporte especificamente ao formato de dados subjacente.

Por exemplo, suponha que você tenha um fluxo de multimídia com três fluxos de dados: vídeo e áudio e dados de URL com carimbo de data/hora para corresponder ao conteúdo do vídeo. Você deseja escrever um aplicativo que adiciona um aviso de direitos autorais em cada quadro de vídeo e grava os dados em outro fluxo para armazenamento, mas seu aplicativo não entende nenhum formato de dados, exceto o fluxo de vídeo. Para o fluxo de vídeo, você cria um exemplo anexado à superfície do DirectDraw desejada. Em seguida, você pode criar um fluxo de saída chamando o método [**IDirectDrawMediaStream:: createsample**](/previous-versions/windows/desktop/api/ddstream/nf-ddstream-idirectdrawmediastream-createsample) com esse ponteiro para a mesma superfície ou [**IMediaStream:: CreateSharedSample**](/previous-versions/windows/desktop/api/mmstream/nf-mmstream-imediastream-createsharedsample). Em ambos os casos, os fluxos de entrada e saída compartilham a superfície do DirectDraw. Como você entende o formato de vídeo, você pode acessar essa superfície conforme necessário.

Para recuperar os outros ponteiros de fluxo de origem (áudio e URL), enumere o fluxo do contêiner de origem e pegue os ponteiros para os fluxos de não vídeo. Cada um desses fluxos de origem tem um fluxo de saída associado no contêiner de fluxo de saída. Recupere esses ponteiros de saída chamando o método [**IMultiMediaStream:: GetMediaStream**](/previous-versions/windows/desktop/api/mmstream/nf-mmstream-imultimediastream-getmediastream) no contêiner de saída com cada um dos ponteiros de fluxo de origem. As etapas a seguir descrevem esse processo.

1.  Chame [**IMultiMediaStream:: EnumMediaStreams**](/previous-versions/windows/desktop/api/mmstream/nf-mmstream-imultimediastream-enummediastreams) para recuperar um ponteiro para um fluxo de origem. Certifique-se de que não seja o fluxo de vídeo, porque seu aplicativo já entende seu formato.
2.  Chame [**IMultiMediaStream:: GetMediaStream**](/previous-versions/windows/desktop/api/mmstream/nf-mmstream-imultimediastream-getmediastream) no fluxo do contêiner de saída com o ponteiro da etapa 1. Isso retorna um ponteiro para o fluxo de saída desejado.
3.  Chame [**AllocateSample**](/previous-versions/windows/desktop/api/mmstream/nf-mmstream-imediastream-allocatesample) no fluxo de origem.
4.  Chame [**CreateSharedSample**](/previous-versions/windows/desktop/api/mmstream/nf-mmstream-imediastream-createsharedsample) no fluxo de saída.
5.  Chame [**Update**](/previous-versions/windows/desktop/api/mmstream/nf-mmstream-istreamsample-update) no fluxo de origem para ler os dados.
6.  Chame [**Update**](/previous-versions/windows/desktop/api/mmstream/nf-mmstream-istreamsample-update) no fluxo de saída para gravar os dados.

Repita essas etapas para cada fluxo cujo formato você não dá suporte. Quando ambos os exemplos terminarem de atualizar, o fluxo de saída terá todos os dados do fluxo de origem e você terminará.

 

 



