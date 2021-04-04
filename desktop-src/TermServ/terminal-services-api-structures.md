---
title: Estruturas de API Serviços de Área de Trabalho Remota
description: Lista as estruturas usadas com a API de Serviços de Área de Trabalho Remota.
ms.assetid: 5d467241-499c-4038-8d9c-4244457e484f
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22fb8de65f7f234f85eb8071cc66743c9c26cc9b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104084568"
---
# <a name="remote-desktop-services-api-structures"></a>Estruturas de API Serviços de Área de Trabalho Remota

As estruturas a seguir são usadas com a API Serviços de Área de Trabalho Remota.

## <a name="in-this-section"></a>Nesta seção

<dl> <dt>

[**DEF. de canal \_**](/windows/desktop/api/Pchannel/ns-pchannel-tagchannel_def)
</dt> <dd>

Contém o nome e as opções de um canal virtual Serviços de Área de Trabalho Remota.

</dd> <dt>

[**\_pontos de entrada de canal \_**](/windows/win32/api/cchannel/ns-cchannel-channel_entry_points)
</dt> <dd>

Contém ponteiros para as funções chamadas por uma DLL do lado do cliente para acessar canais virtuais.

</dd> <dt>

[**\_cabeçalho de PDU do canal \_**](/windows/win32/api/pchannel/ns-pchannel-channel_pdu_header)
</dt> <dd>

Contém informações sobre um bloco de dados que está sendo recebido pela extremidade do servidor de um canal virtual.

</dd> <dt>

[**LSKeyPack**](lskeypack.md)
</dt> <dd>

Contém informações sobre um pacote de chaves de licenciamento Serviços de Área de Trabalho Remota específico.

</dd> <dt>

[**LSLicense**](lslicense.md)
</dt> <dd>

Contém informações sobre uma licença de Serviços de Área de Trabalho Remota específica.

</dd> <dt>

[**WTSCLIENT**](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wtsclienta)
</dt> <dd>

Contém informações sobre um cliente de Conexão de Área de Trabalho Remota (RDC).

</dd> <dt>

[**WTSCONFIGINFO**](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wtsconfiginfoa)
</dt> <dd>

Contém informações sobre uma sessão de Serviços de Área de Trabalho Remota.

</dd> <dt>

[**WTSINFO**](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wtsinfoa)
</dt> <dd>

Contém informações sobre uma sessão de Serviços de Área de Trabalho Remota.

</dd> <dt>

[**WTSINFOEX**](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wtsinfoexa)
</dt> <dd>

Contém uma União de [**\_ nível de WTSINFOEX**](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wtsinfoex_level_a) que contém informações estendidas sobre uma sessão de serviços de área de trabalho remota.

</dd> <dt>

[**WTSINFOEX \_ LEVEL1**](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wtsinfoex_level1_a)
</dt> <dd>

Contém informações estendidas sobre uma sessão de Serviços de Área de Trabalho Remota.

</dd> <dt>

[**WTSLISTENERCONFIG**](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wtslistenerconfiga)
</dt> <dd>

Contém informações sobre um ouvinte de Serviços de Área de Trabalho Remota.

</dd> <dt>

[**\_endereço IP do WTSSBX \_**](/windows/win32/api/tssbx/ns-tssbx-wtssbx_ip_address)
</dt> <dd>

Contém informações sobre o endereço IP de um recurso de rede.

</dd> <dt>

[**\_informações de \_ conexão do computador WTSSBX \_**](/windows/win32/api/tssbx/ns-tssbx-wtssbx_machine_connect_info)
</dt> <dd>

Contém informações sobre um computador que está aceitando conexões remotas.

</dd> <dt>

[**\_informações do computador WTSSBX \_**](/windows/win32/api/tssbx/ns-tssbx-wtssbx_machine_info)
</dt> <dd>

Contém informações sobre um computador e seu estado atual.

</dd> <dt>

[**\_informações da sessão WTSSBX \_**](/windows/win32/api/tssbx/ns-tssbx-wtssbx_session_info)
</dt> <dd>

Contém informações sobre as sessões que estão disponíveis para Conexão de Área de Trabalho Remota Agente (agente de conexão RD).

</dd> <dt>

[**notificação de WTSSESSION \_**](/windows/win32/api/winuser/ns-winuser-wtssession_notification)
</dt> <dd>

Fornece informações sobre a notificação de alteração de sessão. Um serviço recebe essa estrutura em sua função [*HandlerEx*](/windows/desktop/api/winsvc/nc-winsvc-lphandler_function_ex) em resposta a um evento de alteração de sessão.

</dd> <dt>

[**WTSUSERCONFIG**](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wtsuserconfiga)
</dt> <dd>

Contém informações de configuração para um usuário em um controlador de domínio ou em um servidor Host da Sessão da Área de Trabalho Remota (Host da Sessão RD).

</dd> <dt>

[**\_endereço do cliente WTS \_**](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wts_client_address)
</dt> <dd>

Contém o endereço de rede do cliente de uma sessão de Serviços de Área de Trabalho Remota.

</dd> <dt>

[**\_exibição do cliente WTS \_**](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wts_client_display)
</dt> <dd>

Contém informações sobre a exibição de um cliente de Conexão de Área de Trabalho Remota (RDC).

</dd> <dt>

[**\_informações do processo WTS \_**](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wts_process_infoa)
</dt> <dd>

Contém informações sobre um processo em execução em um servidor de Host da Sessão RD.

</dd> <dt>

[**informações do processo WTS por \_ \_ \_ exemplo**](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wts_process_info_exa)
</dt> <dd>

Contém informações estendidas sobre um processo em execução em um servidor de Host da Sessão RD.

</dd> <dt>

[**\_informações do produto WTS \_**](https://msdn.microsoft.com/library/Mt283722(v=VS.85).aspx)
</dt> <dd>

Os detalhes da licença de produto que é necessária para se conectar a um servidor de terminal.

</dd> <dt>

[**\_informações do servidor WTS \_**](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wts_server_infoa)
</dt> <dd>

Contém informações sobre um servidor Serviços de Área de Trabalho Remota específico.

</dd> <dt>

[**\_endereço da sessão WTS \_**](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wts_session_address)
</dt> <dd>

Contém o endereço IP virtual atribuído a uma sessão.

</dd> <dt>

[**\_informações da sessão WTS \_**](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wts_session_infoa)
</dt> <dd>

Contém informações sobre uma sessão de cliente em um servidor de Host da Sessão RD.

</dd> <dt>

[**Informações de sessão do WTS \_ \_ \_ 1**](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wts_session_info_1a)
</dt> <dd>

Contém informações estendidas sobre uma sessão de cliente em um servidor de Host da Sessão RD ou Host de Virtualização de Área de Trabalho Remota (host de virtualização de área de trabalho remota).

</dd> </dl>

 

 