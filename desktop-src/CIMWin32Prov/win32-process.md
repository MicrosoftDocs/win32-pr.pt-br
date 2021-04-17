---
Description: O \_ processo Win32&\# 32; A classe WMI representa um processo em um sistema operacional.
ms.assetid: 51206aca-4784-4d18-95ca-bc0a45691f78
ms.tgt_platform: multiple
title: Classe Win32_Process
ms.topic: reference
ms.custom: snippet-project
ms.date: 07/23/2020
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Process
- Win32_Process.CreationClassName
- Win32_Process.Caption
- Win32_Process.CommandLine
- Win32_Process.CreationDate
- Win32_Process.CSCreationClassName
- Win32_Process.CSName
- Win32_Process.Description
- Win32_Process.ExecutablePath
- Win32_Process.ExecutionState
- Win32_Process.Handle
- Win32_Process.HandleCount
- Win32_Process.InstallDate
- Win32_Process.KernelModeTime
- Win32_Process.MaximumWorkingSetSize
- Win32_Process.MinimumWorkingSetSize
- Win32_Process.Name
- Win32_Process.OSCreationClassName
- Win32_Process.OSName
- Win32_Process.OtherOperationCount
- Win32_Process.OtherTransferCount
- Win32_Process.PageFaults
- Win32_Process.PageFileUsage
- Win32_Process.ParentProcessId
- Win32_Process.PeakPageFileUsage
- Win32_Process.PeakVirtualSize
- Win32_Process.PeakWorkingSetSize
- Win32_Process.Priority
- Win32_Process.PrivatePageCount
- Win32_Process.ProcessId
- Win32_Process.QuotaNonPagedPoolUsage
- Win32_Process.QuotaPagedPoolUsage
- Win32_Process.QuotaPeakNonPagedPoolUsage
- Win32_Process.QuotaPeakPagedPoolUsage
- Win32_Process.ReadOperationCount
- Win32_Process.ReadTransferCount
- Win32_Process.SessionId
- Win32_Process.Status
- Win32_Process.TerminationDate
- Win32_Process.ThreadCount
- Win32_Process.UserModeTime
- Win32_Process.VirtualSize
- Win32_Process.WindowsVersion
- Win32_Process.WorkingSetSize
- Win32_Process.WriteOperationCount
- Win32_Process.WriteTransferCount
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: bb8d1d37bd5d4db59942aaab7170119283c5cc7b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752951"
---
# <a name="win32_process-class"></a>\_Classe de processo Win32

A [classe WMI](../wmisdk/retrieving-a-class.md) de **\_ processo Win32** representa um processo em um sistema operacional.

A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.

> [!NOTE]
> Para uma discussão geral sobre processos e threads no Windows, consulte o tópico [processos e threads](/ProcThread/processes-and-threads.md).

## <a name="syntax"></a>Sintaxe

``` syntax
[Dynamic, Provider("CIMWin32"), SupportsCreate, CreateBy("Create"), SupportsDelete, DeleteBy("DeleteInstance"), UUID("{8502C4DC-5FBB-11D2-AAC1-006008C78BC7}"), DisplayName("Processes"), AMENDMENT]
class Win32_Process : CIM_Process
{
  string   CreationClassName;
  string   Caption;
  string   CommandLine;
  datetime CreationDate;
  string   CSCreationClassName;
  string   CSName;
  string   Description;
  string   ExecutablePath;
  uint16   ExecutionState;
  string   Handle;
  uint32   HandleCount;
  datetime InstallDate;
  uint64   KernelModeTime;
  uint32   MaximumWorkingSetSize;
  uint32   MinimumWorkingSetSize;
  string   Name;
  string   OSCreationClassName;
  string   OSName;
  uint64   OtherOperationCount;
  uint64   OtherTransferCount;
  uint32   PageFaults;
  uint32   PageFileUsage;
  uint32   ParentProcessId;
  uint32   PeakPageFileUsage;
  uint64   PeakVirtualSize;
  uint32   PeakWorkingSetSize;
  uint32   Priority = NULL;
  uint64   PrivatePageCount;
  uint32   ProcessId;
  uint32   QuotaNonPagedPoolUsage;
  uint32   QuotaPagedPoolUsage;
  uint32   QuotaPeakNonPagedPoolUsage;
  uint32   QuotaPeakPagedPoolUsage;
  uint64   ReadOperationCount;
  uint64   ReadTransferCount;
  uint32   SessionId;
  string   Status;
  datetime TerminationDate;
  uint32   ThreadCount;
  uint64   UserModeTime;
  uint64   VirtualSize;
  string   WindowsVersion;
  uint64   WorkingSetSize;
  uint64   WriteOperationCount;
  uint64   WriteTransferCount;
};
```

