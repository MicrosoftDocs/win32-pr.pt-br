---
description: Conectar-se a um namespace do WMI em um computador remoto pode exigir que você altere as configurações do firewall do Windows, UAC (controle de conta de usuário), DCOM ou Gerenciador de objetos do modelo CIM (CIMOm).
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
ms.openlocfilehash: 6ee254e12ecd806cd286d4a55746e203a3136b6c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104505715"
---
# <a name="setting-up-a-remote-wmi-connection"></a>Configurando uma conexão WMI remota

Conectar-se a um namespace do WMI em um computador remoto pode exigir que você altere as configurações do [Firewall do Windows](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc754274(v=ws.11)), [UAC (controle de conta de usuário)](/previous-versions/aa905108(v=msdn.10)), DCOM ou gerenciador de objetos do modelo CIM (CIMOM).

As seções a seguir são discutidas neste tópico:

-   [Configurações do firewall do Windows](#windows-firewall-settings)
-   [Configurações de controle de conta de usuário](#user-account-control-settings)
-   [Configurações do DCOM](#dcom-settings)
-   [Configurações de CIMOm](#cimom-settings)
-   [Tópicos relacionados](#related-topics)

## <a name="windows-firewall-settings"></a>Configurações de Firewall do Windows

As configurações do WMI para as configurações do firewall do Windows habilitam apenas conexões WMI, em vez de outros aplicativos DCOM.

Uma exceção deve ser definida no firewall para WMI no computador de destino remoto. A exceção para o WMI permite que o WMI receba conexões remotas e retornos de chamada assíncronos para Unsecapp.exe. Para obter mais informações, consulte [definindo a segurança em uma chamada assíncrona](setting-security-on-an-asynchronous-call.md).

Se um aplicativo cliente criar seu próprio coletor, esse coletor deverá ser explicitamente adicionado às exceções de firewall para permitir que os retornos de chamada sejam bem-sucedidos.

A exceção para o WMI também funcionará se o WMI tiver sido iniciado com uma porta fixa, usando o comando **/standalonehost winmgmt** . Para obter mais informações, consulte [Configurando uma porta fixa para o WMI](setting-up-a-fixed-port-for-wmi.md).

Você pode habilitar ou desabilitar o tráfego WMI por meio da interface do usuário do firewall do Windows.

**Para habilitar ou desabilitar o tráfego WMI usando a interface do usuário do firewall**

1.  No **painel de controle**, clique em **segurança** e, em seguida, clique em Firewall do **Windows**.
2.  Clique em **alterar configurações** e, em seguida, clique na guia **exceções** .
3.  Na janela exceções, marque a caixa de seleção **Instrumentação de gerenciamento do Windows (WMI)** para habilitar o tráfego WMI por meio do firewall. Para desabilitar o tráfego WMI, desmarque a caixa de seleção.

Você pode habilitar ou desabilitar o tráfego WMI por meio do firewall no prompt de comando.

**Para habilitar ou desabilitar o tráfego WMI no prompt de comando usando o grupo de regras do WMI**

-   Use os comandos a seguir em um prompt de comando. Digite o seguinte para habilitar o tráfego WMI por meio do firewall.

    **netsh advfirewall firewall set rule Group = "Instrumentação de gerenciamento do Windows (WMI)" novo Enable = Yes**

    Digite o comando a seguir para desabilitar o tráfego WMI por meio do firewall.

    **netsh advfirewall firewall set rule Group = "Instrumentação de gerenciamento do Windows (WMI)" novo Enable = no**

Em vez de usar o comando de grupo de regras de WMI único, você também pode usar comandos individuais para cada um dos serviços DCOM, WMI e coletor.

**Para habilitar o tráfego WMI usando regras separadas para DCOM, WMI, coletor de retorno de chamada e conexões de saída**

1.  Para estabelecer uma exceção de firewall para a porta DCOM 135, use o comando a seguir.

    **netsh advfirewall firewall Adicionar regra dir = in name = "DCOM" Program =% raiz_do_sistema% \\ system32 \\svchost.exe Service = RPCSS Action = Allow Protocol = TCP localPort = 135**

2.  Para estabelecer uma exceção de firewall para o serviço WMI, use o comando a seguir.

    **netsh advfirewall firewall add rule dir = in name = "WMI" programa =% SystemRoot% \\ system32 \\svchost.exe Service = winmgmt Action = permitir protocolo = TCP localPort = any**

3.  Para estabelecer uma exceção de firewall para o coletor que recebe retornos de chamada de um computador remoto, use o comando a seguir.

    **netsh advfirewall firewall add rule dir = in name = "UnsecApp" programa =% SystemRoot% \\ System32 \\ WBEM \\unsecapp.exe ação = permitir**

4.  Para estabelecer uma exceção de firewall para conexões de saída com um computador remoto em que o computador local está se comunicando de forma assíncrona, use o comando a seguir.

    **netsh advfirewall firewall add rule dir = out Name = "WMI \_ out" programa =% SystemRoot% \\ System32 \\svchost.exe Service = winmgmt Action = permitir protocolo = TCP localPort = any**

Para desabilitar as exceções de firewall separadamente, use os comandos a seguir.

**Para desabilitar o tráfego WMI usando regras separadas para DCOM, WMI, coletor de retorno de chamada e conexões de saída**

1.  Para desabilitar a exceção DCOM.

    **netsh advfirewall firewall delete rule name = "DCOM"**

2.  Para desabilitar a exceção do serviço WMI.

    **netsh advfirewall firewall delete rule name = "WMI"**

3.  Para desabilitar a exceção de coletor.

    **netsh advfirewall firewall delete rule name = "UnsecApp"**

4.  Para desabilitar a exceção de saída.

    **netsh advfirewall firewall delete rule name = "WMI \_ out"**

## <a name="user-account-control-settings"></a>Configurações de controle de conta de usuário

Acesso de controle de conta de usuário (UAC)-a filtragem de token pode afetar quais operações são permitidas em namespaces WMI ou quais dados são retornados. No UAC, todas as contas no grupo Administradores local são executadas com um [*token de acesso*](/windows/desktop/SecGloss/a-gly)de usuário padrão, também conhecido como filtragem de token de acesso do UAC. Uma conta de administrador pode executar um script com um privilégio elevado: "executar como administrador".

Quando você não estiver se conectando à conta de administrador interno, o UAC afetará as conexões com um computador remoto de forma diferente, dependendo se os dois computadores estão em um domínio ou em um grupo de trabalho. Para obter mais informações sobre o UAC e conexões remotas, consulte [controle de conta de usuário e WMI](user-account-control-and-wmi.md).

## <a name="dcom-settings"></a>Configurações do DCOM

Para obter mais informações sobre as configurações do DCOM, consulte [protegendo uma conexão WMI remota](securing-a-remote-wmi-connection.md). No entanto, o UAC afeta as conexões para contas de usuário que não são de domínio. Se você se conectar a um computador remoto usando uma conta de usuário que não seja de domínio incluída no grupo local de administradores do computador remoto, você deverá conceder explicitamente acesso remoto DCOM, ativação e direitos de inicialização à conta.

## <a name="cimom-settings"></a>Configurações de CIMOm

As configurações de CIMOm devem ser atualizadas se a conexão remota estiver entre computadores que não têm uma relação de confiança; caso contrário, uma conexão assíncrona falhará. Essa configuração não deve ser modificada para computadores no mesmo domínio ou em domínios confiáveis.

A seguinte entrada do registro precisa ser modificada para permitir retornos de chamada anônimos:

**HKEY \_ \_Computador local** \\ **software** \\ **Microsoft** \\ **WBEM** \\ **CIMOM** \\ **AllowAnonymousCallback**<dl> <dt>

               Data type
</dt> <dd>               REG \_ DWORD</dd> </dl>

Se o valor de **AllowAnonymousCallback** for definido como 0, o serviço WMI impedirá retornos de chamada anônimos para o cliente. Se o valor for definido como 1, o serviço WMI permitirá retornos de chamada anônimos para o cliente.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Conectando-se ao WMI em um computador remoto](connecting-to-wmi-on-a-remote-computer.md)
</dt> </dl>

 

 
