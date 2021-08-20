---
description: Conectar-se a um namespace WMI em um computador remoto pode exigir que você altere as configurações do Firewall do Windows, UAC (Controle de Conta de Usuário), DCOM ou CIMOM (gerenciador de objetos modelo CIM).
ms.assetid: 028b3101-0945-4288-bf32-ef4ad12a55f9
ms.tgt_platform: multiple
title: Configurando uma conexão WMI remota
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: b88aa453646e60bf17e31f1197d76506bb4f75453eb800dc0fa272946a3bf8df
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117925698"
---
# <a name="setting-up-a-remote-wmi-connection"></a>Configurando uma conexão WMI remota

Conectar-se a um namespace WMI em um computador remoto pode exigir que você altere as configurações do Firewall do [Windows,](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc754274(v=ws.11)) [UAC (Controle](/previous-versions/aa905108(v=msdn.10))de Conta de Usuário), DCOM ou CIMOM (gerenciador de objetos modelo CIM).

As seções a seguir são discutidas neste tópico:

-   [Windows Firewall Configurações](#windows-firewall-settings)
-   [Configurações de controle de conta de usuário](#user-account-control-settings)
-   [DCOM Configurações](#dcom-settings)
-   [CIMOM Configurações](#cimom-settings)
-   [Tópicos relacionados](#related-topics)

## <a name="windows-firewall-settings"></a>Configurações de Firewall do Windows

As configurações de WMI para Windows firewall permitem apenas conexões WMI, em vez de outros aplicativos DCOM também.

Uma exceção deve ser definida no firewall para WMI no computador de destino remoto. A exceção para WMI permite que o WMI receba conexões remotas e retornos de chamada assíncronos para Unsecapp.exe. Para obter mais informações, consulte [Configurando a segurança em uma chamada assíncrona](setting-security-on-an-asynchronous-call.md).

Se um aplicativo cliente criar seu próprio sink, esse sink deverá ser adicionado explicitamente às exceções de firewall para permitir que os retornos de chamada sejam bem-sucedidos.

A exceção para WMI também funcionará se o WMI tiver sido iniciado com uma porta fixa, usando o **comando winmgmt /standalonehost.** Para obter mais informações, [consulte Configurando uma porta fixa para WMI](setting-up-a-fixed-port-for-wmi.md).

Você pode habilitar ou desabilitar o tráfego WMI por meio da interface do Windows firewall.

**Para habilitar ou desabilitar o tráfego WMI usando a interface do usuário do firewall**

1.  No **Painel de Controle**, clique em **Segurança** e, em **seguida, clique Windows Firewall**.
2.  Clique **em Alterar Configurações** e clique na guia **Exceções.**
3.  Na janela Exceções, marque a caixa de seleção **Windows WMI (Instrumentação** de Gerenciamento) para habilitar o tráfego WMI por meio do firewall. Para desabilitar o tráfego WMI, des marque a caixa de seleção.

Você pode habilitar ou desabilitar o tráfego WMI por meio do firewall no prompt de comando.

**Para habilitar ou desabilitar o tráfego WMI no prompt de comando usando o grupo de regras WMI**

-   Use os comandos a seguir em um prompt de comando. Digite o seguinte para habilitar o tráfego WMI por meio do firewall.

    **netsh advfirewall firewall set rule group="windows management instrumentation (wmi)" new enable=yes**

    Digite o comando a seguir para desabilitar o tráfego WMI por meio do firewall.

    **netsh advfirewall firewall set rule group="windows management instrumentation (wmi)" new enable=no**

Em vez de usar o único comando de grupo de regras WMI, você também pode usar comandos individuais para cada DCOM, serviço WMI e sink.

**Para habilitar o tráfego WMI usando regras separadas para DCOM, WMI, sink de retorno de chamada e conexões de saída**

1.  Para estabelecer uma exceção de firewall para a porta DCOM 135, use o comando a seguir.

    **netsh advfirewall firewall add rule dir=in name="DCOM" program=%systemroot% \\ system32 \\svchost.exe service=rpcss action=allow protocol=TCP localport=135**

2.  Para estabelecer uma exceção de firewall para o serviço WMI, use o comando a seguir.

    **netsh advfirewall firewall add rule dir=in name ="WMI" program=%systemroot% \\ system32 \\svchost.exe service=winmgmt action = allow protocol=TCP localport=any**

3.  Para estabelecer uma exceção de firewall para o sink que recebe retornos de chamada de um computador remoto, use o comando a seguir.

    **netsh advfirewall firewall add rule dir=in name ="UnsecApp" program=%systemroot% \\ system32 \\ wbem \\unsecapp.exe action=allow**

4.  Para estabelecer uma exceção de firewall para conexões de saída para um computador remoto que o computador local está se comunicando de forma assíncrona, use o comando a seguir.

    **netsh advfirewall firewall add rule dir=out name ="WMI \_ OUT" program=%systemroot% \\ system32 \\svchost.exe service=winmgmt action=allow protocol=TCP localport=any**

Para desabilitar as exceções de firewall separadamente, use os comandos a seguir.

**Para desabilitar o tráfego WMI usando regras separadas para DCOM, WMI, sink de retorno de chamada e conexões de saída**

1.  Para desabilitar a exceção DCOM.

    **netsh advfirewall firewall delete rule name="DCOM"**

2.  Para desabilitar a exceção de serviço WMI.

    **netsh advfirewall firewall delete rule name="WMI"**

3.  Para desabilitar a exceção do sink.

    **netsh advfirewall firewall delete rule name="UnsecApp"**

4.  Para desabilitar a exceção de saída.

    **netsh advfirewall firewall delete rule name="WMI \_ OUT"**

## <a name="user-account-control-settings"></a>Configurações de controle de conta de usuário

A filtragem de token de acesso do UAC (Controle de Conta de Usuário) pode afetar quais operações são permitidas em namespaces WMI ou quais dados são retornados. Em UAC, todas as contas no grupo administradores locais são executados com um [*token*](/windows/desktop/SecGloss/a-gly)de acesso de usuário padrão , também conhecido como filtragem de token de acesso UAC. Uma conta de administrador pode executar um script com privilégios elevados— "Executar como Administrador".

Quando você não está se conectando à conta de Administrador, o UAC afeta as conexões com um computador remoto de forma diferente, dependendo se os dois computadores estão em um domínio ou em um grupo de trabalho. Para obter mais informações sobre UAC e conexões remotas, consulte [Controle de Conta de Usuário e WMI](user-account-control-and-wmi.md).

## <a name="dcom-settings"></a>DCOM Configurações

Para obter mais informações sobre as configurações do DCOM, consulte [Proteger uma conexão WMI remota.](securing-a-remote-wmi-connection.md) No entanto, o UAC afeta as conexões para contas de usuário não endêmamas. Se você se conectar a um computador remoto usando uma conta de usuário não endmain incluída no grupo Local de Administradores do computador remoto, deverá conceder explicitamente direitos de acesso DCOM remoto, ativação e início à conta.

## <a name="cimom-settings"></a>CIMOM Configurações

As configurações cimom precisarão ser atualizadas se a conexão remota estiver entre computadores que não têm uma relação de confiança; caso contrário, uma conexão assíncrona falhará. Essa configuração não deve ser modificada para computadores no mesmo domínio ou em domínios confiáveis.

A seguinte entrada do Registro precisa ser modificada para permitir retornos de chamada anônimos:

**HKEY \_ SOFTWARE \_ DE COMPUTADOR LOCAL** \\  \\ **Microsoft** \\ **WBEM** \\ **CIMOM** \\ **AllowAnonymousCallback**<dl> <dt>

               Data type
</dt> <dd>               REG \_ DWORD</dd> </dl>

Se o **valor AllowAnonymousCallback** for definido como 0, o serviço WMI impedirá retornos de chamada anônimos para o cliente. Se o valor for definido como 1, o serviço WMI permitirá retornos de chamada anônimos para o cliente.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Conectando-se ao WMI em um computador remoto](connecting-to-wmi-on-a-remote-computer.md)
</dt> </dl>

 

 
