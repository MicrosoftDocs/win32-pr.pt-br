---
description: Representa um serviço em um sistema de computador executando Windows.
ms.assetid: 713402d3-ee73-4a6c-afb9-ad8033a4c580
ms.tgt_platform: multiple
title: Win32_Service classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Service
- Win32_Service.AcceptPause
- Win32_Service.AcceptStop
- Win32_Service.Caption
- Win32_Service.CheckPoint
- Win32_Service.CreationClassName
- Win32_Service.DelayedAutoStart
- Win32_Service.Description
- Win32_Service.DesktopInteract
- Win32_Service.DisplayName
- Win32_Service.ErrorControl
- Win32_Service.ExitCode
- Win32_Service.InstallDate
- Win32_Service.Name
- Win32_Service.PathName
- Win32_Service.ProcessId
- Win32_Service.ServiceSpecificExitCode
- Win32_Service.ServiceType
- Win32_Service.Started
- Win32_Service.StartMode
- Win32_Service.StartName
- Win32_Service.State
- Win32_Service.Status
- Win32_Service.SystemCreationClassName
- Win32_Service.SystemName
- Win32_Service.TagId
- Win32_Service.WaitHint
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: a33265b3dfc3b114d55b381a229b717e291bbd258716e8305d9995282d29b3f6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119759256"
---
# <a name="win32_service-class"></a>Classe de serviço Win32 \_

A **classe WMI de \_ Serviço Win32** [representa](../wmisdk/retrieving-a-class.md) um serviço em um sistema de computador executando Windows.

