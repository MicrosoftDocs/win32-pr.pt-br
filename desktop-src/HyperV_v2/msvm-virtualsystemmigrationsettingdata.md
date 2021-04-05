---
description: Representa as configurações de migração para migrar um sistema virtual e o armazenamento anexado a um sistema virtual.
ms.assetid: 2d632fe2-31ee-4e4d-b2a6-c1d1f3b4d624
title: Classe Msvm_VirtualSystemMigrationSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemMigrationSettingData
- Msvm_VirtualSystemMigrationSettingData.InstanceID
- Msvm_VirtualSystemMigrationSettingData.Caption
- Msvm_VirtualSystemMigrationSettingData.Description
- Msvm_VirtualSystemMigrationSettingData.ElementName
- Msvm_VirtualSystemMigrationSettingData.MigrationType
- Msvm_VirtualSystemMigrationSettingData.Priority
- Msvm_VirtualSystemMigrationSettingData.Bandwidth
- Msvm_VirtualSystemMigrationSettingData.BandwidthUnit
- Msvm_VirtualSystemMigrationSettingData.OtherTransportType
- Msvm_VirtualSystemMigrationSettingData.TransportType
- Msvm_VirtualSystemMigrationSettingData.RemoveSourceUnmanagedVhds
- Msvm_VirtualSystemMigrationSettingData.AvoidRemovingVHDs
- Msvm_VirtualSystemMigrationSettingData.CPUCappingMagnitude
- Msvm_VirtualSystemMigrationSettingData.CancelIfBlackoutThresholdExceeded
- Msvm_VirtualSystemMigrationSettingData.AllowOverwriteExistingFile
- Msvm_VirtualSystemMigrationSettingData.UnmanagedVhds
- Msvm_VirtualSystemMigrationSettingData.DestinationPlannedVirtualSystemId
- Msvm_VirtualSystemMigrationSettingData.DestinationIPAddressList
- Msvm_VirtualSystemMigrationSettingData.RetainVhdCopiesOnSource
- Msvm_VirtualSystemMigrationSettingData.EnableCompression
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 254884153b3f733691b1103a6eb57f204b5d1764
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826857"
---
# <a name="msvm_virtualsystemmigrationsettingdata-class"></a>\_Classe Msvm VirtualSystemMigrationSettingData

Representa as configurações de migração para migrar um sistema virtual e o armazenamento anexado a um sistema virtual.

A sintaxe a seguir é simplificada formato MOF código (MOF) e inclui todas as propriedades herdadas.

