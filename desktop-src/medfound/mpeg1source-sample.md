---
description: Exemplo de MPEG1Source
ms.assetid: c9f131ff-0b79-487c-9a46-a9b1350553a1
title: Exemplo de MPEG1Source
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c71bd541a7bd01621ca7359eb9e229a08e91a04
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105748948"
---
# <a name="mpeg1source-sample"></a>Exemplo de MPEG1Source

Mostra como gravar uma fonte de mídia personalizada no Microsoft Media Foundation. O exemplo implementa uma fonte de mídia que analisa os fluxos de camada de sistemas MPEG-1 e gera exemplos que contêm cargas MPEG-1.

## <a name="apis-demonstrated"></a>APIs demonstradas

Este exemplo demonstra as seguintes interfaces de Media Foundation:

-   [**IMFByteStreamHandler**](/windows/desktop/api/mfidl/nn-mfidl-imfbytestreamhandler)
-   [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource)
-   [**IMFMediaStream**](/windows/desktop/api/mfidl/nn-mfidl-imfmediastream)

Antes de examinar este exemplo, talvez você queira examinar o [exemplo WavSource](wavsource-sample.md), que fornece uma implementação mais simples de uma fonte de mídia. O exemplo MPEG1Source adiciona alguns recursos que seriam encontrados na maioria das implementações do mundo real de uma fonte de mídia:

-   Vários fluxos
-   Métodos assíncronos
-   E/s assíncrona

No SDK do Windows para o Windows Server 2008, este exemplo também inclui um decodificador de vídeo MPEG-1 de exemplo que exibe o código de tempo para cada quadro de vídeo. (Na verdade, ele não decodifica o fragmentado MPEG-1.)

A partir do SDK do Windows para o Windows 7, o decodificador foi movido para um exemplo separado. Consulte o [exemplo de decodificador](decoder-sample.md).

## <a name="usage"></a>Uso

O exemplo MPEG1Source cria uma DLL que é um servidor COM para a origem de mídia, o manipulador de fluxo de bytes de origem de mídia e o MFT do decodificador. Antes de usar a origem de mídia, você deve registrar a DLL.

Para usar a origem de mídia, você pode executar o [exemplo BasicPlayback](/previous-versions//bb970475(v=vs.85)). O resolvedor de origem carregará automaticamente a origem de mídia se você selecionar um arquivo MPEG-1 para reprodução. (Se ocorrer um erro, verifique se você registrou com êxito a DLL MPEG1Source.)

Você também pode usar a ferramenta TopoEdit para criar uma topologia de reprodução que contenha a origem da mídia. Para obter mais informações sobre TopoEdit, consulte [TopoEdit](topoedit.md).

## <a name="requirements"></a>Requisitos



| Produto                                                        | Versão   |
|----------------------------------------------------------------|-----------|
| [SDK do Windows](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | Windows 7 |



 

## <a name="downloading-the-sample"></a>Baixando o exemplo

Este exemplo está disponível no [repositório GitHub de exemplos clássicos do Windows](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/mpeg1source).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Exemplos de SDK do Media Foundation](media-foundation-sdk-samples.md)
</dt> <dt>

[Fontes de mídia](media-sources.md)
</dt> <dt>

[Manipuladores de esquema e manipuladores de Byte-Stream](scheme-handlers-and-byte-stream-handlers.md)
</dt> <dt>

[Tutorial: escrevendo uma fonte de mídia personalizada](tutorial--writing-a-custom-media-source.md)
</dt> <dt>

[Exemplo de WavSource](wavsource-sample.md)
</dt> </dl>

 

 
