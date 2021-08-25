---
title: Classe Win32_TerminalService
description: Uma subclasse da classe Serviço \_ Win32. Win32 \_ TerminalService representa a propriedade Element da associação Win32 \_ TerminalServiceToSetting.
ms.assetid: 06c69d71-4e6f-48af-b13d-e593b8fcf376
ms.tgt_platform: multiple
keywords:
- Win32_TerminalService classe Serviços de Área de Trabalho Remota
- Win32_TerminalService classe Serviços de Área de Trabalho Remota , descrito
topic_type:
- apiref
api_name:
- Win32_TerminalService
- Win32_TerminalService.AcceptPause
- Win32_TerminalService.AcceptStop
- Win32_TerminalService.Caption
- Win32_TerminalService.CheckPoint
- Win32_TerminalService.CreationClassName
- Win32_TerminalService.DelayedAutoStart
- Win32_TerminalService.Description
- Win32_TerminalService.DesktopInteract
- Win32_TerminalService.DisplayName
- Win32_TerminalService.ErrorControl
- Win32_TerminalService.ExitCode
- Win32_TerminalService.InstallDate
- Win32_TerminalService.Name
- Win32_TerminalService.PathName
- Win32_TerminalService.ProcessId
- Win32_TerminalService.ServiceSpecificExitCode
- Win32_TerminalService.ServiceType
- Win32_TerminalService.Started
- Win32_TerminalService.StartMode
- Win32_TerminalService.StartName
- Win32_TerminalService.State
- Win32_TerminalService.Status
- Win32_TerminalService.SystemCreationClassName
- Win32_TerminalService.SystemName
- Win32_TerminalService.TagId
- Win32_TerminalService.WaitHint
- Win32_TerminalService.DisconnectedSessions
- Win32_TerminalService.TotalSessions
api_location:
- TSCfgWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 735b033017958816e8e9a40caea935847104fdcbe3e9acf3128890d88685d09e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119867846"
---
# <a name="win32_terminalservice-class"></a>Classe Win32 \_ TerminalService

A **classe WMI Win32 \_ TerminalService** é uma subclasse da [**classe Serviço Win32. \_**](/windows/desktop/CIMWin32Prov/win32-service) **Win32 \_ TerminalService** representa **a propriedade Element** da associação [**Win32 \_ TerminalServiceToSetting.**](win32-terminalservicetosetting.md)

A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades definidas e herdadas, em ordem alfabética.

## <a name="syntax"></a>Sintaxe

``` syntax
[dynamic, provider("Win32_WIN32_TERMINALSERVICE_Prov"), ClassContext("local|hkey_local_machine\\SYSTEM\\CurrentControlSet\\Control\\TerminalServer"), AMENDMENT]
class Win32_TerminalService : Win32_Service
{
  boolean  AcceptPause;
  boolean  AcceptStop;
  string   Caption;
  uint32   CheckPoint;
  string   CreationClassName;
  boolean  DelayedAutoStart;
  string   Description;
  boolean  DesktopInteract;
  string   DisplayName;
  string   ErrorControl;
  uint32   ExitCode;
  datetime InstallDate;
  string   Name;
  string   PathName;
  uint32   ProcessId;
  uint32   ServiceSpecificExitCode;
  string   ServiceType;
  boolean  Started;
  string   StartMode;
  string   StartName;
  string   State;
  string   Status;
  string   SystemCreationClassName;
  string   SystemName;
  uint32   TagId;
  uint32   WaitHint;
  uint32   DisconnectedSessions;
  uint32   TotalSessions;
};
```

## <a name="members"></a>Membros

A **classe Win32 \_ TerminalService** tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

A **classe Win32 \_ TerminalService** tem esses métodos.



