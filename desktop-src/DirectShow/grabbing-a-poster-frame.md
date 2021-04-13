---
description: Capturando um quadro de cartaz
ms.assetid: 0727a1ed-1bc7-49fc-a288-00283e637a71
title: Capturando um quadro de cartaz
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2cf06a10d74bb6c81622ac9bad7a1b770f5dc12
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104456868"
---
# <a name="grabbing-a-poster-frame"></a>Capturando um quadro de cartaz

\[Essa API não tem suporte e pode ser alterada ou não estar disponível no futuro.\]

Este artigo descreve como exibir um quadro de cartaz de um arquivo de mídia digital, usando o objeto [detector de mídia (MediaDet)](media-detector--mediadet.md) fornecido com os [serviços de edição do DirectShow](directshow-editing-services.md).

O detector de mídia é um objeto auxiliar que pode obter informações de formato de um arquivo de origem de mídia. Ele também pode pegar uma imagem de bitmap de um fluxo de vídeo no arquivo de origem. Supondo que o arquivo seja pesquisável, você pode obter a imagem de qualquer ponto no arquivo. A imagem retornada sempre está no formato RGB de 24 bits.

O detector de mídia não é um filtro e o aplicativo não precisa usar o Gerenciador de gráfico de filtro nem criar um gráfico de filtro. Internamente, o detector de mídia cria um gráfico de filtro que contém o [**filtro de apoio de exemplo**](sample-grabber-filter.md). Para obter um bitmap, o detector de mídia busca e pausa o gráfico de filtro e, em seguida, recupera o bitmap do filtro de apoio de exemplo. O aplicativo se comunica com o detector de mídia por meio da interface [**IMediaDet**](imediadet.md) . O detector de mídia é um bom exemplo de encapsulamento de um grafo de filtro dentro de um objeto auxiliar, a fim de proteger aplicativos de detalhes relacionados ao grafo.

O detector de mídia opera em dois modos. Ao criá-lo pela primeira vez, o detector de mídia está no modo de "coleta de informações". Você pode especificar o nome de um arquivo de mídia e obter informações sobre cada um dos fluxos no arquivo, como o tipo de formato, a taxa de quadros ou a duração. Se o arquivo contiver um fluxo de vídeo, você poderá alternar o detector de mídia no modo "captura de bitmap" e recuperar os bitmaps da origem. No entanto, depois de fazer isso, você não pode alternar o detector de mídia de volta para seu modo original; Ele é anexado permanentemente a esse fluxo de vídeo. Para trabalhar com outro fluxo ou outro arquivo, você deve criar uma nova instância do detector de mídia.

> [!Note]  
> Os exemplos de código neste tutorial usam a classe **CComPtr** do ATL, que gerencia automaticamente as contagens de referência. Se você preferir usar ponteiros de interface brutos, lembre-se de liberar todas as interfaces quando terminar. Além disso, para resumir, os exemplos de código omitem grande parte da verificação de erros que um aplicativo deve executar. No código de trabalho, sempre verifique valores **HRESULT** .

 

Este tutorial contém as seguintes etapas:

-   [Etapa 1: criar o Windows Framework](step-1--create-the-windows-framework.md)
-   [Etapa 2: adicionar um comando de menu para pegar um quadro de cartaz](step-2--add-a-menu-command-to-grab-a-poster-frame.md)
-   [Etapa 3: implementar a função Frame-Grabbing](step-3--implement-the-frame-grabbing-function.md)
-   [Etapa 4: desenhar o bitmap na área do cliente](step-4--draw-the-bitmap-on-the-client-area.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando os serviços de edição do DirectShow](using-directshow-editing-services.md)
</dt> </dl>

 

 