## <a name="members"></a>Membros

A classe de **\_ processo do Win32** tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

A **classe \_ process do Win32** tem esses métodos.



| Método                                                                   | Descrição                                                                                                                                                                                                                                                                               |
|:-------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AttachDebugger**](attachdebugger-method-in-class-win32-process.md)   | Inicia o depurador atualmente registrado para um processo.<br/>                                                                                                                                                                                                                      |
| [**Criar**](create-method-in-class-win32-process.md)                   | Cria um novo processo.<br/>                                                                                                                                                                                                                                                         |
| [**GetAvailableVirtualSize**](getavailablevirtualsize-win32-process.md) | Recupera o tamanho atual, em bytes, do espaço de endereço virtual livre disponível para o processo.<br/> **Windows server 2012, Windows 8, Windows 7, Windows server 2008 e Windows Vista:** Esse método não tem suporte antes do Windows 8.1 e do Windows Server 2012 R2.<br/> |
| [**GetOwner**](getowner-method-in-class-win32-process.md)               | Recupera o nome de usuário e o nome de domínio sob os quais o processo está em execução.<br/>                                                                                                                                                                                                    |
| [**Getownerid**](getownersid-method-in-class-win32-process.md)         | Recupera o identificador de segurança (SID) do proprietário de um processo.<br/>                                                                                                                                                                                                            |
| [**Setanteriority**](setpriority-method-in-class-win32-process.md)         | Altera a prioridade de execução de um processo.<br/>                                                                                                                                                                                                                                   |
| [**Encerrar**](terminate-method-in-class-win32-process.md)             | Encerra um processo e todos os seus threads.<br/>                                                                                                                                                                                                                                   |



 

### <a name="properties"></a>Propriedades

A **classe \_ process do Win32** tem essas propriedades.

<dl> <dt>

**Legenda**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**maxlen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")
</dt> </dl>

Breve descrição de um objeto — uma cadeia de caracteres de uma linha.

Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

</dd> <dt>

**CommandLine**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("linha de comando para iniciar o processo")
</dt> </dl>

Linha de comando usada para iniciar um processo específico, se aplicável.

</dd> <dt>

**CreationClassName**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**\_ chave CIM**](../wmisdk/standard-wmi-qualifiers.md), [**maxlen**](../wmisdk/standard-qualifiers.md) (256), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("nome da classe")
</dt> </dl>

Nome da classe ou subclasse usada na criação de uma instância. Quando usado com outras propriedades de chave da classe, essa propriedade permite que todas as instâncias da classe e suas subclasses sejam identificadas exclusivamente.

Essa propriedade é herdada [**do \_ processo CIM**](cim-process.md).

</dd> <dt>

**CreationDate**
</dt> <dd> <dl> <dt>

Tipo de dados: **DateTime**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**Fixed**](../wmisdk/standard-wmi-qualifiers.md), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("CreationDate")
</dt> </dl>

Data em que o processo começa a ser executado.

Essa propriedade é herdada [**do \_ processo CIM**](cim-process.md).

</dd> <dt>

**CSCreationClassName**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**propagados**](../wmisdk/standard-qualifiers.md) ("sistema [**\_ operacional CIM**](cim-operatingsystem.md).**CSCreationClassName**"), [**\_ chave CIM**](../wmisdk/standard-wmi-qualifiers.md), [**maxlen**](../wmisdk/standard-qualifiers.md) (256), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" nome da classe do sistema de computador ")
</dt> </dl>

Nome da classe de criação do sistema de computador de escopo.

Essa propriedade é herdada [**do \_ processo CIM**](cim-process.md).

</dd> <dt>

**CSName**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**propagados**](../wmisdk/standard-qualifiers.md) ("sistema [**\_ operacional CIM**](cim-operatingsystem.md).**CSName**"), [**\_ chave CIM**](../wmisdk/standard-wmi-qualifiers.md), [**maxlen**](../wmisdk/standard-qualifiers.md) (256), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" nome do sistema de computador ")
</dt> </dl>

Nome do sistema de computador de escopo.

Essa propriedade é herdada [**do \_ processo CIM**](cim-process.md).

</dd> <dt>

**Descrição**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Descrição")
</dt> </dl>

Descrição de um objeto.

Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

</dd> <dt>

