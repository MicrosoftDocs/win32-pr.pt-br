---
description: A classe WMI abstrata Win32 BaseService representa objetos executáveis que são instalados em um banco de dados do Registro mantido \_ pelo Service Control Manager.
ms.assetid: 63673df9-3e41-4668-98fe-dc0e048328c1
ms.tgt_platform: multiple
title: Win32_BaseService classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_BaseService
- Win32_BaseService.AcceptPause
- Win32_BaseService.AcceptStop
- Win32_BaseService.Caption
- Win32_BaseService.CreationClassName
- Win32_BaseService.Description
- Win32_BaseService.DesktopInteract
- Win32_BaseService.DisplayName
- Win32_BaseService.ErrorControl
- Win32_BaseService.ExitCode
- Win32_BaseService.InstallDate
- Win32_BaseService.Name
- Win32_BaseService.PathName
- Win32_BaseService.ServiceSpecificExitCode
- Win32_BaseService.ServiceType
- Win32_BaseService.Started
- Win32_BaseService.StartMode
- Win32_BaseService.StartName
- Win32_BaseService.State
- Win32_BaseService.Status
- Win32_BaseService.SystemCreationClassName
- Win32_BaseService.SystemName
- Win32_BaseService.TagId
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: b2ce4673b6739639475264f79a60a7fd1b1c7bc5a0f16153d22305a77812759a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119504366"
---
# <a name="win32_baseservice-class"></a>Classe BaseService Win32 \_

A classe [WMI](/windows/desktop/WmiSdk/retrieving-a-class) abstrata **Win32 \_ BaseService** representa objetos executáveis que são instalados em um banco de dados do Registro mantido pelo Service Control Manager. O arquivo executável associado a um serviço pode ser iniciado no momento da inicialização por um programa de inicialização ou pelo sistema. Ele também pode ser iniciado sob demanda pelo Gerenciador de Controle de Serviço. Qualquer serviço ou processo que não pertence a um usuário específico e que fornece uma interface para algumas funcionalidades com suporte pelo sistema de computador é um descendente (ou membro) dessa classe.

Exemplo: o serviço de cliente DHCP (dynamic host configuration protocol) em um sistema de computador que executa Windows Server.

