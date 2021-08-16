---
description: O \_ Thread Win32&\# 8194; A classe WMI representa um thread de execução.
ms.assetid: a284616c-1977-441a-9173-dff4f56b2d39
ms.tgt_platform: multiple
title: Classe Win32_Thread
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Thread
- Win32_Thread.Caption
- Win32_Thread.CreationClassName
- Win32_Thread.CSCreationClassName
- Win32_Thread.CSName
- Win32_Thread.Description
- Win32_Thread.ElapsedTime
- Win32_Thread.ExecutionState
- Win32_Thread.Handle
- Win32_Thread.InstallDate
- Win32_Thread.KernelModeTime
- Win32_Thread.Name
- Win32_Thread.OSCreationClassName
- Win32_Thread.OSName
- Win32_Thread.Priority
- Win32_Thread.PriorityBase
- Win32_Thread.ProcessCreationClassName
- Win32_Thread.ProcessHandle
- Win32_Thread.StartAddress
- Win32_Thread.Status
- Win32_Thread.ThreadState
- Win32_Thread.ThreadWaitReason
- Win32_Thread.UserModeTime
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: f3add3a93cc974c2d6c5b20c360d099d46b688887f81cb646005568240a7cb52
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118416712"
---
# <a name="win32_thread-class"></a>\_Classe de Thread Win32

A  [classe WMI](../wmisdk/retrieving-a-class.md) de **\_ thread do Win32** representa um thread de execução. Embora um processo deva ter um thread de execução, o processo pode criar outros threads para executar tarefas em paralelo. Os threads compartilham o ambiente de processo, assim, vários threads no mesmo processo usam menos memória do que o mesmo número de processos.

