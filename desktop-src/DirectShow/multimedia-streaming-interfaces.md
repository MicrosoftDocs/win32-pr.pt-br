---
description: Interfaces de streaming de multimídia
ms.assetid: 53d639e2-8717-4552-b0d3-b8c500bd38a8
title: Interfaces de streaming de multimídia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b38200d98b0f01b7260508cbf7bd19c6e65efdfb3af78f2efff77be38294e8b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118152952"
---
# <a name="multimedia-streaming-interfaces"></a>Interfaces de streaming de multimídia

> [!Note]  
> Essas APIs são preteridas. os aplicativos devem usar o filtro de [**apoio de exemplo**](sample-grabber-filter.md) ou implementar um filtro personalizado para obter dados de um DirectShow gráfico de filtro.

 

esta seção contém entradas de referência para todas as interfaces de streaming de multimídia e seus métodos, incluindo as que o Microsoft DirectShow suporta.



| Interface                                                  | Descrição                                                                                                                                             |
|------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IAMMediaStream**](/previous-versions/windows/desktop/api/amstream/nn-amstream-iammediastream)                   | manipula as conexões internas entre filtros de DirectShow e gráficos de filtro em aplicativos que usam streaming de multimídia.                            |
| [**IAMMediaTypeSample**](/previous-versions/windows/desktop/api/amstream/nn-amstream-iammediatypesample)           | Contém métodos para manipular exemplos de fluxo com tipos de mídia arbitrários.                                                                            |
| [**IAMMediaTypeStream**](/previous-versions/windows/desktop/api/amstream/nn-amstream-iammediatypestream)           | Contém métodos para criar fluxos de multimídia com tipos de mídia arbitrários.                                                                            |
| [**IAMMultiMediaStream**](/previous-versions/windows/desktop/api/amstream/nn-amstream-iammultimediastream)         | expõe DirectShow funcionalidade aos desenvolvedores de fluxo multimídia.                                                                                       |
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



 

 

 



