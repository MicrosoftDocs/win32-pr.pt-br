---
description: Capturar atributos de dispositivo
ms.assetid: dd24671a-0689-4490-8d18-2a33ed461e9d
title: Capturar atributos de dispositivo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43dd8dbcdf0a441ddb8a5ef2794526e961c22033
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105797493"
---
# <a name="capture-device-attributes"></a>Capturar atributos de dispositivo

Os seguintes atributos estão relacionados a dispositivos de captura:



| Atributo                                                                                                                     | Descrição                                                                         |
|-------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| [\_ \_ nome amigável do atributo MF DEVSOURCE \_ \_](mf-devsource-attribute-friendly-name.md)                                          | O nome de exibição do dispositivo.                                                          |
| [\_tipo de \_ mídia de atributo MF DEVSOURCE \_ \_](mf-devsource-attribute-media-type.md)                                                | O formato de saída do dispositivo.                                                         |
| [\_tipo de \_ origem do atributo MF DEVSOURCE \_ \_](mf-devsource-attribute-source-type.md)                                              | O tipo de dispositivo, como captura de áudio ou captura de vídeo.                         |
| [\_tipo de origem do atributo MF DEVSOURCE \_ \_ \_ \_ AUDCAP \_ ID do ponto de extremidade \_](mf-devsource-attribute-source-type-audcap-endpoint-id.md)     | A ID do ponto de extremidade para um dispositivo de captura de áudio.                                        |
| [\_tipo de origem do atributo MF DEVSOURCE \_ \_ \_ \_ AUDCAP \_ role](mf-devsource-attribute-source-type-audcap-role.md)                    | A função de dispositivo para um dispositivo de captura de áudio.                                        |
| [\_tipo de origem do atributo MF DEVSOURCE \_ \_ \_ \_ VIDCAP \_ categoria](mf-devsource-attribute-source-type-vidcap-category.md)            | A categoria de dispositivo para um dispositivo de vídeo.                                             |
| [\_tipo de fonte de atributo MF DEVSOURCE \_ \_ \_ \_ VIDCAP \_ \_ fonte HW](mf-devsource-attribute-source-type-vidcap-hw-source.md)         | Especifica se uma fonte de captura de vídeo é um dispositivo de hardware ou um dispositivo de software. |
| [\_tipo de fonte de atributo MF DEVSOURCE \_ \_ \_ \_ VIDCAP \_ Max \_ buffers](mf-devsource-attribute-source-type-vidcap-max-buffers.md)     | Especifica o número máximo de quadros que a fonte de captura de vídeo armazenará em buffer.   |
| [\_tipo de origem do atributo MF DEVSOURCE \_ \_ \_ \_ VIDCAP \_ \_ link simbólico](mf-devsource-attribute-source-type-vidcap-symbolic-link.md) | O link simbólico para um driver de captura de vídeo.                                       |
| [\_ \_ Carimbo de data/hora do HW \_ de MFT com \_ \_ atributo QPC](mft-hw-timestamp-with-qpc-attribute.md)                                           | Especifica se a origem do dispositivo usa a hora do sistema para carimbos de data/hora.           |



 

Esses atributos são usados com as seguintes funções:

-   [**MFCreateDeviceSource**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesource)
-   [**MFCreateDeviceSourceActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatedevicesourceactivate)
-   [**MFEnumDeviceSources**](/windows/desktop/api/mfidl/nf-mfidl-mfenumdevicesources)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Atributos de Media Foundation](media-foundation-attributes.md)
</dt> </dl>

 

 



