---
description: Exemplo de WavSink
ms.assetid: 9e1af25f-d55c-45db-8c76-abf814e16700
title: Exemplo de WavSink
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d1bd754e426d848e9d84aea337225ea51940d8727c63d1e1c78c93aeea43110
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118737131"
---
# <a name="wavsink-sample"></a>Exemplo de WavSink

Mostra como implementar um coletor de mídia personalizado no Microsoft Media Foundation. O exemplo implementa um coletor de arquivo que grava áudio PCM não compactado em um arquivo. wav.

## <a name="apis-demonstrated"></a>APIs demonstradas

Este exemplo demonstra as seguintes interfaces de Media Foundation:

-   [**IMFClockStateSink**](/windows/desktop/api/mfidl/nn-mfidl-imfclockstatesink)
-   [**IMFFinalizableMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imffinalizablemediasink)
-   [**IMFMediaSink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink)
-   [**IMFMediaTypeHandler**](/windows/desktop/api/mfidl/nn-mfidl-imfmediatypehandler)
-   [**IMFStreamSink**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink)

## <a name="usage"></a>Uso

o exemplo de WavSink contém dois projetos Visual Studio:

-   WavSink. vcproj cria uma biblioteca estática que contém a implementação do coletor de mídia.
-   WriteWavFile. vcproj cria um aplicativo de console que usa o coletor de mídia para produzir um arquivo. wav. Este aplicativo é vinculado à biblioteca criada pelo projeto WavSink.

## <a name="requirements"></a>Requisitos



| Produto                                                        | Versão   |
|----------------------------------------------------------------|-----------|
| [SDK do Windows](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | Windows 7 |



 

## <a name="downloading-the-sample"></a>Baixando o exemplo

este exemplo está disponível no [repositório github de amostras clássicas do Windows](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/wavsink).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Exemplos de SDK do Media Foundation](media-foundation-sdk-samples.md)
</dt> <dt>

[Coletores de mídia](media-sinks.md)
</dt> </dl>

 

 



