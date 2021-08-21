---
title: estruturas protocolo RDP provedor de dados
description: A API de protocolo remoto personalizado dá suporte às estruturas a seguir.
ms.assetid: 45d17758-4554-42aa-aeb9-c8d4e7fc6bb7
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5f7d1b7b3ea968925cdcace605ed6c136054b023cc12482475196696bdbcc02
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118856232"
---
# <a name="remote-desktop-protocol-provider-structures"></a>estruturas protocolo RDP provedor de dados

A API de protocolo remoto personalizado dá suporte às estruturas a seguir.

## <a name="in-this-section"></a>Nesta seção

<dl> <dt>

[**DADOS DE SUPORTE DO TSMF \_ \_ \_ NO**](tsmf-support-data-in.md)
</dt> <dd>

Contém informações sobre formatos de mídia.

</dd> <dt>

[**DADOS DE SUPORTE DO TSMF \_ \_ \_ OUT**](tsmf-support-data-out.md)
</dt> <dd>

Contém informações sobre formatos de mídia.

</dd> <dt>

[**SUPORTE AO TSMF \_ \_ NODEDATA \_ NO**](tsmf-support-nodedata-in.md)
</dt> <dd>

Usado dentro da estrutura [**TSMF \_ SUPPORT \_ DATA \_ IN**](tsmf-support-data-in.md) para conter informações sobre formatos de mídia com suporte.

</dd> <dt>

[**NODEDATA OUT DE SUPORTE DO TSMF \_ \_ \_**](tsmf-support-nodedata-out.md)
</dt> <dd>

Usado dentro da estrutura [**TSMF \_ SUPPORT \_ DATA \_ OUT**](tsmf-support-data-out.md) para conter informações sobre formatos de mídia com suporte.

</dd> <dt>

[**CONFIGURAÇÕES DE \_ CONEXÃO DO WRDS \_**](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wrds_connection_settings)
</dt> <dd>

Contém informações de configuração de conexão para uma sessão remota.

</dd> <dt>

[**CONFIGURAÇÕES DE \_ CONEXÃO \_ WRDS \_ 1**](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wrds_connection_settings_1)
</dt> <dd>

Contém informações de configuração de conexão para uma sessão remota.

</dd> <dt>

[**INFORMAÇÕES DE \_ FUSO \_ HORÁRIO \_ DINÂMICO DO \_ WRDS**](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wrds_dynamic_time_zone_information)
</dt> <dd>

Contém informações de fuso horário dinâmico.

</dd> <dt>

[**CONFIGURAÇÕES DO \_ OUVINTE DO WRDS \_**](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wrds_listener_settings)
</dt> <dd>

Contém informações de configuração de ouvinte para uma sessão remota.

</dd> <dt>

[**CONFIGURAÇÕES DO \_ OUVINTE \_ WRDS \_ 1**](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wrds_listener_settings_1)
</dt> <dd>

Contém configurações de ouvinte para uma sessão remota.

</dd> <dt>

[**CONFIGURAÇÕES \_ DO WRDS**](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wrds_settings)
</dt> <dd>

Contém informações de configuração relacionadas à política para uma sessão remota.

</dd> <dt>

[**CONFIGURAÇÕES \_ DO WRDS \_ 1**](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wrds_settings_1)
</dt> <dd>

Contém configurações relacionadas à política para uma sessão remota.

</dd> <dt>

[**\_WTS ESTATÍSTICAS \_ DE CACHE**](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wts_cache_stats)
</dt> <dd>

Contém estatísticas de cache de protocolo.

</dd> <dt>

[**\_WTS \_IOCTL DE EXIBIÇÃO**](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wts_display_ioctl)
</dt> <dd>

Contém informações sobre a exibição do cliente.

</dd> <dt>

[**\_WTS DADOS DO \_ CLIENTE**](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wts_client_data)
</dt> <dd>

Contém informações sobre a conexão do cliente.

</dd> <dt>

[**\_WTS FUNCIONALIDADES \_ DE LICENÇA**](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wts_license_capabilities)
</dt> <dd>

Contém informações sobre os recursos de licenciamento do cliente.

</dd> <dt>

[**\_WTS DADOS DE \_ POLÍTICA**](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wts_policy_data)
</dt> <dd>

Contém informações de política passadas pelo serviço Serviços de Área de Trabalho Remota para o protocolo.

</dd> <dt>

[**\_WTS VALOR DA \_ PROPRIEDADE**](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wts_property_value)
</dt> <dd>

Contém informações sobre um valor da propriedade a ser recuperado do protocolo.

</dd> <dt>

[**\_WTS CACHE DE \_ PROTOCOLO**](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wts_protocol_cache)
</dt> <dd>

Contém o número de leituras de cache e acertos de cache.

</dd> <dt>

[**\_WTS CONTADORES \_ DE PROTOCOLO**](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wts_protocol_counters)
</dt> <dd>

Contém contadores de desempenho de protocolo.

</dd> <dt>

[**\_WTS STATUS DO \_ PROTOCOLO**](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wts_protocol_status)
</dt> <dd>

Contém informações sobre o status do protocolo.

</dd> <dt>

[**\_WTS ESTADO \_ DO SERVIÇO**](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wts_service_state)
</dt> <dd>

Contém informações sobre alterações no estado do serviço Serviços de Área de Trabalho Remota serviço.

</dd> <dt>

[**\_WTS \_ID DA SESSÃO**](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wts_session_id)
</dt> <dd>

Contém um **GUID** que identifica exclusivamente uma sessão.

</dd> <dt>

[**\_WTS PEQUENO \_ RECT**](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wts_small_rect)
</dt> <dd>

Contém coordenadas de janela do cliente.

</dd> <dt>

[**\_WTS Sockaddr**](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wts_sockaddr)
</dt> <dd>

Contém um endereço de soquete.

</dd> <dt>

[**\_WTS Systemtime**](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wts_systemtime)
</dt> <dd>

Especifica informações de data e hora para transições entre o horário padrão e o horário de verão.

</dd> <dt>

[**\_WTS INFORMAÇÕES \_ DE FUSO \_ HORÁRIO**](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wts_time_zone_information)
</dt> <dd>

Contém informações de fuso horário do cliente.

</dd> <dt>

[**\_WTS CREDENCIAL \_ DO USUÁRIO**](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wts_user_credential)
</dt> <dd>

Contém informações de credencial para um usuário.

</dd> <dt>

[**\_WTS DADOS DO \_ USUÁRIO**](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wts_user_data)
</dt> <dd>

Contém valores de propriedade do cliente selecionados.

</dd> </dl>

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência protocolo RDP provedor de serviços](custom-remote-protocol-reference.md)
</dt> <dt>

[enumerações protocolo RDP provedor de dados](custom-remote-protocol-enumerations.md)
</dt> <dt>

[interfaces protocolo RDP provedor de dados](custom-remote-protocol-interfaces.md)
</dt> <dt>

[uniões protocolo RDP provedor de serviços](custom-remote-protocol-unions.md)
</dt> </dl>

 

 




