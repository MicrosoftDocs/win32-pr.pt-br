---
description: Os seguintes identificadores globalmente exclusivos (GUIDs) definem tipos de nó para filtros do modo kernel. Para localizar o tipo de nó, consulte o filtro para a interface IKsTopologyInfo.
ms.assetid: 0e133ce3-8815-47d1-a5c3-577a98963912
title: Tipos de nó KS (Ksmedia. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- KSNODETYPE_DEV_SPECIFIC
- KSNODETYPE_VIDEO_CAMERA_TERMINAL
- KSNODETYPE_VIDEO_INPUT_MTT
- KSNODETYPE_VIDEO_INPUT_TERMINAL
- KSNODETYPE_VIDEO_OUTPUT_MTT
- KSNODETYPE_VIDEO_OUTPUT_TERMINAL
- KSNODETYPE_VIDEO_PROCESSING
- KSNODETYPE_VIDEO_SELECTOR
- KSNODETYPE_VIDEO_STREAMING
api_type:
- HeaderDef
api_location:
- Ksmedia.h
ms.openlocfilehash: eadae4fdd70fd80115ea4e8902ba1bb2aa7bf53b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105810390"
---
# <a name="ks-node-types"></a>Tipos de nó KS

Os seguintes identificadores globalmente exclusivos (GUIDs) definem tipos de nó para filtros do modo kernel. Para localizar o tipo de nó, consulte o filtro para a interface [**IKsTopologyInfo**](/previous-versions/windows/desktop/api/Vidcap/nn-vidcap-ikstopologyinfo) .



| GUID                                                                                                                                                                                                                     | Descrição                                                                                                                                                                                                                                                                                              |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="KSNODETYPE_DEV_SPECIFIC"></span><span id="ksnodetype_dev_specific"></span><dl> <dt>**KSNODETYPE \_ desenvolvimento \_ específico**</dt> </dl>                             | Representa uma ou mais funções de processamento específicas do dispositivo. O nó tem uma conexão de entrada e uma conexão de saída.<br/> O nó pode expor uma interface COM personalizada por meio de um plug-in KsProxy, se fornecido pelo fabricante do dispositivo.<br/>                                            |
| <span id="KSNODETYPE_VIDEO_CAMERA_TERMINAL"></span><span id="ksnodetype_video_camera_terminal"></span><dl> <dt>**\_terminal de \_ câmera de vídeo KSNODETYPE \_**</dt> </dl> | Representa os dados que estão sendo movidos para o dispositivo de um sensor de câmera, independentemente do barramento USB. O nó tem uma conexão de saída.<br/> O nó expõe as interfaces [**IAMCameraControl**](/windows/desktop/api/Strmif/nn-strmif-iamcameracontrol) e [**ICameraControl**](/previous-versions/windows/desktop/api/Vidcap/nn-vidcap-icameracontrol) para controlar a câmera.<br/> |
| <span id="KSNODETYPE_VIDEO_INPUT_MTT"></span><span id="ksnodetype_video_input_mtt"></span><dl> <dt>**\_MTT de \_ entrada de vídeo KSNODETYPE \_**</dt> </dl>                   | Representa os dados que são movidos para o dispositivo de um transporte de mídia sequencial, como uma fita VTR, independente do barramento USB. O nó tem uma conexão de saída.<br/> O nó expõe a interface [**IAMExtTransport**](/windows/desktop/api/Strmif/nn-strmif-iamexttransport) para controlar o mecanismo de transporte.<br/>   |
| <span id="KSNODETYPE_VIDEO_INPUT_TERMINAL"></span><span id="ksnodetype_video_input_terminal"></span><dl> <dt>**\_terminal de \_ entrada de vídeo KSNODETYPE \_**</dt> </dl>    | Representa os dados que estão sendo movidos para o dispositivo, independentemente do barramento USB. Por exemplo, esse nó pode representar uma tomada de áudio analógica ou um conector de S/PDIF. O nó tem uma conexão de saída.<br/>                                                                                                             |
| <span id="KSNODETYPE_VIDEO_OUTPUT_MTT"></span><span id="ksnodetype_video_output_mtt"></span><dl> <dt>**\_MTT de \_ saída de vídeo KSNODETYPE \_**</dt> </dl>                | Representa os dados que se movem do dispositivo para um transporte de mídia sequencial, como uma fita VTR, independentemente do barramento USB. O nó tem uma conexão de entrada.<br/> O nó expõe a interface [**IAMExtTransport**](/windows/desktop/api/Strmif/nn-strmif-iamexttransport) para controlar o mecanismo de transporte.<br/>      |
| <span id="KSNODETYPE_VIDEO_OUTPUT_TERMINAL"></span><span id="ksnodetype_video_output_terminal"></span><dl> <dt>**\_terminal de \_ saída de vídeo KSNODETYPE \_**</dt> </dl> | Representa os dados que se movem do dispositivo, independentemente do barramento USB. Por exemplo, esse nó pode representar uma tomada de áudio analógica ou um conector de S/PDIF. O nó tem uma conexão de entrada.<br/>                                                                                                              |
| <span id="KSNODETYPE_VIDEO_PROCESSING"></span><span id="ksnodetype_video_processing"></span><dl> <dt>**\_processamento de vídeo KSNODETYPE \_**</dt> </dl>                 | Representa uma ou mais funções de processamento de vídeo. O nó tem uma conexão de entrada e uma conexão de saída.<br/> O nó expõe as interfaces [**IAMVideoProcAmp**](/windows/desktop/api/Strmif/nn-strmif-iamvideoprocamp) e [**IVideoProcAmp**](/previous-versions/windows/desktop/api/Vidcap/nn-vidcap-ivideoprocamp) para ajustar as qualidades do sinal de vídeo.<br/> |
| <span id="KSNODETYPE_VIDEO_SELECTOR"></span><span id="ksnodetype_video_selector"></span><dl> <dt>**\_seletor de vídeo KSNODETYPE \_**</dt> </dl>                       | Representa um mecanismo para selecionar o caminho de entrada de duas ou mais fontes possíveis. O nó tem duas ou mais conexões de entrada e uma conexão de saída.<br/> O nó expõe a interface [**iseleger**](/previous-versions/windows/desktop/api/Vidcap/nn-vidcap-iselector) para selecionar entre entradas.<br/>                               |
| <span id="KSNODETYPE_VIDEO_STREAMING"></span><span id="ksnodetype_video_streaming"></span><dl> <dt>**\_streaming de vídeo KSNODETYPE \_**</dt> </dl>                    | Representa a movimentação de dados entre o host e o dispositivo. Para dispositivos UVC, esse nó representa um ponto de extremidade USB. Os pontos de extremidade de entrada têm uma conexão de entrada; os pontos de extremidade de saída têm uma conexão de saída.<br/>                                                                                         |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|--------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Ksmedia. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Constantes e GUIDs](constants-and-guids.md)
</dt> </dl>

 

 




