---
description: Mostra como usar Microsoft Media Foundation para decodificar áudio de um arquivo de mídia.
ms.assetid: 29822e6b-8598-4133-b181-7fb0854553b7
title: Exemplo de clipe de áudio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c0e4a3e515d08e2cafd2ab2ba451a528f3d5677
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105794452"
---
# <a name="audio-clip-sample"></a>Exemplo de clipe de áudio

Mostra como usar Microsoft Media Foundation para decodificar áudio de um arquivo de mídia.

O aplicativo de exemplo clipe de áudio lê dados de áudio de um arquivo de mídia e grava o áudio descompactado em um arquivo WAVE.

## <a name="apis-demonstrated"></a>APIs demonstradas

Este exemplo demonstra as seguintes interfaces de Media Foundation:

-   [**IMFSourceReader**](/windows/desktop/api/mfreadwrite/nn-mfreadwrite-imfsourcereader)

## <a name="usage"></a>Uso

Este exemplo é um aplicativo de linha de comando. Ele usa os seguintes argumentos de linha de comando:

``` syntax
audioclip.exe inputfile outputfile.wav
```

-   arquivo_de_entrada: o nome de um arquivo que contém um fluxo de áudio.
-   arquivo_de_saída. wav: o nome do arquivo de som WAVE a ser gravado.

## <a name="requirements"></a>Requisitos



| Produto                                                        | Versão   |
|----------------------------------------------------------------|-----------|
| [SDK do Windows](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | Windows 7 |



 

## <a name="downloading-the-sample"></a>Baixando o exemplo

Este exemplo está disponível no [repositório GitHub de exemplos clássicos do Windows](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/AudioClip).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Exemplos de SDK do Media Foundation](media-foundation-sdk-samples.md)
</dt> <dt>

[Leitor de origem](source-reader.md)
</dt> <dt>

[Tutorial: decodificando áudio](tutorial--decoding-audio.md)
</dt> </dl>

 

 



