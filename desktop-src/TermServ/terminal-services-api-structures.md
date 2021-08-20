---
title: estruturas Serviços de Área de Trabalho Remota API do Serviços de Área de Trabalho Remota
description: Lista as estruturas usadas com a API Serviços de Área de Trabalho Remota.
ms.assetid: 5d467241-499c-4038-8d9c-4244457e484f
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe3161d7c8e8b295e42930af1edcc79b7c60d83b61097b4d02661c1b11b5f1a0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119000096"
---
# <a name="remote-desktop-services-api-structures"></a>estruturas Serviços de Área de Trabalho Remota API do Serviços de Área de Trabalho Remota

As estruturas a seguir são usadas com Serviços de Área de Trabalho Remota API.

## <a name="in-this-section"></a>Nesta seção

<dl> <dt>

[**CHANNEL \_ DEF**](/windows/desktop/api/Pchannel/ns-pchannel-tagchannel_def)
</dt> <dd>

Contém o nome e as opções de um Serviços de Área de Trabalho Remota virtual.

</dd> <dt>

[**PONTOS \_ DE ENTRADA DE \_ CANAL**](/windows/win32/api/cchannel/ns-cchannel-channel_entry_points)
</dt> <dd>

Contém ponteiros para as funções chamadas por uma DLL do lado do cliente para acessar canais virtuais.

</dd> <dt>

[**CHANNEL \_ PDU \_ HEADER**](/windows/win32/api/pchannel/ns-pchannel-channel_pdu_header)
</dt> <dd>

Contém informações sobre um bloco de dados que está sendo recebido pela extremidade do servidor de um canal virtual.

</dd> <dt>

[**LSKeyPack**](lskeypack.md)
</dt> <dd>

Contém informações sobre um pacote de chaves Serviços de Área de Trabalho Remota licenciamento específico.

</dd> <dt>

[**LSLicense**](lslicense.md)
</dt> <dd>

Contém informações sobre uma licença Serviços de Área de Trabalho Remota específica.

</dd> <dt>

[**WTSCLIENT**](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wtsclienta)
</dt> <dd>

Contém informações sobre um Conexão de Área de Trabalho Remota (RDC).

</dd> <dt>

[**WTSCONFIGINFO**](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wtsconfiginfoa)
</dt> <dd>

Contém informações sobre uma Serviços de Área de Trabalho Remota sessão.

</dd> <dt>

[**WTSINFO**](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wtsinfoa)
</dt> <dd>

Contém informações sobre uma Serviços de Área de Trabalho Remota sessão.

</dd> <dt>

[**WTSINFOEX**](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wtsinfoexa)
</dt> <dd>

Contém uma [**união WTSINFOEX \_ LEVEL**](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wtsinfoex_level_a) que contém informações estendidas sobre uma Serviços de Área de Trabalho Remota sessão.

</dd> <dt>

[**WTSINFOEX \_ LEVEL1**](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wtsinfoex_level1_a)
</dt> <dd>

Contém informações estendidas sobre uma Serviços de Área de Trabalho Remota sessão.

</dd> <dt>

[**WTSLISTENERCONFIG**](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wtslistenerconfiga)
</dt> <dd>

Contém informações sobre um Serviços de Área de Trabalho Remota ouvinte.

</dd> <dt>

[**ENDEREÇO IP WTSSBX \_ \_**](/windows/win32/api/tssbx/ns-tssbx-wtssbx_ip_address)
</dt> <dd>

Contém informações sobre o endereço IP de um recurso de rede.

</dd> <dt>

[**INFORMAÇÕES DE CONEXÃO DO COMPUTADOR WTSSBX \_ \_ \_**](/windows/win32/api/tssbx/ns-tssbx-wtssbx_machine_connect_info)
</dt> <dd>

Contém informações sobre um computador que está aceitando conexões remotas.

</dd> <dt>

[**INFORMAÇÕES DO COMPUTADOR WTSSBX \_ \_**](/windows/win32/api/tssbx/ns-tssbx-wtssbx_machine_info)
</dt> <dd>

Contém informações sobre um computador e seu estado atual.

</dd> <dt>

[**INFORMAÇÕES DE SESSÃO DO WTSSBX \_ \_**](/windows/win32/api/tssbx/ns-tssbx-wtssbx_session_info)
</dt> <dd>

Contém informações sobre sessões que estão disponíveis para o Conexão de Área de Trabalho Remota Broker (Agente de Conexão de RD).

</dd> <dt>

[**NOTIFICAÇÃO DE WTSSESSION \_**](/windows/win32/api/winuser/ns-winuser-wtssession_notification)
</dt> <dd>

Fornece informações sobre a notificação de alteração de sessão. Um serviço recebe essa estrutura em sua [*função HandlerEx*](/windows/desktop/api/winsvc/nc-winsvc-lphandler_function_ex) em resposta a um evento de alteração de sessão.

</dd> <dt>

[**WTSUSERCONFIG**](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wtsuserconfiga)
</dt> <dd>

Contém informações de configuração para um usuário em um controlador de domínio ou Host da Sessão da Área de Trabalho Remota (Host da Sessão RD) .

</dd> <dt>

[**\_WTS ENDEREÇO \_ DO CLIENTE**](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wts_client_address)
</dt> <dd>

Contém o endereço de rede do cliente de uma Serviços de Área de Trabalho Remota sessão.

</dd> <dt>

[**\_WTS EXIBIÇÃO DO \_ CLIENTE**](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wts_client_display)
</dt> <dd>

Contém informações sobre a exibição de um Conexão de Área de Trabalho Remota (RDC).

</dd> <dt>

[**\_WTS INFORMAÇÕES DO \_ PROCESSO**](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wts_process_infoa)
</dt> <dd>

Contém informações sobre um processo em execução em um Host da Sessão RD servidor.

</dd> <dt>

[**\_WTS PROCESSAR \_ INFORMAÇÕES \_ EX**](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wts_process_info_exa)
</dt> <dd>

Contém informações estendidas sobre um processo em execução em um Host da Sessão RD servidor.

</dd> <dt>

[**\_WTS INFORMAÇÕES DO \_ PRODUTO**](https://msdn.microsoft.com/library/Mt283722(v=VS.85).aspx)
</dt> <dd>

Os detalhes da licença do produto necessário para se conectar a um servidor terminal.

</dd> <dt>

[**\_WTS INFORMAÇÕES DO \_ SERVIDOR**](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wts_server_infoa)
</dt> <dd>

Contém informações sobre um servidor Serviços de Área de Trabalho Remota específico.

</dd> <dt>

[**\_WTS ENDEREÇO \_ DA SESSÃO**](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wts_session_address)
</dt> <dd>

Contém o endereço IP virtual atribuído a uma sessão.

</dd> <dt>

[**\_WTS INFORMAÇÕES DA \_ SESSÃO**](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wts_session_infoa)
</dt> <dd>

Contém informações sobre uma sessão de cliente em um Host da Sessão RD servidor.

</dd> <dt>

[**\_WTS INFORMAÇÕES \_ DA SESSÃO \_ 1**](/windows/desktop/api/Wtsapi32/ns-wtsapi32-wts_session_info_1a)
</dt> <dd>

Contém informações estendidas sobre uma sessão de cliente em um servidor Host da Sessão RD ou Área de Trabalho Remota host de virtualização de RD (Host de Virtualização de RD).

</dd> </dl>

 

 