A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas. As propriedades e os métodos estão em ordem alfabética, não em ordem de MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4DD-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_Thread : CIM_Thread
{
  string   Caption;
  string   CreationClassName;
  string   CSCreationClassName;
  string   CSName;
  string   Description;
  uint64   ElapsedTime;
  uint16   ExecutionState;
  string   Handle;
  datetime InstallDate;
  uint64   KernelModeTime;
  string   Name;
  string   OSCreationClassName;
  string   OSName;
  uint32   Priority;
  uint32   PriorityBase;
  string   ProcessCreationClassName;
  string   ProcessHandle;
  uint32   StartAddress;
  string   Status;
  uint32   ThreadState;
  uint32   ThreadWaitReason;
  uint64   UserModeTime;
};
```

## <a name="members"></a>Membros

A **classe \_ thread do Win32** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A **classe \_ thread do Win32** tem essas propriedades.

<dl> <dt>

**Legenda**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**maxlen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")
</dt> </dl>

Breve descrição do objeto.

Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

</dd> <dt>

**CreationClassName**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**\_ chave CIM**](../wmisdk/standard-wmi-qualifiers.md), [**maxlen**](../wmisdk/standard-qualifiers.md) (256)
</dt> </dl>

Nome da primeira classe concreta a ser exibida na cadeia de herança usada na criação de uma instância. Quando usado com as outras propriedades de chave da classe, essa propriedade permite que todas as instâncias dessa classe e suas subclasses sejam identificadas exclusivamente.

Essa propriedade é herdada [**do \_ thread CIM**](cim-thread.md).

</dd> <dt>

**CSCreationClassName**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**propagados**](../wmisdk/standard-qualifiers.md) ([**" \_ processo CIM**](cim-process.md).**CSCreationClassName**"), [**\_ chave CIM**](../wmisdk/standard-wmi-qualifiers.md), [**maxlen**](../wmisdk/standard-qualifiers.md) (256)
</dt> </dl>

Nome da classe de criação do sistema de computador de escopo.

Essa propriedade é herdada [**do \_ thread CIM**](cim-thread.md).

</dd> <dt>

**CSName**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**propagados**](../wmisdk/standard-qualifiers.md) ([**" \_ processo CIM**](cim-process.md).**CSName**"), [**\_ chave CIM**](../wmisdk/standard-wmi-qualifiers.md), [**maxlen**](../wmisdk/standard-qualifiers.md) (256)
</dt> </dl>

Nome do sistema de computador de escopo.

Essa propriedade é herdada [**do \_ thread CIM**](cim-thread.md).

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

Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

</dd> <dt>

**ElapsedTime**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt64**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api de \| dados de desempenho de estruturas \| [**PerfTime de \_ \_ tipo de objeto**](/windows/win32/api/winperf/ns-winperf-perf_object_type) \| "), [**unidades**](../wmisdk/standard-qualifiers.md) ("milissegundos")
</dt> </dl>

Tempo de execução total, em milissegundos, fornecido para esse thread desde sua criação.

Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](../wmisdk/creating-a-wmi-script.md).

</dd> <dt>

**ExecutionState**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Condição operacional atual do thread.

Essa propriedade é herdada [**do \_ thread CIM**](cim-thread.md).

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Desconhecido** (0)


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Outro** (1)


</dt> <dd></dd> <dt>

<span id="Ready"></span><span id="ready"></span><span id="READY"></span>

**Pronto** (2)


</dt> <dd></dd> <dt>

<span id="Running"></span><span id="running"></span><span id="RUNNING"></span>

**Em execução** (3)


</dt> <dd></dd> <dt>

<span id="Blocked"></span><span id="blocked"></span><span id="BLOCKED"></span>

**Bloqueado** (4)


</dt> <dd></dd> <dt>

<span id="Suspended_Blocked"></span><span id="suspended_blocked"></span><span id="SUSPENDED_BLOCKED"></span>

**Bloqueado suspenso** (5)


</dt> <dd></dd> <dt>

<span id="Suspended_Ready"></span><span id="suspended_ready"></span><span id="SUSPENDED_READY"></span>

**Pronto suspenso** (6)


</dt> <dd></dd> </dl>

</dd> <dt>

**Handle**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**maxlen**](../wmisdk/standard-qualifiers.md) (256), [**substitua**](../wmisdk/standard-qualifiers.md) ("Handle"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api de \| ferramentas de ajuda da ferramenta \| [**THREADENTRY32**](/windows/win32/api/tlhelp32/ns-tlhelp32-threadentry32) \| th32ThreadID")
</dt> </dl>

Identificador para um thread. O identificador tem direitos de acesso completo por padrão. Com o acesso de segurança correto, o identificador pode ser usado em qualquer função que aceite um identificador de thread. Dependendo do sinalizador de herança especificado quando ele é criado, esse identificador pode ser herdado por processos filho.

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

Tipo de dados: **DateTime**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Componente DMTF \| 1,5 "), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" data de instalação ")
</dt> </dl>

O objeto foi instalado. Essa propriedade não precisa de um valor para indicar que o objeto está instalado.

Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

</dd> <dt>

**KernelModeTime**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt64**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**override**](../wmisdk/standard-qualifiers.md) ("KernelModeTime"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| desempenho estruturas de dados \| [**perf de \_ \_ tipo de objeto**](/windows/win32/api/winperf/ns-winperf-perf_object_type)com \| privilegetime"), [**unidades**](../wmisdk/standard-qualifiers.md) ("100 nanossegundos")
</dt> </dl>

Tempo no modo kernel, em unidades de 100 nanossegundos. Se essas informações não estiverem disponíveis, um valor de 0 (zero) deverá ser usado.

Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](../wmisdk/creating-a-wmi-script.md).

</dd> <dt>

**Nome**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")
</dt> </dl>

Rótulo pelo qual o objeto é conhecido. Quando em uma subclasse, a propriedade pode ser substituída para ser uma propriedade de chave.

Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

</dd> <dt>

**OSCreationClassName**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**propagados**](../wmisdk/standard-qualifiers.md) ([**" \_ processo CIM**](cim-process.md).**OSCreationClassName**"), [**\_ chave CIM**](../wmisdk/standard-wmi-qualifiers.md), [**maxlen**](../wmisdk/standard-qualifiers.md) (256)
</dt> </dl>

Nome da classe de criação do sistema operacional de escopo.

Essa propriedade é herdada [**do \_ thread CIM**](cim-thread.md).

</dd> <dt>

**OSName**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**propagados**](../wmisdk/standard-qualifiers.md) ([**" \_ processo CIM**](cim-process.md).**OSName**"), [**\_ chave CIM**](../wmisdk/standard-wmi-qualifiers.md), [**maxlen**](../wmisdk/standard-qualifiers.md) (256)
</dt> </dl>

Nome do sistema operacional de escopo.

Essa propriedade é herdada [**do \_ thread CIM**](cim-thread.md).

</dd> <dt>

**Prioridade**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**override**](../wmisdk/standard-qualifiers.md) ("Priority"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api da \| ferramenta de ajuda do \| [**THREADENTRY32**](/windows/win32/api/tlhelp32/ns-tlhelp32-threadentry32) \| tpDeltaPri")
</dt> </dl>

Prioridade dinâmica do thread. Cada thread tem uma prioridade dinâmica que o Agendador usa para determinar qual thread deve ser executado. Inicialmente, a prioridade dinâmica de um thread é igual à prioridade base. O sistema pode aumentar e diminuir a prioridade dinâmica, para garantir que ela seja responsiva (garantindo que nenhum thread fique sem falta para o tempo do processador). O sistema não aumenta a prioridade de threads com um nível de prioridade base entre 16 e 31. Somente os threads com uma prioridade básica entre 0 e 15 recebem aumentos de prioridade dinâmica. Números mais altos indicam prioridades mais altas.

</dd> <dt>

**PriorityBase**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api do \| tipo de \| [**\_ objeto perf \_**](/windows/win32/api/winperf/ns-winperf-perf_object_type)de estruturas de dados de desempenho \| PerfPriorityBase")
</dt> </dl>

Prioridade base atual de um thread. O sistema operacional pode aumentar a prioridade dinâmica do thread acima da prioridade base se o thread estiver manipulando a entrada do usuário ou reduzindo-a em direção à prioridade base se o thread se tornar associado à computação. A propriedade **PriorityBase** pode ter um valor entre 0 e 31.

</dd> <dt>

**ProcessCreationClassName**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**propagados**](../wmisdk/standard-qualifiers.md) ([**" \_ processo CIM**](cim-process.md).**CreationClassName**"), [**\_ chave CIM**](../wmisdk/standard-wmi-qualifiers.md), [**maxlen**](../wmisdk/standard-qualifiers.md) (256)
</dt> </dl>

Valor da propriedade **CreationClassName** do processo de escopo.

Essa propriedade é herdada [**do \_ thread CIM**](cim-thread.md).

</dd> <dt>

**ProcessHandle**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**maxlen**](../wmisdk/standard-qualifiers.md) (256), [**override**](../wmisdk/standard-qualifiers.md) ("ProcessHandle"), [**propagado**](../wmisdk/standard-qualifiers.md) ([**" \_ processo CIM**](cim-process.md).**Handle**"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" win32api \| ferramenta ajuda estruturas \| [**THREADENTRY32**](/windows/win32/api/tlhelp32/ns-tlhelp32-threadentry32) \| th32OwnerProcessID ")
</dt> </dl>

Processo que criou o thread. o conteúdo dessa propriedade pode ser usado por Windows elementos da API (interface de programação de aplicativo).

</dd> <dt>

**StartAddress**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| objeto de thread WIn32API \| LPTHREAD lpStartAddress de rotina de \_ inicialização \_ \| ")
</dt> </dl>

Endereço inicial do thread. Como qualquer aplicativo com acesso apropriado ao thread pode alterar o contexto do thread, esse valor pode ser apenas uma aproximação do endereço inicial do thread.

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

**ThreadState**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| estado de thread win32api")
</dt> </dl>

Estado de execução atual do thread.

<dt>

<span id="Initialized"></span><span id="initialized"></span><span id="INITIALIZED"></span>

<span id="Initialized"></span><span id="initialized"></span><span id="INITIALIZED"></span>**Inicializado** (0)


</dt> <dd>

Inicializado — ele é reconhecido pelo microkernel.

</dd> <dt>

<span id="Ready"></span><span id="ready"></span><span id="READY"></span>

<span id="Ready"></span><span id="ready"></span><span id="READY"></span>**Pronto** (1)


</dt> <dd>

Pronto — ele está preparado para ser executado no próximo processador disponível.

</dd> <dt>

<span id="Running"></span><span id="running"></span><span id="RUNNING"></span>

<span id="Running"></span><span id="running"></span><span id="RUNNING"></span>**Em execução** (2)


</dt> <dd>

Em execução — está em execução.

</dd> <dt>

<span id="Standby"></span><span id="standby"></span><span id="STANDBY"></span>

<span id="Standby"></span><span id="standby"></span><span id="STANDBY"></span>Em **espera** (3)


</dt> <dd>

Em espera — está prestes a ser executado, somente um thread pode estar nesse estado por vez.

</dd> <dt>

<span id="Terminated"></span><span id="terminated"></span><span id="TERMINATED"></span>

<span id="Terminated"></span><span id="terminated"></span><span id="TERMINATED"></span>**Encerrado** (4)


</dt> <dd>

Encerrado – concluiu a execução.

</dd> <dt>

<span id="Waiting"></span><span id="waiting"></span><span id="WAITING"></span>

<span id="Waiting"></span><span id="waiting"></span><span id="WAITING"></span>**Aguardando** (5)


</dt> <dd>

Aguardando — ele não está pronto para o processador, quando estiver pronto, ele será reagendado.

</dd> <dt>

<span id="Transition"></span><span id="transition"></span><span id="TRANSITION"></span>

<span id="Transition"></span><span id="transition"></span><span id="TRANSITION"></span>**Transição** (6)


</dt> <dd>

Transição — o thread está aguardando recursos diferentes do processador,

</dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (7)


</dt> <dd>

Desconhecido — o estado do thread é desconhecido.

</dd> </dl>

</dd> <dt>

**ThreadWaitReason**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| motivo de espera de thread win32api")
</dt> </dl>

Motivo pelo qual o thread está aguardando. Esse valor só será válido se o membro **ThreadState** estiver definido como Transition (6). Os pares de eventos permitem a comunicação com subsistemas protegidos.

<dt>

<span id="Executive"></span><span id="executive"></span><span id="EXECUTIVE"></span>

<span id="Executive"></span><span id="executive"></span><span id="EXECUTIVE"></span>**Executivo** (0)


</dt> <dd></dd> <dt>

<span id="FreePage"></span><span id="freepage"></span><span id="FREEPAGE"></span>

<span id="FreePage"></span><span id="freepage"></span><span id="FREEPAGE"></span>**FreePage** (1)


</dt> <dd>

FreePage

</dd> <dt>

<span id="PageIn"></span><span id="pagein"></span><span id="PAGEIN"></span>

<span id="PageIn"></span><span id="pagein"></span><span id="PAGEIN"></span>**Página** (2)


</dt> <dd></dd> <dt>

<span id="PoolAllocation"></span><span id="poolallocation"></span><span id="POOLALLOCATION"></span>

<span id="PoolAllocation"></span><span id="poolallocation"></span><span id="POOLALLOCATION"></span>**PoolAllocation** (3)


</dt> <dd></dd> <dt>

<span id="ExecutionDelay"></span><span id="executiondelay"></span><span id="EXECUTIONDELAY"></span>

<span id="ExecutionDelay"></span><span id="executiondelay"></span><span id="EXECUTIONDELAY"></span>**ExecutionDelay** (4)


</dt> <dd></dd> <dt>

<span id="FreePage"></span><span id="freepage"></span><span id="FREEPAGE"></span>

<span id="FreePage"></span><span id="freepage"></span><span id="FREEPAGE"></span>**FreePage** (5)


</dt> <dd></dd> <dt>

<span id="PageIn"></span><span id="pagein"></span><span id="PAGEIN"></span>

<span id="PageIn"></span><span id="pagein"></span><span id="PAGEIN"></span>**Página** (6)


</dt> <dd></dd> <dt>

<span id="Executive"></span><span id="executive"></span><span id="EXECUTIVE"></span>

<span id="Executive"></span><span id="executive"></span><span id="EXECUTIVE"></span>**Executivo** (7)


</dt> <dd></dd> <dt>

<span id="FreePage"></span><span id="freepage"></span><span id="FREEPAGE"></span>

<span id="FreePage"></span><span id="freepage"></span><span id="FREEPAGE"></span>**FreePage** (8)


</dt> <dd></dd> <dt>

<span id="PageIn"></span><span id="pagein"></span><span id="PAGEIN"></span>

<span id="PageIn"></span><span id="pagein"></span><span id="PAGEIN"></span>**PageIn** (9)


</dt> <dd></dd> <dt>

<span id="PoolAllocation"></span><span id="poolallocation"></span><span id="POOLALLOCATION"></span>

<span id="PoolAllocation"></span><span id="poolallocation"></span><span id="POOLALLOCATION"></span>**PoolAllocation** (10)


</dt> <dd></dd> <dt>

<span id="ExecutionDelay"></span><span id="executiondelay"></span><span id="EXECUTIONDELAY"></span>

<span id="ExecutionDelay"></span><span id="executiondelay"></span><span id="EXECUTIONDELAY"></span>**ExecutionDelay** (11)


</dt> <dd></dd> <dt>

<span id="FreePage"></span><span id="freepage"></span><span id="FREEPAGE"></span>

<span id="FreePage"></span><span id="freepage"></span><span id="FREEPAGE"></span>**FreePage** (12)


</dt> <dd></dd> <dt>

<span id="PageIn"></span><span id="pagein"></span><span id="PAGEIN"></span>

<span id="PageIn"></span><span id="pagein"></span><span id="PAGEIN"></span>**PageIn** (13)


</dt> <dd></dd> <dt>

<span id="EventPairHigh"></span><span id="eventpairhigh"></span><span id="EVENTPAIRHIGH"></span>

<span id="EventPairHigh"></span><span id="eventpairhigh"></span><span id="EVENTPAIRHIGH"></span>**EventPairHigh** (14)


</dt> <dd></dd> <dt>

<span id="EventPairLow"></span><span id="eventpairlow"></span><span id="EVENTPAIRLOW"></span>

<span id="EventPairLow"></span><span id="eventpairlow"></span><span id="EVENTPAIRLOW"></span>**EventPairLow** (15)


</dt> <dd></dd> <dt>

<span id="LPCReceive"></span><span id="lpcreceive"></span><span id="LPCRECEIVE"></span>

<span id="LPCReceive"></span><span id="lpcreceive"></span><span id="LPCRECEIVE"></span>**LPCReceive** (16)


</dt> <dd></dd> <dt>

<span id="LPCReply"></span><span id="lpcreply"></span><span id="LPCREPLY"></span>

<span id="LPCReply"></span><span id="lpcreply"></span><span id="LPCREPLY"></span>**LPCReply** (17)


</dt> <dd></dd> <dt>

<span id="VirtualMemory"></span><span id="virtualmemory"></span><span id="VIRTUALMEMORY"></span>

<span id="VirtualMemory"></span><span id="virtualmemory"></span><span id="VIRTUALMEMORY"></span>**VirtualMemory** (18)


</dt> <dd></dd> <dt>

<span id="PageOut"></span><span id="pageout"></span><span id="PAGEOUT"></span>

<span id="PageOut"></span><span id="pageout"></span><span id="PAGEOUT"></span>**PageOut** (19)


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (20)


</dt> <dd></dd> </dl>

</dd> <dt>

**UserModeTime**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint64**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**Substituir**](../wmisdk/standard-qualifiers.md) ("UserModeTime"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Performance Data Structures \| [**PERF OBJECT \_ \_ TYPE**](/windows/win32/api/winperf/ns-winperf-perf_object_type) \| UserTime"), [**Unidades**](../wmisdk/standard-qualifiers.md) ("100 nanossegundos")
</dt> </dl>

Tempo no modo de usuário, em unidades de 100 nanossegundos. Se essas informações não estão disponíveis, um valor de 0 (zero) deve ser usado.

Para obter mais informações sobre como **usar valores uint64** em scripts, consulte [Scripts no WMI](../wmisdk/creating-a-wmi-script.md).

</dd> </dl>

## <a name="remarks"></a>Comentários

A **classe \_ Thread Win32** é derivada do [**\_ Thread CIM.**](cim-thread.md)

**Visão geral**

Para o monitoramento rotineiro, geralmente há pouco motivo para ter uma lista detalhada de threads e suas propriedades associadas. Os computadores criam e excluem milhares de threads durante um dia, e algumas dessas criações ou exclusões são significativas para qualquer pessoa, menos para o desenvolvedor que escreveu o software.

No entanto, quando você está solucionando problemas com um aplicativo, acompanhar os threads individuais para um processo permite identificar quando os threads são criados e quando (ou se) eles são destruídos. Como os threads criados, mas não destruídos, causam vazamentos de memória, o acompanhamento de threads individuais pode ser uma informação útil para técnicos de suporte. Da mesma forma, identificar prioridades de thread pode ajudar a identificar threads que, executando em uma prioridade anormalmente alta, preempção de ciclos de CPU necessários para outros threads e outros processos.

**Usando o thread Win32 \_**

Conforme implícito no bloco de sintaxe anterior, a classe **\_ Thread win32** não relata o nome do processo no qual cada thread é executado. Em vez disso, ele relata a ID do processo sob o qual o thread é executado. Para retornar o nome de um processo e uma lista de todos os threads, o script deve:

1.  Conexão para a [**classe Processo \_ win32**](win32-process.md) e retornar a lista de processos e suas IDs de processo.
2.  Armazene temporariamente essas informações em uma matriz ou objeto Dictionary.
3.  Para cada ID de processo, retorne a lista de threads para esse processo e, em seguida, exibe o nome do processo e a lista de threads.

## <a name="examples"></a>Exemplos

O exemplo de VBScript a seguir monitora os threads em execução em um computador.


```VB
Set objDictionary = CreateObject("Scripting.Dictionary")
strComputer = "."
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colProcesses = objWMIService.ExecQuery("SELECT * FROM Win32_Process")
For Each objProcess in colProcesses
 objDictionary.Add objProcess.ProcessID, objProcess.Name
Next
Set colThreads = objWMIService.ExecQuery("SELECT * FROM Win32_Thread")
For Each objThread in colThreads
 intProcessID = CInt(objThread.ProcessHandle)
 strProcessName = objDictionary.Item(intProcessID)
 Wscript.Echo strProcessName & VbTab & objThread.ProcessHandle & _
              VbTab & objThread.Handle & VbTab & objThread.ThreadState
Next
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | RAIZ \\ CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**CIM \_ Thread**](cim-thread.md)
</dt> <dt>

[Classes do sistema operacional](./operating-system-classes.md)
</dt> </dl>

 

 
