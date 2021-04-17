---
title: Estruturas de provedor de protocolo RDP
description: A API de protocolo remoto personalizada oferece suporte às seguintes estruturas.
ms.assetid: 45d17758-4554-42aa-aeb9-c8d4e7fc6bb7
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a626db328ede3bac9422a9a47ebe55f05953a22d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105783344"
---
# <a name="remote-desktop-protocol-provider-structures"></a>Estruturas de provedor de protocolo RDP

A API de protocolo remoto personalizada oferece suporte às seguintes estruturas.

## <a name="in-this-section"></a>Nesta seção

<dl> <dt>

[**\_ \_ dados de suporte \_ do TSMF em**](tsmf-support-data-in.md)
</dt> <dd>

Contém informações sobre formatos de mídia.

</dd> <dt>

[**\_saída de \_ dados de suporte do TSMF \_**](tsmf-support-data-out.md)
</dt> <dd>

Contém informações sobre formatos de mídia.

</dd> <dt>

[**TSMF \_ suportam \_ NODEDATA \_**](tsmf-support-nodedata-in.md)
</dt> <dd>

Usado dentro dos [**dados de suporte do TSMF \_ \_ \_ na**](tsmf-support-data-in.md) estrutura para conter informações sobre formatos de mídia com suporte.

</dd> <dt>

[**TSMF \_ suporte \_ NODEDATA \_**](tsmf-support-nodedata-out.md)
</dt> <dd>

Usado na estrutura [**de \_ \_ \_ saída de dados de suporte do TSMF**](tsmf-support-data-out.md) para conter informações sobre formatos de mídia com suporte.

</dd> <dt>

[**\_configurações de conexão do WRDS \_**](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wrds_connection_settings)
</dt> <dd>

Contém informações de configuração de conexão para uma sessão remota.

</dd> <dt>

[**Configurações de conexão do WRDS \_ \_ \_ 1**](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wrds_connection_settings_1)
</dt> <dd>

Contém informações de configuração de conexão para uma sessão remota.

</dd> <dt>

[**\_informações de \_ \_ fuso horário dinâmico do \_ WRDS**](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wrds_dynamic_time_zone_information)
</dt> <dd>

Contém informações de fuso horário dinâmico.

</dd> <dt>

[**\_configurações do ouvinte WRDS \_**](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wrds_listener_settings)
</dt> <dd>

Contém informações de configuração de ouvinte para uma sessão remota.

</dd> <dt>

[**\_Configurações do ouvinte WRDS \_ \_ 1**](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wrds_listener_settings_1)
</dt> <dd>

Contém configurações de ouvinte para uma sessão remota.

</dd> <dt>

[**configurações de WRDS \_**](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wrds_settings)
</dt> <dd>

Contém informações de configuração relacionadas à política para uma sessão remota.

</dd> <dt>

[**Configurações de WRDS \_ \_ 1**](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wrds_settings_1)
</dt> <dd>

Contém configurações relacionadas à política para uma sessão remota.

</dd> <dt>

[**\_Estatísticas de cache WTS \_**](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wts_cache_stats)
</dt> <dd>

Contém estatísticas de cache de protocolo.

</dd> <dt>

[**WTS \_ Exibir \_ IOCTL**](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wts_display_ioctl)
</dt> <dd>

Contém informações sobre a exibição do cliente.

</dd> <dt>

[**\_dados do cliente WTS \_**](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wts_client_data)
</dt> <dd>

Contém informações sobre a conexão do cliente.

</dd> <dt>

[**\_recursos de licença do WTS \_**](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wts_license_capabilities)
</dt> <dd>

Contém informações sobre os recursos de licenciamento do cliente.

</dd> <dt>

[**\_dados de política WTS \_**](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wts_policy_data)
</dt> <dd>

Contém informações de política que são passadas pelo serviço de Serviços de Área de Trabalho Remota para o protocolo.

</dd> <dt>

[**\_valor da propriedade WTS \_**](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wts_property_value)
</dt> <dd>

Contém informações sobre um valor de propriedade a ser recuperado do protocolo.

</dd> <dt>

[**\_cache de protocolo WTS \_**](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wts_protocol_cache)
</dt> <dd>

Contém o número de leituras de cache e acertos de cache.

</dd> <dt>

[**\_contadores de protocolo WTS \_**](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wts_protocol_counters)
</dt> <dd>

Contém contadores de desempenho de protocolo.

</dd> <dt>

[**\_status do protocolo WTS \_**](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wts_protocol_status)
</dt> <dd>

Contém informações sobre o status do protocolo.

</dd> <dt>

[**\_estado do serviço WTS \_**](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wts_service_state)
</dt> <dd>

Contém informações sobre as alterações no estado do serviço de Serviços de Área de Trabalho Remota.

</dd> <dt>

[**\_ID da sessão WTS \_**](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wts_session_id)
</dt> <dd>

Contém um **GUID** que identifica exclusivamente uma sessão.

</dd> <dt>

[**\_Rect WTS pequeno \_**](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wts_small_rect)
</dt> <dd>

Contém coordenadas da janela do cliente.

</dd> <dt>

[**WTS \_ SOCKADDR**](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wts_sockaddr)
</dt> <dd>

Contém um endereço de soquete.

</dd> <dt>

[**WTS \_ SYSTEMTIME**](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wts_systemtime)
</dt> <dd>

Especifica informações de data e hora para transições entre hora padrão e horário de verão.

</dd> <dt>

[**\_informações de \_ fuso \_ horário do WTS**](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wts_time_zone_information)
</dt> <dd>

Contém informações de fuso horário do cliente.

</dd> <dt>

[**\_credencial de usuário WTS \_**](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wts_user_credential)
</dt> <dd>

Contém informações de credenciais para um usuário.

</dd> <dt>

[**WTS \_ dados do usuário \_**](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wts_user_data)
</dt> <dd>

Contém os valores de propriedade de cliente SELECT.

</dd> </dl>

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Referência do provedor de protocolo RDP](custom-remote-protocol-reference.md)
</dt> <dt>

[Enumerações de provedor de protocolo RDP](custom-remote-protocol-enumerations.md)
</dt> <dt>

[Interfaces do provedor de protocolo RDP](custom-remote-protocol-interfaces.md)
</dt> <dt>

[Uniões de provedor de protocolo RDP](custom-remote-protocol-unions.md)
</dt> </dl>

 

 




