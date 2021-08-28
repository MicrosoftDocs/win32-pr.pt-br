---
description: Hierarquia de interface e objeto de streaming multimídia
ms.assetid: dbb6dc3b-b55e-4f6c-918f-068308e2dba9
title: Hierarquia de interface e objeto de streaming multimídia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b73da4777c2d05ff6455758ebde6e64a9a4c8277e8445ed59dca7f17088baea0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120075756"
---
# <a name="multimedia-streaming-object-and-interface-hierarchy"></a>Hierarquia de interface e objeto de streaming multimídia

> [!Note]  
> Essas APIs foram preterida. Os aplicativos devem usar [**o filtro Grabber de**](sample-grabber-filter.md) exemplo ou implementar um filtro personalizado para obter dados de um DirectShow de filtro.

 

O diagrama a seguir mostra a hierarquia de objetos usada no streaming multimídia.

![hierarquia de objetos de fluxo multimídia](images/mmstream02.png)

A arquitetura de streaming multimídia define três tipos gerais de objeto:

-   O **objeto AMMultimediaStream** expõe a interface [**IAMMultiMediaStream.**](/previous-versions/windows/desktop/api/amstream/nn-amstream-iammultimediastream) Internamente, esse objeto envolve o grafo DirectShow filtro.
-   *Objetos de fluxo* de mídia expõem a interface [**IMediaStream**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imediastream) e são específicos de dados. O objeto AMMultimediaStream contém um ou mais fluxos de mídia.
-   *Objetos de exemplo* de fluxo contêm os dados de um fluxo específico.

Há suporte para os seguintes objetos de fluxo de mídia:

-   Fluxo de áudio. Expõe a interface [**IAudioMediaStream.**](/previous-versions/windows/desktop/api/austream/nn-austream-iaudiomediastream)
-   Fluxo do DirectDraw. Representa um fluxo de vídeo que é renderizado para uma superfície directDraw. Expõe a interface [**IDirectDrawMediaStream.**](/previous-versions/windows/desktop/api/ddstream/nn-ddstream-idirectdrawmediastream)
-   Fluxo de tipo de mídia. Representa dados arbitrários. Expõe a interface [**IAMMediaTypeStream.**](/previous-versions/windows/desktop/api/amstream/nn-amstream-iammediatypestream)

Cada objeto de fluxo de mídia cria seu próprio tipo de objeto de exemplo de fluxo:

-   Os fluxos de áudio criam amostras de áudio, que expõem a interface [**IAudioStreamSample.**](/previous-versions/windows/desktop/api/austream/nn-austream-iaudiostreamsample)
-   Os fluxos directDraw criam exemplos do DirectDraw, que expõem a interface [**IDirectDrawStreamSample.**](/previous-versions/windows/desktop/api/ddstream/nn-ddstream-idirectdrawstreamsample)
-   Os fluxos de tipo de mídia criam exemplos de tipo de mídia, que expõem a interface [**IAMMediaTypeSample.**](/previous-versions/windows/desktop/api/amstream/nn-amstream-iammediatypesample)

O diagrama a seguir mostra a hierarquia de interface para as interfaces listadas anteriormente:

![hierarquia de interface de fluxo multimídia](images/mmstream01.png)

 

 



