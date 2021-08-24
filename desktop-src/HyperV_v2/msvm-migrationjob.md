---
description: Essa classe representa um trabalho de operação de migração criado para armazenamento ou migração de sistema virtual pelo serviço de migração de sistema virtual.
ms.assetid: ea9437c4-a34c-4bb1-b2b0-d701fb5796e9
title: Classe Msvm_MigrationJob
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_MigrationJob
- Msvm_MigrationJob.KillJob
- Msvm_MigrationJob.InstanceID
- Msvm_MigrationJob.Caption
- Msvm_MigrationJob.Description
- Msvm_MigrationJob.ElementName
- Msvm_MigrationJob.InstallDate
- Msvm_MigrationJob.Name
- Msvm_MigrationJob.OperationalStatus
- Msvm_MigrationJob.StatusDescriptions
- Msvm_MigrationJob.Status
- Msvm_MigrationJob.HealthState
- Msvm_MigrationJob.CommunicationStatus
- Msvm_MigrationJob.DetailedStatus
- Msvm_MigrationJob.OperatingStatus
- Msvm_MigrationJob.PrimaryStatus
- Msvm_MigrationJob.JobStatus
- Msvm_MigrationJob.TimeSubmitted
- Msvm_MigrationJob.ScheduledStartTime
- Msvm_MigrationJob.StartTime
- Msvm_MigrationJob.ElapsedTime
- Msvm_MigrationJob.JobRunTimes
- Msvm_MigrationJob.RunMonth
- Msvm_MigrationJob.RunDay
- Msvm_MigrationJob.RunDayOfWeek
- Msvm_MigrationJob.RunStartInterval
- Msvm_MigrationJob.LocalOrUtcTime
- Msvm_MigrationJob.UntilTime
- Msvm_MigrationJob.Notify
- Msvm_MigrationJob.Owner
- Msvm_MigrationJob.Priority
- Msvm_MigrationJob.PercentComplete
- Msvm_MigrationJob.DeleteOnCompletion
- Msvm_MigrationJob.ErrorCode
- Msvm_MigrationJob.ErrorDescription
- Msvm_MigrationJob.RecoveryAction
- Msvm_MigrationJob.OtherRecoveryAction
- Msvm_MigrationJob.JobState
- Msvm_MigrationJob.TimeOfLastStateChange
- Msvm_MigrationJob.TimeBeforeRemoval
- Msvm_MigrationJob.Cancellable
- Msvm_MigrationJob.ErrorSummaryDescription
- Msvm_MigrationJob.MigrationType
- Msvm_MigrationJob.VirtualSystemName
- Msvm_MigrationJob.DestinationHost
- Msvm_MigrationJob.NewSystemSettingData
- Msvm_MigrationJob.NewResourceSettingData
- Msvm_MigrationJob.JobType
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: ba979953a9e7a17df70247cdb176cba2f5782d4f9f6fc13d8f4addc161bbaf50
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119521196"
---
# <a name="msvm_migrationjob-class"></a>\_Classe Msvm MigrationJob

Essa classe representa um trabalho de operação de migração criado para armazenamento ou migração de sistema virtual pelo serviço de migração de sistema virtual.

A sintaxe a seguir é simplificada formato MOF código (MOF) e inclui todas as propriedades herdadas.

