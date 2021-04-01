---
description: Solicitações de status OPM
ms.assetid: 428d08c6-e9f0-49fb-9ef9-d0f95416669d
title: Solicitações de status OPM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd994d7cb8d43db23fe59352dba830e741b74b98
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103661485"
---
# <a name="opm-status-requests"></a>Solicitações de status OPM

Esta seção lista as solicitações de status disponíveis para o [Gerenciador de proteção de saída](output-protection-manager.md) (OPM). Para enviar uma solicitação de status OPM, chame [**IOPMVideoOutput:: GetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation). Para cada solicitação, as informações a seguir são listadas.



|              |                                                                                                                                                            |
|--------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| GUID de solicitação | Identifica a solicitação. Defina o membro **guidSetting** da estrutura [**de \_ \_ \_ parâmetros obter informações de OPM**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_get_info_parameters) igual a esse valor. |
| Dados de entrada   | Especifica como interpretar a matriz **abParameters** na estrutura de [**\_ parâmetros obter \_ informações \_ de OPM**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_get_info_parameters) .                      |
| Dados de saída  | Especifica como interpretar a matriz **abRequestedInformation** na estrutura de [**\_ \_ informações de OPM solicitado**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_requested_information) .         |



 

As seguintes solicitações de status são definidas:



| Solicitação de status                                                                                      | Descrição                                                                                                                                           |
|-----------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**os OPM \_ Get \_ ACP \_ e \_ CGMSA \_ Signaling**](opm-get-acp-and-cgmsa-signaling.md)                     | Retorna as seguintes informações sobre uma saída de vídeo:                                                                                               |
| [**formato de saída de OPM de \_ obtenção \_ real \_ \_**](opm-get-actual-output-format.md)                            | Retorna uma descrição do sinal de vídeo que está sendo transmitido pelo conector.                                                               |
| [**nível de proteção do OPM \_ obter \_ real \_ \_**](opm-get-actual-protection-level.md)                      | Retorna o nível de proteção global para um mecanismo de proteção especificado.                                                                             |
| [**\_tipo de \_ barramento de adaptador de obtenção de OPM \_ \_**](opm-get-adapter-bus-type.md)                                    | Retorna o tipo de barramento de e/s usado pela saída de vídeo.                                                                                                 |
| [**\_informações do \_ codec de obtenção de OPM \_**](opm-get-codec-info.md)                                                 | Obtém o valor de mérito de um codec de hardware.                                                                                                             |
| [**\_informações de \_ dispositivo de HDCP de conexão \_ \_ de OPM \_**](opm-get-connected-hdcp-device-information.md) | Obtém informações sobre um dispositivo de Proteção de Conteúdo High-Bandwidth digital (HDCP) anexado à saída de vídeo. As seguintes informações são retornadas: |
| [**\_tipo de \_ conector de obtenção de OPM \_**](opm-get-connector-type.md)                                         | Retorna o tipo de conector físico da saída de vídeo.                                                                                              |
| [**OPM \_ obter \_ versão atual do \_ SRM de HDCP \_ \_**](opm-get-current-hdcp-srm-version.md)                   | Retorna o número de versão da mensagem de renovação do sistema (SRM) usada atualmente pela saída de vídeo.                                               |
| [**OPM \_ obter \_ características de DVI \_**](opm-get-dvi-characteristics.md)                               | Consulta se um conector DVI (Digital Video interface) dá suporte a DVI versão 1,1 ou posterior.                                                          |
| [**\_ID de \_ saída de obtenção de OPM \_**](opm-get-output-id.md)                                                   | Retorna o identificador exclusivo do monitor associado a esta saída de vídeo.                                                                       |
| [**os \_ tipos de proteção de OPM \_ têm suporte \_ \_**](opm-get-supported-protection-types.md)                | Retorna a lista de mecanismos de proteção aos quais o conector dá suporte.                                                                        |
| [**OPM \_ obter \_ \_ nível de proteção virtual \_**](opm-get-virtual-protection-level.md)                    | Retorna o nível de proteção virtual para um mecanismo de proteção especificado.                                                                            |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência de programação de OPM](opm-programming-reference.md)
</dt> <dt>

[Gerenciador de proteção de saída](output-protection-manager.md)
</dt> </dl>

 

 



