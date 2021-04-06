---
description: Usando o mixer de sobreposição na captura de vídeo
ms.assetid: 43468fa2-6dea-439d-9e24-f47a053ad561
title: Usando o mixer de sobreposição na captura de vídeo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72bff115d566654732e80c0bcb0f554c4ad96e65
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011319"
---
# <a name="using-the-overlay-mixer-in-video-capture"></a>Usando o mixer de sobreposição na captura de vídeo

Há certos tipos de vídeo que o filtro de [processador de vídeo](video-renderer-filter.md) não pode exibir por si só. Nessas situações, o processador de vídeo deve funcionar com o filtro de [mixer de sobreposição](overlay-mixer-filter.md) . O mixer de sobreposição gerencia a renderização, enquanto o renderizador de vídeo gerencia a janela de vídeo. O mixer de sobreposição é necessário nas seguintes situações:

-   Pins da porta de vídeo (VP). Se o dispositivo de captura usar uma porta de vídeo, o mixer de sobreposição gerenciará a sobreposição de hardware.
-   Vídeo entrelaçado. Para vídeo entrelaçado, o decodificador requer um formato [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) , ao qual o processador de vídeo não dá suporte.
-   Legendas ocultas. O texto da legenda é renderizado como bitmaps de 8 bits por pixel, que o mixer de sobreposição sobrepõem no vídeo.

O método **RenderStream** do construtor do grafo de captura insere o mixer de sobreposição sempre que necessário. Se você estiver criando o grafo sem usar o construtor de grafo de captura, no entanto, deverá verificar cada uma dessas situações e inserir o mixer de sobreposição por conta própria.

-   \[! Fundamental\]  
    > Se o dispositivo tiver um VP de PIN, você deverá conectar o mixer de sobreposição mesmo se não precisar da funcionalidade de visualização em seu aplicativo. Com uma porta de vídeo, o dispositivo de captura sempre envia os dados de vídeo para a sobreposição de hardware, portanto, o mixer de sobreposição é sempre necessário.

     

Os filtros de processador de mixagem de vídeo (VMR-7 e VMR-9) dão suporte a vídeo entrelaçado e são capazes de misturar bitmaps de legenda oculta no vídeo primário. Se você estiver usando o VMR para esses cenários, não será necessário usar o mixer de sobreposição. O VMR-9 não oferece suporte a conexões de VP de PIN. O VMR-7 dá suporte a conexões de VP de PIN por meio do filtro do Gerenciador de porta de vídeo. No entanto, você pode descobrir que alguns drivers não funcionam corretamente com o Gerenciador de porta de vídeo. Por esse motivo, o mixer de sobreposição ainda é recomendado para VP de pinos.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Tópicos de captura avançada](advanced-capture-topics.md)
</dt> <dt>

[Pins de porta de vídeo](video-port-pins.md)
</dt> <dt>

[Tipo de formato VideoInfo2](videoinfo2-format-type.md)
</dt> </dl>

 

 