## <a name="syntax"></a>Sintaxe

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_MigrationJob : CIM_ConcreteJob
{
  string   InstanceID;
  string   Caption;
  string   Description;
  string   ElementName;
  datetime InstallDate;
  string   Name;
  uint16   OperationalStatus[] = { 2 };
  string   StatusDescriptions[] = { "OK" };
  string   Status;
  uint16   HealthState = 5;
  uint16   CommunicationStatus;
  uint16   DetailedStatus;
  uint16   OperatingStatus;
  uint16   PrimaryStatus;
  string   JobStatus;
  datetime TimeSubmitted;
  datetime ScheduledStartTime;
  datetime StartTime;
  datetime ElapsedTime;
  uint32   JobRunTimes;
  uint8    RunMonth;
  sint8    RunDay;
  sint8    RunDayOfWeek;
  datetime RunStartInterval;
  uint16   LocalOrUtcTime;
  datetime UntilTime;
  string   Notify;
  string   Owner;
  uint32   Priority;
  uint16   PercentComplete;
  boolean  DeleteOnCompletion;
  uint16   ErrorCode;
  string   ErrorDescription;
  uint16   RecoveryAction;
  string   OtherRecoveryAction;
  uint16   JobState;
  datetime TimeOfLastStateChange;
  datetime TimeBeforeRemoval = 00000000000500.000000:000;
  boolean  Cancellable;
  string   ErrorSummaryDescription;
  uint16   MigrationType;
  string   VirtualSystemName;
  string   DestinationHost;
  string   NewSystemSettingData;
  string   NewResourceSettingData[];
  uint16   JobType;
};
```

## <a name="members"></a>Membros

A classe **Msvm \_ MigrationJob** tem estes tipos de membros:

-   [Métodos](#methods)
-   [Propriedades](#properties)

### <a name="methods"></a>Métodos

A classe **Msvm \_ MigrationJob** tem esses métodos.



| Método                                                             | Descrição                                                                                |
|:-------------------------------------------------------------------|:-------------------------------------------------------------------------------------------|
| [**GetError**](geterror-msvm-migrationjob.md)                     | Recupera o objeto de erro para o trabalho de migração, se houver um.<br/>                |
| [**GetErrorEx**](geterrorex-msvm-migrationjob.md)                 | Recupera os objetos de erro para o trabalho de migração, se existir algum.<br/>                |
| **KillJob**                                                        | Não há suporte para o método.<br/>                                                   |
| [**RequestStateChange**](requeststatechange-msvm-migrationjob.md) | Solicita que o estado do trabalho de migração seja alterado para o estado especificado.<br/> |



 

### <a name="properties"></a>Propriedades

A classe **Msvm \_ MigrationJob** tem essas propriedades.

<dl> <dt>

**Cancelável**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Indica se o trabalho pode ser cancelado. O valor dessa propriedade não garante que uma solicitação para cancelar o trabalho seja realizada com sucesso.

</dd> <dt>

**Legenda**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Uma breve descrição do objeto. Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).

</dd> <dt>

**CommunicationStatus**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Indica a capacidade da instrumentação de se comunicar com o elemento gerenciado subjacente. Um valor **nulo** indica que essa propriedade não está implementada. Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).

</dd> <dt>

**DeleteOnCompletion**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Especifica se o trabalho deve ser excluído automaticamente após a conclusão. Essa propriedade é herdada [**do \_ trabalho CIM**](/windows/desktop/CIMWin32Prov/cim-job).

</dd> <dt>

**Descrição**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Uma descrição do objeto . Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).

</dd> <dt>

**DestinationHost**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

O nome do host da plataforma de virtualização de destino para a qual o sistema virtual está migrando. Isso será **nulo** para migração de armazenamento.

</dd> <dt>

**DetailedStatus**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Complementa a propriedade **PrimaryStatus** com detalhes de status adicionais. Um valor **nulo** indica que essa propriedade não está implementada. Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).

</dd> <dt>

**ElapsedTime**
</dt> <dd> <dl> <dt>

Tipo de dados: **DateTime**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

O intervalo de tempo em que o trabalho foi executado ou o tempo de execução total se o trabalho for concluído. Essa propriedade é herdada [**do \_ trabalho CIM**](/windows/desktop/CIMWin32Prov/cim-job).

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Um nome de exibição para o objeto. Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).

</dd> <dt>

**ErrorCode**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Um código de erro específico do fornecedor. O valor deve ser definido como zero se o trabalho for concluído sem erros. Essa propriedade é herdada [**do \_ trabalho CIM**](/windows/desktop/CIMWin32Prov/cim-job).

</dd> <dt>

**ErrorDescription**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Uma cadeia de caracteres que contém a descrição do erro do fornecedor. Essa propriedade é herdada [**do \_ trabalho CIM**](/windows/desktop/CIMWin32Prov/cim-job).

</dd> <dt>

**ErrorSummaryDescription**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**\_ trabalho CIM**](cim-job.md).**ErrorCode**")
</dt> </dl>

Uma descrição resumida do erro, se presente.

</dd> <dt>

**HealthState**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

A integridade atual do elemento. Esse atributo expressa a integridade desse elemento, mas não necessariamente o de seus subcomponentes. Os valores possíveis são 0 a 30, em que 5 significa que o elemento está totalmente íntegro e 30 significa que o elemento é completamente não funcional. Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)e é sempre definida como 5.

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

Tipo de dados: **DateTime**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

A data e a hora em que a configuração da máquina virtual foi criada. Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **chave**
</dt> </dl>

Identifica exclusivamente uma instância dessa classe. Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)e é sempre definida como **NULL**.

</dd> <dt>

**JobRunTimes**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

O número de vezes que o trabalho deve ser executado. Um valor de 1 indica que o trabalho não é recorrente, enquanto qualquer valor diferente de zero indica um limite para o número de vezes que o trabalho será recorrente. Zero indica que não há nenhum limite para o número de vezes que o trabalho pode ser processado, mas será encerrado após o tempo de espera ter sido atingido **ou o trabalho** será encerrado manualmente. Essa propriedade é herdada [**do \_ trabalho CIM**](/windows/desktop/CIMWin32Prov/cim-job).

</dd> <dt>

**JobState**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

**JobState** é uma enumeração de inteiro que indica o estado operacional de um trabalho. Ele também pode indicar transições entre esses Estados, por exemplo, "desligando" e "Iniciando". Essa propriedade é herdada do [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).



| Valor                                                                                                                                                                                                                                                                 | Significado                                                                                                                                                                                                                                            |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="New"></span><span id="new"></span><span id="NEW"></span><dl> <dt>**Novo**</dt> <dt>2</dt> </dl>                                                           | O trabalho nunca foi iniciado.<br/>                                                                                                                                                                                                         |
| <span id="Starting"></span><span id="starting"></span><span id="STARTING"></span><dl> <dt>**Iniciando**</dt> em <dt>3</dt> </dl>                                       | O trabalho está sendo movido dos Estados 2 (novo), 5 (suspensos) ou 11 (serviço) para o estado 4 (em execução).<br/>                                                                                                                                    |
| <span id="Running"></span><span id="running"></span><span id="RUNNING"></span><dl> <dt>**Executando**</dt> <dt>4</dt> </dl>                                           | O trabalho está em execução.<br/>                                                                                                                                                                                                                     |
| <span id="Suspended"></span><span id="suspended"></span><span id="SUSPENDED"></span><dl> <dt>**Suspenso**</dt> <dt>5</dt> </dl>                                   | O trabalho é interrompido, mas pode ser reiniciado de maneira direta.<br/>                                                                                                                                                                       |
| <span id="Shutting_Down"></span><span id="shutting_down"></span><span id="SHUTTING_DOWN"></span><dl> <dt>**Desligando**</dt> <dt>6</dt> </dl>                   | O trabalho está mudando para um estado de 7 (concluído), 8 (encerrado) ou 9 (eliminado).<br/>                                                                                                                                                              |
| <span id="Completed"></span><span id="completed"></span><span id="COMPLETED"></span><dl> <dt>**Concluído**</dt> em <dt>7</dt> </dl>                                   | O trabalho foi concluído normalmente.<br/>                                                                                                                                                                                                         |
| <span id="Terminated"></span><span id="terminated"></span><span id="TERMINATED"></span><dl> <dt>**Terminada**</dt> em <dt>8</dt> </dl>                               | O trabalho foi interrompido por uma solicitação de alteração de estado "Terminate". O trabalho e todos os seus processos subjacentes são encerrados e podem ser reiniciados apenas como um novo trabalho. O requisito de que o trabalho seja reiniciado somente como um novo trabalho é específico do trabalho.<br/> |
| <span id="Killed"></span><span id="killed"></span><span id="KILLED"></span><dl> <dt>**Encerrado**</dt> <dt>9</dt> </dl>                                               | O trabalho foi interrompido por uma solicitação de alteração de estado "Kill". Os processos subjacentes ainda podem estar em execução, e uma limpeza pode ser necessária para liberar recursos.<br/>                                                                            |
| <span id="Exception"></span><span id="exception"></span><span id="EXCEPTION"></span><dl> <dt>**Exceção**</dt> <dt>10</dt> </dl>                                  | O trabalho está em um estado anormal que pode indicar uma condição de erro. O status real do trabalho pode estar disponível por meio de objetos específicos do trabalho.<br/>                                                                           |
| <span id="Service"></span><span id="service"></span><span id="SERVICE"></span><dl> <dt>**Serviço**</dt> <dt>11</dt> </dl>                                          | O trabalho está em um estado específico do fornecedor que dá suporte à descoberta de problemas ou à resolução, ou ambos.<br/>                                                                                                                                          |
| <span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span><dl> <dt>**DMTF reservado**</dt> <dt>12 32767</dt> </dl>            | Reservado.<br/>                                                                                                                                                                                                                               |
| <span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span><dl> <dt>**Fornecedor reservado**</dt> <dt>32768 65535</dt> </dl> | Reservado.<br/>                                                                                                                                                                                                                               |



 

</dd> <dt>

**JobStatus**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Uma cadeia de caracteres que representa o status do trabalho. Essa propriedade é herdada [**do \_ trabalho CIM**](/windows/desktop/CIMWin32Prov/cim-job).

</dd> <dt>

**JobType**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Indica o tipo de trabalho que está sendo acompanhado por este objeto.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Desconhecido** (0)


</dt> <dd></dd> <dt>

<span id="Creating_Remote_Virtual_Machine"></span><span id="creating_remote_virtual_machine"></span><span id="CREATING_REMOTE_VIRTUAL_MACHINE"></span>

**Criando máquina virtual remota** (300)


</dt> <dd></dd> <dt>

<span id="Checking_Virtual_Machine_Compatibility"></span><span id="checking_virtual_machine_compatibility"></span><span id="CHECKING_VIRTUAL_MACHINE_COMPATIBILITY"></span>

**Verificando a compatibilidade da máquina virtual** (301)


</dt> <dd></dd> <dt>

<span id="Checking_Virtual_Machine_and_Storage_Compatibility"></span><span id="checking_virtual_machine_and_storage_compatibility"></span><span id="CHECKING_VIRTUAL_MACHINE_AND_STORAGE_COMPATIBILITY"></span>

**verificando a compatibilidade de máquina Virtual e Armazenamento** (302)


</dt> <dd></dd> <dt>

<span id="Checking_Storage_Compatibility"></span><span id="checking_storage_compatibility"></span><span id="CHECKING_STORAGE_COMPATIBILITY"></span>

**verificando a compatibilidade de Armazenamento** (303)


</dt> <dd></dd> <dt>

<span id="Checking_Storage_Migration"></span><span id="checking_storage_migration"></span><span id="CHECKING_STORAGE_MIGRATION"></span>

**verificando a migração de Armazenamento** (304)


</dt> <dd></dd> <dt>

<span id="Moving_Virtual_Machine"></span><span id="moving_virtual_machine"></span><span id="MOVING_VIRTUAL_MACHINE"></span>

**Movendo máquina virtual** (305)


</dt> <dd></dd> <dt>

<span id="Moving_Virtual_Machine_and_Storage"></span><span id="moving_virtual_machine_and_storage"></span><span id="MOVING_VIRTUAL_MACHINE_AND_STORAGE"></span>

**movendo máquina Virtual e Armazenamento** (306)


</dt> <dd></dd> <dt>

<span id="Moving_Storage"></span><span id="moving_storage"></span><span id="MOVING_STORAGE"></span>

**movendo Armazenamento** (307)


</dt> <dd></dd> </dl>

</dd> <dt>

**LocalOrUtcTime**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Essa propriedade é herdada [**do \_ trabalho CIM**](/windows/desktop/CIMWin32Prov/cim-job).

Indica se as horas representadas nas propriedades **RunStartInterval** e **UntilTime** representam horários locais ou horários UTC.

<dl> <dt>

<span id="Local_Time"></span><span id="local_time"></span><span id="LOCAL_TIME"></span>**Hora local** (1)
</dt> <dt>

<span id="UTC_Time_"></span><span id="utc_time_"></span><span id="UTC_TIME_"></span>**Hora UTC** (2)
</dt> </dl>

</dd> <dt>

**MigrationType**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**Msvm \_ VirtualSystemMigrationSettingData**](msvm-virtualsystemmigrationsettingdata.md).**MigrationType**")
</dt> </dl>

O tipo de migração representado por esse objeto de trabalho. Esse será um dos valores definidos para a propriedade **migratype** da classe [**Msvm \_ VirtualSystemMigrationSettingData**](msvm-virtualsystemmigrationsettingdata.md) .

</dd> <dt>

**Nome**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **chave**, **maxlen** (256)
</dt> </dl>

O nome de exibição para esta instância de um trabalho. Além disso, o nome de exibição pode ser usado como uma propriedade para uma pesquisa ou consulta. Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement).

</dd> <dt>

**NewResourceSettingData**
</dt> <dd> <dl> <dt>

Tipo de dados: matriz de **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Para uma migração dinâmica, isso sempre será definido como **nulo**.

Para uma migração de armazenamento, se isso for **NULL**, nenhum dos VHDs (discos rígidos virtuais) da máquina virtual será movido. Caso contrário, isso conterá uma matriz de instâncias inseridas da classe [**Msvm \_ StorageAllocationSettingData**](msvm-storageallocationsettingdata.md) que representam os VHDs a serem movidos. A propriedade **Connection** dessas instâncias especificará o local de destino do VHD.

</dd> <dt>

**NewSystemSettingData**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Para uma migração dinâmica, isso sempre será definido como **nulo**.

Para uma migração de armazenamento, se isso for **NULL**, as raízes de dados da máquina virtual não serão movidas. Caso contrário, isso conterá uma instância incorporada da classe [**Msvm \_ VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) , em que as propriedades **ExternalDataRoot**, **SnapshotDataRoot** e **SwapFileDataRoot** especificarão as novas raízes de dados.

</dd> <dt>

**Notificar**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

O usuário que é notificado após a conclusão ou falha do trabalho. Essa propriedade é herdada do [**Trabalho CIM. \_**](/windows/desktop/CIMWin32Prov/cim-job)

</dd> <dt>

**OperatingStatus**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Fornece informações de status atuais para a condição operacional do elemento e pode ser usado para fornecer mais detalhes em relação ao valor da **propriedade EnabledState.** Um **valor** Nulo indica que essa propriedade não está implementada. Essa propriedade é herdada de [**CIM \_ ManagedSystemElement.**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)

</dd> <dt>

**OperationalStatus**
</dt> <dd> <dl> <dt>

Tipo de dados: **matriz uint16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Os status atuais do objeto. Essa propriedade é herdada de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)e cada elemento de matriz é sempre definido como 2 (OK).

</dd> <dt>

**OtherRecoveryAction**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Uma cadeia de caracteres que descreve a ação de recuperação quando a **propriedade RecoveryAction** da instância é 1 (Outro). Essa propriedade é herdada do [**Trabalho CIM. \_**](/windows/desktop/CIMWin32Prov/cim-job)

</dd> <dt>

**Proprietário**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

O usuário que enviou o trabalho. Essa propriedade é herdada do [**Trabalho CIM. \_**](/windows/desktop/CIMWin32Prov/cim-job)

</dd> <dt>

**PercentComplete**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **MinValue** ( 0 ), **MaxValue** ( 100 ), **Units** ( "Percent" )
</dt> </dl>

O percentual de conclusão do trabalho. Essa propriedade é herdada do [**Trabalho CIM. \_**](/windows/desktop/CIMWin32Prov/cim-job)

</dd> <dt>

**PrimaryStatus**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Fornece informações de status de alto nível. Essa propriedade deve ser usada em conjunto com a propriedade **DetailedStatus** para fornecer status de saúde detalhado e de alto nível do elemento e seus subcomponentes. Um **valor** Nulo indica que essa propriedade não está implementada. Essa propriedade é herdada de [**CIM \_ ManagedSystemElement.**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)

</dd> <dt>

**Prioridade**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

A importância da execução de um trabalho. Essa propriedade é herdada do [**Trabalho CIM. \_**](/windows/desktop/CIMWin32Prov/cim-job)

</dd> <dt>

**RecoveryAction**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Descreve a ação de recuperação a ser tomada para um trabalho executado sem êxito. Essa propriedade é herdada do [**Trabalho CIM. \_**](/windows/desktop/CIMWin32Prov/cim-job)

<dl> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)
</dt> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outros** (1)
</dt> <dt>

<span id="Do_Not_Continue"></span><span id="do_not_continue"></span><span id="DO_NOT_CONTINUE"></span>**Não continuar** (2)
</dt> <dt>

<span id="Continue_With_Next_Job"></span><span id="continue_with_next_job"></span><span id="CONTINUE_WITH_NEXT_JOB"></span>**Continuar com o próximo trabalho** (3)
</dt> <dt>

<span id="Re-run_Job"></span><span id="re-run_job"></span><span id="RE-RUN_JOB"></span>**Executar trabalho de novo** (4)
</dt> <dt>

<span id="Run_Recovery_Job_"></span><span id="run_recovery_job_"></span><span id="RUN_RECOVERY_JOB_"></span>**Executar trabalho de recuperação** (5 )
</dt> </dl>

</dd> <dt>

**RunDay**
</dt> <dd> <dl> <dt>

Tipo de dados: **sint8**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **MinValue** ( -31 ), **MaxValue** ( 31 )
</dt> </dl>

O dia do mês em que o trabalho deve ser processado. Há interpretações diferentes para essa propriedade, dependendo do valor de **RunDayOfWeek**.

Quando **RunDayOfWeek** é 0 e RunDay é positivo, **o RunDay** define o dia do mês em que o trabalho é processado.  Por exemplo, se **RunDayOfWeek** for 0 e **RunDay** for 12, o trabalho será processado no dia 12 <sup></sup> do mês.

Quando **RunDayOfWeek** é 0 e RunDay é negativo, **o RunDay** define o número de dias antes do último dia do mês em que o trabalho é processado.   1 indica o último dia do mês, 2 indica um dia antes do último dia do mês e assim por diante. Por exemplo, se **RunDayOfWeek** for 0 e **RunDay** for 1, o trabalho será processado no último dia do mês.

Quando **RunDayOfWeek** não é 0, **RunDayOfWeek** é o dia da semana em que o trabalho será processado, em relação ao **RunDay.** Por exemplo, se **RunDay** for 15 e **RunDayOfWeek** for 7 (+Sábado), o trabalho será processado no primeiro sábado no dia ou após o 15º dia do mês.<sup></sup> Se **RunDay** for 20 e **RunDayOfWeek** for 7 ( sábado), o trabalho será processado no primeiro sábado no dia ou antes do dia 20 <sup></sup> do mês. Se **RunDay** for 1 e **RunDayOfWeek** for 1 ( domingo), o trabalho será processado no último domingo do mês.

Essa propriedade é herdada do [**Trabalho CIM. \_**](/windows/desktop/CIMWin32Prov/cim-job)

</dd> <dt>

**RunDayOfWeek**
</dt> <dd> <dl> <dt>

Tipo de dados: **sint8**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Um inteiro positivo ou negativo usado em conjunto com **o RunDay** para indicar o dia da semana ou mês em que o trabalho é processado. Consulte a descrição da **propriedade RunDay** para obter mais informações. Essa propriedade é herdada do [**Trabalho CIM. \_**](/windows/desktop/CIMWin32Prov/cim-job)

<dl> <dt>

<span id="-Saturday"></span><span id="-saturday"></span><span id="-SATURDAY"></span>**-Saturday** ( 7)
</dt> <dt>

<span id="-Friday"></span><span id="-friday"></span><span id="-FRIDAY"></span>**-Friday** ( 6)
</dt> <dt>

<span id="-Thursday"></span><span id="-thursday"></span><span id="-THURSDAY"></span>**-Thursday** ( 5)
</dt> <dt>

<span id="-Wednesday"></span><span id="-wednesday"></span><span id="-WEDNESDAY"></span>**-Wednesday** ( 4)
</dt> <dt>

<span id="-Tuesday"></span><span id="-tuesday"></span><span id="-TUESDAY"></span>**-Tuesday** ( 3)
</dt> <dt>

<span id="-Monday"></span><span id="-monday"></span><span id="-MONDAY"></span>**-Monday** ( 2)
</dt> <dt>

<span id="-Sunday"></span><span id="-sunday"></span><span id="-SUNDAY"></span>**-Sunday** ( 1)
</dt> <dt>

<span id="ExactDayOfMonth"></span><span id="exactdayofmonth"></span><span id="EXACTDAYOFMONTH"></span>**ExactDayOfMonth** (0)
</dt> <dt>

<span id="Sunday"></span><span id="sunday"></span><span id="SUNDAY"></span>**Domingo** (1)
</dt> <dt>

<span id="Monday"></span><span id="monday"></span><span id="MONDAY"></span>**Segunda-feira** (2)
</dt> <dt>

<span id="Tuesday"></span><span id="tuesday"></span><span id="TUESDAY"></span>**Terça-feira** (3)
</dt> <dt>

<span id="Wednesday"></span><span id="wednesday"></span><span id="WEDNESDAY"></span>**Quarta-feira** (4)
</dt> <dt>

<span id="Thursday"></span><span id="thursday"></span><span id="THURSDAY"></span>**Quinta-feira** (5)
</dt> <dt>

<span id="Friday"></span><span id="friday"></span><span id="FRIDAY"></span>**Sexta-feira** (6)
</dt> <dt>

<span id="Saturday_"></span><span id="saturday_"></span><span id="SATURDAY_"></span>**Sábado** (7 )
</dt> </dl>

</dd> <dt>

**RunMonth**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint8**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

O mês durante o qual o trabalho deve ser processado. Essa propriedade é herdada do [**Trabalho CIM. \_**](/windows/desktop/CIMWin32Prov/cim-job)

<dl> <dt>

<span id="January"></span><span id="january"></span><span id="JANUARY"></span>**Janeiro** (0)
</dt> <dt>

<span id="February"></span><span id="february"></span><span id="FEBRUARY"></span>**Fevereiro** (1)
</dt> <dt>

<span id="March"></span><span id="march"></span><span id="MARCH"></span>**Março** (2)
</dt> <dt>

<span id="April"></span><span id="april"></span><span id="APRIL"></span>**Abril** (3)
</dt> <dt>

<span id="May"></span><span id="may"></span><span id="MAY"></span>**Maio** (4)
</dt> <dt>

<span id="June"></span><span id="june"></span><span id="JUNE"></span>**Junho** (5)
</dt> <dt>

<span id="July"></span><span id="july"></span><span id="JULY"></span>**Julho** (6)
</dt> <dt>

<span id="August"></span><span id="august"></span><span id="AUGUST"></span>**Agosto** (7)
</dt> <dt>

<span id="September"></span><span id="september"></span><span id="SEPTEMBER"></span>**Setembro** (8)
</dt> <dt>

<span id="October"></span><span id="october"></span><span id="OCTOBER"></span>**Outubro** (9)
</dt> <dt>

<span id="November"></span><span id="november"></span><span id="NOVEMBER"></span>**Novembro** (10)
</dt> <dt>

<span id="December_"></span><span id="december_"></span><span id="DECEMBER_"></span>**Dezembro** (11 )
</dt> </dl>

</dd> <dt>

**RunStartInterval**
</dt> <dd> <dl> <dt>

Tipo de dados: **datetime**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

O intervalo de tempo após a meia-noite em que o trabalho deve ser processado. Essa propriedade é herdada do [**Trabalho CIM. \_**](/windows/desktop/CIMWin32Prov/cim-job)

</dd> <dt>

**ScheduledStartTime**
</dt> <dd> <dl> <dt>

Tipo de dados: **datetime**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

A hora de início agendada para o trabalho, se aplicável. Essa propriedade é herdada do [**Trabalho CIM. \_**](/windows/desktop/CIMWin32Prov/cim-job)

</dd> <dt>

**StartTime**
</dt> <dd> <dl> <dt>

Tipo de dados: **datetime**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

A hora em que o trabalho começou. Essa propriedade é herdada do [**Trabalho CIM. \_**](/windows/desktop/CIMWin32Prov/cim-job)

</dd> <dt>

**Status**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Essa propriedade é herdada [**de CIM \_ ManagedSystemElement,**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)mas não é usada.

</dd> <dt>

**StatusDescriptions**
</dt> <dd> <dl> <dt>

Tipo de dados: matriz **de cadeia de** caracteres
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Cadeias de caracteres que descrevem os **vários valores de matriz OperationalStatus.** Essa propriedade é herdada de [**CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)e cada elemento de matriz é sempre definido como "OK".

</dd> <dt>

**TimeBeforeRemoval**
</dt> <dd> <dl> <dt>

Tipo de dados: **datetime**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

A quantidade de tempo, em minutos, que o trabalho é retido após a execução concluída, seja com êxito ou falhando nessa execução. O trabalho deve permanecer em existência por algum período, independentemente do valor da **propriedade DeleteOnCompletion.** O padrão é de cinco minutos. Essa propriedade é herdada [**de CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85))e sempre é definida como 00000000000500.000000:000.

</dd> <dt>

**TimeOfLastStateChange**
</dt> <dd> <dl> <dt>

Tipo de dados: **datetime**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

A data ou a hora em que o estado do trabalho foi alterado pela última vez. Se o estado do trabalho não tiver sido alterado e essa propriedade for populada, ela deverá ser definida como um valor de intervalo 0. Se uma alteração de estado tiver sido solicitada, mas rejeitada ou ainda não processada, a propriedade não deverá ser atualizada. Essa propriedade é herdada de [**CIM \_ ConcreteJob.**](/previous-versions//cc136808(v=vs.85))

</dd> <dt>

**TimeSubmitted**
</dt> <dd> <dl> <dt>

Tipo de dados: **datetime**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

A hora em que o trabalho foi enviado. Essa propriedade é herdada do [**Trabalho CIM. \_**](/windows/desktop/CIMWin32Prov/cim-job)

</dd> <dt>

**UntilTime**
</dt> <dd> <dl> <dt>

Tipo de dados: **datetime**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

A hora em que o trabalho não é válido ou deve ser interrompido. Essa propriedade é herdada do [**Trabalho CIM. \_**](/windows/desktop/CIMWin32Prov/cim-job)

</dd> <dt>

**VirtualSystemName**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

O nome exclusivo do sistema virtual afetado.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Windows 8 somente aplicativos da área de trabalho\]<br/>                                                              |
| Servidor mínimo com suporte<br/> | \[Windows Server 2012 somente aplicativos da área de trabalho\]<br/>                                                    |
| Namespace<br/>                | Virtualização \\ raiz \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

