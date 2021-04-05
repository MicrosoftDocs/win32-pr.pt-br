---
description: Exemplo de WavSource
ms.assetid: 905fbba5-0a04-4048-80bd-f8707c4879da
title: Exemplo de WavSource
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 050edb9df75032384f93c6e1f37c52e89f14a748
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827791"
---
# <a name="wavsource-sample"></a>Exemplo de WavSource

Mostra como criar uma fonte de mídia personalizada no Microsoft Media Foundation. O exemplo implementa uma fonte de mídia que analisa arquivos de áudio. wav.

Este exemplo é um exemplo relativamente simples de uma fonte de mídia:

-   Há apenas um fluxo, portanto, não há nenhum código para implementar a seleção de fluxo.
-   A origem da mídia não implementa o controle de taxa (isto é, reprodução rápida ou inversa).
-   Todos os métodos de origem e de fluxo são implementados como métodos síncronos.
-   Como a parte de dados de um arquivo. wav é um único bloco de áudio PCM descompactado, a origem da mídia não precisa ler cabeçalhos de pacote ou analisar o fluxo durante a reprodução, além de ler o cabeçalho [**WAVEFORMAT**](/windows/win32/api/mmreg/ns-mmreg-waveformat) inicial.

Para obter um exemplo mais avançado de uma fonte de mídia, consulte o [exemplo MPEG1Source](mpeg1source-sample.md).

## <a name="apis-demonstrated"></a>APIs demonstradas

Este exemplo demonstra as seguintes interfaces de Media Foundation:

-   [**IMFByteStreamHandler**](/windows/desktop/api/mfidl/nn-mfidl-imfbytestreamhandler)
-   [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource)
-   [**IMFMediaStream**](/windows/desktop/api/mfidl/nn-mfidl-imfmediastream)

## <a name="usage"></a>Uso

O exemplo WavSource cria uma DLL que é um servidor COM para o manipulador de fluxo de bytes de origem de mídia e de mídia. Antes de usar a origem de mídia, você deve registrar a DLL.

Para usar a origem de mídia, você pode executar o [BasicPlayback](/previous-versions//bb970475(v=vs.85)). O resolvedor de origem carregará automaticamente a origem de mídia se você selecionar um arquivo. wav para reprodução. (Se ocorrer um erro, verifique se você registrou com êxito a DLL WavSource.)

Você também pode usar a ferramenta TopoEdit para criar uma topologia de reprodução que contenha a origem da mídia. Para obter mais informações sobre TopoEdit, consulte [TopoEdit](topoedit.md).

## <a name="requirements"></a>Requisitos



| Produto                                                        | Versão   |
|----------------------------------------------------------------|-----------|
| [SDK do Windows](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | Windows 7 |



 

## <a name="downloading-the-sample"></a>Baixando o exemplo

Este exemplo está disponível no [repositório GitHub de exemplos clássicos do Windows](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/wavsource).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Exemplos de SDK do Media Foundation](media-foundation-sdk-samples.md)
</dt> <dt>

[Fontes de mídia](media-sources.md)
</dt> <dt>

[Exemplo de MPEG1Source](mpeg1source-sample.md)
</dt> <dt>

[Manipuladores de esquema e manipuladores de Byte-Stream](scheme-handlers-and-byte-stream-handlers.md)
</dt> <dt>

[Gravando uma fonte de mídia personalizada](writing-a-custom-media-source.md)
</dt> </dl>

 

 
