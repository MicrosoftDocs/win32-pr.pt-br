---
title: AppIDFlags
description: Um conjunto de sinalizadores que controlam o comportamento de ativação de um servidor COM.
ms.assetid: ab98e7d3-85c6-4328-84c4-1d4583df69ce
keywords:
- COM valor do registro AppIDFlags COM
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

Esse é um valor de **reg \_ DWORD** .



| Valor de sinalizador | Constante                                              |
|------------|-------------------------------------------------------|
| 0x1        | APPIDREGFLAGS \_ ativar o \_ IUSERVER \_ indesktop          |
| 0x2        | \_ \_ processo de servidor seguro APPIDREGFLAGS \_ \_ \_ de SD e \_ ligação |
| 0x4        | \_ \_ RPC de ativação do problema APPIDREGFLAGS \_ \_ em \_ identificar   |



 

### <a name="appidregflags_activate_iuserver_indesktop-description"></a>APPIDREGFLAGS \_ Ativar \_ \_ Descrição de INárea de trabalho do IUSERVER

Se o sinalizador **APPIDREGFLAGS \_ ativar o \_ \_ indesktop IUSERVER** for limpo em **AppIDFlags** ou se **AppIDFlags** não estiver presente, o cliente em uma sessão do Terminal Server fazendo uma solicitação de ativação para um servidor com de [usuário interativo](interactive-user.md) se associará ou iniciará e associará ao servidor com na área de trabalho "padrão" da estação de [janela](/windows/desktop/winstation/window-stations) "winsta0" da sessão na solicitação de ativação. Por exemplo, se o cliente estiver executando "winsta0 \\ desktop1" da sessão 3, a solicitação de ativação para a sessão 3 será associada ou iniciada e associada ao servidor com em "winsta0 \\ padrão" da sessão 3, mesmo que uma instância do servidor com já esteja em execução em "winsta0 \\ desktop1" da sessão 3.

Se o sinalizador **APPIDREGFLAGS \_ ativar o \_ \_ indesktop IUSERVER** for definido no valor **AppIDFlags** , o com será associado ou iniciado e associado ao processo do servidor em execução na área de trabalho do cliente e na sessão na solicitação de ativação. Por exemplo, se o cliente estiver executando "winsta0 \\ desktop1" na sessão 3, a solicitação de ativação para a sessão 3 será associada ou iniciada e associada ao servidor com em "winsta0 \\ desktop1" na sessão 3, mesmo que uma instância do servidor com já esteja em execução em "winsta0 \\ padrão" na sessão 3.

O cliente pode usar o [moniker de sessão](/windows/desktop/TermServ/session-monikers) para especificar uma sessão diferente da sessão do cliente quando ele faz a solicitação de ativação.

O sinalizador **APPIDREGFLAGS \_ ativar o \_ \_ indesktop IUSERVER** aplica-se somente a servidores com que são configurados para "[usuário interativo](interactive-user.md)" runas.

### <a name="appidregflags_secure_server_process_sd_and_bind-description"></a>APPIDREGFLAGS \_ o \_ \_ processo de servidor seguro \_ SD e a \_ \_ Descrição de ligação

Se o **sinalizador \_ \_ \_ \_ SD \_ e \_ BIND do APPIDREGFLAGS Secure Server** for definido em **AppIDFlags**, os servidores com configurados para executar como runas "Activator" serão iniciados com um descritor de segurança do processo que permite [processar \_ todo o \_ acesso](/windows/desktop/ProcThread/process-security-and-access-rights) ao SID de LogonId do token de processo. Além disso, o proprietário do descritor de segurança será definido como o SID de LogonId do token de processo.

Se o **sinalizador \_ \_ \_ \_ SD \_ e \_ BIND do APPIDREGFLAGS Secure Server** for definido em **AppIDFlags**, os servidores com configurados para executar como "este usuário" serão iniciados com um descritor de segurança do processo que permite [processar \_ todo o \_ acesso](/windows/desktop/ProcThread/process-security-and-access-rights) no SID de LogonId do token de processo. Além disso, o proprietário do descritor de segurança será definido como o SID de LogonId do token de processo. Além disso, o SCM (Gerenciador de controle de serviço) do COM modifica o token do processo do servidor COM da seguinte maneira:

