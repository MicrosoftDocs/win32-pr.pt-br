---
title: AppIDFlags
description: Um conjunto de sinalizadores que controlam o comportamento de ativação de um servidor COM.
ms.assetid: ab98e7d3-85c6-4328-84c4-1d4583df69ce
keywords:
- Valor do Registro AppIDFlags COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44ecf7d0d112d2ceff913f3de6250c130e16455c1810cc6234db63a6aaf463fe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119048864"
---
# <a name="appidflags"></a>AppIDFlags

Um conjunto de sinalizadores que controlam o comportamento de ativação de um servidor COM.

## <a name="registry-entry"></a>Entrada do Registro

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\AppID
   {AppID_GUID}
      AppIDFlags = flags
```

## <a name="remarks"></a>Comentários

Esse é um **valor \_ REG DWORD.**



| Valor de sinalizador | Constante                                              |
|------------|-------------------------------------------------------|
| 0x1        | APPIDREGFLAGS \_ ACTIVATE \_ IUSERVER \_ INDESKTOP          |
| 0x2        | APPIDREGFLAGS \_ SECURE \_ SERVER \_ PROCESS \_ SD \_ AND \_ BIND |
| 0x4        | APPIDREGFLAGS \_ EM QUESTÃO \_ RPC DE \_ ATIVAÇÃO EM \_ \_ IDENTIFICAR   |



 

### <a name="appidregflags_activate_iuserver_indesktop-description"></a>APPIDREGFLAGS \_ ACTIVATE \_ IUSERVER \_ INDESKTOP Description

Se o sinalizador **APPIDREGFLAGS \_ ACTIVATE \_ IUSERVER \_ INDESKTOP** estiver limpo em **AppIDFlags** ou se **AppIDFlags** não estiver presente, o cliente em uma sessão do servidor de terminal que está fazendo uma solicitação de ativação para um servidor [COM](interactive-user.md) do Usuário Interativo, será vinculado ou iniciará e se vinculará ao servidor COM na área de trabalho "padrão" da estação de janela "winsta0" [](/windows/desktop/winstation/window-stations) da sessão na solicitação de ativação. Por exemplo, se o cliente estiver executando "winsta0 desktop1" da sessão 3, a solicitação de ativação da sessão 3 será vinculada ou iniciará e se vinculará ao servidor COM em "winsta0 default" da sessão 3, mesmo se uma instância do servidor COM já estiver em execução em \\ \\ "winsta0 desktop1" da sessão \\ 3.

Se o sinalizador **APPIDREGFLAGS \_ ACTIVATE \_ IUSERVER \_ INDESKTOP** estiver definido no valor **AppIDFlags,** o COM será ligado ou iniciará e se vinculará ao processo do servidor em execução na área de trabalho do cliente e na sessão na solicitação de ativação. Por exemplo, se o cliente estiver executando "winsta0 desktop1" na sessão 3, a solicitação de ativação da sessão 3 será vinculada ou iniciará e se vinculará ao servidor COM em "winsta0 desktop1" na sessão 3, mesmo se uma instância do servidor COM já estiver em execução \\ \\ em "winsta0 default" na sessão \\ 3.

O cliente pode usar o [moniker](/windows/desktop/TermServ/session-monikers) de sessão para especificar uma sessão diferente da sessão do cliente ao fazer a solicitação de ativação.

O **sinalizador APPIDREGFLAGS \_ ACTIVATE \_ IUSERVER \_ INDESKTOP** aplica-se somente a servidores COM configurados para RunAs "[Interactive User](interactive-user.md)".

### <a name="appidregflags_secure_server_process_sd_and_bind-description"></a>APPIDREGFLAGS \_ SECURE \_ SERVER \_ PROCESS \_ SD \_ AND \_ BIND Description

Se o sinalizador **APPIDREGFLAGS \_ SECURE SERVER PROCESS \_ \_ \_ SD AND \_ \_ BIND** estiver definido em **AppIDFlags,** os servidores COM configurados para RunAs "Activator" serão lançados com um descritor de segurança de processo que permite PROCESSAR [ \_ TODO \_](/windows/desktop/ProcThread/process-security-and-access-rights) O ACESSO ao SID logonID do token de processo. Além disso, o proprietário do descritor de segurança será definido como o SID logonID do token de processo.

Se o sinalizador **APPIDREGFLAGS \_ SECURE SERVER PROCESS \_ \_ \_ SD \_ \_** AND BIND estiver definido em **AppIDFlags,** os servidores COM configurados como RunAs "This User" serão lançados com um descritor de segurança de processo que permite PROCESSAR [ \_ TODO \_](/windows/desktop/ProcThread/process-security-and-access-rights) O ACESSO no SID logonID do token de processo. Além disso, o proprietário do descritor de segurança será definido como o SID logonID do token de processo. Além disso, o SCM (Gerenciador de Controle de Serviço) COM modifica o token do processo do servidor COM da seguinte forma:

-   Ele adiciona um SID appid ao token. Ele concede ao SID appid acesso completo na DACL (lista de controle de acesso discricionário) padrão do token. No Windows Vista e versões posteriores do Windows, ele concede a permissão OwnerRights SID READ CONTROL na \_ DACL padrão do token. Em versões Windows Vista do Windows, ele define o proprietário do token como o SID appid.

As seguintes considerações de segurança devem ser levadas em conta ao usar o sinalizador **APPIDREGFLAGS \_ SECURE SERVER PROCESS \_ \_ \_ SD AND \_ \_ BIND:**

-   O sinalizador **APPIDREGFLAGS \_ SECURE SERVER PROCESS \_ \_ \_ SD \_ \_** AND BIND deve ser definido por servidores COM que são lançados em um dos contextos de segurança de serviço integrados; as contas NetworkService ou LocalService. Se os servidores representarem clientes privilegiados e se o sinalizador **APPIDREGFLAGS \_ SECURE SERVER PROCESS \_ \_ \_ SD \_ \_** AND BIND não estiver definido, o código mal-intencionado em execução em outros processos com o mesmo contexto de segurança poderá elevar o privilégio sequestro dos tokens de representação dos clientes privilegiados do processo do servidor COM.
-   Quando o **sinalizador APPIDREGFLAGS \_ SECURE SERVER PROCESS \_ \_ \_ SD AND \_ \_ BIND** estiver definido, o COM protegerá o descritor de segurança do objeto de processo no caso de servidores COM RunAs "Activator". Para esses servidores, o cliente COM deve proteger o token que ele usa para a ativação COM.
-   Quando o **sinalizador APPIDREGFLAGS \_ SECURE SERVER PROCESS \_ \_ \_ SD \_ \_** AND BIND é definido, o COM protegerá o descritor de segurança do objeto de processo no caso de servidores COM RunAs "This User". Ele também protegerá o token de processo do servidor COM, pois o COM SCM é a entidade que cria o token.

O sinalizador **APPIDREGFLAGS \_ SECURE SERVER PROCESS \_ \_ \_ SD \_ \_** AND BIND tem suporte no Windows XP, Windows Server 2003, Windows Vista e Windows Server 2008 somente quando o patch MSRC8322 (boletim de segurança [MS09-012)](https://support.microsoft.com/kb/959454)é aplicado. Ele tem suporte nativo no Windows 7 e versões posteriores do Windows.

O **sinalizador APPIDREGFLAGS \_ SECURE SERVER PROCESS \_ \_ \_ SD AND \_ \_ BIND** se aplica somente a servidores COM configurados para RunAs "Activator" ou "This User". Ele não se aplica a servidores COM que são serviços NT.

### <a name="appidregflags_issue_activation_rpc_at_identify-description"></a>APPIDREGFLAGS \_ ISSUE \_ ACTIVATION \_ RPC \_ AT \_ IDENTIFY Description

Se o sinalizador **APPIDREGFLAGS EMITIR ATIVAÇÃO \_ \_ \_ RPC \_ AT \_ IDENTIFY** estiver definido em **AppIDFlags,** o SCM COM emitirá solicitações de ativação de objeto para o processo de servidor COM usando um nível de representação de [RPC C IMP \_ LEVEL \_ \_ \_ IDENTIFY](impersonation-levels.md).

Se o sinalizador **APPIDREGFLAGS \_ ISSUE \_ ACTIVATION \_ RPC AT \_ \_ IDENTIFY** não estiver definido, o SCM COM emitirá solicitações de ativação de objeto para os processos do servidor COM usando um nível de representação de [RPC C IMP LEVEL \_ \_ \_ \_ IMPERSONATE](impersonation-levels.md).

As seguintes considerações de segurança devem ser levadas em conta ao usar o sinalizador **APPIDREGFLAGS \_ ISSUE \_ ACTIVATION \_ RPC AT \_ \_ IDENTIFY:**

-   O **sinalizador APPIDREGFLAGS \_ ISSUE ACTIVATION \_ \_ RPC AT \_ \_ IDENTIFY** deve ser usado por servidores COM que não executam o trabalho em nome de clientes em solicitações de ativação de objeto. Para esses servidores, fazer com que as solicitações de ativação de objeto de problema do COM SCM em [RPC \_ C IMP \_ LEVEL \_ \_ IDENTIFY](impersonation-levels.md) minimizem as chances de tokens privilegiados com ES [**de NOME \_ IMPERSONATE \_**](/windows/desktop/SecAuthZ/privilege-constants) aparecendo no processo.

O **sinalizador APPIDREGFLAGS \_ ISSUE ACTIVATION \_ \_ RPC AT \_ \_ IDENTIFY** tem suporte no Windows 7 e versões posteriores do Windows.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Desktops](/windows/desktop/winstation/desktops)
</dt> <dt>

[Níveis de representação](impersonation-levels.md)
</dt> <dt>

[Usuário interativo](interactive-user.md)
</dt> <dt>

[Monikers de sessão](/windows/desktop/TermServ/session-monikers)
</dt> <dt>

[Estações de Janela](/windows/desktop/winstation/window-stations)
</dt> </dl>

 

 