**ExecutablePath**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**Privileges**](../wmisdk/standard-wmi-qualifiers.md) ("SeDebugPrivilege"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api de \| ferramentas de ajuda da ferramenta \| [**MODULEENTRY32**](/windows/win32/api/tlhelp32/ns-tlhelp32-moduleentry32) \| szExePath"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("caminho executável")
</dt> </dl>

Caminho para o arquivo executável do processo.

Exemplo: "C: \\ Windows \\ System \\Explorer.Exe"

</dd> <dt>

**ExecutionState**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("estado de execução")
</dt> </dl>

Condição operacional atual do processo.

Essa propriedade é herdada [**do \_ processo CIM**](cim-process.md).

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)


</dt> <dd>

Unknown

</dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outro** (1)


</dt> <dd>

Outro

</dd> <dt>

<span id="Ready"></span><span id="ready"></span><span id="READY"></span>

<span id="Ready"></span><span id="ready"></span><span id="READY"></span>**Pronto** (2)


</dt> <dd></dd> <dt>

<span id="Running"></span><span id="running"></span><span id="RUNNING"></span>

<span id="Running"></span><span id="running"></span><span id="RUNNING"></span>**Em execução** (3)


</dt> <dd></dd> <dt>

<span id="Blocked"></span><span id="blocked"></span><span id="BLOCKED"></span>

<span id="Blocked"></span><span id="blocked"></span><span id="BLOCKED"></span>**Bloqueado** (4)


</dt> <dd>

Bloqueado

</dd> <dt>

<span id="Suspended_Blocked"></span><span id="suspended_blocked"></span><span id="SUSPENDED_BLOCKED"></span>

<span id="Suspended_Blocked"></span><span id="suspended_blocked"></span><span id="SUSPENDED_BLOCKED"></span>**Bloqueado suspenso** (5)


</dt> <dd></dd> <dt>

<span id="Suspended_Ready"></span><span id="suspended_ready"></span><span id="SUSPENDED_READY"></span>

<span id="Suspended_Ready"></span><span id="suspended_ready"></span><span id="SUSPENDED_READY"></span>**Pronto suspenso** (6)


</dt> <dd></dd> <dt>

<span id="Terminated"></span><span id="terminated"></span><span id="TERMINATED"></span>

<span id="Terminated"></span><span id="terminated"></span><span id="TERMINATED"></span>**Encerrado** (7)


</dt> <dd></dd> <dt>

<span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>

<span id="Stopped"></span><span id="stopped"></span><span id="STOPPED"></span>**Parado** (8)


</dt> <dd></dd> <dt>

<span id="Growing"></span><span id="growing"></span><span id="GROWING"></span>

<span id="Growing"></span><span id="growing"></span><span id="GROWING"></span>**Crescendo** (9)


</dt> <dd></dd> </dl>

</dd> <dt>

**Handle**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**Key**](../wmisdk/key-qualifier.md), [**maxlen**](../wmisdk/standard-qualifiers.md) (256), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Handle")
</dt> </dl>

Identificador de processo.

Essa propriedade é herdada [**do \_ processo CIM**](cim-process.md).

</dd> <dt>

**HandleCount**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api de \| status do processo de processamento do \| sistema \_ \_ \| HandleCount"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("contagem de identificadores")
</dt> </dl>

Número total de identificadores abertos de Propriedade do processo. **HandleCount** é a soma dos identificadores abertos no momento por cada thread nesse processo. Um identificador é usado para examinar ou modificar os recursos do sistema. Cada identificador tem uma entrada em uma tabela mantida internamente. As entradas contêm os endereços dos recursos e dados para identificar o tipo de recurso.

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

Tipo de dados: **DateTime**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Componente DMTF \| 1,5 "), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" data de instalação ")
</dt> </dl>

Data em que um objeto é instalado. O objeto pode ser instalado sem que um valor seja gravado nessa propriedade.

Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

</dd> <dt>

**KernelModeTime**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt64**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**override**](../wmisdk/standard-qualifiers.md) ("KernelModeTime"), [**Units**](../wmisdk/standard-qualifiers.md) ("100 nanossegundos")
</dt> </dl>

Tempo no modo kernel, em milissegundos. Se essas informações não estiverem disponíveis, use um valor de 0 (zero).

Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](../wmisdk/creating-a-wmi-script.md).

</dd> <dt>