| Método                                                                       | Descrição                                                                                          |
|:-----------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------|
| [**Alteração**](win32-terminalservice-change.md)                               | Modifica um serviço.<br/>                                                                       |
| [**ChangeStartMode**](win32-terminalservice-changestartmode.md)             | Modifica o modo de início de um serviço.<br/>                                                     |
| [**Criar**](win32-terminalservice-create.md)                               | Cria um serviço novo.<br/>                                                                    |
| [**Excluir**](win32-terminalservice-delete.md)                               | Exclui um serviço existente.<br/>                                                              |
| [**GetSecurityDescriptor**](win32-terminalservice-getsecuritydescriptor.md) | Retorna o descritor de segurança que controla o acesso ao serviço.<br/>                      |
| [**Service**](win32-terminalservice-interrogateservice.md)       | Solicita que um serviço atualize seu estado para o gerenciador de serviços.<br/>                          |
| [**PauseService**](win32-terminalservice-pauseservice.md)                   | Tenta colocar um serviço no estado pausado.<br/>                                          |
| [**ResumeService**](win32-terminalservice-resumeservice.md)                 | Tenta colocar um serviço no estado retomado.<br/>                                         |
| [**SetSecurityDescriptor**](win32-terminalservice-setsecuritydescriptor.md) | Grava uma versão atualizada do descritor de segurança que controla o acesso ao serviço.<br/> |
| [**Startservice**](win32-terminalservice-startservice.md)                   | Tenta colocar um serviço no estado de inicialização.<br/>                                       |
| [**StopService**](win32-terminalservice-stopservice.md)                     | Coloca um serviço no estado parado.<br/>                                                    |
| [**UserControlService**](win32-terminalservice-usercontrolservice.md)       | Tenta enviar um código de controle definido pelo usuário para um serviço.<br/>                                |



 

### <a name="properties"></a>Propriedades

A **classe Win32 \_ TerminalService** tem essas propriedades.

<dl> <dt>

**AcceptPause**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliana**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Service Structures SERVICE \| [**\_ STATUS**](/windows/desktop/api/winsvc/ns-winsvc-service_status) \| dwControlsAccepted \| SERVICE ACCEPT PAUSE \_ \_ \_ CONTINUE"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Service Accepts Pause")
</dt> </dl>

Indica se o serviço pode ser pausado.

Essa propriedade é herdada de [**Win32 \_ BaseService.**](/windows/desktop/CIMWin32Prov/win32-baseservice)

</dd> <dt>

**AcceptStop**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliana**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Service Structures SERVICE \| [**\_ STATUS**](/windows/desktop/api/winsvc/ns-winsvc-service_status) \| dwControlsAccepted \| SERVICE ACCEPT \_ \_ STOP"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Service Accepts Stop")
</dt> </dl>

Indica se o serviço pode ser interrompido.

Essa propriedade é herdada de [**Win32 \_ BaseService.**](/windows/desktop/CIMWin32Prov/win32-baseservice)

</dd> <dt>

**Legenda**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Legenda")
</dt> </dl>

Breve descrição do serviço de uma cadeia de caracteres de uma linha.

Essa propriedade é herdada de [**CIM \_ ManagedSystemElement.**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)

</dd> <dt>

**Checkpoint**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Service Structures SERVICE \| [**\_ STATUS**](/windows/desktop/api/winsvc/ns-winsvc-service_status) \| dwCheckPoint"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Check Point Count")
</dt> </dl>

Valor que o serviço incrementa periodicamente para relatar seu progresso durante uma operação de início longo, parada, pausa ou continuação. Por exemplo, o serviço incrementa esse valor à medida que conclui cada etapa de sua inicialização quando está iniciando. O programa de interface do usuário que invoca a operação no serviço usa esse valor para acompanhar o progresso do serviço durante uma operação demorada. Esse valor não é válido e deve ser zero quando o serviço não tem uma operação de início, parada, pausa ou continuação pendente.

Essa propriedade é herdada do [**Serviço Win32. \_**](/windows/desktop/CIMWin32Prov/win32-service)

</dd> <dt>

**CreationClassName**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**\_ Chave CIM,**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Nome da Classe")
</dt> </dl>

Nome da primeira classe concreta a ser exibida na cadeia de herança usada na criação de uma instância. Quando usada com as outras propriedades de chave da classe , essa propriedade permite que todas as instâncias dessa classe e suas subclasses sejam identificadas exclusivamente.

Essa propriedade é herdada do [**Serviço CIM. \_**](/windows/desktop/CIMWin32Prov/cim-service)

</dd> <dt>