A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas. As propriedades e os métodos estão em ordem alfabética, não em ordem MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
[Dynamic, Provider("CIMWin32"), SupportsUpdate, UUID("{8502C4D9-5FBB-11D2-AAC1-006008C78BC7}"), DisplayName("Services"), AMENDMENT]
class Win32_Service : Win32_BaseService
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
};
```

## <a name="members"></a>Membros

A **classe \_ Serviço Win32** tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

A **classe \_ Serviço Win32** tem esses métodos.



| Método                                                                               | Descrição                                                                                          |
|:-------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------|
| [**Alteração**](change-method-in-class-win32-service.md)                               | Modifica um serviço.<br/>                                                                       |
| [**ChangeStartMode**](changestartmode-method-in-class-win32-service.md)             | Modifica o modo de início de um serviço.<br/>                                                     |
| [**Criar**](create-method-in-class-win32-service.md)                               | Cria um serviço novo.<br/>                                                                    |
| [**Excluir**](delete-method-in-class-win32-service.md)                               | Exclui um serviço existente.<br/>                                                              |
| [**GetSecurityDescriptor**](getsecuritydescriptor-method-in-class-win32-service.md) | Retorna o descritor de segurança que controla o acesso ao serviço.<br/>                      |
| [**Service**](interrogateservice-method-in-class-win32-service.md)       | Solicita que um serviço atualize seu estado para o gerenciador de serviços.<br/>                          |
| [**PauseService**](pauseservice-method-in-class-win32-service.md)                   | Tenta colocar um serviço no estado pausado.<br/>                                          |
| [**ResumeService**](resumeservice-method-in-class-win32-service.md)                 | Tenta colocar um serviço no estado retomado.<br/>                                         |
| [**SetSecurityDescriptor**](setsecuritydescriptor-method-in-class-win32-service.md) | Grava uma versão atualizada do descritor de segurança que controla o acesso ao serviço.<br/> |
| [**Startservice**](startservice-method-in-class-win32-service.md)                   | Tenta colocar um serviço no estado de inicialização.<br/>                                       |
| [**StopService**](stopservice-method-in-class-win32-service.md)                     | Coloca um serviço no estado parado.<br/>                                                    |
| [**UserControlService**](usercontrolservice-method-in-class-win32-service.md)       | Tenta enviar um código de controle definido pelo usuário para um serviço.<br/>                                |



 

### <a name="properties"></a>Propriedades

A **classe \_ Serviço Win32** tem essas propriedades.

<dl> <dt>

**AcceptPause**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliana**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Service Structures SERVICE \| [**\_ STATUS**](/windows/win32/api/winsvc/ns-winsvc-service_status) \| dwControlsAccepted \| SERVICE ACCEPT PAUSE \_ \_ \_ CONTINUE"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Service Accepts Pause")
</dt> </dl>

Indica se o serviço pode ser pausado.

Essa propriedade é herdada de [**Win32 \_ BaseService.**](win32-baseservice.md)

</dd> <dt>

**AcceptStop**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliana**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Service Structures SERVICE \| [**\_ STATUS**](/windows/win32/api/winsvc/ns-winsvc-service_status) \| dwControlsAccepted \| SERVICE ACCEPT \_ \_ STOP"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Service Accepts Stop")
</dt> </dl>

Indica se o serviço pode ser interrompido.

Essa propriedade é herdada de [**Win32 \_ BaseService.**](win32-baseservice.md)

</dd> <dt>

**Legenda**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Legenda")
</dt> </dl>

Descrição curta do serviço – uma cadeia de caracteres de uma linha.

Essa propriedade é herdada de [**CIM \_ ManagedSystemElement.**](cim-managedsystemelement.md)

</dd> <dt>

**Checkpoint**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Service Structures SERVICE \| [**\_ STATUS**](/windows/win32/api/winsvc/ns-winsvc-service_status) \| dwCheckPoint"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Check Point Count")
</dt> </dl>

Valor que o serviço incrementa periodicamente para relatar seu progresso durante uma operação de início longo, parada, pausa ou continuação. Por exemplo, o serviço incrementa esse valor à medida que conclui cada etapa de sua inicialização quando está iniciando. O programa de interface do usuário que invoca a operação no serviço usa esse valor para acompanhar o progresso do serviço durante uma operação demorada. Esse valor não é válido e deve ser zero quando o serviço não tem uma operação de início, parada, pausa ou continuação pendente.

</dd> <dt>

**CreationClassName**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**\_ Chave CIM,**](../wmisdk/standard-wmi-qualifiers.md) [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Nome da Classe")
</dt> </dl>

Nome da primeira classe concreta a ser exibida na cadeia de herança usada na criação de uma instância. Quando usada com as outras propriedades de chave da classe , essa propriedade permite que todas as instâncias dessa classe e suas subclasses sejam identificadas exclusivamente.

Essa propriedade é herdada do [**Serviço CIM. \_**](cim-service.md)

</dd> <dt>

**DelayedAutoStart**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliana**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Service \| [**\_ DELAYED AUTO START \_ \_ \_ INFO**](/windows/win32/api/winsvc/ns-winsvc-service_delayed_auto_start_info) \| fDelayedAutostart"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Início Automático Atrasado")
</dt> </dl>

Se **True**, o serviço será iniciado depois que outros serviços de início automático são iniciados, além de um pequeno atraso.

**Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 e Windows Vista:** Essa propriedade não é suportada antes Windows Server 2016 e Windows 10.

</dd> <dt>

**Descrição**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Descrição")
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

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Service Structures \| [**QUERY SERVICE \_ \_ CONFIG**](/windows/win32/api/winsvc/ns-winsvc-query_service_configa) \| dwServiceType \| SERVICE INTERACTIVE \_ \_ PROCESS"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Interage com a área de trabalho")
</dt> </dl>

Indica se o serviço pode criar ou se comunicar com janelas na área de trabalho e, portanto, interagir de alguma forma com um usuário. Os serviços interativos devem ser executados na conta sistema local. A maioria dos serviços não é interativa; ou seja, eles não se comunicam com o usuário de forma alguma.

Essa propriedade é herdada de [**Win32 \_ BaseService.**](win32-baseservice.md)

</dd> <dt>

**DisplayName**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Service Structures \| [**QUERY SERVICE \_ \_ CONFIG**](/windows/win32/api/winsvc/ns-winsvc-query_service_configa) \| lpDisplayName"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Nome de Exibição")
</dt> </dl>

Nome do serviço conforme exibido no snap-in Serviços. Essa cadeia de caracteres tem um tamanho máximo de 256 caracteres. Observe que o nome de exibição e o nome do serviço (que é armazenado no registro) nem sempre são os mesmos. Por exemplo, o serviço de cliente DHCP tem o nome de serviço DHCP, mas o nome de exibição cliente DHCP. O nome é, por caso, preservado no Gerenciador de controle de serviço. No entanto, as comparações **DisplayName** sempre diferenciam maiúsculas de minúsculas.

Restrição: aceita o mesmo valor que a propriedade **Name** .

Exemplo: "atdisk"

Esta propriedade é herdada do [**Win32 \_ BaseService**](win32-baseservice.md).

</dd> <dt>

**ErrorControl**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| do serviço de \| [**consulta da \_ \_ configuração do serviço**](/windows/win32/api/winsvc/ns-winsvc-query_service_configa) \| DwErrorControl"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("severidade de falha na inicialização")
</dt> </dl>

Severidade do erro se esse serviço não for iniciado durante a inicialização. O valor indica a ação tomada pelo programa de inicialização se ocorrer falha. Todos os erros são anotados pelo sistema de computador.

<dt>

<span id="Ignore"></span><span id="ignore"></span><span id="IGNORE"></span>

<span id="Ignore"></span><span id="ignore"></span><span id="IGNORE"></span>**Ignorar** ("ignorar")


</dt> <dd>

O usuário não é notificado.

</dd> <dt>

<span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>

<span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>**Normal** ("normal")


</dt> <dd>

O usuário é notificado. Normalmente, essa será uma caixa de mensagem exibida notificando o usuário do problema.

</dd> <dt>

<span id="Severe"></span><span id="severe"></span><span id="SEVERE"></span>

<span id="Severe"></span><span id="severe"></span><span id="SEVERE"></span>**Grave** ("severo")


</dt> <dd>

Sistema é reiniciado com a última configuração bem-sucedida conhecida.

</dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Crítico** ("crítico")


</dt> <dd>

O sistema tenta reiniciar com uma configuração adequada. Se o serviço não for iniciado pela segunda vez, a inicialização falhará.

</dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** ("desconhecido")


</dt> <dd>

A severidade do erro é desconhecida.

</dd> </dl>

Esta propriedade é herdada do [**Win32 \_ BaseService**](win32-baseservice.md).

</dd> <dt>

**ExitCode**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| Service structures \| [**Service \_ status**](/windows/win32/api/winsvc/ns-winsvc-service_status) \| dwWin32ExitCode"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("código de saída")
</dt> </dl>

Windows código de erro que define os erros encontrados na inicialização ou na interrupção do serviço. Essa propriedade é definida como **\_ \_ \_ erro específico do serviço de erro** (1066) quando o erro é exclusivo para o serviço representado por essa classe e as informações sobre o erro estão disponíveis na propriedade **ServiceSpecificExitCode** . O serviço define esse valor como **sem \_ erros** durante a execução e novamente após o término normal.

Esta propriedade é herdada do [**Win32 \_ BaseService**](win32-baseservice.md).

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

Tipo de dados: **DateTime**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Componente DMTF \| 1,5 "), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" data de instalação ")
</dt> </dl>

O objeto de data está instalado. Essa propriedade não requer um valor para indicar que o objeto está instalado.

Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

</dd> <dt>

**Nome**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [ **chave**](../wmisdk/key-qualifier.md)
</dt> </dl>

Identificador exclusivo do serviço que fornece uma indicação da funcionalidade que é gerenciada. Essa funcionalidade é descrita na propriedade **Descrição** do objeto.

Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

</dd> <dt>

**PathName**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api do \| serviço de consulta de estruturas de serviços \| [**\_ \_**](/windows/win32/api/winsvc/ns-winsvc-query_service_configa) \| LpBinaryPathName"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("nome do caminho do arquivo")
</dt> </dl>

Caminho totalmente qualificado para o arquivo binário de serviço que implementa o serviço.

Exemplo: " \\ systemroot \\ System32 \\ drivers \\afd.sys"

Esta propriedade é herdada do [**Win32 \_ BaseService**](win32-baseservice.md).

</dd> <dt>

**ProcessId**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| código de status do serviço de estruturas de serviço win32api \| [**\_ \_**](/windows/win32/api/winsvc/ns-winsvc-service_status_process) \| DwProcessId"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("ID do processo")
</dt> </dl>

Identificador do processo do serviço.

Exemplo: 324

</dd> <dt>

**ServiceSpecificExitCode**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| Service structures \| [**Service \_ status**](/windows/win32/api/winsvc/ns-winsvc-service_status) \| dwServiceSpecificExitCode"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("código de saída específico do servidor")
</dt> </dl>

Código de erro específico do serviço para erros que ocorrem enquanto o serviço está sendo iniciado ou interrompido. Os códigos de saída são definidos pelo serviço representado por essa classe. Esse valor só é definido quando o valor da propriedade **ExitCode** é um **\_ \_ \_ erro específico do serviço de erro** (1066).

Esta propriedade é herdada do [**Win32 \_ BaseService**](win32-baseservice.md).

</dd> <dt>

**ServiceType**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api do \| serviço de consulta de estruturas de serviços \| [**\_ \_**](/windows/win32/api/winsvc/ns-winsvc-query_service_configa) \| DwServiceType"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("tipo de serviço")
</dt> </dl>

Tipo de serviço fornecido a processos de chamada.

Os valores são:

<dt>

<span id="Kernel_Driver"></span><span id="kernel_driver"></span><span id="KERNEL_DRIVER"></span>

**Driver de kernel** ("driver de kernel")


</dt> <dd></dd> <dt>

<span id="File_System_Driver"></span><span id="file_system_driver"></span><span id="FILE_SYSTEM_DRIVER"></span>

**Driver do sistema de arquivos** ("driver do sistema de arquivos")


</dt> <dd></dd> <dt>

<span id="Adapter"></span><span id="adapter"></span><span id="ADAPTER"></span>

**Adaptador** ("adaptador")


</dt> <dd></dd> <dt>

<span id="Recognizer_Driver"></span><span id="recognizer_driver"></span><span id="RECOGNIZER_DRIVER"></span>

**Driver do reconhecedor** ("driver do reconhecedor")


</dt> <dd></dd> <dt>

<span id="Own_Process"></span><span id="own_process"></span><span id="OWN_PROCESS"></span>

**Próprio processo** ("processo próprio")


</dt> <dd></dd> <dt>

<span id="Share_Process"></span><span id="share_process"></span><span id="SHARE_PROCESS"></span>

**Processo de compartilhamento** ("processo de compartilhamento")


</dt> <dd></dd> <dt>

<span id="Interactive_Process"></span><span id="interactive_process"></span><span id="INTERACTIVE_PROCESS"></span>

**Processo interativo** ("processo interativo")


</dt> <dd></dd> </dl>

Esta propriedade é herdada do [**Win32 \_ BaseService**](win32-baseservice.md).

</dd> <dt>

**Iniciado**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("iniciado")
</dt> </dl>

Indica se o serviço é iniciado ou não.

Essa propriedade é herdada [**do \_ serviço CIM**](cim-service.md).

</dd> <dt>

**StartMode**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("modo de início")
</dt> </dl>

modo de início do serviço base de Windows.

<dt>

<span id="Boot"></span><span id="boot"></span><span id="BOOT"></span>

<span id="Boot"></span><span id="boot"></span><span id="BOOT"></span>**Inicialização** ("inicialização")


</dt> <dd>

Driver de dispositivo iniciado pelo carregador do sistema operacional (válido somente para serviços de driver).

</dd> <dt>

<span id="System"></span><span id="system"></span><span id="SYSTEM"></span>

<span id="System"></span><span id="system"></span><span id="SYSTEM"></span>**Sistema** ("sistema")


</dt> <dd>

Driver de dispositivo iniciado pelo processo de inicialização do sistema operacional. Esse valor só é válido para serviços do driver.

</dd> <dt>

<span id="Auto"></span><span id="auto"></span><span id="AUTO"></span>

<span id="Auto"></span><span id="auto"></span><span id="AUTO"></span>**Automático** ("auto")


</dt> <dd>

Serviço a ser iniciado automaticamente pelo gerenciador de controle de serviço durante a inicialização do sistema. Os serviços automáticos são iniciados mesmo se um usuário não fizer logon.

</dd> <dt>

<span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>

<span id="Manual"></span><span id="manual"></span><span id="MANUAL"></span>**Manual** ("manual")


</dt> <dd>

Serviço a ser iniciado pelo Gerenciador de controle de serviço quando um processo chama o método [**StartService**](startservice-method-in-class-win32-service.md) . Esses serviços não são iniciados, a menos que um usuário faça logon e os inicie.

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** ("desabilitado")


</dt> <dd>

Serviço que não pode ser iniciado até que seu StartMode seja alterado para automático ou manual.

</dd> </dl>

Essa propriedade é herdada [**do \_ serviço CIM**](cim-service.md).

</dd> <dt>

**StartName**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api do \| serviço de consulta de estruturas de serviços \| [**\_ \_**](/windows/win32/api/winsvc/ns-winsvc-query_service_configa) \| LpServiceStartName"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("nome da conta inicial")
</dt> </dl>

Nome da conta sob a qual um serviço é executado. Dependendo do tipo de serviço, o nome da conta pode estar na forma de "DomainName \\ username" ou do formato UPN (" *Username@DomainName* "). O processo de serviço é registrado usando uma dessas duas formas quando é executado. Se a conta pertencer ao domínio interno, então ". \\ Username "pode ser especificado. Para drivers de nível de kernel ou de sistema, o **StartName** contém o nome do objeto de driver (ou seja, " \\ FileSystem \\ rdr" ou " \\ Driver \\ XNS") que o sistema de e/s usa para carregar o driver de dispositivo. Além disso, se **NULL** for especificado, o driver será executado com um nome de objeto padrão criado pelo sistema de e/s com base no nome do serviço.

Exemplo: "administrador do DWDOM \\ "

Esta propriedade é herdada do [**Win32 \_ BaseService**](win32-baseservice.md).

</dd> <dt>

**State**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| Service estruturas \| [**Service \_ status**](/windows/win32/api/winsvc/ns-winsvc-service_status) \| dwCurrentState"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("State")
</dt> </dl>

Estado atual do serviço base.

Os valores são:

<dt>

<span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>

**Parado** ("parado")


</dt> <dd></dd> <dt>

<span id="Start_Pending"></span><span id="start_pending"></span><span id="START_PENDING"></span>

**Início pendente** ("início pendente")


</dt> <dd></dd> <dt>

<span id="Stop_Pending"></span><span id="stop_pending"></span><span id="STOP_PENDING"></span>

**Parada pendente** ("parar pendente")


</dt> <dd></dd> <dt>

<span id="Running"></span><span id="running"></span><span id="RUNNING"></span>

**Em execução** ("em execução")


</dt> <dd></dd> <dt>

<span id="Continue_Pending"></span><span id="continue_pending"></span><span id="CONTINUE_PENDING"></span>

**Continuação pendente** ("continuar pendente")


</dt> <dd></dd> <dt>

<span id="Pause_Pending"></span><span id="pause_pending"></span><span id="PAUSE_PENDING"></span>

**Pausa pendente** ("pausa pendente")


</dt> <dd></dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

Em **pausa** ("pausado")


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Desconhecido** ("desconhecido")


</dt> <dd></dd> </dl>

**Windows Server 2008 e Windows Vista:** esta propriedade é somente leitura antes de Windows 7 e Windows Server 2008 R2.

Esta propriedade é herdada do [**Win32 \_ BaseService**](win32-baseservice.md).

</dd> <dt>

**Status**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**maxlen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("status")
</dt> </dl>

Status atual do objeto. Vários status de operação e não operacional podem ser definidos. Os status operacionais incluem: "OK", "degradado" e "Pred falha" (um elemento, como uma unidade de disco rígido habilitado para inteligente, pode estar funcionando corretamente, mas prevendo uma falha em um futuro próximo). Os status não operacionais incluem: "erro", "Iniciando", "parando" e "serviço". O último, "Service", pode ser aplicado durante o espelhamento de espelho de um disco, recarregar uma lista de permissões de usuário ou outro trabalho administrativo. Nem todo esse trabalho está online, mas o elemento gerenciado não é "OK" nem em um dos outros Estados.

Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

Os valores são:

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

Qualificadores: [**propagados**](../wmisdk/standard-qualifiers.md) ([**" \_ sistema CIM**](cim-system.md).**CreationClassName**"), [**\_ chave CIM**](../wmisdk/standard-wmi-qualifiers.md), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" nome da classe do sistema ")
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

Qualificadores: [**propagados**](../wmisdk/standard-qualifiers.md) ([**" \_ sistema CIM**](cim-system.md).**Name**"), [**\_ chave CIM**](../wmisdk/standard-wmi-qualifiers.md), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" nome do sistema ")
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

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api do \| serviço de consulta de estruturas de serviços \| [**\_ \_**](/windows/win32/api/winsvc/ns-winsvc-query_service_configa) \| DwTagId"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("ID da marca")
</dt> </dl>

Valor de marca exclusivo para este serviço no grupo. Um valor de 0 (zero) indica que o serviço não tem uma marca. Uma marca pode ser usada para ordenar a inicialização do serviço dentro de um grupo de ordem de carregamento, especificando um vetor de ordem de marca no Registro localizado em:

**HKEY \_ \_** Controle do sistema de computador local \\  \\ **CurrentControlSet** \\  \\ **GroupOrderList**    

As marcas são avaliadas somente para os serviços de tipo de inicialização driver de kernel e driver de sistema de arquivos que têm os modos de inicialização do sistema ou inicializados.

Esta propriedade é herdada do [**Win32 \_ BaseService**](win32-baseservice.md).

</dd> <dt>

**WaitHint**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| Service structures \| [**Service \_ status**](/windows/win32/api/winsvc/ns-winsvc-service_status) \| dwWaitHint"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("tempo de espera estimado")
</dt> </dl>

Tempo estimado necessário, em milissegundos, para uma operação de início, parada, pausa ou continuação pendente. Depois que o tempo especificado tiver decorrido, o serviço fará sua próxima chamada para o método **falha em SetServiceStatus** com um valor de **ponto de verificação** incrementado ou uma alteração no **CurrentState**. Se o tempo especificado por **WaitHint** passa e o ponto de **verificação** não tiver sido incrementado ou **CurrentState** não tiver sido alterado, o Gerenciador de controle de serviço ou o programa de controle de serviço assumirá que ocorreu um erro.

</dd> </dl>

## <a name="remarks"></a>Comentários

A classe de **\_ serviço do Win32** é derivada do [**Win32 \_ BaseService**](win32-baseservice.md).

A maneira como você gerencia um computador específico depende muito da função que o computador desempenha. Por exemplo, você geralmente monitora diferentes aspectos de um servidor DNS do que um servidor DHCP. Embora nenhuma única propriedade possa informar se um computador específico é um servidor de banco de dados, um servidor de email ou um servidor de multimídia, geralmente é possível identificar a função que um computador desempenha identificando os serviços instalados nele.

Em grandes organizações, é provável que apenas um dos principais serviços (como email) seja instalado em um único computador. seria incomum que um servidor de email também fosse executado como um servidor para os arquivos de player do Microsoft® Windows Media® technologies. Por isso, a identificação de um serviço instalado em um computador pode ajudar a identificar a função do computador na rede. se o serviço de Exchange Server da Microsoft® estiver instalado e em execução em um computador, geralmente é seguro supor que esse computador funciona como um servidor de email.

Você pode usar a classe **de \_ serviço WMI Win32** para enumerar os serviços instalados em um computador. Além disso, você pode usar essa classe para determinar se esses serviços estão em execução no momento e para retornar outras informações necessárias sobre esse serviço e como ele foi configurado.

um aplicativo de serviço está em conformidade com as regras de interface do SCM (gerenciador de controle de serviço) e pode ser iniciado por um usuário automaticamente na inicialização do sistema por meio do utilitário do painel de controle de serviços ou por um aplicativo que usa as funções de serviço incluídas na API de Windows. Os serviços podem ser iniciados quando não há usuários conectados ao computador.

Um usuário que se conecta a partir de um computador remoto deve ter o privilégio do **sc \_ Manager \_ Connect** habilitado para poder enumerar essa classe. Para obter mais informações, consulte [segurança de serviço e direitos de acesso](../services/service-security-and-access-rights.md).

## <a name="examples"></a>Exemplos

A [consulta PS-WMI que retorna o serviço ' estado ' em um grupo de dispositivos](https://Gallery.TechNet.Microsoft.Com/0f1ab629-d463-4406-be54-ec2c4c23bc1f) exemplo do PowerShell na galeria do TechNet usa o **\_ serviço Win32** para criar uma lista de dispositivos de Active Directory e, em seguida, consultar cada dispositivo que responde com pingfor um serviço específico em execução.

A amostra do PowerShell de [relatório do servidor](https://Gallery.TechNet.Microsoft.Com/Server-Report-7b4ac2fb) na galeria do TechNet usa o **\_ serviço Win32** para coletar informações do servidor e publicar no documento do Word.

O exemplo de código VBScript a seguir exibe todos os serviços instalados no momento.


```VB
for each Service in _ 
    GetObject("winmgmts:").InstancesOf ("Win32_Service")
 WScript.Echo ""
 WScript.Echo Service.Name

 description = Service.Description 
 if IsNull(description) then description = "<No description>"

 pathName = Service.PathName
 if IsNull(pathName) then pathName = "<No path>"

 startName = Service.StartName
 if IsNull(startName) then startName = "<None>"

 WScript.Echo "  Description:  ", description
 WScript.Echo "  Executable:   ", pathName
 WScript.Echo "  Status:       ", Service.Status
 WScript.Echo "  State:        ", Service.State
 WScript.Echo "  Start Mode:   ", Service.StartMode
 Wscript.Echo "  Start Name:   ", startName