**MaximumWorkingSetSize**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**Privileges**](../wmisdk/standard-wmi-qualifiers.md) ("SeDebugPrivilege"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32 \| Winnt. H \| cota \_ limita \| MaximumWorkingSetSize "), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" tamanho máximo do conjunto de trabalho "), [**unidades**](../wmisdk/standard-qualifiers.md) (" quilobytes ")
</dt> </dl>

Tamanho máximo do conjunto de trabalho do processo. O conjunto de trabalho de um processo é o conjunto de páginas de memória visíveis para o processo na RAM física. Essas páginas são residentes e estão disponíveis para um aplicativo usar sem disparar uma falha de página.

Exemplo: 1413120

</dd> <dt>

**MinimumWorkingSetSize**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**Privileges**](../wmisdk/standard-wmi-qualifiers.md) ("SeDebugPrivilege"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32 \| Winnt. H \| cota \_ limita \| MinimumWorkingSetSize "), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" tamanho mínimo do conjunto de trabalho "), [**unidades**](../wmisdk/standard-qualifiers.md) (" quilobytes ")
</dt> </dl>

Tamanho mínimo do conjunto de trabalho do processo. O conjunto de trabalho de um processo é o conjunto de páginas de memória visíveis para o processo na RAM física. Essas páginas são residentes e estão disponíveis para um aplicativo usar sem disparar uma falha de página.

Exemplo: 20480

</dd> <dt>

**Nome**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")
</dt> </dl>

Nome do arquivo executável responsável pelo processo, equivalente à propriedade nome da imagem no Gerenciador de tarefas.

Quando herdado por uma subclasse, a propriedade pode ser substituída para ser uma propriedade de chave. O nome é embutido em código no próprio aplicativo e não é afetado pela alteração do nome do arquivo. Por exemplo, mesmo se você renomear Calc.exe, o nome Calc.exe ainda será exibido no Gerenciador de tarefas e em qualquer script WMI que recupere o nome do processo.

Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

</dd> <dt>

**OSCreationClassName**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**propagados**](../wmisdk/standard-qualifiers.md) ("sistema [**\_ operacional CIM**](cim-operatingsystem.md).**CreationClassName**"), [**\_ chave CIM**](../wmisdk/standard-wmi-qualifiers.md), [**maxlen**](../wmisdk/standard-qualifiers.md) (256), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" nome da classe do sistema operacional ")
</dt> </dl>

Nome da classe de criação do sistema operacional de escopo.

Essa propriedade é herdada [**do \_ processo CIM**](cim-process.md).

</dd> <dt>

**OSName**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**propagados**](../wmisdk/standard-qualifiers.md) ("sistema [**\_ operacional CIM**](cim-operatingsystem.md).**Name**"), [**CIM \_ Key**](../wmisdk/standard-wmi-qualifiers.md), [**maxlen**](../wmisdk/standard-qualifiers.md) (256), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" nome do sistema operacional ")
</dt> </dl>

Nome do sistema operacional de escopo.

Essa propriedade é herdada [**do \_ processo CIM**](cim-process.md).

</dd> <dt>

**OtherOperationCount**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt64**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| processo e estruturas de thread \| informações do processo do sistema \_ \_ \| OtherOperationCount"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("outra contagem de operação")
</dt> </dl>

Número de operações de e/s executadas que não são operações de leitura ou gravação.

Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](../wmisdk/creating-a-wmi-script.md).

</dd> <dt>

**OtherTransferCount**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt64**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| processo e estruturas de thread \| informações do processo do sistema \_ \_ \| OtherTransferCount"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("outras contagens de transferência"), [**unidades**](../wmisdk/standard-qualifiers.md) ("bytes")
</dt> </dl>

Quantidade de dados transferidos durante operações que não são operações de leitura ou de gravação.

Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](../wmisdk/creating-a-wmi-script.md).

</dd> <dt>

**PageFaults**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| de status \| \_ do processo \_ de processos do sistema \| PageFaultCount"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("número de falhas de página")
</dt> </dl>

Número de falhas de página que um processo gera.

Exemplo: 10

</dd> <dt>

**PageFileUsage**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api processo de status do processo do \| \| sistema \_ \_ \| PagefileUsage"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("uso do arquivo de paginação"), [**unidades**](../wmisdk/standard-qualifiers.md) ("quilobytes")
</dt> </dl>

Quantidade de espaço de arquivo de paginação que um processo está usando no momento. Esse valor é consistente com o valor de **VMSize** em TaskMgr.exe.

Exemplo: 102435

</dd> <dt>

**ParentProcessId**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api processo de status do processo do \| \| sistema \_ \_ \| InheritedFromUniqueProcessId"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("ID do processo pai")
</dt> </dl>

Identificador exclusivo do processo que cria um processo. Os números de identificador de processo são reutilizados, portanto, eles identificam apenas um processo durante o tempo de vida desse processo. É possível que o processo identificado pelo **ParentProcessID** seja encerrado; portanto, **ParentProcessID** pode não se referir a um processo em execução. Também é possível que o **ParentProcessID** incorretamente faça referência a um processo que reutiliza um identificador de processo. Você pode usar a propriedade **CreationDate** para determinar se o pai especificado foi criado depois que o processo representado por essa instância de **\_ processo Win32** foi criado.