**DelayedAutoStart**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliana**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Service \| [**\_ DELAYED AUTO START \_ \_ \_ INFO**](/windows/desktop/api/winsvc/ns-winsvc-service_delayed_auto_start_info) \| fDelayedAutostart"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Início Automático Atrasado")
</dt> </dl>

Se **True**, o serviço será iniciado depois que outros serviços de início automático são iniciados, além de um pequeno atraso.

**Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 e Windows Vista:** Essa propriedade não é suportada antes Windows Server 2016 e Windows 10.

Essa propriedade é herdada do [**Serviço Win32. \_**](/windows/desktop/CIMWin32Prov/win32-service)

</dd> <dt>

**Descrição**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Descrição")
</dt> </dl>

Descrição do objeto.

Essa propriedade é herdada de [**CIM \_ ManagedSystemElement.**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)

</dd> <dt>

**DesktopInteract**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliana**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Service Structures \| [**QUERY SERVICE \_ \_ CONFIG**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa) \| dwServiceType \| SERVICE INTERACTIVE \_ \_ PROCESS"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Interage com a área de trabalho")
</dt> </dl>

Indica se o serviço pode criar ou se comunicar com janelas na área de trabalho e, portanto, interagir de alguma forma com um usuário. Os serviços interativos devem ser executados na conta sistema local. A maioria dos serviços não é interativa; ou seja, eles não se comunicam com o usuário de forma alguma.

Essa propriedade é herdada de [**Win32 \_ BaseService.**](/windows/desktop/CIMWin32Prov/win32-baseservice)

</dd> <dt>

**DisconnectedSessions**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

O número de sessões desconectadas no servidor atual. Essas sessões ainda podem estar consumindo ativamente recursos do servidor, no entanto, atualmente, não têm nenhuma conexão de rede com um cliente.

</dd> <dt>

**DisplayName**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Service Structures \| [**QUERY SERVICE \_ \_ CONFIG**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa) \| lpDisplayName"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Nome de Exibição")
</dt> </dl>

Nome do serviço conforme exibido no snap-in Serviços. Essa cadeia de caracteres tem um tamanho máximo de 256 caracteres. Observe que o nome de exibição e o nome do serviço (que é armazenado no Registro) nem sempre são os mesmos. Por exemplo, o serviço cliente DHCP tem o nome do serviço Dhcp, mas o nome de exibição Cliente DHCP. O nome é preservado em caso no Gerenciador de Controle de Serviço. No entanto, [**as comparações**](/windows/desktop/CIMWin32Prov/win32-service) de DisplayName sempre não fazem maiúsculas de minúsculas.

Restrição: aceita o mesmo valor que a [**propriedade**](/windows/desktop/CIMWin32Prov/win32-service) Name.

Exemplo: "Atdisk"

Essa propriedade é herdada de [**Win32 \_ BaseService.**](/windows/desktop/CIMWin32Prov/win32-baseservice)

</dd> <dt>

**ErrorControl**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Service Structures \| [**QUERY SERVICE \_ \_ CONFIG**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa) \| dwErrorControl"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Gravidade da falha de inicialização")
</dt> </dl>

Severidade do erro se esse serviço não for inicializado durante a inicialização. O valor indica a ação tomada pelo programa de inicialização se ocorrer uma falha. Todos os erros são anotados pelo sistema de computador.

<dt>

<span id="Ignore"></span><span id="ignore"></span><span id="IGNORE"></span>

<span id="Ignore"></span><span id="ignore"></span><span id="IGNORE"></span>**Ignorar** ("Ignorar")


</dt> <dd>

O usuário não é notificado.

</dd> <dt>

<span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>

<span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>**Normal** ("Normal")


</dt> <dd>

O usuário é notificado. Normalmente, essa será uma exibição de caixa de mensagem notificando o usuário sobre o problema.

</dd> <dt>

<span id="Severe"></span><span id="severe"></span><span id="SEVERE"></span>

<span id="Severe"></span><span id="severe"></span><span id="SEVERE"></span>**Grave** ("grave")


</dt> <dd>

Sistema é reiniciado com a última configuração bem-sucedida conhecida.

</dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Crítico** ("Crítico")


</dt> <dd>

O sistema tenta reiniciar com uma configuração adequada. Se o serviço não for inicializado uma segunda vez, a inicialização falhará.

</dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** ("Desconhecido")


</dt> <dd>

A gravidade do erro é desconhecida.

</dd> </dl>

Essa propriedade é herdada de [**Win32 \_ BaseService.**](/windows/desktop/CIMWin32Prov/win32-baseservice)

</dd> <dt>

**Exitcode**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Service Structures SERVICE \| [**\_ STATUS**](/windows/desktop/api/winsvc/ns-winsvc-service_status) \| dwWin32ExitCode"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Exit Code")
</dt> </dl>

Windows código de erro que define os erros encontrados ao iniciar ou parar o serviço. Essa propriedade é definida como **ERROR \_ SERVICE SPECIFIC \_ \_ ERROR** (1066) quando o erro é exclusivo para o serviço representado por essa classe e as informações sobre o erro estão disponíveis na propriedade [**ServiceSpecificExitCode.**](/windows/desktop/CIMWin32Prov/win32-service) O serviço define esse valor como **NENHUM \_ ERRO ao** executar e novamente após o término normal.

Essa propriedade é herdada de [**Win32 \_ BaseService.**](/windows/desktop/CIMWin32Prov/win32-baseservice)

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

Tipo de dados: **datetime**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Data de instalação")
</dt> </dl>

O objeto Date está instalado. Essa propriedade não requer um valor para indicar que o objeto está instalado.

Essa propriedade é herdada de [**CIM \_ ManagedSystemElement.**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)

</dd> <dt>

**Nome**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [ **Chave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Identificador exclusivo do serviço que fornece uma indicação da funcionalidade gerenciada. Essa funcionalidade é descrita na propriedade [**Description**](/windows/desktop/CIMWin32Prov/win32-service) do objeto .

Essa propriedade é herdada de [**CIM \_ ManagedSystemElement.**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)

</dd> <dt>

**PathName**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Service Structures \| [**QUERY SERVICE \_ \_ CONFIG**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa) \| lpBinaryPathName"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Nome do Caminho do Arquivo")
</dt> </dl>

Caminho totalmente qualificado para o arquivo binário de serviço que implementa o serviço.

Exemplo: \\ "Drivers systemRoot \\ System32 \\ \\afd.sys"

Essa propriedade é herdada de [**Win32 \_ BaseService.**](/windows/desktop/CIMWin32Prov/win32-baseservice)

</dd> <dt>

**Processid**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Service Structures SERVICE STATUS \| [**\_ \_ PROCESS**](/windows/desktop/api/winsvc/ns-winsvc-service_status_process) \| dwProcessId"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Id do processo")
</dt> </dl>

Identificador de processo do serviço.

Exemplo: 324

Essa propriedade é herdada do [**Serviço Win32. \_**](/windows/desktop/CIMWin32Prov/win32-service)

</dd> <dt>

**ServiceSpecificExitCode**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Service Structures SERVICE \| [**\_ STATUS**](/windows/desktop/api/winsvc/ns-winsvc-service_status) \| dwServiceSpecificExitCode"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Código de Saída Específico do Servidor")
</dt> </dl>

Código de erro específico do serviço para erros que ocorrem enquanto o serviço está iniciando ou parando. Os códigos de saída são definidos pelo serviço representado por essa classe. Esse valor só é definido quando o [**valor da propriedade ExitCode**](/windows/desktop/CIMWin32Prov/win32-service) é **ERROR SERVICE SPECIFIC \_ \_ \_ ERROR** (1066).

Essa propriedade é herdada de [**Win32 \_ BaseService.**](/windows/desktop/CIMWin32Prov/win32-baseservice)

</dd> <dt>

**ServiceType**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Service Structures \| [**QUERY SERVICE \_ \_ CONFIG**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa) \| dwServiceType"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Tipo de Serviço")
</dt> </dl>

Tipo de serviço fornecido a processos de chamada.

Os valores são:

<dt>

<span id="Kernel_Driver"></span><span id="kernel_driver"></span><span id="KERNEL_DRIVER"></span>

**Driver de kernel** ("Kernel Driver")


</dt> <dd></dd> <dt>

<span id="File_System_Driver"></span><span id="file_system_driver"></span><span id="FILE_SYSTEM_DRIVER"></span>

