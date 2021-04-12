---
description: Modelo de objeto de origem de mídia
ms.assetid: 88373028-8a34-4bf1-8300-d1a7e4c7dd75
title: Modelo de objeto de origem de mídia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c0d05cc9d5341bff433d6276b5ee67505361b78f
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "104297955"
---
# <a name="media-source-object-model"></a>Modelo de objeto de origem de mídia

Este tópico descreve o modelo de objeto para fontes de mídia no Microsoft Media Foundation. Uma fonte de mídia deve implementar dois objetos:

-   Um descritor de apresentação, que descreve o conteúdo da origem, incluindo o número de fluxos e o formato de cada fluxo. Para obter mais informações sobre descritores de apresentação, consulte [descritores de apresentação](presentation-descriptors.md).
-   Um ou mais fluxos de mídia, que geram os dados de origem.

A origem não cria os fluxos até que a reprodução seja iniciada.

## <a name="media-source-interfaces"></a>Interfaces de origem de mídia

Uma origem de mídia deve expor as seguintes interfaces por meio de **QueryInterface**.



| Interface                                                | Descrição                                                                                                     |
|----------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource)                 | Necessário para todas as fontes de mídia.                                                                                 |
| [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) | Necessário para todas as fontes de mídia. A interface [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) herda essa interface. |



 

Opcionalmente, uma fonte de mídia pode implementar a interface [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice) e implementar qualquer uma das seguintes interfaces como serviços:



| Interface de serviço                                  | Descrição                                                       |
|----------------------------------------------------|-------------------------------------------------------------------|
| [**IMFRateControl**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol)           | Controla a taxa de reprodução.                                       |
| [**IMFRateSupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport)           | Relata o intervalo de taxas de reprodução com suporte.           |
| [**IMFQualityAdvise**](/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise)       | Permite que o Gerenciador de qualidade ajuste a qualidade de áudio ou vídeo. |
| [**IMFMetadataProvider**](/windows/desktop/api/mfidl/nn-mfidl-imfmetadataprovider) | Fornece metadados.                                                |



 

Se a origem da mídia puder ser executada em taxas diferentes da velocidade normal (1,0), ela deverá expor o serviço de controle de taxa ([**IMFRateControl**](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol) e [**IMFRateSupport**](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport)). Caso contrário, supõe-se que a origem só dá suporte à reprodução em velocidade normal. Para obter mais informações, consulte [implementando o controle de taxa](implementing-rate-control.md).

Para obter mais informações sobre interfaces de serviço e [**IMFGetService**](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice), consulte [interfaces de serviço](service-interfaces.md).

## <a name="media-stream-interfaces"></a>Interfaces de fluxo de mídia

Os fluxos de mídia devem implementar as seguintes interfaces.



| Interface                                                | Descrição                                                                                                     |
|----------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| [**IMFMediaStream**](/windows/desktop/api/mfidl/nn-mfidl-imfmediastream)                 | Necessário para todos os fluxos de mídia.                                                                                 |
| [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) | Necessário para todos os fluxos de mídia. A interface [**IMFMediaStream**](/windows/desktop/api/mfidl/nn-mfidl-imfmediastream) herda essa interface. |



 

No momento, nenhuma interface de serviço é definida para fluxos de mídia.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Fontes de mídia](media-sources.md)
</dt> </dl>

 

 