</dd> <dt>

**PeakPageFileUsage**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api de \| status do processo de estado do \| sistema \_ \_ \| PeakPagefileUsage"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("uso de arquivo de página de pico"), [**unidades**](../wmisdk/standard-qualifiers.md) ("kilobytes")
</dt> </dl>

Quantidade máxima de espaço de arquivo de paginação usada durante a vida útil de um processo.

Exemplo: 102367

</dd> <dt>

**PeakVirtualSize**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt64**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api processo de status do processo do \| \| sistema \_ \_ \| PeakVirtualSize"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("pico de uso do espaço de endereço de virtual"), [**unidades**](../wmisdk/standard-qualifiers.md) ("bytes")
</dt> </dl>

Espaço de endereço virtual máximo que um processo usa a qualquer momento. O uso do espaço de endereço virtual não implica necessariamente o uso correspondente do disco ou das páginas de memória principal. No entanto, o espaço virtual é finito e usar muito o processo pode não ser capaz de carregar bibliotecas.

Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](../wmisdk/creating-a-wmi-script.md).

</dd> <dt>

**PeakWorkingSetSize**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api estado do processo do \| \| sistema status \_ \_ \| PeakWorkingSetSize"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("tamanho do conjunto de trabalho de pico"), [**unidades**](../wmisdk/standard-qualifiers.md) ("quilobytes")
</dt> </dl>

Tamanho do conjunto de trabalho de pico de um processo.

Exemplo: 1413120

</dd> <dt>

**Prioridade**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**substituir**](../wmisdk/standard-qualifiers.md) ("Priority"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| processo de estado do sistema de status \| \_ \_ \| BasePriority"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Priority")
</dt> </dl>

Prioridade de agendamento de um processo em um sistema operacional. Quanto maior o valor, maior a prioridade que um processo recebe. Os valores de prioridade podem variar de 0 (zero), que é a prioridade mais baixa para 31, que é a prioridade mais alta.

Exemplo: 7

</dd> <dt>

**PrivatePageCount**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt64**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api de \| status do processo de processos do \| sistema \_ \_ \| PrivatePageCount"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("contagem de páginas particulares")
</dt> </dl>

Número atual de páginas alocadas que só podem ser acessadas pelo processo representado por essa instância de **\_ processo Win32** .

Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](../wmisdk/creating-a-wmi-script.md).

</dd> <dt>

**ProcessId**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api processo \| e estruturas de thread \| [**\_ informações de processo**](/windows/win32/api/processthreadsapi/ns-processthreadsapi-process_information) \| dwProcessId"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("ID do processo")
</dt> </dl>

Identificador numérico usado para distinguir um processo de outro. As ProcessIDs são válidas do tempo de criação do processo para processar o encerramento. Após o encerramento, esse mesmo identificador numérico pode ser aplicado a um novo processo.

Isso significa que você não pode usar o ProcessID sozinho para monitorar um processo específico. Por exemplo, um aplicativo pode ter um ProcessID de 7 e, em seguida, falhar. Quando um novo processo é iniciado, o novo processo pode ser atribuído a ProcessID 7. Um script que é verificado apenas para um ProcessID especificado poderia, portanto, ser "enganado" para pensar que o aplicativo original ainda estava em execução.

</dd> <dt>

**QuotaNonPagedPoolUsage**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api processo de status do processo do \| \| sistema \_ \_ \| QuotaNonPagedPoolUsage"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("cota de uso de pool não paginável")
</dt> </dl>

Valor da cota de uso de pool não paginável para um processo.

Exemplo: 15

</dd> <dt>

**QuotaPagedPoolUsage**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api processo de status do processo do \| \| sistema \_ \_ \| QuotaPagedPoolUsage"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("cota de uso do pool paginado")
</dt> </dl>

Quantidade de cota de uso de pool paginável para um processo.

Exemplo: 22

</dd> <dt>

**QuotaPeakNonPagedPoolUsage**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api processo de status do processo do \| \| sistema \_ \_ \| QuotaPeakNonPagedPoolUsage"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("pico de cota de uso de pool não paginável")
</dt> </dl>

Valor da cota de pico do uso do pool não paginado para um processo.

Exemplo: 31

</dd> <dt>

**QuotaPeakPagedPoolUsage**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api processo de status do processo do \| \| sistema \_ \_ \| QuotaPeakPagedPoolUsage"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("cota de uso do pool de picos de página")
</dt> </dl>

