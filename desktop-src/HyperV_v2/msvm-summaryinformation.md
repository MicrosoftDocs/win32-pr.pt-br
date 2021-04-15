---
description: Usado nos métodos GetSummaryInformation e GetDefinitionFileSummaryInformation da \_ classe Msvm VirtualSystemManagementService para recuperar rapidamente informações comuns relacionadas a uma máquina virtual ou instantâneo.
ms.assetid: 8D188BB2-4A56-4738-94DD-64D9F9B90B73
title: Classe Msvm_SummaryInformation
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SummaryInformation
- Msvm_SummaryInformation.InstanceID
- Msvm_SummaryInformation.AllocatedGPU
- Msvm_SummaryInformation.Shielded
- Msvm_SummaryInformation.AsynchronousTasks
- Msvm_SummaryInformation.CreationTime
- Msvm_SummaryInformation.ElementName
- Msvm_SummaryInformation.EnabledState
- Msvm_SummaryInformation.OtherEnabledState
- Msvm_SummaryInformation.GuestOperatingSystem
- Msvm_SummaryInformation.HealthState
- Msvm_SummaryInformation.Heartbeat
- Msvm_SummaryInformation.MemoryUsage
- Msvm_SummaryInformation.MemoryAvailable
- Msvm_SummaryInformation.AvailableMemoryBuffer
- Msvm_SummaryInformation.SwapFilesInUse
- Msvm_SummaryInformation.Name
- Msvm_SummaryInformation.Notes
- Msvm_SummaryInformation.Version
- Msvm_SummaryInformation.NumberOfProcessors
- Msvm_SummaryInformation.OperationalStatus
- Msvm_SummaryInformation.ProcessorLoad
- Msvm_SummaryInformation.ProcessorLoadHistory
- Msvm_SummaryInformation.Snapshots
- Msvm_SummaryInformation.StatusDescriptions
- Msvm_SummaryInformation.ThumbnailImage
- Msvm_SummaryInformation.ThumbnailImageHeight
- Msvm_SummaryInformation.ThumbnailImageWidth
- Msvm_SummaryInformation.UpTime
- Msvm_SummaryInformation.ReplicationState
- Msvm_SummaryInformation.ReplicationStateEx
- Msvm_SummaryInformation.ReplicationHealth
- Msvm_SummaryInformation.ReplicationHealthEx
- Msvm_SummaryInformation.ReplicationMode
- Msvm_SummaryInformation.TestReplicaSystem
- Msvm_SummaryInformation.ApplicationHealth
- Msvm_SummaryInformation.IntegrationServicesVersionState
- Msvm_SummaryInformation.MemorySpansPhysicalNumaNodes
- Msvm_SummaryInformation.ReplicationProviderId
- Msvm_SummaryInformation.EnhancedSessionModeState
- Msvm_SummaryInformation.VirtualSwitchNames
- Msvm_SummaryInformation.VirtualSystemSubType
- Msvm_SummaryInformation.HostComputerSystemName
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 817d025551ae10002b008a181edd8a7dfd2ec68c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105747563"
---
# <a name="msvm_summaryinformation-class"></a>\_Classe Msvm SummaryInformation

Usado nos métodos [**GetSummaryInformation**](getsummaryinformation-msvm-virtualsystemmanagementservice.md) e [**GetDefinitionFileSummaryInformation**](getdefinitionfilesummaryinformation-msvm-virtualsystemmanagementservice.md) da classe [**Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) para recuperar rapidamente informações comuns relacionadas a uma máquina virtual ou instantâneo.

A sintaxe a seguir é simplificada formato MOF código (MOF).

