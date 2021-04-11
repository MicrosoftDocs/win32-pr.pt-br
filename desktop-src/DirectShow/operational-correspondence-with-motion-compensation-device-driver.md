---
description: Correspondência operacional com o driver de dispositivo de compensação de movimento
ms.assetid: bd92a0f4-98d9-497a-99b9-0cf432347daf
title: Correspondência operacional com o driver de dispositivo de compensação de movimento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5cca960ed8cbdae212bbe5e9f3b25316125a7456
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104163745"
---
# <a name="operational-correspondence-with-motion-compensation-device-driver"></a>Correspondência operacional com o driver de dispositivo de compensação de movimento

Esta seção contém uma descrição do lado do driver de dispositivo de compensação de movimento da interface do DirectX VA. (Referência: Windows 2000 DDK-drivers gráficos-guia de design-3,0 DirectDraw DDI-3,12 compensação de movimento. Consulte o Windows DDK para obter a documentação sobre as estruturas em negrito.)

Os itens a seguir se referem a entradas acessadas por meio da estrutura **DD \_ MOTIONCOMPCALLBACKS** :

1.  No início do processamento relevante, o **DdMoCompCreate** do driver de dispositivo é usado para notificar o driver de que o decodificador de software começará a usar um objeto de aceleração de vídeo.
2.  GUIDs recebidos de [**IAMVideoAccelerator:: GetVideoAcceleratorGUIDs**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-getvideoacceleratorguids) originam-se do **DdMoCompGetGUIDs** do driver do dispositivo.
3.  Uma chamada para o [**IAMVideoAccelerator:: GetUncompFormatsSupported**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-getuncompformatssupported) do pino de entrada downstream retorna dados do **DdMoCompGetFormats** do driver do dispositivo.
4.  A \_ estrutura de dados DXVA ConnectMode do [**IAMVideoAcceleratorNotify:: GetCreateVideoAcceleratorData**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoacceleratornotify-getcreatevideoacceleratordata) do decodificador é passada para o **DdMoCompCreate** do driver do dispositivo.
5.  Os dados retornados de [**IAMVideoAccelerator:: GetCompBufferInfo**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-getcompbufferinfo) são provenientes do **DdMoCompGetBuffInfo** do driver do dispositivo.
6.  Os buffers enviados usando [**IAMVideoAccelerator:: execute**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-execute) são recebidos pelo **DdMoCompRender** do driver do dispositivo.
7.  O uso de [**IAMVideoAccelerator:: QueryRenderStatus**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-queryrenderstatus) invoca o **DdMoCompQueryStatus** do driver do dispositivo. Um código de retorno de DDERR \_ WASSTILLDRAWING de DdMoCompQueryStatus será visto pelo decodificador de host como um código de retorno de E \_ pendente de **IAMVideoAccelerator:: QueryRenderStatus**.
8.  Os dados enviados para [**IAMVideoAccelerator:: BeginFrame**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-beginframe) são recebidos pelo **DdMoCompBeginFrame** do driver do dispositivo. Um código de retorno de E \_ pendente é necessário de DdMoCompBeginFrame para que E \_ pendente seja visto pelo decodificador do host em resposta a **IAMVideoAccelerator:: BeginFrame**.
9.  Os dados enviados para [**IAMVideoAccelerator:: endframe**](/previous-versions/windows/desktop/api/videoacc/nf-videoacc-iamvideoaccelerator-endframe) são recebidos pelo **DdMoCompEndFrame** do driver de dispositivo.
10. No final do processamento relevante, o **DdMoCompDestroy** do driver de dispositivo é usado para notificar o driver de que o objeto de aceleração de vídeo atual não será mais usado, para que o driver possa executar qualquer limpeza necessária.

 

 