Valor da cota de pico do uso do pool paginado para um processo.

Exemplo: 31

</dd> <dt>

**ReadOperationCount**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt64**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| processo e estruturas de thread \| informações do processo do sistema \_ \_ \| ReadOperationCount"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("contagem de operação de leitura")
</dt> </dl>

Número de operações de leitura executadas.

Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](../wmisdk/creating-a-wmi-script.md).

</dd> <dt>

**ReadTransferCount**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt64**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| processo e estruturas de thread \| informações do processo do sistema \_ \_ \| ReadTransferCount"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("contagem de transferência de leitura"), [**unidades**](../wmisdk/standard-qualifiers.md) ("bytes")
</dt> </dl>

Quantidade de dados lidos.

Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](../wmisdk/creating-a-wmi-script.md).

</dd> <dt>

**SessionId**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api de \| status do processo de processamento do sistema ID do processo \| \_ \_ \| "), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("ID da sessão")
</dt> </dl>

Identificador exclusivo que um sistema operacional gera quando uma sessão é criada. Uma sessão abrange um período de tempo desde o logon até o logoff de um sistema específico.

</dd> <dt>

**Status**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**maxlen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("status")
</dt> </dl>

Esta propriedade não está implementada e não é preenchida para nenhuma instância dessa classe. Ele é sempre **nulo**.

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

**TerminationDate**
</dt> <dd> <dl> <dt>

Tipo de dados: **DateTime**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("data de término")
</dt> </dl>

O processo foi interrompido ou encerrado. Para obter o tempo de encerramento, um identificador para o processo deve ser mantido aberto. Caso contrário, essa propriedade retornará **NULL**.

Essa propriedade é herdada [**do \_ processo CIM**](cim-process.md).

</dd> <dt>

**ThreadCount**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api processo de status do processo do \| \| sistema \_ \_ \| NumberOfThreads"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("contagem de threads")
</dt> </dl>

Número de threads ativos em um processo. Uma instrução é a unidade básica de execução em um processador e um thread é o objeto que executa uma instrução. Cada processo em execução tem pelo menos um thread.

</dd> <dt>

**Usermodetime**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt64**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**substituir**](../wmisdk/standard-qualifiers.md) ("usermodetime"), [**Units**](../wmisdk/standard-qualifiers.md) ("100 nanossegundos")
</dt> </dl>

Tempo no modo de usuário, em unidades de 100 nanossegundos. Se essas informações não estiverem disponíveis, use um valor de 0 (zero).

Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](../wmisdk/creating-a-wmi-script.md).

</dd> <dt>

**VirtualSize**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt64**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api processo de status do processo do \| \| sistema \_ \_ \| VirtualSize"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("uso do espaço de endereço virtual"), [**unidades**](../wmisdk/standard-qualifiers.md) ("bytes")
</dt> </dl>

Tamanho atual do espaço de endereço virtual que um processo está usando, não a memória física ou virtual realmente usada pelo processo. O uso do espaço de endereço virtual não implica necessariamente o uso correspondente do disco ou das páginas de memória principal. O espaço virtual é finito e, usando muito, o processo pode não ser capaz de carregar bibliotecas. Esse valor é consistente com o que você vê no Perfmon.exe.

Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](../wmisdk/creating-a-wmi-script.md).

</dd> <dt>

**WindowsVersion**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| process and thread Functions \| GetProcessVersion"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("versão do Windows")
</dt> </dl>

Versão do Windows em que o processo está sendo executado.

Exemplo: 4,0

</dd> <dt>

**WorkingSetSize**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt64**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("tamanho do conjunto de trabalho"), [**unidades**](../wmisdk/standard-qualifiers.md) ("bytes")
</dt> </dl>

Quantidade de memória, em bytes, que um processo precisa para ser executado com eficiência — para um sistema operacional que usa o gerenciamento de memória baseado em página. Se o sistema não tiver memória suficiente (menos que o tamanho do conjunto de trabalho), ultrapaginação ocorrerá. Se o tamanho do conjunto de trabalho não for conhecido, use **NULL** ou 0 (zero). Se os dados do conjunto de trabalho forem fornecidos, você poderá monitorar as informações para entender os requisitos de memória em constante mudança de um processo.

Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](../wmisdk/creating-a-wmi-script.md).

Essa propriedade é herdada [**do \_ processo CIM**](cim-process.md).

</dd> <dt>

**WriteOperationCount**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt64**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| processo e estruturas de thread \| informações do processo do sistema \_ \_ \| WriteOperationCount"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("contagem da operação de gravação")
</dt> </dl>

