---
description: Exemplo wavSource
ms.assetid: 905fbba5-0a04-4048-80bd-f8707c4879da
title: Exemplo wavSource
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ffba8ab5bfd5ae1ccfb4df4c90b447c412e9e835a403d496834224f012f8bad7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118972535"
---
# <a name="wavsource-sample"></a>Exemplo wavSource

Mostra como criar uma fonte de mídia personalizada no Microsoft Media Foundation. O exemplo implementa uma fonte de mídia que avalia arquivos de áudio .wav.

Este exemplo é um exemplo relativamente simples de uma fonte de mídia:

-   Há apenas um fluxo, portanto, não há nenhum código para implementar a seleção de fluxo.
-   A fonte de mídia não implementa o controle de taxa (ou seja, reprodução rápida ou inversa).
-   Todos os métodos de origem e fluxo são implementados como métodos síncronos.
-   Como a parte de dados de um arquivo .wav é um único bloco de áudio PCM descompactado, a fonte de mídia não precisa ler os headers de pacote ou analisar o fluxo durante a reprodução, além de ler o header [**WAVEFORMAT**](/windows/win32/api/mmreg/ns-mmreg-waveformat) inicial.

Para obter um exemplo mais avançado de uma fonte de mídia, consulte o [Exemplo de MPEG1Source](mpeg1source-sample.md).

## <a name="apis-demonstrated"></a>APIs demonstradas

Este exemplo demonstra as seguintes Media Foundation interfaces:

-   [**IMFByteStreamHandler**](/windows/desktop/api/mfidl/nn-mfidl-imfbytestreamhandler)
-   [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource)
-   [**IMFMediaStream**](/windows/desktop/api/mfidl/nn-mfidl-imfmediastream)

## <a name="usage"></a>Uso

O exemplo WavSource cria uma DLL que é um servidor COM para o manipulador de fluxo de byte da fonte de mídia e da fonte de mídia. Antes de usar a fonte de mídia, você deve registrar a DLL.

Para usar a fonte de mídia, você pode executar [o BasicPlayback](/previous-versions//bb970475(v=vs.85)). O resolvedor de origem carregará automaticamente a fonte de mídia se você selecionar um arquivo .wav para reprodução. (Se ocorrer um erro, certifique-se de que você registrou com êxito a DLL wavSource.)

Você também pode usar a ferramenta TopoEdit para criar uma topologia de reprodução que contém a fonte de mídia. Para obter mais informações sobre TopEdit, consulte [TopoEdit](topoedit.md).

## <a name="requirements"></a>Requisitos



| Produto                                                        | Versão   |
|----------------------------------------------------------------|-----------|
| [SDK do Windows](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | Windows 7 |



 

## <a name="downloading-the-sample"></a>Baixando o exemplo

Este exemplo está disponível no repositório [Windows github de exemplos clássicos.](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/wavsource)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Exemplos de SDK do Media Foundation](media-foundation-sdk-samples.md)
</dt> <dt>

[Fontes de mídia](media-sources.md)
</dt> <dt>

[Exemplo de MPEG1Source](mpeg1source-sample.md)
</dt> <dt>

[Manipuladores de esquema e Byte-Stream manipuladores](scheme-handlers-and-byte-stream-handlers.md)
</dt> <dt>

[Escrevendo uma fonte de mídia personalizada](writing-a-custom-media-source.md)
</dt> </dl>

 

 
