---
description: Tipo de formato VideoInfo2
ms.assetid: edd2013a-f0c5-4176-ba3a-a3af719ce31d
title: Tipo de formato VideoInfo2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74b0f435e0e2a1b5b1d948c42a881f19300a9c6f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105789823"
---
# <a name="videoinfo2-format-type"></a>Tipo de formato VideoInfo2

O tipo de mídia preferencial de um PIN de visualização pode ser um tipo com um formato [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) . Essa estrutura de formato dá suporte a recursos especiais, como taxas de proporção de vídeo e imagem entrelaçadas.

O VMR-7 e o VMR-9 dão suporte ao [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) diretamente. Quando você conectar o VMR ao decodificador, ele negociará o melhor formato. No entanto, o filtro de processamento de vídeo mais antigo não oferece suporte a **VIDEOINFOHEADER2**. Para usar os tipos de formato **VIDEOINFOHEADER2** com o filtro de processador de vídeo, você deve inserir o filtro de [mixer de sobreposição](overlay-mixer-filter.md) no grafo.

1.  Enumere os tipos de mídia preferenciais no pino de saída do filtro de decodificador, usando o método [**IPin:: EnumMediaTypes**](/windows/desktop/api/Strmif/nf-strmif-ipin-enummediatypes) .
2.  Verifique o primeiro tipo de mídia na sequência de enumeração.
3.  Se o tipo de formato for **Format \_ VideoInfo2**, conecte o pino de saída ao mixer de sobreposição. Em seguida, conecte o mixer de sobreposição ao processador de vídeo. (Consulte [Pins de porta de vídeo](video-port-pins.md).)

Se você não se preocupa com esses recursos, não precisa usar o mixer de sobreposição. Conecte o decodificador diretamente ao processador de vídeo e ele se conectará com um formato [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) .

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Tópicos de captura avançada](advanced-capture-topics.md)
</dt> <dt>

[Usando o mixer de sobreposição na captura de vídeo](using-the-overlay-mixer-in-video-capture.md)
</dt> </dl>

 

 