Número de operações de gravação executadas.

Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](../wmisdk/creating-a-wmi-script.md).

</dd> <dt>

**WriteTransferCount**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt64**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("win32api \| processo e estruturas de thread \| informações do processo do sistema \_ \_ \| WriteTransferCount"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("contagem de transferência de gravação"), [**unidades**](../wmisdk/standard-qualifiers.md) ("bytes")
</dt> </dl>

Quantidade de dados gravados.

Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](../wmisdk/creating-a-wmi-script.md).

</dd> </dl>

## <a name="remarks"></a>Comentários

A classe de **\_ processo do Win32** é derivada do [**\_ processo CIM**](cim-process.md). O processo de chamada que usa essa classe deve ter o privilégio **se \_ Restore \_ Name** no computador em que o registro reside. Para obter mais informações, consulte [executando operações privilegiadas](../wmisdk/executing-privileged-operations.md).

### <a name="overview"></a>Visão geral

Processa quase tudo o que acontece em um computador. Na verdade, a causa raiz da maioria dos problemas do computador pode ser rastreada para processos; por exemplo, muitos processos podem estar em execução em um computador (e contendendo um conjunto finito de recursos), ou um único processo pode estar usando mais do que sua parcela de recursos. Esses fatores tornam importante manter uma inspeção próxima dos processos em execução em um computador. O monitoramento de processos, a principal atividade no gerenciamento de processos, permite que você determine o que um computador realmente faz, quais aplicativos o computador executa e como esses aplicativos são afetados por alterações no ambiente computacional.

### <a name="monitoring-a-process"></a>Monitorando um processo

O monitoramento de processos regularmente ajuda a garantir que um computador seja executado no máximo de eficiência e que ele execute suas tarefas deferidas conforme o esperado. Por exemplo, monitorando processos você pode ser notificado imediatamente de qualquer aplicativo que tenha parado de responder e, em seguida, executar etapas para encerrar esse processo. Além disso, o monitoramento de processos permite que você identifique problemas antes que eles ocorram. Por exemplo, verificando repetidamente a quantidade de memória usada por um processo, você pode identificar um vazamento de memória. Em seguida, você pode parar o processo antes que o aplicativo errônea use toda a memória disponível e coloque o computador em uma parada.

O monitoramento de processos também ajuda a minimizar as interrupções causadas por interrupções planejadas para atualizações e manutenção. Por exemplo, ao verificar o status de um aplicativo de banco de dados em execução em computadores cliente, você pode determinar o impacto de colocar o banco de dados offline para atualizar o software.

Monitorando a disponibilidade do processo. Mede a porcentagem de tempo em que um processo está disponível. A disponibilidade normalmente é monitorada pelo uso de uma investigação simples, que relata se o processo ainda está em execução. Ao manter o controle dos resultados de cada investigação, você pode calcular a disponibilidade do processo. Por exemplo, um processo que é investigado 100 vezes e responde em 95 dessas ocasiões tem uma disponibilidade de 95%. Esse tipo de monitoramento normalmente é reservado para bancos de dados, programas de email e outros aplicativos que devem ser executados em todos os momentos. Não é apropriado para programas de processamento de texto, planilhas ou outros aplicativos que são rotineiramente iniciados e interrompidos várias vezes por dia.

Você pode criar uma instância da classe [**Win32 \_ ProcessStartup**](win32-processstartup.md) para configurar o processo.

Você pode monitorar o desempenho do processo com a classe de [**\_ \_ \_ processo Win32 PerfFormattedData PerfProc**](../wmisdk/retrieving-raw-and-formatted-performance-data.md) e um objeto atualizador WMI, como [**SWbemRefresher**](../wmisdk/swbemrefresher.md). Para obter mais informações, consulte [monitorando dados de desempenho](../wmisdk/monitoring-performance-data.md).

## <a name="examples"></a>Exemplos

