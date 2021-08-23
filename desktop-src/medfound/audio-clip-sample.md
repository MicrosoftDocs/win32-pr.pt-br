---
description: Mostra como usar o Microsoft Media Foundation para decodificar o áudio de um arquivo de mídia.
ms.assetid: 29822e6b-8598-4133-b181-7fb0854553b7
title: Exemplo de clipe de áudio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f180dfb7c4b0e456f45169d36fdfb1f77701b0e82250690706208a715fdd3ce5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119035484"
---
# <a name="audio-clip-sample"></a>Exemplo de clipe de áudio

Mostra como usar o Microsoft Media Foundation para decodificar o áudio de um arquivo de mídia.

O aplicativo de exemplo de Clipe de Áudio lê dados de áudio de um arquivo de mídia e grava o áudio descompactado em um arquivo WAVE.

## <a name="apis-demonstrated"></a>APIs demonstradas

Este exemplo demonstra as seguintes Media Foundation interfaces:

-   [**IMFSourceReader**](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsourcereader)

## <a name="usage"></a>Uso

Este exemplo é um aplicativo de linha de comando. Ele usa os seguintes argumentos de linha de comando:

``` syntax
audioclip.exe inputfile outputfile.wav
```

-   inputfile: o nome de um arquivo que contém um fluxo de áudio.
-   outputfile.wav: o nome do arquivo WAVE a ser escrito.

## <a name="requirements"></a>Requisitos



| Produto                                                        | Versão   |
|----------------------------------------------------------------|-----------|
| [SDK do Windows](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | Windows 7 |



 

## <a name="downloading-the-sample"></a>Baixando o exemplo

Este exemplo está disponível no repositório [Windows github de exemplos clássicos.](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/AudioClip)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Exemplos de SDK do Media Foundation](media-foundation-sdk-samples.md)
</dt> <dt>

[Leitor de Origem](source-reader.md)
</dt> <dt>

[Tutorial: Decodificação de áudio](tutorial--decoding-audio.md)
</dt> </dl>

 

 