**Driver do Sistema de Arquivos** ("Driver do Sistema de Arquivos")


</dt> <dd></dd> <dt>

<span id="Adapter"></span><span id="adapter"></span><span id="ADAPTER"></span>

**Adaptador** ("Adaptador")


</dt> <dd></dd> <dt>

<span id="Recognizer_Driver"></span><span id="recognizer_driver"></span><span id="RECOGNIZER_DRIVER"></span>

**Driver do Reconhecedor** ("Driver do Reconhecedor")


</dt> <dd></dd> <dt>

<span id="Own_Process"></span><span id="own_process"></span><span id="OWN_PROCESS"></span>

**Processo próprio** ("processo próprio")


</dt> <dd></dd> <dt>

<span id="Share_Process"></span><span id="share_process"></span><span id="SHARE_PROCESS"></span>

**Processo de compartilhamento** ("Processo de compartilhamento")


</dt> <dd></dd> <dt>

<span id="Interactive_Process"></span><span id="interactive_process"></span><span id="INTERACTIVE_PROCESS"></span>

**Processo interativo** ("Processo Interativo")


</dt> <dd></dd> </dl>

Essa propriedade é herdada de [**Win32 \_ BaseService.**](/windows/desktop/CIMWin32Prov/win32-baseservice)

</dd> <dt>

**Iniciado**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliana**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Started")
</dt> </dl>

Indica se o serviço foi iniciado ou não.

Essa propriedade é herdada do [**Serviço CIM. \_**](/windows/desktop/CIMWin32Prov/cim-service)

</dd> <dt>

**StartMode**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Modo inicial")
</dt> </dl>

Modo de início do serviço Windows base.

<dt>

<span id="Boot"></span><span id="boot"></span><span id="BOOT"></span>

<span id="Boot"></span><span id="boot"></span><span id="BOOT"></span>**Inicialização** ("Inicialização")


</dt> <dd>

Driver de dispositivo iniciado pelo carregador do sistema operacional (válido somente para serviços de driver).

</dd> <dt>

<span id="System"></span><span id="system"></span><span id="SYSTEM"></span>

<span id="System"></span><span id="system"></span><span id="SYSTEM"></span>**Sistema** ("Sistema")


</dt> <dd>

Driver de dispositivo iniciado pelo processo de inicialização do sistema operacional. Esse valor só é válido para serviços do driver.

</dd> <dt>

<span id="Auto"></span><span id="auto"></span><span id="AUTO"></span>

<span id="Auto"></span><span id="auto"></span><span id="AUTO"></span>**Auto** ("Auto")


</dt> <dd>

Serviço a ser iniciado automaticamente pelo gerenciador de controle de serviço durante a inicialização do sistema. Os serviços automáticos são iniciados mesmo que um usuário não faça logoff.

</dd> <dt>

<span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>

<span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>**Manual** ("Manual")


</dt> <dd>

Serviço a ser iniciado pelo Gerenciador de Controle de Serviço quando um processo chama o [**método StartService.**](/windows/desktop/CIMWin32Prov/startservice-method-in-class-win32-service) Esses serviços não são iniciados, a menos que um usuário faça login e inicie-os.

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Desabilitado** ("Desabilitado")


</dt> <dd>

Serviço que não pode ser iniciado até que seu StartMode seja alterado para Automático ou Manual.

</dd> </dl>

Essa propriedade é herdada do [**Serviço CIM. \_**](/windows/desktop/CIMWin32Prov/cim-service)

</dd> <dt>

**Startname**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Service Structures \| [**QUERY SERVICE \_ \_ CONFIG**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa) \| lpServiceStartName"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Nome da Conta Inicial")
</dt> </dl>

Nome da conta sob a qual um serviço é executado. Dependendo do tipo de serviço, o nome da conta pode estar na forma de "Nome de usuário domainname" ou \\ formato UPN (" *Username@DomainName* "). O processo de serviço é registrado usando um desses dois formulários quando ele é executado. Se a conta pertencer ao domínio integrado, ". \\ Nome de usuário" pode ser especificado. Para drivers no nível do kernel ou do sistema, [**StartName**](/windows/desktop/CIMWin32Prov/win32-service) contém o nome do objeto do driver (ou seja, " FileSystem Rdr" ou " Driver Xns") que o sistema de \\ E/S usa para carregar o driver de \\ \\ \\ dispositivo. Além disso, se **NULL** for especificado, o driver será executado com um nome de objeto padrão criado pelo sistema de E/S com base no nome do serviço.

