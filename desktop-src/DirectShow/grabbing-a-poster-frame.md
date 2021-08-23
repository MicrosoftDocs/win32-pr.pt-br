---
description: Pegar um quadro de cartaz
ms.assetid: 0727a1ed-1bc7-49fc-a288-00283e637a71
title: Pegar um quadro de cartaz
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6668526d83f17c4ceab260f3a31ed43d19ec1d142bd8f8fdae080161350ded8b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119536566"
---
# <a name="grabbing-a-poster-frame"></a>Pegar um quadro de cartaz

\[Essa API não tem suporte e pode ser alterada ou não disponível no futuro.\]

Este artigo descreve como exibir um quadro de cartaz de um arquivo de mídia digital usando o objeto [MediaDet (MediaDet)](media-detector--mediadet.md) fornecido com o [DirectShow Editing Services](directshow-editing-services.md).

O Detector de Mídia é um objeto auxiliar que pode obter informações de formato de um arquivo de origem de mídia. Ele também pode pegar uma imagem de bitmap de um fluxo de vídeo no arquivo de origem. Supondo que o arquivo seja buscado, você pode obter a imagem de qualquer ponto no arquivo. A imagem retornada está sempre no formato RGB de 24 bits.

O Detector de Mídia não é um filtro e o aplicativo não precisa usar o Gerenciador Graph Filtro nem criar um grafo de filtro. Internamente, o Detector de Mídia cria um grafo de filtro que contém o [**Filtro de Captura de Amostra**](sample-grabber-filter.md). Para obter um bitmap, o Detector de Mídia busca e pausa o grafo de filtro e, em seguida, recupera o bitmap do filtro Grabber de Exemplo. O aplicativo se comunica com o Detector de Mídia por meio da interface [**IMediaDet.**](imediadet.md) O Detector de Mídia é um bom exemplo de encapsulamento de um grafo de filtro dentro de um objeto auxiliar, a fim de proteger aplicativos de detalhes relacionados ao grafo.

O Detector de Mídia opera em dois modos. Quando você o cria pela primeira vez, o Detector de Mídia está no modo de "coleta de informações". Você pode especificar o nome de um arquivo de mídia e obter informações sobre cada um dos fluxos no arquivo, como o tipo de formato, a taxa de quadros ou a duração. Se o arquivo contiver um fluxo de vídeo, você poderá alternar o Detector de Mídia para o modo de "captura de bitmap" e recuperar bitmaps da origem. No entanto, depois de fazer isso, você não poderá alternar o Detector de Mídia de volta para seu modo original; ele é anexado permanentemente a esse fluxo de vídeo. Para trabalhar com outro fluxo ou outro arquivo, você deve criar uma nova instância do Detector de Mídia.

> [!Note]  
> Os exemplos de código neste tutorial usam a classe **CComPtr** da ATL, que gerencia automaticamente as contagens de referência. Se você preferir usar ponteiros de interface brutos, lembre-se de liberar todas as interfaces quando terminar de usá-la. Além disso, para a brevidade, os exemplos de código omitem grande parte da verificação de erro que um aplicativo deve executar. No código de trabalho, sempre verifique **os valores HRESULT.**

 

Este tutorial contém as seguintes etapas:

-   [Etapa 1: Criar o Windows Framework](step-1--create-the-windows-framework.md)
-   [Etapa 2: Adicionar um comando de menu para pegar um quadro de cartaz](step-2--add-a-menu-command-to-grab-a-poster-frame.md)
-   [Etapa 3: Implementar a função Frame-Grabbing dados](step-3--implement-the-frame-grabbing-function.md)
-   [Etapa 4: Desenhar o bitmap na área do cliente](step-4--draw-the-bitmap-on-the-client-area.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Usando DirectShow de edição](using-directshow-editing-services.md)
</dt> </dl>

 

 