## <a name="syntax"></a>Sintaxe

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SummaryInformation : Msvm_SummaryInformationBase
{
  string                       InstanceID;
  string                       AllocatedGPU;
  boolean                      Shielded;
  CIM_ConcreteJob              AsynchronousTasks[];
  DateTime                     CreationTime;
  string                       ElementName;
  uint16                       EnabledState;
  string                       OtherEnabledState;
  string                       GuestOperatingSystem;
  uint16                       HealthState;
  uint16                       Heartbeat;
  uint64                       MemoryUsage;
  sint32                       MemoryAvailable;
  sint32                       AvailableMemoryBuffer;
  boolean                      SwapFilesInUse;
  string                       Name;
  string                       Notes;
  string                       Version;
  uint16                       NumberOfProcessors;
  uint16                       OperationalStatus[];
  uint16                       ProcessorLoad;
  uint16                       ProcessorLoadHistory[];
  CIM_VirtualSystemSettingData Snapshots[];
  string                       StatusDescriptions[];
  uint8                        ThumbnailImage[];
  uint16                       ThumbnailImageHeight;
  uint16                       ThumbnailImageWidth;
  uint64                       UpTime;
  uint16                       ReplicationState;
  uint16                       ReplicationStateEx[];
  uint16                       ReplicationHealth;
  uint16                       ReplicationHealthEx[];
  uint16                       ReplicationMode;
  CIM_ComputerSystem       REF TestReplicaSystem;
  uint16                       ApplicationHealth;
  uint16                       IntegrationServicesVersionState;
  boolean                      MemorySpansPhysicalNumaNodes;
  string                       ReplicationProviderId[];
  uint16                       EnhancedSessionModeState;
  string                       VirtualSwitchNames[];
  string                       VirtualSystemSubType;
  string                       HostComputerSystemName;
};
```

## <a name="members"></a>Membros

A classe **Msvm \_ SummaryInformation** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **Msvm \_ SummaryInformation** tem essas propriedades.

<dl> <dt>

**AllocatedGPU**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

O identificador da GPU (unidade de processamento gráfico) física alocada a esta máquina virtual. Essa propriedade só se aplica a máquinas virtuais que usam o RemoteFX.

</dd> <dt>

**ApplicationHealth**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

O status de integridade do aplicativo atual para a máquina virtual. Esta propriedade não é válida para instâncias de **Msvm \_ SummaryInformation** que representam um instantâneo de máquina virtual.

<dt>

<span id="OK"></span><span id="ok"></span>

**OK** (2)


</dt> <dd></dd> <dt>

<span id="Application_Critical"></span><span id="application_critical"></span><span id="APPLICATION_CRITICAL"></span>

**Aplicativo crítico** (32782)


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

**Desabilitado** (32896)


</dt> <dd></dd> </dl>

</dd> <dt>

**AsynchronousTasks**
</dt> <dd> <dl> <dt>

Tipo de dados: matriz de **\_ ConcreteJob CIM**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado")
</dt> </dl>

Uma matriz de instâncias do [**Msvm \_ ConcreteJob**](msvm-concretejob.md) que representam as operações assíncronas relacionadas à máquina virtual em execução no momento. Esta propriedade não é válida para instâncias de **Msvm \_ SummaryInformation** que representam um instantâneo de máquina virtual.

</dd> <dt>

**AvailableMemoryBuffer**
</dt> <dd> <dl> <dt>

Tipo de dados: **sint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

A porcentagem de buffer de memória disponível para a máquina virtual. Quando a memória dinâmica está habilitada para uma máquina virtual, essa propriedade representa a taxa de buffer de memória disponível para o buffer de memória ideal para a máquina virtual. O tamanho de buffer de memória ideal é configurado usando a propriedade **TargetMemoryBuffer** da classe [**Msvm \_ MemorySettingData**](msvm-memorysettingdata.md) .

Essa propriedade não é válida para instâncias da classe **Msvm \_ SummaryInformation** que representam máquinas virtuais para as quais a memória dinâmica não está habilitada.

Essa propriedade não é válida para instâncias da classe **Msvm \_ SummaryInformation** que representa um instantâneo de máquina virtual.

</dd> <dt>

**CreationTime**
</dt> <dd> <dl> <dt>

Tipo de dados: **DateTime**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

A hora em que a máquina virtual ou o instantâneo foi criado.

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

O nome de exibição para a máquina virtual ou o instantâneo.

</dd> <dt>

**EnabledState**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

O estado atual da máquina virtual ou do instantâneo. Consulte a propriedade **enabledstate** da classe [**Msvm \_ ComputerSystem**](msvm-computersystem.md) para obter os valores possíveis.

</dd> <dt>

**EnhancedSessionModeState**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Indica se as conexões de modo avançado são permitidas pelo host e, se forem permitidas, se estão disponíveis para a máquina virtual.

**Windows 8.1:** Não há suporte para esse valor até Windows 8.1 e Windows Server 2012 R2.

<dt>

<span id="Allowed_and_available"></span><span id="allowed_and_available"></span><span id="ALLOWED_AND_AVAILABLE"></span>

**Permitido e disponível** (2)


</dt> <dd></dd> <dt>

<span id="Not_allowed"></span><span id="not_allowed"></span><span id="NOT_ALLOWED"></span>

**Não permitido** (3)


</dt> <dd></dd> <dt>

<span id="Allowed_but_not_available"></span><span id="allowed_but_not_available"></span><span id="ALLOWED_BUT_NOT_AVAILABLE"></span>

**Permitido, mas não disponível** (6)


</dt> <dd></dd> </dl>

</dd> <dt>

**GuestOperatingSystem**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

O nome do sistema operacional convidado, se disponível. Se essas informações não estiverem disponíveis, o valor dessa propriedade será **NULL**. Esta propriedade não é válida para instâncias de **Msvm \_ SummaryInformation** que representam um instantâneo de máquina virtual.

</dd> <dt>

**HealthState**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

O estado de integridade atual para a máquina virtual. Esta propriedade não é válida para instâncias de **Msvm \_ SummaryInformation** que representam um instantâneo de máquina virtual.

</dd> <dt>

**Pulsação**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

O status de pulsação atual para a máquina virtual. Para obter mais informações, consulte a documentação da propriedade [**StatusDescriptions**](msvm-heartbeatcomponent.md) da classe **Msvm \_ HeartbeatComponent** . Esta propriedade não é válida para instâncias de **Msvm \_ SummaryInformation** que representam um instantâneo de máquina virtual.

<dl> <dt>

<span id="OK"></span><span id="ok"></span>**OK** (2)
</dt> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>**Erro** (6)
</dt> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>**Sem contato** (12)
</dt> <dt>

<span id="Lost_Communication"></span><span id="lost_communication"></span><span id="LOST_COMMUNICATION"></span>**Comunicação perdida** (13)
</dt> </dl>

</dd> <dt>

**HostComputerSystemName**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

O nome do computador que hospeda esta máquina virtual.

> [!Note]  
> Adicionado no Windows 10.

 

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**substituir**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ managedelement. InstanceId"), [**chave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

InstanceID é uma propriedade opcional que pode ser usada para identificar de forma opaca e exclusiva uma instância dessa classe dentro do escopo do namespace de instanciação. Várias subclasses dessa classe podem substituir essa propriedade para torná-la necessária ou uma chave. Essas subclasses também podem modificar os algoritmos preferenciais para garantir a exclusividade definida abaixo.

Para garantir a exclusividade no NameSpace, o valor de InstanceID deve ser construído usando o seguinte algoritmo "preferencial":

<OrgID>:<LocalID>

Onde <OrgID> e <LocalID> são separados por dois-pontos (:), e onde <OrgID> devem incluir um nome de direitos autorais, com marca registrada ou exclusivo que pertença à entidade de negócios que está criando ou definindo a InstanceId ou que é uma ID registrada atribuída à entidade de negócios por uma autoridade global reconhecida. (Esse requisito é semelhante ao <Schema Name> \_ <Class Name> estrutura de nomes de classe de esquema.) Além disso, para garantir a exclusividade, <OrgID> não deve conter dois-pontos (:). Ao usar esse algoritmo, os primeiros dois-pontos a serem exibidos em InstanceID devem aparecer entre <OrgID> e <LocalID> .

<LocalID> é escolhido pela entidade de negócios e não deve ser reutilizado para identificar elementos subjacentes (reais) diferentes. Se não for nulo e o algoritmo "preferencial" acima não for usado, a entidade de definição deverá garantir que a InstanceID resultante não seja reutilizada em quaisquer InstanceIDs produzidas por este ou outros provedores para o NameSpace dessa instância.

Se não estiver definido como nulo para instâncias definidas por DMTF, o algoritmo "preferencial" deverá ser usado com o <OrgID> conjunto como CIM.

> [!Note]  
> Adicionado no Windows 10.

 

</dd> <dt>

**IntegrationServicesVersionState**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Indica se os serviços de integração instalados na máquina virtual estão atualizados.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Desconhecido** (0)


</dt> <dd></dd> <dt>

<span id="UpToDate"></span><span id="uptodate"></span><span id="UPTODATE"></span>

**UpToDate** (1)


</dt> <dd></dd> <dt>

<span id="Mismatch"></span><span id="mismatch"></span><span id="MISMATCH"></span>

**Incompatibilidade** (2)


</dt> <dd></dd> </dl>

</dd> <dt>

**MemoryAvailable**
</dt> <dd> <dl> <dt>

Tipo de dados: **sint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

A porcentagem da memória atual disponível para a máquina virtual. Quando a memória dinâmica está habilitada para uma máquina virtual, essa propriedade representa a taxa de memória disponível da máquina virtual para a memória física total atribuída à máquina virtual. Quando uma máquina virtual não tem memória disponível, essa propriedade será negativa e conterá a taxa de memória necessária para a máquina virtual para a memória física total atribuída à máquina virtual.

Essa propriedade não é válida para instâncias da classe **Msvm \_ SummaryInformation** que representam máquinas virtuais para as quais a memória dinâmica não está habilitada.

Essa propriedade não é válida para instâncias da classe **Msvm \_ SummaryInformation** que representa um instantâneo de máquina virtual.

</dd> <dt>

**MemorySpansPhysicalNumaNodes**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Indica se a memória de um ou mais nós NUMA (acesso virtual não uniforme de memória) da máquina virtual abrange vários nós NUMA físicos do sistema de computador host. Contém **true** se a memória abranger vários nós numa físicos ou **false** caso contrário.

</dd> <dt>

**MemoryUsage**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt64**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

O uso de memória atual, em megabytes, da máquina virtual. Esta propriedade não é válida para instâncias de **Msvm \_ SummaryInformation** que representam um instantâneo de máquina virtual.

</dd> <dt>

**Nome**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

O nome exclusivo para a máquina virtual ou o instantâneo.

</dd> <dt>

**Observações**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

As notas associadas à máquina virtual ou ao instantâneo.

</dd> <dt>

**NumberOfProcessors**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

O número total de processadores virtuais alocados para a máquina virtual ou instantâneo.

</dd> <dt>

**OperationalStatus**
</dt> <dd> <dl> <dt>

Tipo de dados: a matriz **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado")
</dt> </dl>

Os status operacionais atuais da máquina virtual. Consulte a propriedade **OperationalStatus** da classe [**Msvm \_ ComputerSystem**](msvm-computersystem.md) para obter os valores possíveis.

</dd> <dt>

**OtherEnabledState**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Uma cadeia de caracteres que descreve o estado habilitado ou desabilitado do elemento quando a propriedade **enabledstate** é definida como 1. Essa propriedade será definida como **NULL** quando **enabledstate** for qualquer valor diferente de 1.

</dd> <dt>

**ProcessorLoad**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

O uso atual do processador da máquina virtual, em porcentagem. Esta propriedade não é válida para instâncias de **Msvm \_ SummaryInformation** que representam um instantâneo de máquina virtual.

</dd> <dt>

**ProcessorLoadHistory**
</dt> <dd> <dl> <dt>

Tipo de dados: a matriz **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado")
</dt> </dl>

Uma matriz dos 100 exemplos anteriores do uso do processador, em porcentagem, para a máquina virtual. Esta propriedade não é válida para instâncias de **Msvm \_ SummaryInformation** que representam um instantâneo de máquina virtual.

</dd> <dt>

**ReplicationHealth**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**preteridos**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("**Msvm \_ SummaryInformation**.**ReplicationHealthEx**")
</dt> </dl>

A integridade da replicação para a máquina virtual. Consulte a propriedade **ReplicationHealth** da classe [**Msvm \_ ComputerSystem**](msvm-computersystem.md) para obter os valores possíveis.

> [!Note]  
> Esta propriedade foi preterida a partir de Windows 8.1; em vez disso, use o **ReplicationHealthEx**.

 

<dt>

<span id="Not_applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

**Não aplicável** (0)


</dt> <dd></dd> <dt>

<span id="Ok"></span><span id="ok"></span><span id="OK"></span>

**OK** (1)


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

**Aviso** (2)


</dt> <dd></dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

**Crítico** (3)


</dt> <dd></dd> </dl>

</dd> <dt>

**ReplicationHealthEx**
</dt> <dd> <dl> <dt>

Tipo de dados: a matriz **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado")
</dt> </dl>

A matriz de valores de integridade de replicação para os vários relacionamentos de replicação da máquina virtual. Consulte a propriedade **ReplicationHealth** da classe [**Msvm \_ ReplicationRelationship**](msvm-replicationrelationship.md) para obter os valores possíveis.

<dt>

<span id="Not_applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

**Não aplicável** (0)


</dt> <dd></dd> <dt>

<span id="Ok"></span><span id="ok"></span><span id="OK"></span>

**OK** (1)


</dt> <dd></dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

**Aviso** (2)


</dt> <dd></dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

**Crítico** (3)


</dt> <dd></dd> </dl>

</dd> <dt>

**ReplicationMode**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

O tipo de replicação para a máquina virtual. Consulte a propriedade **replicationmode** da classe [**Msvm \_ ComputerSystem**](msvm-computersystem.md) para obter os valores possíveis.

<dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

**Nenhum** (0)


</dt> <dd></dd> <dt>

<span id="Primary"></span><span id="primary"></span><span id="PRIMARY"></span>

**Primário** (1)


</dt> <dd></dd> <dt>

<span id="Replica"></span><span id="replica"></span><span id="REPLICA"></span>

**Réplica** (2)


</dt> <dd></dd> <dt>

<span id="Test_Replica"></span><span id="test_replica"></span><span id="TEST_REPLICA"></span>

**Réplica de teste** (3)


</dt> <dd></dd> <dt>

<span id="Extended_Replica"></span><span id="extended_replica"></span><span id="EXTENDED_REPLICA"></span>

**Réplica estendida** (4)


</dt> <dd></dd> </dl>

</dd> <dt>

**ReplicationProviderId**
</dt> <dd> <dl> <dt>

Tipo de dados: matriz de **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado")
</dt> </dl>

Para a máquina virtual de réplica primária ou estendida, esta é a ID de provedor de replicação primária. Para uma máquina virtual de réplica e se a replicação estendida estiver habilitada, essa será a ID do provedor para a relação estendida.

**Windows 8.1:** Não há suporte para esse valor até Windows 8.1 e Windows Server 2012 R2.

</dd> <dt>

**ReplicationState**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**preteridos**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("**Msvm \_ SummaryInformation**.**ReplicationStateEx**")
</dt> </dl>

O estado de replicação para a máquina virtual. Consulte a propriedade **replicationstate** da classe [**Msvm \_ ComputerSystem**](msvm-computersystem.md) para obter os valores possíveis.

> [!Note]  
> Esta propriedade foi preterida a partir de Windows 8.1; em vez disso, use o **ReplicationStateEx**.

 

<dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

**Desabilitado** (0)


</dt> <dd></dd> <dt>

<span id="Ready_for_replication"></span><span id="ready_for_replication"></span><span id="READY_FOR_REPLICATION"></span>

**Pronto para replicação** (1)


</dt> <dd></dd> <dt>

<span id="Waiting_to_complete_initial_replication"></span><span id="waiting_to_complete_initial_replication"></span><span id="WAITING_TO_COMPLETE_INITIAL_REPLICATION"></span>

**Aguardando para concluir a replicação inicial** (2)


</dt> <dd></dd> <dt>

<span id="Replicating"></span><span id="replicating"></span><span id="REPLICATING"></span>

**Replicando** (3)


</dt> <dd></dd> <dt>

<span id="Synced_replication_complete"></span><span id="synced_replication_complete"></span><span id="SYNCED_REPLICATION_COMPLETE"></span>

**Replicação sincronizada concluída** (4)


</dt> <dd></dd> <dt>

<span id="Recovered"></span><span id="recovered"></span><span id="RECOVERED"></span>

**Recuperado** (5)


</dt> <dd></dd> <dt>

<span id="Committed"></span><span id="committed"></span><span id="COMMITTED"></span>

**Confirmado** (6)


</dt> <dd></dd> <dt>

<span id="Suspended"></span><span id="suspended"></span><span id="SUSPENDED"></span>

**Suspenso** (7)


</dt> <dd></dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

**Crítico** (8)


</dt> <dd></dd> <dt>

<span id="Waiting_to_start_resynchronization"></span><span id="waiting_to_start_resynchronization"></span><span id="WAITING_TO_START_RESYNCHRONIZATION"></span>

**Aguardando para iniciar a ressincronização** (9)


</dt> <dd></dd> <dt>

<span id="Resynchronizing"></span><span id="resynchronizing"></span><span id="RESYNCHRONIZING"></span>

**Ressincronização** (10)


</dt> <dd></dd> <dt>

<span id="Resynchronization_suspended"></span><span id="resynchronization_suspended"></span><span id="RESYNCHRONIZATION_SUSPENDED"></span>

**Ressincronização suspensa** (11)


</dt> <dd></dd> <dt>

<span id="Failover_in_progress"></span><span id="failover_in_progress"></span><span id="FAILOVER_IN_PROGRESS"></span>

**Failover em andamento** (12)


</dt> <dd></dd> </dl>

</dd> <dt>

**ReplicationStateEx**
</dt> <dd> <dl> <dt>

Tipo de dados: a matriz **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado")
</dt> </dl>

A matriz de valores de estado de replicação para os vários relacionamentos de replicação da máquina virtual. Consulte a propriedade **replicationstate** da classe [**Msvm \_ ReplicationRelationship**](msvm-replicationrelationship.md) para obter os valores possíveis.

<dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Desabilitado** (0)


</dt> <dd></dd> <dt>

<span id="Ready_for_replication"></span><span id="ready_for_replication"></span><span id="READY_FOR_REPLICATION"></span>

<span id="Ready_for_replication"></span><span id="ready_for_replication"></span><span id="READY_FOR_REPLICATION"></span>**Pronto para replicação** (1)


</dt> <dd></dd> <dt>

<span id="Waiting_to_complete_initial_replication"></span><span id="waiting_to_complete_initial_replication"></span><span id="WAITING_TO_COMPLETE_INITIAL_REPLICATION"></span>

<span id="Waiting_to_complete_initial_replication"></span><span id="waiting_to_complete_initial_replication"></span><span id="WAITING_TO_COMPLETE_INITIAL_REPLICATION"></span>**Aguardando para concluir a replicação inicial** (2)


</dt> <dd></dd> <dt>

<span id="Replicating"></span><span id="replicating"></span><span id="REPLICATING"></span>

<span id="Replicating"></span><span id="replicating"></span><span id="REPLICATING"></span>**Replicando** (3)


</dt> <dd></dd> <dt>

<span id="Synced_replication_complete"></span><span id="synced_replication_complete"></span><span id="SYNCED_REPLICATION_COMPLETE"></span>

<span id="Synced_replication_complete"></span><span id="synced_replication_complete"></span><span id="SYNCED_REPLICATION_COMPLETE"></span>**Replicação sincronizada concluída** (4)


</dt> <dd></dd> <dt>

<span id="Recovered"></span><span id="recovered"></span><span id="RECOVERED"></span>

<span id="Recovered"></span><span id="recovered"></span><span id="RECOVERED"></span>**Recuperado** (5)


</dt> <dd></dd> <dt>

<span id="Committed"></span><span id="committed"></span><span id="COMMITTED"></span>

<span id="Committed"></span><span id="committed"></span><span id="COMMITTED"></span>**Confirmado** (6)


</dt> <dd></dd> <dt>

<span id="Suspended"></span><span id="suspended"></span><span id="SUSPENDED"></span>

<span id="Suspended"></span><span id="suspended"></span><span id="SUSPENDED"></span>**Suspenso** (7)


</dt> <dd></dd> <dt>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>

<span id="Critical"></span><span id="critical"></span><span id="CRITICAL"></span>**Crítico** (8)


</dt> <dd></dd> <dt>

<span id="Waiting_to_start_resynchronization"></span><span id="waiting_to_start_resynchronization"></span><span id="WAITING_TO_START_RESYNCHRONIZATION"></span>

<span id="Waiting_to_start_resynchronization"></span><span id="waiting_to_start_resynchronization"></span><span id="WAITING_TO_START_RESYNCHRONIZATION"></span>**Aguardando para iniciar a ressincronização** (9)


</dt> <dd></dd> <dt>

<span id="Resynchronizing"></span><span id="resynchronizing"></span><span id="RESYNCHRONIZING"></span>

<span id="Resynchronizing"></span><span id="resynchronizing"></span><span id="RESYNCHRONIZING"></span>**Ressincronização** (10)


</dt> <dd></dd> <dt>

<span id="Resynchronization_suspended"></span><span id="resynchronization_suspended"></span><span id="RESYNCHRONIZATION_SUSPENDED"></span>

<span id="Resynchronization_suspended"></span><span id="resynchronization_suspended"></span><span id="RESYNCHRONIZATION_SUSPENDED"></span>**Ressincronização suspensa** (11)


</dt> <dd></dd> <dt>

<span id="Failover_in_progress"></span><span id="failover_in_progress"></span><span id="FAILOVER_IN_PROGRESS"></span>

<span id="Failover_in_progress"></span><span id="failover_in_progress"></span><span id="FAILOVER_IN_PROGRESS"></span>**Failover em andamento** (12)


</dt> <dd></dd> <dt>

<span id="Failback_in_progress"></span><span id="failback_in_progress"></span><span id="FAILBACK_IN_PROGRESS"></span>

<span id="Failback_in_progress"></span><span id="failback_in_progress"></span><span id="FAILBACK_IN_PROGRESS"></span>**Failback em andamento** (13)


</dt> <dd></dd> <dt>

<span id="Failback_complete"></span><span id="failback_complete"></span><span id="FAILBACK_COMPLETE"></span>

<span id="Failback_complete"></span><span id="failback_complete"></span><span id="FAILBACK_COMPLETE"></span>**Failback concluído** (14)


</dt> <dd></dd> <dt>

<span id="Disk_update_in_progress"></span><span id="disk_update_in_progress"></span><span id="DISK_UPDATE_IN_PROGRESS"></span>

<span id="Disk_update_in_progress"></span><span id="disk_update_in_progress"></span><span id="DISK_UPDATE_IN_PROGRESS"></span>**Atualização de disco em andamento** (15)


</dt> <dd>

> [!Note]  
> Adicionado no Windows 10, versão 1703 e Windows Server 2016.

 

</dd> <dt>

<span id="Disk_update_critical"></span><span id="disk_update_critical"></span><span id="DISK_UPDATE_CRITICAL"></span>

<span id="Disk_update_critical"></span><span id="disk_update_critical"></span><span id="DISK_UPDATE_CRITICAL"></span>**Atualização de disco crítica** (16)


</dt> <dd>

> [!Note]  
> Adicionado no Windows 10, versão 1703 e Windows Server 2016.

 

</dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (17)


</dt> <dd>

> [!Note]  
> Adicionado no Windows 10, versão 1703 e Windows Server 2016.

 

</dd> <dt>

<span id="Repurpose_replication_in_progress"></span><span id="repurpose_replication_in_progress"></span><span id="REPURPOSE_REPLICATION_IN_PROGRESS"></span>

<span id="Repurpose_replication_in_progress"></span><span id="repurpose_replication_in_progress"></span><span id="REPURPOSE_REPLICATION_IN_PROGRESS"></span>**Replicação de redefinição em andamento** (18)


</dt> <dd>

> [!Note]  
> Adicionado no Windows 10, versão 1703 e Windows Server 2016.

 

</dd> <dt>

<span id="Prepared_for_sync_replication"></span><span id="prepared_for_sync_replication"></span><span id="PREPARED_FOR_SYNC_REPLICATION"></span>

<span id="Prepared_for_sync_replication"></span><span id="prepared_for_sync_replication"></span><span id="PREPARED_FOR_SYNC_REPLICATION"></span>**Preparado para replicação de sincronização** (19)


</dt> <dd>

> [!Note]  
> Adicionado no Windows 10, versão 1703 e Windows Server 2016.

 

</dd> <dt>

<span id="Prepared_for_group_reverse_replication"></span><span id="prepared_for_group_reverse_replication"></span><span id="PREPARED_FOR_GROUP_REVERSE_REPLICATION"></span>

<span id="Prepared_for_group_reverse_replication"></span><span id="prepared_for_group_reverse_replication"></span><span id="PREPARED_FOR_GROUP_REVERSE_REPLICATION"></span>**Preparado para replicação inversa de grupo** (20)


</dt> <dd>

> [!Note]  
> Adicionado no Windows 10, versão 1703 e Windows Server 2016.

 

</dd> <dt>

<span id="Firedrill_in_progress"></span><span id="firedrill_in_progress"></span><span id="FIREDRILL_IN_PROGRESS"></span>

<span id="Firedrill_in_progress"></span><span id="firedrill_in_progress"></span><span id="FIREDRILL_IN_PROGRESS"></span>**Firedrill em andamento** (21)


</dt> <dd>

> [!Note]  
> Adicionado no Windows 10, versão 1703 e Windows Server 2016.

 

</dd> </dl>

</dd> <dt>

**Blindado**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Indica se a blindagem está configurada para a máquina virtual.

> [!Note]  
> Adicionado no Windows 10, versão 1703 e Windows Server 2016.

 

</dd> <dt>

**Instantâneos**
</dt> <dd> <dl> <dt>

Tipo de dados: matriz de **\_ VirtualSystemSettingData CIM**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado")
</dt> </dl>

Uma matriz de instâncias [**Msvm \_ VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) que representam os instantâneos para a máquina virtual. Esta propriedade não é válida para instâncias de **Msvm \_ SummaryInformation** que representam um instantâneo de máquina virtual.

</dd> <dt>

**StatusDescriptions**
</dt> <dd> <dl> <dt>

Tipo de dados: matriz de **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado")
</dt> </dl>

Cadeias de caracteres que descrevem os valores correspondentes da matriz **OperationalStatus** . Isso corresponde à propriedade **StatusDescriptions** da classe [**Msvm \_ ComputerSystem**](msvm-computersystem.md) .

</dd> <dt>

**SwapFilesInUse**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Indica se a paginação de segundo nível está ativa. Contém **true** se a paginação de segundo nível estiver ativa ou **false** caso contrário.

</dd> <dt>

**TestReplicaSystem**
</dt> <dd> <dl> <dt>

Tipo de dados **: \_ sistema de ComputerSystem CIM**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Referência a uma instância de [**\_ sistema**](/windows/desktop/CIMWin32Prov/cim-computersystem) de computador CIM que representa a máquina virtual de réplica de teste para a máquina virtual. Esta propriedade não é válida para instâncias de **Msvm \_ SummaryInformation** que representam um instantâneo de máquina virtual.

</dd> <dt>

**ThumbnailImage**
</dt> <dd> <dl> <dt>

Tipo de dados: matriz **uint8**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **octetstring**, [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**Msvm \_ SummaryInformation**.**ThumbnailImageWidth**","**Msvm \_ SummaryInformation**.**ThumbnailImageHeight**")
</dt> </dl>

Uma matriz que contém uma imagem pequena e de tamanho de miniatura da área de trabalho para a máquina virtual ou o instantâneo no formato RGB565.

</dd> <dt>

**ThumbnailImageHeight**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**Msvm \_ SummaryInformation**.**ThumbnailImage**")
</dt> </dl>

A altura em pixels da imagem na propriedade ThumbnailImage.

> [!Note]  
> Adicionado no Windows 10.

 

</dd> <dt>

**ThumbnailImageWidth**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**Msvm \_ SummaryInformation**.**ThumbnailImage**")
</dt> </dl>

A largura em pixels da imagem na propriedade ThumbnailImage.

> [!Note]  
> Adicionado no Windows 10.

 

</dd> <dt>

**Atividade**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt64**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

A quantidade de tempo desde a última inicialização da máquina virtual. Esta propriedade não é válida para instâncias de **Msvm \_ SummaryInformation** que representam um instantâneo de máquina virtual.

</dd> <dt>

**Versão**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

A versão do sistema virtual em um formato de "Major. Minor", por exemplo, "2,0".

> [!Note]  
> Adicionado no Windows 10.

 

</dd> <dt>

**VirtualSwitchNames**
</dt> <dd> <dl> <dt>

Tipo de dados: matriz de **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado")
</dt> </dl>

Cadeias de caracteres que especificam os nomes amigáveis dos comutadores virtuais aos quais a máquina virtual está conectada.

**Windows 8.1:** Não há suporte para esse valor até Windows 8.1 e Windows Server 2012 R2.

</dd> <dt>

**VirtualSystemSubType**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

O subtipo do sistema virtual.

**Windows 8.1:** Não há suporte para esse valor até Windows 8.1 e Windows Server 2012 R2.

<dt>

<span id="Microsoft_Hyper-V_SubType_1"></span><span id="microsoft_hyper-v_subtype_1"></span><span id="MICROSOFT_HYPER-V_SUBTYPE_1"></span>

**Microsoft: Hyper-V: subtipo: 1** ()


</dt> <dd></dd> <dt>

<span id="Microsoft_Hyper-V_SubType_2"></span><span id="microsoft_hyper-v_subtype_2"></span><span id="MICROSOFT_HYPER-V_SUBTYPE_2"></span>

**Microsoft: Hyper-V: subtipo: 2** ()


</dt> <dd></dd> </dl>

</dd> </dl>

## <a name="remarks"></a>Comentários

O acesso à classe **Msvm \_ SummaryInformation** pode ser restringido pela filtragem do UAC. Para obter mais informações, consulte [controle de conta de usuário e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 8\]<br/>                                                              |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2012\]<br/>                                                    |
| Namespace<br/>                | \\Virtualização \\ v2 de raiz<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Msvm \_ SummaryInformationBase**](msvm-summaryinformationbase.md)
</dt> <dt>

[Classes de sistema virtual](virtual-system-classes.md)
</dt> </dl>

 