next
```



O exemplo de código VBScript a seguir descreve os serviços em pausa, em execução e parado no computador especificado.


```VB
On Error Resume Next
 StateString = "Paused,Running,Stopped"
 StateArray = Split(StateString, ",", -1, 1) 
 ComputerName = InputBox("Enter the computer name", "List Service", "localhost")

 For x = 0 to Ubound (StateArray)
 Set Services = GetObject("winmgmts:\\" & ComputerName & "\Root\CIMv2").ExecQuery("SELECT * FROM Win32_Service where State='" & StateArray(x) & "'")
 
 For Each Service in Services
  SList = SList & Service.Name & VBlf 
 Next

 WScript.Echo StateArray(x) & " Services: " & VBlf & SList
 SList = ""

Next
```



O script Perl a seguir demonstra como recuperar uma lista de serviços em execução de instâncias **do \_ serviço Win32**.


```
use strict;
use Win32::OLE;

my ( $ServiceSet, $Service );

eval { $ServiceSet = Win32::OLE->GetObject("winmgmts:{impersonationLevel=impersonate}!\\\\.\\Root\\CIMv2")->
 ExecQuery("SELECT * FROM Win32_Service WHERE State=\"Running\""); };
unless ($@)
{
 print "\n";
 foreach $Service (in $ServiceSet) 
 {
  print $Service->{Name}, "\n";
  if( $Service->{Description} ) 
   {
    print "  $Service->{Description}\n";
   }
  else
   {
    print "  <No description>\n";
   }
  print "  Process ID: ", $Service->{ProcessId}, "\n";
  print "  Start Mode: ", $Service->{StartMode}, "\n";
  print "\n";
 }
}
else
{
 print STDERR Win32::OLE->LastError, "\n";
}
```



O exemplo c a seguir \# usa [Microsoft. Management. Infrastructure](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958(v=vs.85)) para recuperar todos os serviços em execução no computador local.


```CSharp
static void QueryInstanceFunc()
        {
 
            CimSession session = CimSession.Create("localHost");
            IEnumerable<CimInstance> queryInstance = session.QueryInstances(@"root\cimv2", "WQL", "SELECT * FROM Win32_Service");

            foreach (CimInstance cimObj in queryInstance)
            {
                Console.WriteLine(cimObj.CimInstanceProperties["Name"].ToString());
                Console.WriteLine(cimObj.CimInstanceProperties["State"].ToString());
                Console.WriteLine(cimObj.CimInstanceProperties["Status"].ToString());
                
                //Console.WriteLine(cimObj.CimInstanceProperties["NetworkAddress"].ToString());
                Console.WriteLine();

            }

            Console.ReadLine();
        }
    
