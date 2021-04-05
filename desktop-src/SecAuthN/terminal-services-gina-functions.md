---
description: Quando os serviços de terminal são habilitados, a GINA deve chamar funções de suporte do Winlogon para concluir a configuração de cada usuário, consultar as credenciais de uma sessão de cliente dos serviços de terminal e desconectar-se de uma sessão de rede dos serviços de terminal. Observe que as DLLs GINAs são ignoradas no Windows Vista.
ms.assetid: 70b55b99-b350-4638-84ba-e5580d9d992f
title: Funções de GINA de serviços de terminal
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19452fb73f00ef4ace0dd85083578334b6fb1038
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827029"
---
# <a name="terminal-services-gina-functions"></a>Funções de GINA de serviços de terminal

Quando os serviços de terminal são habilitados, a [*Gina*](../secgloss/g-gly.md) deve chamar funções de suporte do [*Winlogon*](../secgloss/w-gly.md) para concluir a configuração de cada usuário, consultar as [*credenciais*](../secgloss/c-gly.md) de uma sessão de cliente dos serviços de terminal e desconectar-se de uma sessão de rede dos serviços de terminal.

> [!Note]  
> As DLLs GINAs são ignoradas no Windows Vista.

 

Essas funções de suporte incluem o seguinte.



| Função                                                                     | Descrição                                                                                         |
|------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| [**WlxWin31Migrate**](/windows/win32/api/winwlx/nc-winwlx-pwlx_win31_migrate)                                   | Conclui a configuração do usuário.                                                                    |
| [**WlxQueryClientCredentials**](/windows/win32/api/winwlx/nc-winwlx-pwlx_query_client_credentials)               | Chamado para consultar as credenciais de clientes remotos que não estão usando uma licença de conector da Internet. |
| [**WlxQueryInetConnectorCredentials**](/windows/win32/api/winwlx/nc-winwlx-pwlx_query_ic_credentials) | Chamado para consultar as credenciais de clientes remotos que estão usando uma licença de conector da Internet.     |
| [**WlxQueryTerminalServicesData**](/windows/win32/api/winwlx/nc-winwlx-pwlx_query_terminal_services_data)         | Chamado para recuperar informações de configuração do usuário dos serviços de terminal.                                |
| [**WlxDisconnect**](/windows/win32/api/winwlx/nc-winwlx-pwlx_disconnect)                                       | Chamado para desconectar-se de uma sessão de rede dos serviços de terminal.                                      |



 

Para acessar essas funções de suporte do Winlogon, a DLL GINA deve usar a estrutura de [**expedição WLX da \_ \_ versão \_ 1 \_ 3**](/windows/desktop/api/Winwlx/ns-winwlx-wlx_dispatch_version_1_3) . Na função [**WlxNegotiate**](/windows/desktop/api/Winwlx/nf-winwlx-wlxnegotiate) da Gina, ambos os parâmetros devem ser pelo menos WLX \_ versão \_ 1 \_ 3.

 

 
