---
description: O log de segurança foi projetado para ser usado pelo sistema. no entanto, os usuários podem ler e limpar o log de segurança se tiverem recebido o \_ privilégio de nome de segurança ES \_ (o \# direito de usuário &0034; gerenciar auditoria e log de segurança&\# 0034;. Para obter mais informações, consulte privilégios.
ms.assetid: 861be39a-012e-473b-a2d3-2a8c7ba3adaa
title: Segurança do log de eventos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b52f6c801b061290ebb4d6f47fe78efebc09e1b2d23dc4a598dc9f97c1b3a46d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118151546"
---
# <a name="event-logging-security"></a>Segurança do log de eventos

O log de **segurança** foi projetado para ser usado pelo sistema. no entanto, os usuários podem ler e limpar o log de **segurança** se tiverem recebido o privilégio de ES \_ nome de segurança \_ (o direito de usuário "gerenciar auditoria e log de segurança"). Para obter mais informações, consulte [privilégios](/windows/desktop/SecAuthZ/privileges).

Somente a autoridade de segurança local (Lsass.exe) tem permissão de gravação para o log de **segurança** . Nenhuma outra conta pode solicitar esse privilégio. Para gravar um evento no log de **segurança** , use a função [**AuthzReportSecurityEvent**](/windows/desktop/api/authz/nf-authz-authzreportsecurityevent) .

O acesso ao log do **aplicativo** , o log do **sistema** e os logs personalizados são restritos. O sistema concede acesso com base nos direitos de acesso concedidos à conta sob a qual o thread está sendo executado. A tabela a seguir mostra quais tipos de acesso são exigidos pelas funções de log de eventos.



| Direito de acesso                 | Descrição                                                                                            |
|------------------------------|--------------------------------------------------------------------------------------------------------|
| \_ \_ 0X0004 (Elf logfile Clear) | Exigido por [**ClearEventLog**](/windows/desktop/api/Winbase/nf-winbase-cleareventloga).                                                    |
| \_Leitura de arquivo de log Elf \_ (0x0001)  | Exigido por [**OpenBackupEventLog**](/windows/desktop/api/Winbase/nf-winbase-openbackupeventloga) e [**OpenEventLog**](/windows/desktop/api/Winbase/nf-winbase-openeventloga). |
| \_ \_ Gravação de Logfile de Elf (0x0002) | Exigido por [**RegisterEventSource**](/windows/desktop/api/Winbase/nf-winbase-registereventsourcea).                                        |



 

Use o valor do registro **imposto alfandegário** para configurar a segurança do log do **aplicativo** , o log do **sistema** e os logs personalizados. Para obter mais informações, consulte [EventLog Key](eventlog-key.md).

**Windows XP/2000:** A tabela a seguir descreve os direitos de acesso concedidos para cada conta em cada log.

| Log             | Conta                 | Ler | Gravar | Limpar |
|-----------------|-------------------------|------|-------|-------|
| **Aplicativo** | Administradores (sistema) | X    | X     | X     |
|                 | Administradores (domínio) | X    | X     | X     |
|                 | LocalSystem             | X    | X     | X     |
|                 | Usuário interativo        | X    | X     |       |
| **System**      | Administradores (sistema) | X    | X     | X     |
|                 | Administradores (domínio) | X    |       | X     |
|                 | LocalSystem             | X    | X     | X     |
|                 | Usuário interativo        | X    |       |       |
| *Personalizado*        | Administradores (sistema) | X    | X     | X     |
|                 | Administradores (domínio) | X    | X     | X     |
|                 | LocalSystem             | X    | X     | X     |
|                 | Usuário interativo        | X    | X     |       |



 

Para conceder acesso aos membros da conta de convidado, altere o seguinte valor de registro:

**HKEY \_ Sistema de \_ máquina local** \\  \\ **CurrentControlSet** \\ **Serviços** \\ log de **EventLog** \\  \\ **RestrictGuestAccess**

 

 