Exemplo: "Administrador do \\ DWDOM"

Essa propriedade é herdada de [**Win32 \_ BaseService.**](/windows/desktop/CIMWin32Prov/win32-baseservice)

</dd> <dt>

**State**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Leitura/gravação
</dt> <dt>

Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Service Structures SERVICE \| [**\_ STATUS**](/windows/desktop/api/winsvc/ns-winsvc-service_status) \| dwCurrentState "), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("State")
</dt> </dl>

Estado atual do serviço base.

Os valores são:

<dt>

<span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>

**Parado** ("Parado")


</dt> <dd></dd> <dt>

<span id="Start_Pending"></span><span id="start_pending"></span><span id="START_PENDING"></span>

**Iniciar Pendente** ("Iniciar Pendente")


</dt> <dd></dd> <dt>

<span id="Stop_Pending"></span><span id="stop_pending"></span><span id="STOP_PENDING"></span>

**Parar Pendente** ("Parar Pendente")


</dt> <dd></dd> <dt>

<span id="Running"></span><span id="running"></span><span id="RUNNING"></span>

**Executando** ("Em execução")


</dt> <dd></dd> <dt>

<span id="Continue_Pending"></span><span id="continue_pending"></span><span id="CONTINUE_PENDING"></span>

**Continuar Pendente** ("Continuar Pendente")


</dt> <dd></dd> <dt>

<span id="Pause_Pending"></span><span id="pause_pending"></span><span id="PAUSE_PENDING"></span>

**Pausa pendente** ("Pausar Pendente")


</dt> <dd></dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

**Pausado** ("Pausado")


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Desconhecido** ("Desconhecido")


</dt> <dd></dd> </dl>

**Windows Server 2008 e Windows Vista:** Essa propriedade é somente leitura antes Windows 7 e Windows Server 2008 R2.

Essa propriedade é herdada de [**Win32 \_ BaseService.**](/windows/desktop/CIMWin32Prov/win32-baseservice)

</dd> <dt>

**Status**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Status")
</dt> </dl>

Status atual do objeto. Vários status operacionais e não operacionais podem ser definidos. Os status operacionais incluem: "OK", "Degradado" e "Pred Fail" (um elemento, como uma unidade de disco rígido habilitada para SMART, pode estar funcionando corretamente, mas prevendo uma falha em um futuro próximo). Os status nãooperacionais incluem: "Error", "Starting", "Stopping" e "Service". O último, "Serviço", pode ser aplicado durante o espelhamento de um disco, o recarregamento de uma lista de permissões de usuário ou outro trabalho administrativo. Nem todo esse trabalho está online, mas o elemento gerenciado não é "OK" nem em um dos outros estados.

Os valores são:

<dt>

<span id="OK"></span><span id="ok"></span>

**OK** ("OK")


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

**Erro** ("Erro")


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

**Degradado** ("Degradado")


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Desconhecido** ("Desconhecido")


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

**Pred Fail** ("Pred Fail")


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

**Iniciando** ("Iniciando")


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

**Parando** ("Parando")


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

**Serviço** ("Serviço")


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

**Stressed** ("Stressed")


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

**NonRecover** ("NonRecover")


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

**Sem contato** ("Sem contato")


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

**Perda de vírgula** ("comm perdida")


</dt> <dd></dd> </dl>

Essa propriedade é herdada de [**CIM \_ ManagedSystemElement.**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)

</dd> <dt>

**SystemCreationClassName**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**Sistema CIM \_**](/windows/desktop/CIMWin32Prov/cim-system). CreationClassName"), [**CIM \_ Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("System Class Name")
</dt> </dl>

Digite o nome do sistema que hospeda esse serviço.

Essa propriedade é herdada do [**Serviço CIM. \_**](/windows/desktop/CIMWin32Prov/cim-service)

</dd> <dt>

**Systemname**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**Sistema CIM \_**](/windows/desktop/CIMWin32Prov/cim-system). Name"), [**CIM \_ Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Nome do Sistema")
</dt> </dl>