```



O exemplo de código C a seguir \# usa o namespace [System. Management](/dotnet/api/system.management) para recuperar todos os serviços em execução no computador local.

> [!Note]  
> [System. Management](/dotnet/api/system.management) contém as classes originais usadas para acessar o WMI; no entanto, eles são considerados mais lentos e geralmente não são dimensionados, bem como seus equivalentes de [Microsoft. Management. Infrastructure](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958(v=vs.85)) .

 


```CSharp
using System.Management;
...
        static void oldSchoolQueryInstanceFunc()
        {

            ObjectQuery query = new ObjectQuery("SELECT * FROM Win32_Service");
            ManagementObjectSearcher searcher = new ManagementObjectSearcher(query);


            ManagementObjectCollection queryCollection = searcher.Get();
            foreach (ManagementObject m in queryCollection)
            {
                Console.WriteLine("ServiceName : {0}", m["Name"]);
                Console.WriteLine("State : {0}", m["State"]);
                Console.WriteLine("Status : {0}", m["Status"]);
                Console.WriteLine();
            }

            Console.ReadLine();


        }
```



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

[**\_BaseService Win32**](win32-baseservice.md)
</dt> <dt>

[Classes do sistema operacional](./operating-system-classes.md)
</dt> <dt>

[Tarefas do WMI: serviços](../wmisdk/wmi-tasks--services.md)
</dt> </dl>

 

 
