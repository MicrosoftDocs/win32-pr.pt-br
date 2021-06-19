---
title: Estruturas WMDM
description: Este artigo inclui artigos de referência sobre estruturas definidas pelo Windows Media Gerenciador de Dispositivos, como _BITMAPINFOHEADER e MTP_COMMAND_DATA_IN.
ms.assetid: 3068359f-5ac0-41e0-a09b-283b439527a0
keywords:
- Gerenciador de Dispositivos de mídia do Windows, estruturas
- Gerenciador de Dispositivos, estruturas
- referência de programação, estruturas
- referência para Windows Media Gerenciador de Dispositivos, estruturas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7cc49deb3f4dd28695f5e0e7c3a871c53fa96300
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112406499"
---
# <a name="wmdm-structures"></a>Estruturas WMDM

O Windows Media Gerenciador de Dispositivos define as estruturas a seguir.



| Estrutura                                                   | Descrição                                                                                                                                                                                                                                              |
|-------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_BITMAPINFOHEADER**](-bitmapinfoheader.md)             | Define o formato do quadro de vídeo.                                                                                                                                                                                                                       |
| [**\_ \_ dados de comando MTP \_ em**](/windows/desktop/api/MtpExt/ns-mtpext-mtp_command_data_in)       | Contém os comandos personalizados do MTP (protocolo de transporte de mídia) que são enviados para o dispositivo usando o método [**IWMDMDevice3::D eviceiocontrol**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-deviceiocontrol) .                                                                           |
| [**\_saída de \_ dados de comando MTP \_**](/windows/desktop/api/MtpExt/ns-mtpext-mtp_command_data_out)     | Contém as respostas de MTP (protocolo de transporte de mídia) que são preenchidas pelo driver de dispositivo.                                                                                                                                                                  |
| [**OPAQUECOMMAND**](opaquecommand.md)                      | Contém dados para comandos que são passados pelo Windows Media Gerenciador de Dispositivos para um dispositivo, mas que não devem ser afetados pelo Windows Media Gerenciador de Dispositivos.                                                                                       |
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

 

 