-   Ele adiciona um SID do APPID ao token. Ele concede ao APPID SID Full Access na DACL (lista de controle de acesso discricionário) padrão do token. no Windows Vista e versões posteriores do Windows, ele concede a permissão de controle de leitura de SID OwnerRights \_ na DACL padrão do token. nas versões Windows Vista do Windows, ele define o proprietário do token para o SID do APPID.

As considerações de segurança a seguir devem ser levadas em conta ao usar o **\_ processo de servidor seguro APPIDREGFLAGS do SD e o sinalizador \_ \_ \_ \_ de \_ ligação** :

-   O **sinalizador \_ \_ \_ \_ SD \_ e \_ BIND do APPIDREGFLAGS Secure Server** deve ser definido por servidores com que são iniciados em um dos contextos de segurança do serviço interno; tanto as contas NetworkService quanto LocalService. Se os servidores representarem clientes privilegiados e se o sinalizador **\_ \_ \_ \_ SD \_ e \_ BIND do APPIDREGFLAGS Secure Server** não estiver definido, o código mal-intencionado em execução em outros processos com o mesmo contexto de segurança poderá elevar o privilégio ao seqüestrar os tokens de representação dos clientes com privilégios do processo do servidor com.
-   Quando o **sinalizador \_ \_ \_ \_ SD \_ and \_ BIND do processo de servidor seguro do APPIDREGFLAGS** é definido, o com protege o descritor de segurança do objeto de processo no caso de servidores com "ativados" do runas. Para esses servidores, espera-se que o cliente COM proteja o token que ele usa para a ativação COM.
-   Quando o **sinalizador \_ \_ \_ \_ SD \_ and \_ BIND do processo do servidor seguro do APPIDREGFLAGS** é definido, o com protege o descritor de segurança do objeto de processo no caso dos servidores com "este usuário" do runas. Ele também protege o token do processo do servidor COM, já que o SCM COM é a entidade que cria o token.

o **sinalizador \_ \_ \_ \_ SD \_ e \_ BIND do processo APPIDREGFLAGS SECURE SERVER** tem suporte no Windows XP, Windows server 2003, Windows Vista e Windows server 2008 somente quando o patch MSRC8322 ([boletim de segurança MS09-012](https://support.microsoft.com/kb/959454)) é aplicado. há suporte nativo no Windows 7 e em versões posteriores do Windows.

O **sinalizador \_ \_ \_ \_ SD \_ e \_ BIND do APPIDREGFLAGS Secure Server** aplica-se somente a servidores com que são configurados para executar como runas "Activator" ou "este usuário". Ele não se aplica a servidores COM que são serviços NT.

### <a name="appidregflags_issue_activation_rpc_at_identify-description"></a>\_ \_ RPC de ativação do problema APPIDREGFLAGS \_ \_ na \_ Descrição da identificação

Se o **RPC de ativação do problema de APPIDREGFLAGS no sinalizador de \_ \_ \_ \_ \_ identificação** estiver definido em **AppIDFlags**, o SCM com emitirá solicitações de ativação do objeto para o processo do servidor com usando um nível de representação de [identificação do nível de imp do RPC \_ C \_ \_ \_](impersonation-levels.md).

Se o sinalizador de **ativação do problema de APPIDREGFLAGS não estiver definido, o SCM com emitirá \_ \_ \_ \_ \_** solicitações de ativação de objeto para os processos de servidor com usando um nível de representação de [Impersonate de nível de imp do RPC \_ C \_ \_ \_](impersonation-levels.md).

As considerações de segurança a seguir devem ser levadas em conta ao usar o **\_ RPC de ativação do problema APPIDREGFLAGS no sinalizador \_ \_ \_ de \_ identificação** :

-   O **\_ RPC de ativação do problema APPIDREGFLAGS \_ \_ \_ no \_** sinalizador de identificação deve ser usado por servidores com que não executam o trabalho em nome de clientes em solicitações de ativação de objeto. para esses servidores, ter as solicitações de ativação do objeto de emissão de SCM no [RPC \_ C \_ IMP \_ level \_ identifica](impersonation-levels.md) minimiza as chances de tokens com privilégios com ES representar o nível de [**\_ \_ nome**](/windows/desktop/SecAuthZ/privilege-constants) que aparece no processo.

o **APPIDREGFLAGS de \_ ativação do problema de \_ \_ RPC \_ no \_** sinalizador de identificação tem suporte no Windows 7 e em versões posteriores do Windows.

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

[Estações de janela](/windows/desktop/winstation/window-stations)
</dt> </dl>

 

 