Nome do sistema que hospeda esse serviço.

Essa propriedade é herdada do [**Serviço CIM. \_**](/windows/desktop/CIMWin32Prov/cim-service)

</dd> <dt>

**TagId**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Service Structures \| [**QUERY SERVICE \_ \_ CONFIG**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa) \| dwTagId"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Tag Id")
</dt> </dl>

Valor de marca exclusivo para esse serviço no grupo. Um valor de 0 (zero) indica que o serviço não tem uma marca. Uma marca pode ser usada para ordenar a inicialização do serviço dentro de um grupo de ordem de carregamento especificando um vetor de ordem de marca no registro localizado em:

**HKEY \_ Grupo \_ de controle CurrentControlSet** do sistema \\  \\ **LOCAL** \\  \\ **MACHINEOrderList**    

As marcas são avaliadas apenas para serviços de tipo de inicialização do Driver do Kernel e do Driver do Sistema de Arquivos que têm modos de inicialização ou inicialização do sistema.

Essa propriedade é herdada de [**Win32 \_ BaseService.**](/windows/desktop/CIMWin32Prov/win32-baseservice)

</dd> <dt>

**TotalSessions**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

O número total de sessões no servidor atual. Isso inclui sessões conectadas e desconectadas.

</dd> <dt>

**WaitHint**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("win32api \| Service structures \| [**Service \_ status**](/windows/desktop/api/winsvc/ns-winsvc-service_status) \| dwWaitHint"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("tempo de espera estimado")
</dt> </dl>

Tempo estimado necessário, em milissegundos, para uma operação de início, parada, pausa ou continuação pendente. Depois que o tempo especificado tiver decorrido, o serviço fará sua próxima chamada para o método **falha em SetServiceStatus** com um valor de [**ponto de verificação**](/windows/desktop/CIMWin32Prov/win32-service) incrementado ou uma alteração no **CurrentState**. Se o tempo especificado por **WaitHint** passa e o ponto de **verificação** não tiver sido incrementado ou **CurrentState** não tiver sido alterado, o Gerenciador de controle de serviço ou o programa de controle de serviço assumirá que ocorreu um erro.

Essa propriedade é herdada [**do \_ serviço Win32**](/windows/desktop/CIMWin32Prov/win32-service).

</dd> </dl>

## <a name="remarks"></a>Comentários

Como a classe **Win32 \_ TerminalService** é uma subclasse da classe de [**\_ serviço do Win32**](/windows/desktop/CIMWin32Prov/win32-service) , a classe herda todas as propriedades e métodos do **\_ serviço Win32**.

[**Win32 \_ TerminalServiceSetting**](win32-terminalservicesetting.md) está associado ao **Win32 \_ TerminalService** como a propriedade **Setting** da Associação [**Win32 \_ TerminalServiceToSetting**](win32-terminalservicetosetting.md) .

[**Win32 \_ TSSessionDirectory**](win32-tssessiondirectory.md) está associado ao **Win32 \_ TerminalService** como a propriedade **Setting** da Associação [**Win32 \_ TSSessionDirectorySetting**](win32-tssessiondirectorysetting.md) .

os arquivos de formato MOF (MOF) contêm as definições de classes de Instrumentação de Gerenciamento do Windows (WMI). os arquivos MOF não são instalados como parte do SDK (Software Development Kit) do Microsoft Windows. Eles são instalados no servidor quando você adiciona a função associada usando o Gerenciador do Servidor. Para obter mais informações sobre arquivos MOF, consulte [formato MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | Raiz\\CIMv2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>TSCfgWmi. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_Serviço Win32**](/windows/desktop/CIMWin32Prov/win32-service)
</dt> <dt>

[**\_TerminalServiceToSetting Win32**](win32-terminalservicetosetting.md)
</dt> <dt>

[**\_TSSessionDirectory Win32**](win32-tssessiondirectory.md)
</dt> <dt>

[**\_BaseService Win32**](/windows/desktop/CIMWin32Prov/win32-baseservice)
</dt> <dt>

[**\_Serviço CIM**](/windows/desktop/CIMWin32Prov/cim-service)
</dt> </dl>

 

