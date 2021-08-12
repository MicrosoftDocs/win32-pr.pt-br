---
description: usando o Mixer de sobreposição na captura de vídeo
ms.assetid: 43468fa2-6dea-439d-9e24-f47a053ad561
title: usando o Mixer de sobreposição na captura de vídeo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 134ada11ca55009b3ad67ba80c82575ab2d9bdf5a7329a88157ed4e003eca74c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118651190"
---
# <a name="using-the-overlay-mixer-in-video-capture"></a>usando o Mixer de sobreposição na captura de vídeo

Há certos tipos de vídeo que o filtro de [processador de vídeo](video-renderer-filter.md) não pode exibir por si só. nessas situações, o processador de vídeo deve funcionar com a [sobreposição Mixer](overlay-mixer-filter.md) filtro. a sobreposição Mixer gerencia a renderização, enquanto o renderizador de vídeo gerencia a janela de vídeo. o Mixer de sobreposição é necessário nas seguintes situações:

-   Pins da porta de vídeo (VP). se o dispositivo de captura usar uma porta de vídeo, a sobreposição Mixer gerenciará a sobreposição de hardware.
-   Vídeo entrelaçado. Para vídeo entrelaçado, o decodificador requer um formato [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) , ao qual o processador de vídeo não dá suporte.
-   Legendas ocultas. o texto da legenda é renderizado como bitmaps de 8 bits por pixel, que a sobreposição Mixer sobreposição no vídeo.

o método **RenderStream** do construtor de Graph de captura insere a sobreposição Mixer sempre que necessário. se você estiver criando o grafo sem usar o construtor de Graph de captura, no entanto, deverá verificar cada uma dessas situações e inserir a sobreposição Mixer você mesmo.

-   \[! Fundamental\]  
    > se o dispositivo tiver um VP de pin, você deverá conectar a sobreposição Mixer mesmo que não precise de funcionalidade de visualização em seu aplicativo. com uma porta de vídeo, o dispositivo de captura sempre envia os dados de vídeo para a sobreposição de hardware, de modo que a sobreposição Mixer sempre é necessária.

     

Os filtros de processador de mixagem de vídeo (VMR-7 e VMR-9) dão suporte a vídeo entrelaçado e são capazes de misturar bitmaps de legenda oculta no vídeo primário. Se você estiver usando o VMR para esses cenários, não precisará usar a Mixer de sobreposição. O VMR-9 não oferece suporte a conexões de VP de PIN. O VMR-7 dá suporte a conexões de VP de PIN por meio do filtro do Gerenciador de porta de vídeo. No entanto, você pode descobrir que alguns drivers não funcionam corretamente com o Gerenciador de porta de vídeo. por esse motivo, a sobreposição Mixer ainda é recomendada para VP de pinos.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Tópicos de captura avançada](advanced-capture-topics.md)
</dt> <dt>

[Pins de porta de vídeo](video-port-pins.md)
</dt> <dt>

[Tipo de formato VideoInfo2](videoinfo2-format-type.md)
</dt> </dl>

 

 



