---
description: Solicitações de status do OPM
ms.assetid: 428d08c6-e9f0-49fb-9ef9-d0f95416669d
title: Solicitações de status do OPM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cdbf7338fe1309feb49fd191e3f4a1a22f3639b4
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120171"
---
# <a name="opm-status-requests"></a>Solicitações de status do OPM

Esta seção lista as solicitações de status disponíveis para o OPM (Gerenciador de Proteção de [Saída).](output-protection-manager.md) Para enviar uma solicitação de status do OPM, chame [**IOPMVideoOutput::GetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation). Para cada solicitação, as informações a seguir são listadas.



| Valor             | Descrição                                                                                                                                                           |
|--------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| GUID de solicitação | Identifica a solicitação. De definir **o membro guidSetting** da estrutura [**GET INFO \_ \_ \_ PARAMETERS do OPM**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_get_info_parameters) igual a esse valor. |
| Dados de entrada   | Especifica como interpretar a matriz **abParameters** na estrutura [**GET INFO \_ \_ \_ PARAMETERS do OPM.**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_get_info_parameters)                      |
| Dados de saída  | Especifica como interpretar a **matriz abRequestedInformation** na estrutura [**\_ OPM REQUESTED \_ INFORMATION.**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_requested_information)         |



 

As seguintes solicitações de status são definidas:



| Solicitação de status                                                                                      | Descrição                                                                                                                                           |
|-----------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**OPM \_ OBTER \_ SINALIZAÇÃO ACP \_ E \_ CGMSA \_**](opm-get-acp-and-cgmsa-signaling.md)                     | Retorna as seguintes informações sobre uma saída de vídeo:                                                                                               |
| [**OBTER FORMATO \_ \_ DE SAÍDA \_ \_ REAL DO OPM**](opm-get-actual-output-format.md)                            | Retorna uma descrição do sinal de vídeo que está sendo transmitido pelo conector.                                                               |
| [**OBTER NÍVEL DE \_ \_ PROTEÇÃO REAL DO \_ OPM \_**](opm-get-actual-protection-level.md)                      | Retorna o nível de proteção global para um mecanismo de proteção especificado.                                                                             |
| [**OBTER TIPO DE \_ \_ BARRAMENTO \_ DO ADAPTADOR \_ DO OPM**](opm-get-adapter-bus-type.md)                                    | Retorna o tipo de barramento de E/S usado pela saída de vídeo.                                                                                                 |
| [**OBTER \_ INFORMAÇÕES \_ DO CODEC DO OPM \_**](opm-get-codec-info.md)                                                 | Obtém o valor de um codec de hardware.                                                                                                             |
| [**OBTER INFORMAÇÕES DE \_ \_ DISPOSITIVO \_ HDCP \_ \_ CONECTADAS DO OPM**](opm-get-connected-hdcp-device-information.md) | Obtém informações sobre um High-Bandwidth HDCP (Proteção de Conteúdo digital) anexado à saída de vídeo. As seguintes informações são retornadas: |
| [**TIPO DE \_ CONECTOR GET \_ DO OPM \_**](opm-get-connector-type.md)                                         | Retorna o tipo de conector físico da saída de vídeo.                                                                                              |
| [**OBTER \_ A \_ VERSÃO ATUAL DO \_ \_ HDCP SRM \_ DO OPM**](opm-get-current-hdcp-srm-version.md)                   | Retorna o número de versão da SRM (mensagem de renovação do sistema) usada atualmente pela saída de vídeo.                                               |
| [**CARACTERÍSTICAS DO OPM \_ \_ GET \_ DVI**](opm-get-dvi-characteristics.md)                               | Consulta se um conector DVI (interface de vídeo digital) dá suporte à DVI versão 1.1 ou posterior.                                                          |
| [**OPM \_ GET \_ OUTPUT \_ ID**](opm-get-output-id.md)                                                   | Retorna o identificador exclusivo do monitor associado a esta saída de vídeo.                                                                       |
| [**OBTER TIPOS \_ \_ DE PROTEÇÃO COM \_ \_ SUPORTE DO OPM**](opm-get-supported-protection-types.md)                | Retorna a lista de mecanismos de proteção compatíveis com o conector.                                                                        |
| [**OBTER NÍVEL DE \_ \_ PROTEÇÃO VIRTUAL \_ DO OPM \_**](opm-get-virtual-protection-level.md)                    | Retorna o nível de proteção virtual para um mecanismo de proteção especificado.                                                                            |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência de programação do OPM](opm-programming-reference.md)
</dt> <dt>

[Gerenciador de Proteção de Saída](output-protection-manager.md)
</dt> </dl>

 

 



