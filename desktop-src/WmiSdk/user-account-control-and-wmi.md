---
description: O UAC (controle de conta de usuário) afeta os dados do WMI que são retornados de uma ferramenta de linha de comando, acesso remoto e como os scripts devem ser executados. Para obter mais informações sobre o UAC, consulte Introdução com controle de conta de usuário.
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
ms.openlocfilehash: 39d48abcffa537d886397092c6d4a7b558825021
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105796223"
---
# <a name="user-account-control-and-wmi"></a>Controle de conta de usuário e WMI

O UAC (controle de conta de usuário) afeta os dados do WMI que são retornados de uma ferramenta de linha de comando, acesso remoto e como os scripts devem ser executados. Para obter mais informações sobre o UAC, consulte [introdução com controle de conta de usuário](https://support.microsoft.com/help/922708/how-to-use-user-account-control-uac-in-windows-vista).

As seções a seguir descrevem a funcionalidade do UAC:

-   [Controle de conta de usuário](#user-account-control-and-wmi)
-   [Conta necessária para executar as ferramentas de Command-Line WMI](#account-needed-to-run-wmi-command-line-tools)
-   [Manipulando conexões remotas no UAC](#handling-remote-connections-under-uac)
-   [Efeito do UAC nos dados do WMI retornados para scripts ou aplicativos](#uac-effect-on-wmi-data-returned-to-scripts-or-applications)
-   [Tópicos relacionados](#related-topics)

## <a name="user-account-control"></a>Controle de Conta de Usuário

No UAC, as contas no grupo Administradores local têm dois [*tokens de acesso*](/windows/desktop/SecGloss/a-gly), um com privilégios de usuário padrão e um com privilégios de administrador. Devido à filtragem de token de acesso do UAC, um script normalmente é executado sob o token de usuário padrão, a menos que seja executado "como administrador" no modo de privilégio elevado. Nem todos os scripts exigiram privilégios administrativos.

Os scripts não podem determinar programaticamente se estão sendo executados sob um token de segurança de usuário padrão ou um token de administrador. O script pode falhar com um erro de acesso negado. Se o script exigir privilégios de administrador, ele deverá ser executado no modo com privilégios elevados. O acesso aos namespaces do WMI difere dependendo se o script é executado no modo elevado. Algumas operações de WMI, como obter dados ou executar a maioria dos métodos, não exigem que a conta seja executada como administrador. Para obter mais informações sobre permissões de acesso padrão, consulte [acesso a namespaces do WMI](access-to-wmi-namespaces.md) e [execução de operações privilegiadas](executing-privileged-operations.md).

Por causa do controle de conta de usuário, a conta que executa o script deve estar no grupo Administradores no computador local para poder executar com direitos elevados.

Você pode executar um script ou um aplicativo com direitos elevados executando um dos seguintes métodos:

**Para executar um script no modo elevado**

1.  Abra uma janela de prompt de comando clicando com o botão direito do mouse em prompt de comando no menu iniciar e clicando em **Executar como administrador**.
2.  Agende o script para executar com privilégios elevados usando Agendador de Tarefas. Para obter mais informações, consulte [contextos de segurança para tarefas em execução](/windows/desktop/TaskSchd/security-contexts-for-running-tasks).
3.  Execute o script usando a conta de administrador interna.

## <a name="account-needed-to-run-wmi-command-line-tools"></a>Conta necessária para executar as ferramentas de Command-Line WMI

Para executar as seguintes [ferramentas de Command-Line do WMI](wmi-command-line-tools.md), sua conta deve estar no grupo Administradores e a ferramenta deve ser executada em um prompt de comando com privilégios elevados. A conta interna de administrador também pode executar essas ferramentas.

-   [**Mofcomp**](mofcomp.md)

-   [**wmic**](wmic.md)

    Na primeira vez que você executar o WMIC após a instalação do sistema, ele deverá ser executado em um prompt de comando com privilégios elevados. O modo elevado pode não ser necessário para execuções subsequentes do WMIC, a menos que as operações WMI exijam privilégios de administrador.

-   [**winmgmt**](winmgmt.md)

-   [**Wmiadap**](wmiadap.md)

Para executar o [*controle WMI*](gloss-w.md) (wmimgmt. msc) e fazer alterações nas configurações de auditoria ou segurança do namespace WMI, sua conta deve ter o direito de segurança editar explicitamente concedido ou estar no grupo Administradores local. A conta interna de administrador também pode alterar a segurança ou a auditoria de um namespace.

Wbemtest.exe, uma ferramenta de linha de comando que não tem suporte dos serviços de atendimento ao cliente da Microsoft, pode ser executada por contas que não estão no grupo local de administradores, a menos que uma operação específica exija privilégios que normalmente são concedidos a contas de administrador.

## <a name="handling-remote-connections-under-uac"></a>Manipulando conexões remotas no UAC

Se você está se conectando a um computador remoto em um domínio ou em um grupo de trabalho determina se a filtragem UAC ocorre.

Se o computador fizer parte de um domínio, conecte-se ao computador de destino usando uma conta de domínio que esteja no grupo local de administradores do computador remoto. Em seguida, a filtragem de token de acesso do UAC não afetará as contas de domínio no grupo local de administradores. Não use uma conta local e não de domínio no computador remoto, mesmo que a conta esteja no grupo Administradores.

Em um grupo de trabalho, a conta que se conecta ao computador remoto é um usuário local nesse computador. Mesmo que a conta esteja no grupo Administradores, a filtragem UAC significa que um script é executado como usuário padrão. Uma prática recomendada é criar um grupo de usuários local dedicado ou uma conta de usuário no computador de destino especificamente para conexões remotas.

A segurança deve ser ajustada para poder usar essa conta porque a conta nunca teve privilégios administrativos. Forneça ao usuário local:

-   Direitos de inicialização e ativação remotas para acessar DCOM. Para obter mais informações, consulte [conectando-se ao WMI em um computador remoto](connecting-to-wmi-on-a-remote-computer.md).
-   Direitos para acessar o namespace WMI remotamente (habilitação remota). Para obter mais informações, consulte [Access to WMI namespaces](access-to-wmi-namespaces.md).
-   Direito de acessar o objeto protegível específico, dependendo da segurança exigida pelo objeto.

Se você usar uma conta local, porque você está em um grupo de trabalho ou é uma conta de computador local, você pode ser forçado a fornecer tarefas específicas para um usuário local. Por exemplo, você pode conceder ao usuário o direito de parar ou iniciar um serviço específico por meio do comando SC.exe, os métodos [**GetSecurityDescriptor**](/windows/desktop/CIMWin32Prov/getsecuritydescriptor-method-in-class-win32-service) e [**SetSecurityDescriptor**](/windows/desktop/CIMWin32Prov/setsecuritydescriptor-method-in-class-win32-service) do [**\_ serviço Win32**](/windows/desktop/CIMWin32Prov/win32-service)ou por meio de política de grupo usando gpedit. msc. Alguns objetos protegíveis podem não permitir que um usuário padrão execute tarefas e não ofereça nenhum meio de alterar a segurança padrão. Nesse caso, talvez seja necessário desabilitar o UAC para que a conta de usuário local não seja filtrada e, em vez disso, se torne um administrador completo. Lembre-se de que, por motivos de segurança, desabilitar o UAC deve ser um último recurso.

Desabilitar o UAC remoto alterando a entrada do registro que controla o UAC remoto não é recomendado, mas pode ser necessário em um grupo de trabalho. A entrada do registro é **HKEY \_ local \_ Machine** \\ **software** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **Policies** \\ **System** \\ **LocalAccountTokenFilterPolicy**. Quando o valor dessa entrada for zero (0), a filtragem de token de acesso do UAC remoto será habilitada. Quando o valor for 1, o UAC remoto será desabilitado.

## <a name="uac-effect-on-wmi-data-returned-to-scripts-or-applications"></a>Efeito do UAC nos dados do WMI retornados para scripts ou aplicativos

Se um script ou aplicativo estiver sendo executado em uma conta no grupo Administradores, mas não estiver em execução com um privilégio elevado, você não poderá obter todos os dados retornados, pois essa conta está sendo executada como usuário padrão. Os [*provedores*](gloss-p.md) WMI para algumas classes não retornam todas as instâncias para uma conta de usuário padrão ou uma conta de administrador que não está sendo executada como administrador completo devido à filtragem de UAC.

As classes a seguir não retornam algumas instâncias quando a conta é filtrada pelo UAC:

-   [**\_Barramento Win32**](/windows/desktop/CIMWin32Prov/win32-bus)
-   [**\_Impressora Win32**](/windows/desktop/CIMWin32Prov/win32-printer)
-   [**\_ComponentCategory Win32**](/windows/desktop/CIMWin32Prov/win32-componentcategory)
-   [**\_LogicalProgramGroupItem Win32**](/windows/desktop/CIMWin32Prov/win32-logicalprogramgroupitem)
-   [**\_LogicalProgramGroup Win32**](/windows/desktop/CIMWin32Prov/win32-logicalprogramgroup)
-   [**\_NetworkConnection Win32**](/windows/desktop/CIMWin32Prov/win32-networkconnection)
-   [**Conta userwin32 \_**](/windows/desktop/CIMWin32Prov/win32-useraccount)
-   [**\_PrinterDriver Win32**](/windows/desktop/CIMWin32Prov/win32-printerdriver)
-   [**\_PortResource Win32**](/windows/desktop/CIMWin32Prov/win32-portresource)
-   [**\_DeviceMemoryAddress Win32**](/windows/desktop/CIMWin32Prov/win32-devicememoryaddress)

As classes a seguir não retornam algumas propriedades quando a conta é filtrada pelo UAC:

-   [**\_NetworkAdapterConfiguration Win32**](/windows/desktop/CIMWin32Prov/win32-networkadapterconfiguration)
-   [**\_DCOMApplicationSetting Win32**](/windows/desktop/CIMWin32Prov/win32-dcomapplicationsetting)
-   [**\_DCOMApplication Win32**](/windows/desktop/CIMWin32Prov/win32-dcomapplication)
-   [**Placa-base do Win32 \_**](/windows/desktop/CIMWin32Prov/win32-baseboard)
-   [**\_Sistema de ComputerSystem Win32**](/windows/desktop/CIMWin32Prov/win32-computersystem)
-   [**\_Adaptador Win32**](/windows/desktop/CIMWin32Prov/win32-networkadapter)
-   [**\_MotherboardDevice Win32**](/windows/desktop/CIMWin32Prov/win32-motherboarddevice)
-   [**\_DiskDrive Win32**](/windows/desktop/CIMWin32Prov/win32-diskdrive)
-   [**\_PnPEntity Win32**](/windows/desktop/CIMWin32Prov/win32-pnpentity)
-   [**\_VideoController Win32**](/windows/desktop/CIMWin32Prov/win32-videocontroller)
-   [**\_ParallelPort Win32**](/windows/desktop/CIMWin32Prov/win32-parallelport)
-   [**Disco \_ lógico do Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk)
-   [**Systemdrive do Win32 \_**](/windows/desktop/CIMWin32Prov/win32-systemdriver)
-   [**\_IRQResource Win32**](/windows/desktop/CIMWin32Prov/win32-irqresource)
-   [**\_NetworkProtocol Win32**](/windows/desktop/CIMWin32Prov/win32-networkprotocol)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sobre o WMI](about-wmi.md)
</dt> <dt>

[Acesso a objetos protegíveis do WMI](access-to-wmi-securable-objects.md)
</dt> <dt>

[Alterando a segurança de acesso em objetos protegíveis](changing-access-security-on-securable-objects.md)
</dt> </dl>

 

 
