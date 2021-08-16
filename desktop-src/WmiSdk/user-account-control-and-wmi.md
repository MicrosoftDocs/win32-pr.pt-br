---
description: O UAC (Controle de Conta de Usuário) afeta os dados WMI retornados de uma ferramenta de linha de comando, acesso remoto e como os scripts devem ser executados. Para obter mais informações sobre o UAC, consulte Ponto de Partida com o Controle de Conta de Usuário.
ms.assetid: f6840aaa-834b-42c8-b641-01c570078fcb
ms.tgt_platform: multiple
title: Controle de conta de usuário e WMI
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 2da001117fa75ccef737647038d3e58b942f666ba40e1fd14ec98cb4ebdd44af
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118553312"
---
# <a name="user-account-control-and-wmi"></a>Controle de conta de usuário e WMI

O UAC (Controle de Conta de Usuário) afeta os dados WMI retornados de uma ferramenta de linha de comando, acesso remoto e como os scripts devem ser executados. Para obter mais informações sobre o UAC, [consulte Ponto de Partida com o Controle de Conta de Usuário](https://support.microsoft.com/help/922708/how-to-use-user-account-control-uac-in-windows-vista).

As seções a seguir descrevem a funcionalidade do UAC:

-   [Controle de conta de usuário](#user-account-control-and-wmi)
-   [Conta necessária para executar as ferramentas de Command-Line WMI](#account-needed-to-run-wmi-command-line-tools)
-   [Manipulando conexões remotas em UAC](#handling-remote-connections-under-uac)
-   [Efeito UAC nos dados WMI retornados para scripts ou aplicativos](#uac-effect-on-wmi-data-returned-to-scripts-or-applications)
-   [Tópicos relacionados](#related-topics)

## <a name="user-account-control"></a>Controle de Conta de Usuário

Em UAC, as contas no grupo administradores locais têm dois [*tokens*](/windows/desktop/SecGloss/a-gly)de acesso, um com privilégios de usuário padrão e outro com privilégios de administrador. Devido à filtragem de token de acesso UAC, um script normalmente é executado sob o token de usuário padrão, a menos que seja executado "como administrador" no modo de privilégio elevado. Nem todos os scripts exigiam privilégios administrativos.

Os scripts não podem determinar programaticamente se eles estão sendo executados em um token de segurança de usuário padrão ou um token de Administrador. O script pode falhar com um erro de acesso negado. Se o script exigir privilégios de administrador, ele deverá ser executado no modo elevado. O acesso a namespaces WMI difere dependendo se o script é executado no modo elevado. Algumas operações WMI, como obter dados ou executar a maioria dos métodos, não exigem que a conta seja executada como administrador. Para obter mais informações sobre permissões de acesso padrão, consulte [Access to WMI Namespaces](access-to-wmi-namespaces.md) and [Executing Privileged Operations](executing-privileged-operations.md).

Devido ao Controle de Conta de Usuário, a conta que executa o script deve estar no grupo Administradores no computador local para ter a capacidade de executar com direitos elevados.

Você pode executar um script ou um aplicativo com direitos elevados executando um dos seguintes métodos:

**Para executar um script no modo elevado**

1.  Abra uma janela do Prompt de Comando clicando com o botão direito do mouse em Prompt de Comando no menu Iniciar e, em seguida, clicando em **Executar como administrador.**
2.  Agende o script para ser executado com elevação usando Agendador de Tarefas. Para obter mais informações, consulte [Contextos de segurança para executar tarefas](/windows/desktop/TaskSchd/security-contexts-for-running-tasks).
3.  Execute o script usando a conta de Administrador integrado.

## <a name="account-needed-to-run-wmi-command-line-tools"></a>Conta necessária para executar as ferramentas de Command-Line WMI

Para executar o [seguinte WMI Command-Line Ferramentas](wmi-command-line-tools.md), sua conta deve estar no grupo Administradores e a ferramenta deve ser executado em um prompt de comando com privilégios elevados. A conta de administrador integrado também pode executar essas ferramentas.

-   [**mofcomp**](mofcomp.md)

-   [**wmic**](wmic.md)

    Na primeira vez que você executar o Wmic após a instalação do sistema, ele deverá ser executado em um prompt de comando com elevado. O modo elevado pode não ser necessário para execuções subsequentes do Wmic, a menos que as operações WMI exigem privilégio de administrador.

-   [**Winmgmt**](winmgmt.md)

-   [**wmiadap**](wmiadap.md)

Para executar o [*WMI Control*](gloss-w.md) (Wmimgmt.msc) e fazer alterações nas configurações de segurança ou auditoria do namespace WMI, sua conta deve ter o direito Editar Segurança explicitamente concedido ou estar no grupo Local de Administradores. A conta de Administrador interna também pode alterar a segurança ou a auditoria de um namespace.

Wbemtest.exe, uma ferramenta de linha de comando que não é suportada pelos serviços de Suporte ao Cliente da Microsoft, pode ser executado por contas que não estão no grupo administradores local, a menos que uma operação específica exija privilégios que normalmente são concedidos a contas de administrador.

## <a name="handling-remote-connections-under-uac"></a>Manipulando conexões remotas em UAC

Se você está se conectando a um computador remoto em um domínio ou em um grupo de trabalho determina se a filtragem de UAC ocorre.

Se o computador faz parte de um domínio, conecte-se ao computador de destino usando uma conta de domínio que está no grupo administradores local do computador remoto. Em seguida, a filtragem de token de acesso do UAC não afetará as contas de domínio no grupo administradores local. Não use uma conta local e não local no computador remoto, mesmo se a conta estiver no grupo Administradores.

Em um grupo de trabalho, a conta que se conecta ao computador remoto é um usuário local nesse computador. Mesmo se a conta estiver no grupo Administradores, a filtragem de UAC significa que um script é executado como um usuário padrão. Uma melhor prática é criar um grupo de usuários local dedicado ou uma conta de usuário no computador de destino especificamente para conexões remotas.

A segurança deve ser ajustada para poder usar essa conta porque a conta nunca teve privilégios administrativos. Dê ao usuário local:

-   Iniciar e ativar direitos remotos para acessar o DCOM. Para obter mais informações, [consulte Conectando-se ao WMI em um computador remoto.](connecting-to-wmi-on-a-remote-computer.md)
-   Direitos para acessar o namespace WMI remotamente (Habilitar Remotamente). Para obter mais informações, [consulte Acesso a namespaces WMI](access-to-wmi-namespaces.md).
-   Direito de acessar o objeto seguro específico, dependendo da segurança exigida pelo objeto .

Se você usar uma conta local, por estar em um grupo de trabalho ou por ser uma conta de computador local, poderá ser forçado a dar tarefas específicas a um usuário local. Por exemplo, você pode conceder ao usuário o direito de parar ou iniciar um serviço específico por meio do comando SC.exe, dos métodos [**GetSecurityDescriptor**](/windows/desktop/CIMWin32Prov/getsecuritydescriptor-method-in-class-win32-service) e [**SetSecurityDescriptor**](/windows/desktop/CIMWin32Prov/setsecuritydescriptor-method-in-class-win32-service) do [**Serviço Win32 \_**](/windows/desktop/CIMWin32Prov/win32-service)ou por meio do Política de Grupo usando Gpedit.msc. Alguns objetos de segurança podem não permitir que um usuário padrão execute tarefas e não ofereça nenhum meio de alterar a segurança padrão. Nesse caso, talvez seja necessário desabilitar o UAC para que a conta de usuário local não seja filtrada e, em vez disso, se torne um administrador completo. Esteja ciente de que, por motivos de segurança, desabilitar o UAC deve ser um último recurso.

Desabilitar o UAC Remoto alterando a entrada do Registro que controla o UAC remoto não é recomendado, mas pode ser necessário em um grupo de trabalho. A entrada do Registro é **HKEY \_ LOCAL \_ MACHINE** \\ **SOFTWARE** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **Policies** \\ **system** \\ **LocalAccountTokenFilterPolicy**. Quando o valor dessa entrada é zero (0), a filtragem de token de acesso UAC remoto é habilitada. Quando o valor for 1, o UAC remoto será desabilitado.

## <a name="uac-effect-on-wmi-data-returned-to-scripts-or-applications"></a>Efeito UAC nos dados WMI retornados para scripts ou aplicativos

Se um script ou aplicativo estiver em execução em uma conta no grupo Administradores, mas não estiver em execução com um privilégio elevado, talvez você não receba todos os dados retornados porque essa conta está sendo executado como um usuário padrão. Os [*provedores*](gloss-p.md) WMI para algumas classes não retornam todas as instâncias para uma conta de usuário padrão ou uma conta de Administrador que não está sendo executado como administrador completo devido à filtragem de UAC.

As classes a seguir não retornam algumas instâncias quando a conta é filtrada pelo UAC:

-   [**Barramento \_ Win32**](/windows/desktop/CIMWin32Prov/win32-bus)
-   [**Impressora \_ Win32**](/windows/desktop/CIMWin32Prov/win32-printer)
-   [**Componente \_ Win32Categoria**](/windows/desktop/CIMWin32Prov/win32-componentcategory)
-   [**Win32 \_ LogicalProgramGroupItem**](/windows/desktop/CIMWin32Prov/win32-logicalprogramgroupitem)
-   [**Win32 \_ LogicalProgramGroup**](/windows/desktop/CIMWin32Prov/win32-logicalprogramgroup)
-   [**Win32 \_ NetworkConnection**](/windows/desktop/CIMWin32Prov/win32-networkconnection)
-   [**Win32 \_ UserAccount**](/windows/desktop/CIMWin32Prov/win32-useraccount)
-   [**Win32 \_ PrinterDriver**](/windows/desktop/CIMWin32Prov/win32-printerdriver)
-   [**Win32 \_ PortResource**](/windows/desktop/CIMWin32Prov/win32-portresource)
-   [**Win32 \_ DeviceMemoryAddress**](/windows/desktop/CIMWin32Prov/win32-devicememoryaddress)

As classes a seguir não retornam algumas propriedades quando a conta é filtrada pelo UAC:

-   [**Win32 \_ NetworkAdapterConfiguration**](/windows/desktop/CIMWin32Prov/win32-networkadapterconfiguration)
-   [**Win32 \_ DCOMApplicationSetting**](/windows/desktop/CIMWin32Prov/win32-dcomapplicationsetting)
-   [**Win32 \_ DCOMApplication**](/windows/desktop/CIMWin32Prov/win32-dcomapplication)
-   [**Placa base do Win32 \_**](/windows/desktop/CIMWin32Prov/win32-baseboard)
-   [**Win32 \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/win32-computersystem)
-   [**Win32 \_ NetworkAdapter**](/windows/desktop/CIMWin32Prov/win32-networkadapter)
-   [**Win32 \_ MotherboardDevice**](/windows/desktop/CIMWin32Prov/win32-motherboarddevice)
-   [**Win32 \_ DiskDrive**](/windows/desktop/CIMWin32Prov/win32-diskdrive)
-   [**Win32 \_ PnPEntity**](/windows/desktop/CIMWin32Prov/win32-pnpentity)
-   [**VideoController do Win32 \_**](/windows/desktop/CIMWin32Prov/win32-videocontroller)
-   [**Win32 \_ ParallelPort**](/windows/desktop/CIMWin32Prov/win32-parallelport)
-   [**LogicalDisk do Win32 \_**](/windows/desktop/CIMWin32Prov/win32-logicaldisk)
-   [**Win32 \_ SystemDriver**](/windows/desktop/CIMWin32Prov/win32-systemdriver)
-   [**Win32 \_ IRQResource**](/windows/desktop/CIMWin32Prov/win32-irqresource)
-   [**Win32 \_ NetworkProtocol**](/windows/desktop/CIMWin32Prov/win32-networkprotocol)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sobre o WMI](about-wmi.md)
</dt> <dt>

[Acesso a objetos de segurança WMI](access-to-wmi-securable-objects.md)
</dt> <dt>

[Alterando a segurança de acesso em objetos securáveis](changing-access-security-on-securable-objects.md)
</dt> </dl>

 

 
