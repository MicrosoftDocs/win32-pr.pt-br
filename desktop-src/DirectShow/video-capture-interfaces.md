---
description: Interfaces de captura de vídeo
ms.assetid: a7ec6607-d6fe-4cf4-b3f2-8636c4d15982
title: Interfaces de captura de vídeo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bfee9807a94f381fef3a294dcd405de6fe8b67fafef3ace562309fe5e10d2ee
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119633056"
---
# <a name="video-capture-interfaces"></a>Interfaces de captura de vídeo

essas interfaces dão suporte à captura de vídeo, usando dispositivos WDM (microsoft® Windows® Driver Model) ou microsoft® video herdado para dispositivos Windows® (VFW).



| Interface                                                        | Descrição                                                                                                  |
|------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| [**IAMAnalogVideoDecoder**](/windows/desktop/api/Strmif/nn-strmif-iamanalogvideodecoder)           | Controle a digitalização de vídeo em uma placa de captura de vídeo WDM.                                                      |
| [**IAMBufferNegotiation**](/windows/desktop/api/Strmif/nn-strmif-iambuffernegotiation)             | Controle como um PIN aloca buffers.                                                                         |
| [**IAMCopyCaptureFileProgress**](/windows/desktop/api/Strmif/nn-strmif-iamcopycapturefileprogress) | Interface de retorno de chamada para receber o progresso de uma operação de cópia de arquivo.                                         |
| [**IAMCrossbar**](/windows/desktop/api/Strmif/nn-strmif-iamcrossbar)                               | Crie uma conexão de hardware entre uma fonte de áudio ou vídeo WDM e um dispositivo de captura WDM.                   |
| [**IAMDroppedFrames**](/windows/desktop/api/Strmif/nn-strmif-iamdroppedframes)                     | Consulte um filtro de captura sobre o desempenho de captura.                                                            |
| [**IAMStreamControl**](/windows/desktop/api/Strmif/nn-strmif-iamstreamcontrol)                     | Controle as horas de início e de término de fluxos individuais.                                                      |
| [**IAMStreamConfig**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig)                       | Consulte e defina o formato de saída do filtro de captura.                                                            |
| [**IAMVfwCaptureDialogs**](/windows/desktop/api/Strmif/nn-strmif-iamvfwcapturedialogs)             | Exiba as caixas de diálogo fornecidas pelos drivers de captura do VFW.                                                    |
| [**IAMVideoControl**](/windows/desktop/api/Strmif/nn-strmif-iamvideocontrol)                       | Controle a imagem de um dispositivo de captura.                                                                   |
| [**IAMVideoProcAmp**](/windows/desktop/api/Strmif/nn-strmif-iamvideoprocamp)                       | Ajuste as qualidades de um sinal de vídeo, como brilho, contraste, matiz, saturação, gama e nitidez. |
| [**ICaptureGraphBuilder2**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2)           | Crie gráficos de filtro para captura de vídeo.                                                                       |
| [**IFileSinkFilter2**](/windows/desktop/api/Strmif/nn-strmif-ifilesinkfilter2)                     | Especifique o nome e os atributos de um arquivo de saída.                                                           |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Interfaces de controle de dispositivo externo](external-device-control-interfaces.md)
</dt> <dt>

[Captura de vídeo](video-capture.md)
</dt> </dl>

 

 