A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas. As propriedades são listadas em ordem alfabética, não em ordem MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
[SupportsCreate, CreateBy("Create"), SupportsDelete, DeleteBy("DeleteInstance"), Abstract, Provider("CIMWin32"), UUID("{8502C4C4-5FBB-11D2-AAC1-006008C78BC7}"), DisplayName("System Drivers and Services"), AMENDMENT]
class Win32_BaseService : CIM_Service
{
  boolean  AcceptPause;
  boolean  AcceptStop;
  string   Caption;
  string   CreationClassName;
  string   Description;
  boolean  DesktopInteract;
  string   DisplayName;
  string   ErrorControl;
  uint32   ExitCode;
  datetime InstallDate;
  string   Name;
  string   PathName;
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
};
```

## <a name="members"></a>Membros

A **classe \_ BaseService Win32** tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

A **classe \_ BaseService Win32** tem esses métodos.



| Método                                                                             | Descrição                                                                   |
|:-----------------------------------------------------------------------------------|:------------------------------------------------------------------------------|
| [**Alteração**](change-method-in-class-win32-baseservice.md)                         | Modifica um serviço.<br/>                                                |
| [**ChangeStartMode**](changestartmode-method-in-class-win32-baseservice.md)       | Modifica o modo de início de um serviço.<br/>                              |
| [**Criar**](create-method-in-class-win32-baseservice.md)                         | Cria um serviço novo.<br/>                                             |
| [**Excluir**](delete-method-in-class-win32-baseservice.md)                         | Exclui um serviço existente.<br/>                                       |
| [**Service**](interrogateservice-method-in-class-win32-baseservice.md) | Solicita que o serviço atualize seu estado para o gerenciador de serviços.<br/> |
| [**PauseService**](pauseservice-method-in-class-win32-baseservice.md)             | Tenta colocar o serviço no estado de pausado.<br/>                 |
| [**ResumeService**](resumeservice-method-in-class-win32-baseservice.md)           | Tenta colocar o serviço no estado de reiniciado.<br/>                |
| [**Startservice**](startservice-method-in-class-win32-baseservice.md)             | Tenta colocar o serviço em seu estado de inicialização.<br/>              |
| [**StopService**](stopservice-method-in-class-win32-baseservice.md)               | Método de classe que coloca o serviço no estado parado.<br/>         |
| [**UserControlService**](usercontrolservice-method-in-class-win32-baseservice.md) | Tenta enviar um código de controle definido pelo usuário para um serviço.<br/>         |



 

### <a name="properties"></a>Propriedades

A **classe \_ BaseService Win32** tem essas propriedades.

<dl> <dt>

**AcceptPause**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliana**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Service Structures SERVICE \| [**\_ STATUS**](/windows/desktop/api/winsvc/ns-winsvc-service_status) \| dwControlsAccepted \| SERVICE ACCEPT PAUSE \_ \_ \_ CONTINUE"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Service Accepts Pause")
</dt> </dl>

O serviço pode ser pausado.

</dd> <dt>

**AcceptStop**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliana**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Service Structures SERVICE \| [**\_ STATUS**](/windows/desktop/api/winsvc/ns-winsvc-service_status) \| dwControlsAccepted \| SERVICE ACCEPT \_ \_ STOP"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Service Accepts Stop")
</dt> </dl>

O serviço pode ser interrompido.

</dd> <dt>

**Legenda**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Legenda")
</dt> </dl>

Descrição curta do objeto.

Essa propriedade é herdada de [**CIM \_ ManagedSystemElement.**](cim-managedsystemelement.md)

</dd> <dt>

**CreationClassName**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**\_ Chave CIM,**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Nome da Classe")
</dt> </dl>

Nome da primeira classe concreta a ser exibida na cadeia de herança usada na criação de uma instância. Quando usada com as outras propriedades de chave da classe , a propriedade permite que todas as instâncias dessa classe e suas subclasses sejam identificadas exclusivamente.

Essa propriedade é herdada do [**Serviço CIM. \_**](cim-service.md)

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

Essa propriedade é herdada de [**CIM \_ ManagedSystemElement.**](cim-managedsystemelement.md)

</dd> <dt>

**DesktopInteract**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliana**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Service Structures \| [**QUERY SERVICE \_ \_ CONFIG**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa) \| dwServiceType \| SERVICE INTERACTIVE \_ \_ PROCESS"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Interage com a área de trabalho")
</dt> </dl>

O serviço pode criar ou se comunicar com janelas na área de trabalho.

</dd> <dt>

**DisplayName**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Service Structures \| [**QUERY SERVICE \_ \_ CONFIG**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa) \| lpDisplayName"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Nome de Exibição")
</dt> </dl>

Nome de exibição do serviço. Essa cadeia de caracteres tem um tamanho máximo de 256 caracteres. O nome é preservado em caso no Gerenciador de Controle de Serviço. Comparações de **DisplayName sempre** não fazem maiúsculas de minúsculas.

Restrições: aceita o mesmo valor que a **propriedade** Name.

Exemplo: "Atdisk"

</dd> <dt>

**ErrorControl**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Service Structures \| [**QUERY SERVICE \_ \_ CONFIG**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa) \| dwErrorControl"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Gravidade da falha de inicialização")
</dt> </dl>

Gravidade do erro. Falha ao iniciar o serviço. O valor indica a ação tomada pelo programa de inicialização se ocorrer uma falha. Todos os erros são anotados pelo sistema de computador.

<dt>

<span id="Ignore"></span><span id="ignore"></span><span id="IGNORE"></span>

<span id="Ignore"></span><span id="ignore"></span><span id="IGNORE"></span>**Ignorar** ("Ignorar")


</dt> <dd>

O usuário não é notificado.

</dd> <dt>

<span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>

<span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>**Normal** ("Normal")


</dt> <dd>

O usuário é notificado.

</dd> <dt>

<span id="Severe"></span><span id="severe"></span><span id="SEVERE"></span>

<span id="Severe"></span><span id="severe"></span><span id="SEVERE"></span>**Grave** ("grave")


</dt> <dd>

O sistema foi reiniciado com a última configuração boa conhecida.

</dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Crítico** ("Crítico")


</dt> <dd>

O sistema tenta reiniciar com uma configuração adequada.

</dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** ("Desconhecido")


</dt> <dd>

A ação tomada não é especificada.

</dd> </dl>

</dd> <dt>

**Exitcode**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Service Structures SERVICE \| [**\_ STATUS**](/windows/desktop/api/winsvc/ns-winsvc-service_status) \| dwWin32ExitCode"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Exit Code")
</dt> </dl>

Definir quaisquer problemas encontrados ao iniciar ou parar o serviço. Essa propriedade é definida como **ERROR \_ SERVICE SPECIFIC \_ \_ ERROR** (1066) quando o erro é exclusivo para o serviço representado por essa classe e as informações sobre o erro estão disponíveis na propriedade **ServiceSpecificExitCode.** O serviço define esse valor como **NENHUM \_ ERRO ao** executar e novamente após o término normal.

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

Tipo de dados: **datetime**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001.5"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Data de instalação")
</dt> </dl>

O objeto foi instalado. Essa propriedade não precisa de um valor para indicar que o objeto está instalado.

Essa propriedade é herdada de [**CIM \_ ManagedSystemElement.**](cim-managedsystemelement.md)

</dd> <dt>

**Nome**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [ **Chave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Identificador exclusivo do serviço, que fornece uma indicação da funcionalidade gerenciada. Essa funcionalidade é descrita em mais detalhes na propriedade **Description do** objeto.

Essa propriedade é herdada de [**CIM \_ ManagedSystemElement.**](cim-managedsystemelement.md)

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

</dd> <dt>

**ServiceSpecificExitCode**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Service Structures SERVICE \| [**\_ STATUS**](/windows/desktop/api/winsvc/ns-winsvc-service_status) \| dwServiceSpecificExitCode"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Código de Saída Específico do Servidor")
</dt> </dl>

Código de erro específico do serviço para erros que ocorrem enquanto o serviço está iniciando ou parando. Os códigos de saída são definidos pelo serviço representado por essa classe. Esse valor só é definido quando **o valor ExitCodeproperty** é **ERROR SERVICE SPECIFIC \_ \_ \_ ERROR** (1066).

</dd> <dt>

**ServiceType**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Service Structures \| [**QUERY SERVICE \_ \_ CONFIG**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa) \| dwServiceType"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Tipo de Serviço")
</dt> </dl>

Serviço fornecido para processos de chamada.

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

</dd> <dt>

**Iniciado**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliana**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Started")
</dt> </dl>

O serviço foi iniciado.

Essa propriedade é herdada do [**Serviço CIM. \_**](cim-service.md)

</dd> <dt>

**StartMode**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**Substituir**](/windows/desktop/WmiSdk/standard-qualifiers) ("StartMode"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Modo inicial")
</dt> </dl>

Modo de início do serviço Windows base.

Essa propriedade é herdada do [**Serviço CIM. \_**](cim-service.md)

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

Serviço a ser iniciado automaticamente pelo gerenciador de controle de serviço durante a início do sistema.

</dd> <dt>

<span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>

<span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>**Manual** ("Manual")


</dt> <dd>

Serviço a ser iniciado pelo gerenciador de controle de serviço quando um processo chama o [**método StartService.**](startservice-method-in-class-win32-baseservice.md)

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Desabilitado** ("Desabilitado")


</dt> <dd>

Serviço que não pode mais ser iniciado.

</dd> </dl>

</dd> <dt>

**Startname**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("Win32API \| Service Structures \| [**QUERY SERVICE \_ \_ CONFIG**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa) \| lpServiceStartName"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("Nome da Conta Inicial")
</dt> </dl>

Nome da conta sob a qual o serviço é executado. Dependendo do tipo de serviço, o nome da conta pode estar na forma de "Nome de usuário \\ domainname" ou formato UPN ( Username@DomainName ). O processo de serviço será registrado usando um desses dois formulários quando ele for executado. Se a conta pertencer ao domínio integrado, ". \\ Nome de usuário" pode ser especificado. Se **NULL** for especificado, o serviço será conectado como a conta LocalSystem. Para drivers no nível do kernel ou do sistema, **StartName** contém o nome do objeto do driver (ou seja, FileSystem Rdr ou Driver Xns) que o sistema de entrada e saída \\ \\ \\ (E/S) usa para carregar o driver de \\ dispositivo. Além disso, se **NULL** for especificado, o driver será executado com um nome de objeto padrão criado pelo sistema de E/S com base no nome do serviço. Exemplo: "Administrador do \\ DWDOM".

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

**Windows Server 2008 e Windows Vista:** Essa propriedade é somente leitura.

</dd> <dt>

**Status**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("status")
</dt> </dl>

Status atual do objeto. Vários status de operação e não operacional podem ser definidos. Os status operacionais incluem: "OK", "degradado" e "Pred falha" (um elemento, como uma unidade de disco rígido habilitado para inteligente, pode estar funcionando corretamente, mas prevendo uma falha em um futuro próximo). Os status não operacionais incluem: "erro", "Iniciando", "parando" e "serviço". O último, "Service", pode ser aplicado durante o espelhamento de espelho de um disco, recarregar uma lista de permissões de usuário ou outro trabalho administrativo. Nem todo esse trabalho está online, mas o elemento gerenciado não é "OK" nem em um dos outros Estados.

Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

Os valores incluem o seguinte:

<dt>

<span id="OK"></span><span id="ok"></span>

**OK** ("OK")


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

**Erro** ("erro")


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

**Degradado** ("degradado")


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Desconhecido** ("desconhecido")


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

**Falha de Pred** ("Pred Fail")


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

**Iniciando** ("Iniciando")


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

**Parando** ("parando")


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

**Serviço** ("serviço")


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

**Sob estresse** ("sob estresse")


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

Não **recuperar** ("Recover")


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

**Sem contato** ("sem contato")


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

**Perda de comunicação** ("perda de comunicação")


</dt> <dd></dd> </dl>

</dd> <dt>

**SystemCreationClassName**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ sistema CIM**](cim-system.md).**CreationClassName**"), [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" nome da classe do sistema ")
</dt> </dl>

Digite o nome do sistema que hospeda este serviço.

Essa propriedade é herdada [**do \_ serviço CIM**](cim-service.md).

</dd> <dt>

**SystemName**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ([**" \_ sistema CIM**](cim-system.md).**Name**"), [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) (" nome do sistema ")
</dt> </dl>

Nome do sistema que hospeda este serviço.

Essa propriedade é herdada [**do \_ serviço CIM**](cim-service.md).

</dd> <dt>

**TagId**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("win32api do \| serviço de consulta de estruturas de serviços \| [**\_ \_**](/windows/desktop/api/winsvc/ns-winsvc-query_service_configa) \| DwTagId"), [**DisplayName**](/windows/desktop/WmiSdk/standard-qualifiers) ("ID da marca")
</dt> </dl>

Valor de marca exclusivo para este serviço no grupo. Um valor de 0 (zero) indica que não foi atribuída uma marca ao serviço. Uma marca pode ser usada para ordenar o Service Star scrip em um grupo de ordem de carregamento, especificando um vetor de ordem de marca no Registro localizado em: HKEY \_ local \_ Machine \\ System \\ CurrentControlSet \\ Control \\ GroupOrderList. As marcas são avaliadas somente para serviços de inicialização de driver de kernel e driver de sistema de arquivos que têm os modos inicializar ou iniciar sistema.

</dd> </dl>

## <a name="remarks"></a>Comentários

A classe **Win32 \_ BaseService** é derivada do [**\_ serviço CIM**](cim-service.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | Raiz \\ cimv2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_Serviço CIM**](cim-service.md)
</dt> <dt>

[Classes do sistema operacional](/previous-versions//aa392727(v=vs.85))
</dt> </dl>

 

