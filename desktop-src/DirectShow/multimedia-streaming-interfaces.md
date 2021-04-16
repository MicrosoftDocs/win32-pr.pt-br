---
description: Interfaces de streaming de multimídia
ms.assetid: 53d639e2-8717-4552-b0d3-b8c500bd38a8
title: Interfaces de streaming de multimídia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d654bae73ee822f553a1494e3b374cf35b8ac4a1
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "104506363"
---
# <a name="multimedia-streaming-interfaces"></a>Interfaces de streaming de multimídia

> [!Note]  
> Essas APIs são preteridas. Os aplicativos devem usar o filtro de [**apoio de exemplo**](sample-grabber-filter.md) ou implementar um filtro personalizado para obter dados de um grafo de filtro do DirectShow.

 

Esta seção contém entradas de referência para todas as interfaces de streaming de multimídia e seus métodos, incluindo as que o Microsoft DirectShow dá suporte.



| Interface                                                  | Descrição                                                                                                                                             |
|------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IAMMediaStream**](/previous-versions/windows/desktop/api/amstream/nn-amstream-iammediastream)                   | Manipula as conexões internas entre os filtros do DirectShow e os gráficos de filtro em aplicativos que usam streaming de multimídia.                            |
| [**IAMMediaTypeSample**](/previous-versions/windows/desktop/api/amstream/nn-amstream-iammediatypesample)           | Contém métodos para manipular exemplos de fluxo com tipos de mídia arbitrários.                                                                            |
| [**IAMMediaTypeStream**](/previous-versions/windows/desktop/api/amstream/nn-amstream-iammediatypestream)           | Contém métodos para criar fluxos de multimídia com tipos de mídia arbitrários.                                                                            |
| [**IAMMultiMediaStream**](/previous-versions/windows/desktop/api/amstream/nn-amstream-iammultimediastream)         | Expõe a funcionalidade do DirectShow aos desenvolvedores de fluxo multimídia.                                                                                       |
| [**IAudioData**](/previous-versions/windows/desktop/api/austream/nn-austream-iaudiodata)                           | Fornece métodos que permitem que os aplicativos definam e obtenham os dados de áudio subjacentes aos quais os fluxos de áudio serão referenciados.                                   |
| [**IAudioMediaStream**](/previous-versions/windows/desktop/api/austream/nn-austream-iaudiomediastream)             | Controla fluxos de mídia de áudio fornecendo métodos que definem e obtêm o formato do fluxo.                                                                 |
| [**IAudioStreamSample**](/previous-versions/windows/desktop/api/austream/nn-austream-iaudiostreamsample)           | Recupera informações dos objetos de dados [**IAudioData**](/previous-versions/windows/desktop/api/austream/nn-austream-iaudiodata) subjacentes.                                                                |
| [**IDirectDrawMediaStream**](/previous-versions/windows/desktop/api/ddstream/nn-ddstream-idirectdrawmediastream)   | Controla os fluxos de mídia que aparecem no Microsoft® DirectDraw® superfícies.                                                                                  |
| [**IDirectDrawStreamSample**](/previous-versions/windows/desktop/api/ddstream/nn-ddstream-idirectdrawstreamsample) | Fornece métodos que definem e recuperam ponteiros para a superfície do DirectDraw associada ao exemplo de fluxo atual.                                    |
| [**IMediaStream**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imediastream)                       | Fornece acesso às características de um fluxo de mídia, como o tipo de mídia e a ID de finalidade do fluxo. Ele também tem métodos que criam amostras de dados. |
| [**IMediaStreamFilter**](/previous-versions/windows/desktop/api/amstream/nn-amstream-imediastreamfilter)           | Com suporte pelo filtro de fluxo de mídia, que é usado internamente pelo objeto de fluxo de multimídia. .                                                       |
| [**IMemoryData**](/previous-versions/windows/desktop/api/austream/nn-austream-imemorydata)                         | Contém métodos que definem e recuperam dados de memória em objetos de dados de áudio.                                                                               |
| [**IMultiMediaStream**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imultimediastream)             | Fornece métodos que controlam um fluxo de multimídia e fornecem acesso a seus fluxos de mídia subjacentes.                                                   |
| [**IStreamSample**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-istreamsample)                     | Fornece controle sobre o comportamento de amostras de fluxo.                                                                                                   |



 

 

 