## <a name="syntax"></a>Sintaxe

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualSystemMigrationSettingData : CIM_VirtualSystemMigrationSettingData
{
  string  InstanceID;
  string  Caption = "Migration Setting Data";
  string  Description = "Virtual System Migration Setting Data";
  string  ElementName;
  uint16  MigrationType;
  uint16  Priority;
  uint16  Bandwidth;
  string  BandwidthUnit;
  string  OtherTransportType;
  uint16  TransportType;
  boolean RemoveSourceUnmanagedVhds;
  boolean AvoidRemovingVHDs;
  uint16  CPUCappingMagnitude;
  boolean CancelIfBlackoutThresholdExceeded;
  boolean AllowOverwriteExistingFile;
  string  UnmanagedVhds[];
  string  DestinationPlannedVirtualSystemId;
  string  DestinationIPAddressList[];
  boolean RetainVhdCopiesOnSource;
  boolean EnableCompression;
};
```

## <a name="members"></a>Membros

A classe **Msvm \_ VirtualSystemMigrationSettingData** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **Msvm \_ VirtualSystemMigrationSettingData** tem essas propriedades.

<dl> <dt>

**AllowOverwriteExistingFile**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

Permitir que a operação de migração de armazenamento substitua arquivos. vhdx existentes.

> [!Note]  
> Essa propriedade foi adicionada no Windows 10, versão 1703.

 

</dd> <dt>

**AvoidRemovingVHDs**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

Não remova nenhum VHDs durante a migração, ou seja, VHDs na origem em VHDs successand no destino em caso de falha.

> [!Note]  
> Adicionado no Windows 10, versão 1703 e Windows Server 2016.

 

</dd> <dt>

**Largura de banda**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Especifica a largura de banda atribuída ou solicitada para uma operação de migração de sistema virtual. As unidades de largura de banda são especificadas pela propriedade **BandwidthUnit** . Em uma migração, um valor de 0 indica a largura de banda padrão. Caso contrário, um valor de 0 indica que não há suporte para larguras de banda.

A **largura de banda** e a **prioridade** podem ser usadas em conjunto. Os processos de migração que têm o maior valor de prioridade igual compartilham a largura de banda disponível com base na largura de banda solicitada. Se nem toda a largura de banda for consumida por esse conjunto de processos, os processos de migração com a próxima prioridade inferior menor compartilharão a largura de banda restante. Se ainda houver mais largura de banda restante, os processos de migração com a próxima prioridade menor inferior serão considerados e assim por diante.

Essa propriedade é herdada do **CIM \_ VirtualSystemMigrationSettingData**.

</dd> <dt>

**BandwidthUnit**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Especifica as unidades usadas pela propriedade **Bandwidth** . O valor dessa propriedade deve ser um valor válido do qualificador de unidades programáticas, conforme definido no Apêndice C. 1 de DSP0004 V 2.4 ou posterior.

Se o valor dessa propriedade for "percent", o valor da propriedade **Bandwidth** deverá estar entre 0 e 100, com valores mais altos indicando uma maior largura de banda. Um valor de 100 indica a largura de banda total disponível para executar operações de migração de sistema virtual. Os valores entre 1 e 100 devem correlacionar linearmente com o intervalo de largura de banda disponível. Por exemplo, um valor de 50 deve solicitar metade da largura de banda disponível.

Essa propriedade é herdada do **CIM \_ VirtualSystemMigrationSettingData**.

</dd> <dt>

**CancelIfBlackoutThresholdExceeded**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

Cancelará a migração se o tempo limite de blecaute for excedido.

> [!Note]  
> Adicionado no Windows 10, versão 1709.

 

</dd> <dt>

**Legenda**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Uma breve descrição do objeto. Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).

</dd> <dt>

**CPUCappingMagnitude**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> <dt>

Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CPUCappingMagnitude")
</dt> </dl>

Grau de limitação de CPU durante a migração.

> [!Note]  
> Adicionado no Windows 10, versão 1709.

 

<dt>

<span id="Normal"></span><span id="normal"></span><span id="NORMAL"></span>

**Normal** (0)


</dt> <dd></dd> <dt>

<span id="Low"></span><span id="low"></span><span id="LOW"></span>

**Baixo** (1)


</dt> <dd></dd> <dt>

<span id="High"></span><span id="high"></span><span id="HIGH"></span>

**Alta** (2)


</dt> <dd></dd> </dl>

</dd> <dt>

**Descrição**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Uma descrição do objeto . Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).

</dd> <dt>

**DestinationIPAddressList**
</dt> <dd> <dl> <dt>

Tipo de dados: matriz de **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

Isso será **nulo** para migração de armazenamento. Para a migração do sistema virtual, isso pode conter uma lista de endereços IP do host de destino.

</dd> <dt>

**DestinationPlannedVirtualSystemId**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

Se uma máquina virtual planejada existir no destino de migração, essa propriedade será definida como o GUID da máquina virtual planejada de destino onde a máquina virtual precisa ser migrada. Isso é útil para casos em que um usuário criou uma máquina virtual planejada no destino, juntamente com a configuração do recurso, e quer que uma máquina virtual da origem seja migrada para essa máquina virtual planejada.

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Um nome de exibição para o objeto. Essa propriedade é herdada do [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85)).

</dd> <dt>

**EnableCompression**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

Indica se o tráfego de migração ao vivo deve ser compactado. **Verdadeiro** indica compactar; caso contrário, **false**.

**Windows 8.1:** Não há suporte para esse valor até Windows 8.1 e Windows Server 2012 R2.

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **chave**
</dt> </dl>

Identifica exclusivamente uma instância dessa classe. Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).

</dd> <dt>

**MigrationType**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> <dt>

Qualificadores: [**substituir**](/windows/desktop/WmiSdk/standard-qualifiers) ("MigrationType")
</dt> </dl>

Especifica o tipo de operação de migração a ser executada. Essa propriedade é herdada do **CIM \_ VirtualSystemMigrationSettingData**.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)


</dt> <dd></dd> <dt>

<span id="VirtualSystem"></span><span id="virtualsystem"></span><span id="VIRTUALSYSTEM"></span>

<span id="VirtualSystem"></span><span id="virtualsystem"></span><span id="VIRTUALSYSTEM"></span>**VirtualSystem** (32768)


</dt> <dd>

Migra o sistema virtual para o host de destino.

</dd> <dt>

<span id="Storage"></span><span id="storage"></span><span id="STORAGE"></span>

<span id="Storage"></span><span id="storage"></span><span id="STORAGE"></span>**Armazenamento** (32769)


</dt> <dd>

Migra somente os recursos de armazenamento do sistema virtual.

</dd> <dt>

<span id="Staged"></span><span id="staged"></span><span id="STAGED"></span>

<span id="Staged"></span><span id="staged"></span><span id="STAGED"></span>**Preparado** (32770)


</dt> <dd>

Usando a configuração do sistema virtual, o cria um sistema virtual planejado no host de destino.

</dd> <dt>

<span id="VirtualSystemAndStorage"></span><span id="virtualsystemandstorage"></span><span id="VIRTUALSYSTEMANDSTORAGE"></span>

<span id="VirtualSystemAndStorage"></span><span id="virtualsystemandstorage"></span><span id="VIRTUALSYSTEMANDSTORAGE"></span>**VirtualSystemAndStorage** (32771)


</dt> <dd>

Migra o sistema virtual e seu armazenamento para o host de destino.

</dd> <dt>

<span id="StorageDeepCheck"></span><span id="storagedeepcheck"></span><span id="STORAGEDEEPCHECK"></span>

<span id="StorageDeepCheck"></span><span id="storagedeepcheck"></span><span id="STORAGEDEEPCHECK"></span>**StorageDeepCheck** (32772)


</dt> <dd>

Executa uma verificação de capacidade de migração de recursos de armazenamento de sistema virtual no host de destino.

</dd> </dl>

</dd> <dt>

**OtherTransportType**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Especifica o tipo de transporte a ser aplicado se o valor de **TransportType** for 1 (outro). Essa propriedade é herdada do **CIM \_ VirtualSystemMigrationSettingData**.

</dd> <dt>

**Prioridade**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Especifica uma importância de migração relativa, que o sistema de migração pode usar para ordenar ou, de outra forma, dar preferência entre várias solicitações de migração pendentes. Quanto menor o valor, maior a prioridade. Em uma migração, um valor de 0 indica a prioridade padrão. Caso contrário, um valor de 0 indica que não há suporte para as prioridades.

Essa propriedade é herdada do **CIM \_ VirtualSystemMigrationSettingData**.

</dd> <dt>

**RemoveSourceUnmanagedVhds**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

Remover VHDs não gerenciados de origem.

> [!Note]  
> Adicionado ao Windows 10 e ao Windows Server 2016.

 

</dd> <dt>

**RetainVhdCopiesOnSource**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

Para uma migração de armazenamento, isso especifica se os VHDs somente leitura no host de origem devem ser removidos após a conclusão da migração.

</dd> <dt>

**TransportType**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> <dt>

Qualificadores: [**substituir**](/windows/desktop/WmiSdk/standard-qualifiers) ("TransportType")
</dt> </dl>

Especifica o tipo de transporte a ser aplicado a uma operação de migração de sistema virtual. Essa propriedade é herdada do **CIM \_ VirtualSystemMigrationSettingData**.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Desconhecido** (0)


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Outro** (1)


</dt> <dd></dd> <dt>

<span id="SSH"></span><span id="ssh"></span>

**SSH** (2)


</dt> <dd></dd> <dt>

<span id="TLS"></span><span id="tls"></span>

**TLS** (3)


</dt> <dd></dd> <dt>

<span id="TLS_Strict"></span><span id="tls_strict"></span><span id="TLS_STRICT"></span>

**TLS estrito** (4)


</dt> <dd></dd> <dt>

<span id="TCP"></span><span id="tcp"></span>

**TCP** (5)


</dt> <dd></dd> <dt>

<span id="IPC"></span><span id="ipc"></span>

**IPC** (6)


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

**DMTF reservado** (..)


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

**Fornecedor reservado** (32768..)


</dt> <dd></dd> </dl>

Para a migração dinâmica, essa propriedade especifica o tipo de transporte a ser usado para transferir o estado do sistema virtual para o host de destino. Os valores com suporte são:

<dt>

<span id="TCP"></span><span id="tcp"></span>

<span id="TCP"></span><span id="tcp"></span>**TCP** (5)


</dt> <dd>

Indica o tipo de transporte TCP.

</dd> <dt>

<span id="SMB"></span><span id="smb"></span>

<span id="SMB"></span><span id="smb"></span>**SMB** (32768)


</dt> <dd>

Indica que o tipo de transporte para transferência do estado da máquina virtual é SMB.

</dd> </dl>

</dd> <dt>

**UnmanagedVhds**
</dt> <dd> <dl> <dt>

Tipo de dados: matriz de **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> <dt>

Qualificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado"), **HyperVEmbeddedInstance** ("Msvm \_ MoveUnmanagedVhd")
</dt> </dl>

Uma matriz de instâncias [**Msvm \_ MoveUnmanagedVhd**](msvm-moveunmanagedvhd.md) inseridas que contêm informações de VHDs não gerenciados.

> [!Note]  
> Adicionado ao Windows 10 e ao Windows Server 2016.

 

</dd> </dl>

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

[**\_VIRTUALSYSTEMMIGRATIONSETTINGDATA CIM**](cim-virtualsystemmigrationsettingdata.md)
</dt> <dt>

[**MigrateVirtualSystemToHost**](migratevirtualsystemtohost-msvm-virtualsystemmigrationservice.md)
</dt> </dl>

 