A [lista as propriedades do exemplo de código do PowerShell de classes WMI](https://Gallery.TechNet.Microsoft.Com/a7918bf3-bc03-4553-990f-aba13cf196b7) na galeria do TechNet descreve a classe de **\_ processo do Win32** e gera os resultados no formato do Excel.

O [processo de encerramento em execução em vários servidores](https://Gallery.TechNet.Microsoft.Com/698c2512-2bbd-40ee-b3bf-a9cebdad2faf) encerra um processo em execução em um único ou vários computadores.

No [exemplo: chamando um](../wmisdk/example--calling-a-provider-method.md) tópico de método de provedor, o código usa C++ para chamar o **\_ processo Win32** para criar um processo.

A disponibilidade é a forma mais simples de monitoramento de processos: com essa abordagem, você simplesmente garante que o processo esteja em execução. Quando você monitora a disponibilidade do processo, normalmente recupera uma lista de processos em execução em um computador e, em seguida, verifica se um processo específico ainda está ativo. Se o processo estiver ativo, ele será considerado disponível. Se o processo não estiver ativo, ele não estará disponível. O exemplo de VBScript a seguir monitora a disponibilidade do processo verificando a lista de processos em execução em um computador e emitindo uma notificação se o processo de Database.exe não for encontrado.


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colProcesses = objWMIService.ExecQuery("SELECT * FROM Win32_Process WHERE Name = 'Database.exe'")
If colProcesses.Count = 0 Then
 Wscript.Echo "Database.exe is not running."
Else
 Wscript.Echo "Database.exe is running."
End If
```



O exemplo de VBScript a seguir monitora a criação de processos usando um consumidor de evento temporário.


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colMonitoredProcesses = objWMIService.ExecNotificationQuery("SELECT * FROM __InstanceCreationEvent " _
                                                     & "WITHIN 10 WHERE TargetInstance ISA 'Win32_Process'")
i = 0
Do While i = 0
 Set objLatestProcess = colMonitoredProcesses.NextEvent
 Wscript.Echo objLatestProcess.TargetInstance.Name, Now
Loop
```



O VBScript a seguir monitora as informações de desempenho do processo.


```VB
strComputer = "."
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")
Set colProcessList = objWMIService.ExecQuery("SELECT * FROM Win32_Process")
For Each objProcess in colProcessList
 Wscript.Echo "Process: " & objProcess.Name
 Wscript.Echo "Process ID: " & objProcess.ProcessID
 Wscript.Echo "Thread Count: " & objProcess.ThreadCount
 Wscript.Echo "Page File Size: " & objProcess.PageFileUsage
 Wscript.Echo "Page Faults: " & objProcess.PageFaults
 Wscript.Echo "Working Set Size: " & objProcess.WorkingSetSize
Next
```



O exemplo de código VBScript a seguir mostra como obter o proprietário de cada processo em um computador local. Você pode usar esse script para obter dados de um computador remoto, por exemplo, para determinar quais usuários têm processos executando o Terminal Server, substituir o nome do computador remoto por "." na primeira linha. Você também deve ser um administrador no computador remoto.


```VB
strComputer = "." 
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2")

Set colProcesses = objWMIService.ExecQuery("select * from win32_process" )
For Each objProcess in colProcesses

  If objProcess.GetOwner ( User, Domain ) = 0 Then
    Wscript.Echo "Process " & objProcess.Caption & " belongs to " & Domain & "\" & User
  Else
    Wscript.Echo "Problem " & Rtn & " getting the owner for process " & objProcess.Caption
  End If
Next
```



O exemplo de código VBScript a seguir mostra como obter a sessão de logon associada a um processo em execução. Um processo deve estar em execução Notepad.exe antes de o script ser iniciado. O exemplo localiza as instâncias de [**\_ LogonSession do Win32**](win32-logonsession.md) associadas ao **\_ processo Win32** que representa Notepad.exe. [**Win32 \_ SessionProcess**](win32-sessionprocess.md) é especificado como a classe de associação. Para obter mais informações, consulte [ASSOCIATORS of Statement.](../wmisdk/associators-of-statement.md)


```VB
On error resume next
Set objWMIService = GetObject("winmgmts:{impersonationLevel=impersonate}!\\.\root\cimv2")
Set colProcesses = objWMIService.ExecQuery("Select * from Win32_Process Where Name = 'Notepad.exe'")
For Each objProcess in colProcesses
  ProcessId = objProcess.ProcessId
  Set colLogonSessions = objWMIService.ExecQuery("Associators of {Win32_Process='" & ProcessId & "'} " _
                                               & "Where Resultclass = Win32_LogonSession Assocclass = Win32_SessionProcess", "WQL", 48)
  If Err <> 0 Then
    WScript.Echo "Error on associators query= " & Err.number & " " & Err.Description
    WScript.Quit
  End If
  For Each LogonSession in colLogonSessions
    Wscript.Echo " Logon id is " & LogonSession.LogonId
  Next
Next
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

[**\_Processo CIM**](cim-process.md)
</dt> <dt>

[Classes do sistema operacional](./operating-system-classes.md)
</dt> <dt>

[Tarefas do WMI: processos](../wmisdk/wmi-tasks--processes.md)
</dt> </dl>

 

 
