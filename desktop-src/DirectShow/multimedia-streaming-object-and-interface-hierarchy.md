---
description: Hierarquia de interface e objeto de streaming de multimídia
ms.assetid: dbb6dc3b-b55e-4f6c-918f-068308e2dba9
title: Hierarquia de interface e objeto de streaming de multimídia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52339644730139af22fd21fa2c24b8448a1afaf3
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "103837685"
---
# <a name="multimedia-streaming-object-and-interface-hierarchy"></a>Hierarquia de interface e objeto de streaming de multimídia

> [!Note]  
> Essas APIs são preteridas. Os aplicativos devem usar o filtro de [**apoio de exemplo**](sample-grabber-filter.md) ou implementar um filtro personalizado para obter dados de um grafo de filtro do DirectShow.

 

O diagrama a seguir mostra a hierarquia de objetos usada no streaming de multimídia.

![hierarquia de objetos multimediastreaming](images/mmstream02.png)

A arquitetura de streaming de multimídia define três tipos gerais de objeto:

-   O objeto **AMMultimediaStream** expõe a interface [**IAMMultiMediaStream**](/previous-versions/windows/desktop/api/amstream/nn-amstream-iammultimediastream) . Internamente, esse objeto encapsula o grafo de filtro do DirectShow.
-   Os objetos de *fluxo de mídia* expõem a interface [**IMediaStream**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imediastream) e são específicos de dados. O objeto AMMultimediaStream contém um ou mais fluxos de mídia.
-   Os objetos de *exemplo de fluxo* contêm os dados para um fluxo específico.

Há suporte para os seguintes objetos de fluxo de mídia:

-   Fluxo de áudio. Expõe a interface [**IAudioMediaStream**](/previous-versions/windows/desktop/api/austream/nn-austream-iaudiomediastream) .
-   Fluxo do DirectDraw. Representa um fluxo de vídeo que é processado para uma superfície do DirectDraw. Expõe a interface [**IDirectDrawMediaStream**](/previous-versions/windows/desktop/api/ddstream/nn-ddstream-idirectdrawmediastream) .
-   Fluxo do tipo de mídia. Representa dados arbitrários. Expõe a interface [**IAMMediaTypeStream**](/previous-versions/windows/desktop/api/amstream/nn-amstream-iammediatypestream) .

Cada objeto de fluxo de mídia cria seu próprio tipo de objeto de exemplo de fluxo:

-   Fluxos de áudio criam amostras de áudio, que expõem a interface [**IAudioStreamSample**](/previous-versions/windows/desktop/api/austream/nn-austream-iaudiostreamsample) .
-   Os fluxos do DirectDraw criam exemplos do DirectDraw, que expõem a interface [**IDirectDrawStreamSample**](/previous-versions/windows/desktop/api/ddstream/nn-ddstream-idirectdrawstreamsample) .
-   Os fluxos de tipo de mídia criam amostras de tipo de mídia, que expõem a interface [**IAMMediaTypeSample**](/previous-versions/windows/desktop/api/amstream/nn-amstream-iammediatypesample) .

O diagrama a seguir mostra a hierarquia de interface para as interfaces listadas anteriormente:

![hierarquia de interface multimediastreaming](images/mmstream01.png)

 

 



