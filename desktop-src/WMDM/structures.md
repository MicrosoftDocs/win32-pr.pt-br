---
title: Estruturas WMDM
description: este artigo inclui artigos de referência sobre estruturas definidas por Windows Gerenciador de Dispositivos de mídia, como _BITMAPINFOHEADER e MTP_COMMAND_DATA_IN.
ms.assetid: 3068359f-5ac0-41e0-a09b-283b439527a0
keywords:
- Windows Gerenciador de Dispositivos de mídia, estruturas
- Gerenciador de Dispositivos, estruturas
- referência de programação, estruturas
- referência para Windows Gerenciador de Dispositivos de mídia, estruturas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5fd0048a7cf3b87f09bb46ef6f6db74531b4b67a7364acd28099feed04bb8dec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119865536"
---
# <a name="wmdm-structures"></a>Estruturas WMDM

Windows Gerenciador de Dispositivos de mídia define as estruturas a seguir.



| Estrutura                                                   | Descrição                                                                                                                                                                                                                                              |
|-------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_BITMAPINFOHEADER**](-bitmapinfoheader.md)             | Define o formato do quadro de vídeo.                                                                                                                                                                                                                       |
| [**\_ \_ dados de comando MTP \_ em**](/windows/desktop/api/MtpExt/ns-mtpext-mtp_command_data_in)       | Contém os comandos personalizados do MTP (protocolo de transporte de mídia) que são enviados para o dispositivo usando o método [**IWMDMDevice3::D eviceiocontrol**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-deviceiocontrol) .                                                                           |
| [**\_saída de \_ dados de comando MTP \_**](/windows/desktop/api/MtpExt/ns-mtpext-mtp_command_data_out)     | Contém as respostas de MTP (protocolo de transporte de mídia) que são preenchidas pelo driver de dispositivo.                                                                                                                                                                  |
| [**OPAQUECOMMAND**](opaquecommand.md)                      | contém dados para comandos que são transmitidos por meio de Windows Gerenciador de Dispositivos de mídia para um dispositivo, mas que não devem ser afetados por Windows Gerenciador de Dispositivos de mídia.                                                                                       |
| [**\_VIDEOINFOHEADER**](-videoinfoheader.md)               | Define o formato de um fluxo de vídeo.                                                                                                                                                                                                                    |
| [**\_WAVEFORMATEX**](-waveformatex.md)                     | Define o formato dos dados de Wave-Audio.                                                                                                                                                                                                               |
| [**\_funcionalidade de formato WMDM \_**](wmdm-format-capability.md)  | Descreve os recursos de um dispositivo para um formato específico. Essa estrutura contém um conjunto de configurações de propriedade em uma matriz de estruturas de [**\_ \_ configuração de prop do WMDM**](wmdm-prop-config.md) .                                                       |
| [**\_configuração de prop do WMDM \_**](wmdm-prop-config.md)              | Descreve um conjunto de valores de propriedade compatíveis em todas as propriedades com suporte pelo dispositivo para um formato específico. Essa estrutura contém várias descrições de propriedade em uma matriz de estruturas [**\_ \_ desc prop do WMDM**](wmdm-prop-desc.md) . |
| [**WMDM \_ prop \_ desc**](wmdm-prop-desc.md)                  | Descreve os valores válidos de uma propriedade em uma configuração de propriedade específica.                                                                                                                                                                             |
| [**\_enumeração de \_ valores de prop do WMDM \_**](wmdm-prop-values-enum.md)   | Contém um conjunto enumerado de valores válidos para uma propriedade específica em uma configuração de propriedade específica.                                                                                                                                             |
| [**\_intervalo de \_ valores de prop do WMDM \_**](wmdm-prop-values-range.md) | Descreve o intervalo de valores válidos para uma propriedade específica em uma configuração de propriedade específica.                                                                                                                                                        |
| [**WMDMDATETIME**](wmdmdatetime.md)                        | Contém uma data e hora.                                                                                                                                                                                                                                |
| [**WMDMID**](wmdmid.md)                                    | Descreve os números de série e as IDs de grupo.                                                                                                                                                                                                                  |
| [**WMDMMetadataView**](wmdmmetadataview.md)                | Define a exibição de metadados.                                                                                                                                                                                                                               |
| [**WMDMRIGHTS**](wmdmrights.md)                            | Descreve os direitos de uso de conteúdo.                                                                                                                                                                                                                            |
| [**WMFILECAPABILITIES**](wmfilecapabilities.md)            | Descreve um tipo MIME.                                                                                                                                                                                                                                   |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Referência de programação**](programming-reference.md)
</dt> </dl>

 

 




