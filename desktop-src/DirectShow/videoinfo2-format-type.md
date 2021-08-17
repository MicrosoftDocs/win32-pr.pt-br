---
description: Tipo de formato VideoInfo2
ms.assetid: edd2013a-f0c5-4176-ba3a-a3af719ce31d
title: Tipo de formato VideoInfo2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a820ea6a53c457d2d000be8b4c0e8966213c1aeeb2b5f55a780c4801a4182907
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119071920"
---
# <a name="videoinfo2-format-type"></a>Tipo de formato VideoInfo2

O tipo de mídia preferencial de um pino de visualização pode ser um tipo com um [**formato VIDEOINFOHEADER2.**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) Essa estrutura de formato dá suporte a recursos especiais, como taxas de proporção de vídeo e imagem entrelaçadas.

A VMR-7 e a VMR-9 são suportadas [**diretamente por VIDEOINFOHEADER2.**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) Quando você conectar a VMR ao decodificador, ela negociará o melhor formato. No entanto, o filtro mais antigo do Video Renderer não dá **suporte a VIDEOINFOHEADER2.** Para usar **tipos de formato VIDEOINFOHEADER2** com o filtro Do renderador de vídeo, você deve inserir o filtro sobreposição [Mixer](overlay-mixer-filter.md) no grafo.

1.  Enumerar os tipos de mídia preferenciais no pino de saída do filtro de decodificador usando o [**método IPin::EnumMediaTypes.**](/windows/desktop/api/Strmif/nf-strmif-ipin-enummediatypes)
2.  Verifique o primeiro tipo de mídia na sequência de enumeração.
3.  Se o tipo de formato **for FORMAT \_ VideoInfo2**, conecte o pino de saída à Mixer. Em seguida, conecte o Mixer sobreposição ao renderador de vídeo. (Consulte [Pinos de porta de vídeo](video-port-pins.md).)

Se você não se importa com esses recursos, não precisa usar o controle sobreposição Mixer. Conexão decodificador diretamente ao Renderador de Vídeo e ele se conectará com um [**formato VIDEOINFOHEADER.**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Tópicos de captura avançada](advanced-capture-topics.md)
</dt> <dt>

[Usando a camada de Mixer na Captura de Vídeo](using-the-overlay-mixer-in-video-capture.md)
</dt> </dl>

 

 



