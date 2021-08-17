---
description: Para se conectar a um computador remoto usando o WMI, verifique se as configurações de DCOM corretas e as configurações de segurança do namespace WMI estão habilitadas para a conexão.
ms.assetid: 96ebaa9b-a062-4300-a637-8eb71cb80d1c
ms.tgt_platform: multiple
title: Protegendo uma conexão WMI remota
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8650ee47c549121a51e5d131055a84c176da944c6146f0532ffc86f1d2f9e4c6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117739510"
---
# <a name="securing-a-remote-wmi-connection"></a>Protegendo uma conexão WMI remota

Para se conectar a um computador remoto usando o WMI, verifique se as configurações de DCOM corretas e as configurações de segurança do namespace WMI estão habilitadas para a conexão.

O WMI tem configurações padrão de representação, autenticação e serviço de autenticação (NTLM ou Kerberos) que o computador de destino em uma conexão remota exige. Seu computador local pode usar padrões diferentes que o sistema de destino não aceita. Você pode alterar essas configurações na chamada de conexão.

As seções a seguir são discutidas neste tópico:

-   [Configurações de autenticação e representação DCOM para WMI](#dcom-impersonation-and-authentication-settings-for-wmi)
-   [Definindo a segurança DCOM para permitir que um usuário acesse um computador remotamente](#setting-dcom-security-to-allow-a-user-to-access-a-computer-remotely)
-   [Permitindo que os usuários acessem um namespace WMI específico](#allowing-users-access-to-a-specific-wmi-namespace)
-   [Definindo a segurança do namespace para exigir a criptografia de dados para conexões remotas](#setting-namespace-security-to-require-data-encryption-for-remote-connections)
-   [Tópicos relacionados](#related-topics)

## <a name="dcom-impersonation-and-authentication-settings-for-wmi"></a>Configurações de autenticação e representação DCOM para WMI

O WMI tem configurações de representação, autenticação e serviço de autenticação (NTLM ou Kerberos) padrão do DCOM que o sistema remoto exige. Seu sistema local pode usar padrões diferentes que o sistema remoto de destino não aceita. Você pode alterar essas configurações na chamada de conexão. Para obter mais informações, consulte [definindo a segurança do processo do aplicativo cliente](setting-client-application-process-security.md). No entanto, para o serviço de autenticação, é recomendável que você especifique o **\_ \_ \_ padrão de autenticação RPC C** e permitir que o DCOM escolha o serviço apropriado para o computador de destino.

Você pode fornecer configurações em parâmetros para as chamadas para [**CoInitializeSecurity**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) ou [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) em C++. Em scripts, você pode estabelecer configurações de segurança em chamadas para [**SWbemLocator. ConnectServer**](swbemlocator-connectserver.md), em um objeto [**SWbemSecurity**](swbemsecurity.md) ou na cadeia de caracteres do [moniker do identificador](constructing-a-moniker-string.md) de script.

Para obter uma lista de todas as constantes de representação de C++, consulte [definindo o nível de segurança do processo padrão usando C++](setting-the-default-process-security-level-using-c-.md). para obter as constantes de Visual Basic e as cadeias de caracteres de script para usar a conexão do moniker, consulte [definindo o nível de segurança do processo padrão usando o VBScript](setting-the-default-process-security-level-using-vbscript.md).

A tabela a seguir lista as configurações padrão de representação, autenticação e serviço de autenticação do DCOM exigidas pelo computador de destino (computador B) em uma conexão remota. Para obter mais informações, consulte protegendo uma conexão WMI remota.



| Sistema operacional do computador B | Cadeia de caracteres de script de nível de representação | Cadeia de caracteres de script do nível de autenticação | Serviço de autenticação |
|-----------------------------|--------------------------------------|---------------------------------------|------------------------|
| Windows Vista ou posterior      | Impersonate                          | PCT                                   | Kerberos               |



 

as conexões remotas do WMI são afetadas pelo [controle de conta de usuário (UAC)](/previous-versions/aa905108(v=msdn.10)) e pelo [Firewall Windows](https://www.microsoft.com/technet/itsolutions/network/wf/default.mspx). para obter mais informações, consulte [conectando-se ao WMI remotamente a partir do Vista](connecting-to-wmi-remotely-starting-with-vista.md) e [conectando por meio do Firewall Windows](/windows/desktop/WmiSdk/connecting-to-wmi-remotely-starting-with-vista).

Lembre-se de que conectar-se ao WMI no computador local tem um nível de autenticação padrão de **PktPrivacy**.

## <a name="setting-dcom-security-to-allow-a-user-to-access-a-computer-remotely"></a>Definindo a segurança DCOM para permitir que um usuário acesse um computador remotamente

A segurança no WMI está relacionada à conexão com um namespace WMI. O WMI usa DCOM para lidar com chamadas remotas. Um motivo para a falha de conexão a um computador remoto é devido a uma falha DCOM (erro "DCOM Access Denied" decimal-2147024891 ou hex 0x80070005). Para obter mais informações sobre segurança DCOM no WMI para aplicativos C++, consulte [definindo a segurança do processo do aplicativo cliente](setting-client-application-process-security.md).

Você pode definir as configurações do DCOM para o WMI usando o utilitário de configuração do DCOM (**DCOMCnfg.exe**) encontrado em **Ferramentas administrativas** no **painel de controle**. Esse utilitário expõe as configurações que permitem que determinados usuários se conectem ao computador remotamente por meio do DCOM. Os membros do grupo Administradores têm permissão para se conectar remotamente ao computador por padrão. Com esse utilitário, você pode definir a segurança para iniciar, acessar e configurar o serviço WMI.

O procedimento a seguir descreve como conceder permissões de inicialização remota DCOM e ativação para determinados usuários e grupos. Se o computador A estiver se conectando remotamente ao computador B, você poderá definir essas permissões no computador B para permitir que um usuário ou grupo que não faça parte do grupo Administradores no computador B execute chamadas de inicialização e ativação do DCOM no computador B.

**Para conceder permissões de inicialização remota de DCOM e ativação para um usuário ou grupo**

1.  Clique em **Iniciar**, **executar**, digite **DCOMCNFG** e clique em **OK**.
2.  Na caixa de diálogo **serviços de componentes** , expanda **serviços de componentes**, expanda **computadores** e clique com o botão direito do mouse em **meu computador** e clique em **Propriedades**.
3.  Na caixa de diálogo **Propriedades do meu computador** , clique na guia **segurança com** .
4.  Em **permissões de inicialização e ativação**, clique em **Editar limites**.
5.  Na caixa de diálogo **permissão de inicialização** , siga estas etapas se o seu nome ou grupo não aparecer na **lista grupos ou nomes de usuário**:

    1.  Na caixa de diálogo **permissão de inicialização** , clique em **Adicionar**.
    2.  Na caixa de diálogo **Selecionar usuários, computadores ou grupos** , adicione seu nome e o grupo na caixa **digite os nomes de objeto a serem selecionados** e clique em **OK**.

6.  Na caixa de diálogo **permissão de inicialização** , selecione o usuário e o grupo na caixa **nomes de grupo ou de usuário** . Na coluna **permitir** em **permissões para usuário**, selecione **inicialização remota** e selecione **ativação remota** e clique em **OK**.

O procedimento a seguir descreve como conceder permissões de acesso remoto DCOM para determinados usuários e grupos. Se o computador A estiver se conectando remotamente ao computador B, você poderá definir essas permissões no computador B para permitir que um usuário ou grupo que não faça parte do grupo de administradores no computador B se conecte ao computador B.

**Para conceder permissões de acesso remoto DCOM**

1.  Clique em **Iniciar**, **executar**, digite **DCOMCNFG** e clique em **OK**.
2.  Na caixa de diálogo **serviços de componentes** , expanda **serviços de componentes**, expanda **computadores** e clique com o botão direito do mouse em **meu computador** e clique em **Propriedades**.
3.  Na caixa de diálogo **Propriedades do meu computador** , clique na guia **segurança com** .
4.  Em **permissões de acesso**, clique em **Editar limites**.
5.  Na caixa de diálogo **permissão de acesso** , selecione nome de **logon anônimo** na caixa **nomes de grupo ou de usuário** . Na coluna **permitir** , em **permissões para usuário**, selecione **acesso remoto** e clique em **OK**.

## <a name="allowing-users-access-to-a-specific-wmi-namespace"></a>Permitindo que os usuários acessem um namespace WMI específico

Você pode permitir ou impedir que os usuários acessem um namespace WMI específico definindo a permissão "Habilitar remotamente" no controle WMI para um namespace. Se um usuário tentar se conectar a um namespace ao qual ele não tem permissão de acesso, ele receberá o erro 0x80041003. Por padrão, essa permissão é habilitada somente para administradores. Um administrador pode habilitar o acesso remoto a namespaces WMI específicos para um usuário não administrador.

O procedimento a seguir define permissões de habilitação remota para um usuário não administrador.

**Para definir permissões de habilitação remota**

1.  Conexão ao computador remoto usando o controle WMI.

    Para obter mais informações sobre o controle WMI, consulte [definindo a segurança do namespace com o controle WMI](setting-namespace-security-with-the-wmi-control.md).

2.  Na guia **segurança** , selecione o namespace e clique em **segurança**.
3.  Localize a conta apropriada e marque **habilitar remotamente** na lista de **permissões** .

## <a name="setting-namespace-security-to-require-data-encryption-for-remote-connections"></a>Definindo a segurança do namespace para exigir a criptografia de dados para conexões remotas

Um administrador ou um arquivo MOF pode configurar um namespace do WMI para que nenhum dado seja retornado, a menos que você use a privacidade do pacote (a **privacidade do PCT do \_ nível de \_ autenticação RPC \_ \_ \_ C** ou **PktPrivacy** como um moniker em um script) em uma conexão com esse namespace. Isso garante que os dados sejam criptografados enquanto atravessam a rede. Se você tentar definir um nível de autenticação inferior, receberá uma mensagem de acesso negado. Para obter mais informações, consulte [exigindo uma conexão criptografada para um namespace](requiring-an-encrypted-connection-to-a-namespace.md).

O exemplo de código VBScript a seguir mostra como se conectar a um namespace criptografado usando "pktPrivacy".


```VB
strComputer = "RemoteComputer"
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate,authenticationLevel=pktPrivacy}!\\" _
                              & strComputer & "\root\EncryptedNamespace")
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Delegando com WMI](connecting-to-a-3rd-computer-delegation.md)
</dt> <dt>

[Criando processos remotamente com o WMI](creating-processes-remotely.md)
</dt> <dt>

[Protegendo clientes e provedores do C++](securing-c---clients-and-providers.md)
</dt> <dt>

[Protegendo clientes de script](securing-scripting-clients.md)
</dt> </dl>

 

 
