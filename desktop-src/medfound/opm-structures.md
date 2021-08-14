---
description: As estruturas a seguir são usadas com o Gerenciador de proteção de saída (OPM).
ms.assetid: 676a60ca-393e-4b5d-89d3-50cf4b771492
title: Estruturas OPM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b35d72c5a5301dbc07b990aa4076f14fc221a1fde6af9c81e1f4a37fb424e24
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118737643"
---
# <a name="opm-structures"></a>Estruturas OPM

As estruturas a seguir são usadas com o [Gerenciador de proteção de saída](output-protection-manager.md) (OPM).



| Estrutura                                                                                              | Descrição                                                                                                                                                |
|--------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_cabeçalho grl**](grl-header.md)                                                                      | Contém o cabeçalho do GRL (lista de revogação global).                                                                                                          |
| [**\_assinatura MF**](mf-signature.md)                                                                  | Contém uma assinatura de GRL (lista de revogação global).                                                                                                         |
| [**\_ \_ \_ sinalização de CGMSA \_ e ACP OPM**](/windows/desktop/api/opmapi/ns-opmapi-opm_acp_and_cgmsa_signaling)                                 | Contém o resultado de uma consulta de [**\_ \_ \_ \_ \_ sinalização Get ACP e CGMSA de OPM**](opm-get-acp-and-cgmsa-signaling.md) .                                         |
| [**\_formato de \_ saída \_ real OPM**](/windows/desktop/api/opmapi/ns-opmapi-opm_actual_output_format)                                        | Contém o resultado de uma consulta de [**formato de saída de OPM de \_ obter \_ real \_ \_**](opm-get-actual-output-format.md) no Gerenciador de proteção de saída (OPM).               |
| [**\_parâmetros de configuração de OPM \_**](/windows/desktop/api/opmapi/ns-opmapi-opm_configure_parameters)                                         | Contém um comando OPM ou do Gerenciador de proteção de saída certificado (COPP).                                                                                     |
| [**\_informações de \_ dispositivo de HDCP conectado \_ a OPM \_**](/windows/desktop/api/opmapi/ns-opmapi-opm_connected_hdcp_device_information)             | Contém o resultado de uma consulta de [**\_ informações de dispositivo de \_ \_ \_ \_ dados de HDCP do OPM**](opm-get-connected-hdcp-device-information.md) .                     |
| [**\_parâmetros de \_ \_ informações get \_ compatíveis com a Copp de \_ OPM**](/windows/desktop/api/opmapi/ns-opmapi-opm_copp_compatible_get_info_parameters)        | Contém parâmetros para o método [**IOPMVideoOutput:: COPPCompatibleGetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-coppcompatiblegetinformation) . |
| [**\_parâmetros de \_ inicialização criptografada em OPM \_**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_encrypted_initialization_parameters)          | Contém parâmetros de inicialização para uma sessão OPM.                                                                                                     |
| [**informações de informações do codec de obtenção de OPM \_ \_ \_ \_**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_get_codec_info_information)                           | Contém o resultado de uma consulta de [**informações de codec de obtenção de OPM \_ \_ \_**](opm-get-codec-info.md) .                                                                     |
| [**\_parâmetros de \_ informações de codec de obtenção de OPM \_ \_**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_get_codec_info_parameters)                             | Contém informações para o comando [**OPM \_ Get \_ codec \_ info**](opm-get-codec-info.md) .                                                                  |
| [**\_parâmetros de \_ informações de obtenção de OPM \_**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_get_info_parameters)                                          | Contém parâmetros para o método [**IOPMVideoOutput:: GetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation) .                             |
| [**\_vetor de \_ seleção de chave de HDCP OPM \_ \_**](/windows/desktop/api/opmapi/ns-opmapi-opm_hdcp_key_selection_vector)                             | Contém o vetor de seleção de chave (KSV) para um receptor de High-Bandwidth digital Proteção de Conteúdo (HDCP).                                                   |
| [**\_OMAC OPM**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_omac)                                                                          | Contém um Message Authentication Code (MAC) para uma mensagem OPM.                                                                                           |
| [**\_dados de \_ ID de saída OPM \_**](/windows/desktop/api/opmapi/ns-opmapi-opm_output_id_data)                                                    | Contém o resultado de uma solicitação de status de [**\_ obter \_ \_ ID de saída de OPM**](opm-get-output-id.md) .                                                              |
| [**\_número aleatório de OPM \_**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_random_number)                                                       | Contém um número aleatório de 128 bits para uso com OPM.                                                                                                         |
| [**\_informações solicitadas de OPM \_**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_requested_information)                                       | Contém o resultado de uma solicitação de status OPM.                                                                                                              |
| [**\_ \_ \_ \_ \_ parâmetros de sinalização Set ACP e CGMSA de \_ OPM**](/windows/desktop/api/opmapi/ns-opmapi-opm_set_acp_and_cgmsa_signaling_parameters) | Contém informações para o [**OPM \_ set \_ ACP e o comando de \_ \_ \_ sinalização CGMSA**](opm-set-acp-and-cgmsa-signaling.md) em OPM.                               |
| [**os \_ \_ parâmetros de \_ SRM de HDCP definidos de OPM \_**](/windows/desktop/api/opmapi/ns-opmapi-opm_set_hdcp_srm_parameters)                                 | Contém parâmetros para o comando [**OPM \_ set \_ HDCP \_ SRM**](opm-set-hdcp-srm.md) .                                                                       |
| [**OPM \_ define \_ os \_ parâmetros de nível de proteção \_**](/windows/desktop/api/opmapi/ns-opmapi-opm_set_protection_level_parameters)                 | Contém dados para o comando de [ \_ nível de \_ proteção \_ de OPM definido](opm-set-protection-level.md) em OPM.                                                          |
| [**\_informações padrão de OPM \_**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_standard_information)                                         | Contém o resultado de uma solicitação de status OPM.                                                                                                            |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência de programação de OPM](opm-programming-reference.md)
</dt> <dt>

[Gerenciador de proteção de saída](output-protection-manager.md)
</dt> </dl>

 

 



