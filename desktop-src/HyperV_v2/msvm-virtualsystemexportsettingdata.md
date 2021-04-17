---
description: Fornece informações adicionais a serem usadas com o método ExportSystemDefinition da classe Msvm \_ VirtualSystemManagementService.
ms.assetid: 86396A76-83EC-476E-86A9-83861A002152
title: Classe Msvm_VirtualSystemExportSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemExportSettingData
- Msvm_VirtualSystemExportSettingData.CaptureLiveState
- Msvm_VirtualSystemExportSettingData.InstanceID
- Msvm_VirtualSystemExportSettingData.Caption
- Msvm_VirtualSystemExportSettingData.Description
- Msvm_VirtualSystemExportSettingData.ElementName
- Msvm_VirtualSystemExportSettingData.CopySnapshotConfiguration
- Msvm_VirtualSystemExportSettingData.CopyVmRuntimeInformation
- Msvm_VirtualSystemExportSettingData.CopyVmStorage
- Msvm_VirtualSystemExportSettingData.CreateVmExportSubdirectory
- Msvm_VirtualSystemExportSettingData.SnapshotVirtualSystem
- Msvm_VirtualSystemExportSettingData.BackupIntent
- Msvm_VirtualSystemExportSettingData.ExportForLiveMigration
- Msvm_VirtualSystemExportSettingData.DisableDifferentialOfIgnoredStorage
- Msvm_VirtualSystemExportSettingData.ExcludedVirtualHardDisks
- Msvm_VirtualSystemExportSettingData.DifferentialBackupBase
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 77bd451912063ec1164abf14247d81e1d258f56f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105775723"
---
# <a name="msvm_virtualsystemexportsettingdata-class"></a>\_Classe Msvm VirtualSystemExportSettingData

Fornece informações adicionais a serem usadas com o método [**ExportSystemDefinition**](exportsystemdefinition-msvm-virtualsystemmanagementservice.md) da classe [**Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) .

A sintaxe a seguir é simplificada formato MOF código (MOF) e inclui todas as propriedades herdadas.

## <a name="syntax"></a>Sintaxe

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualSystemExportSettingData : CIM_SettingData
{
  uint8   CaptureLiveState;
  string  InstanceID;
  string  Caption;
  string  Description;
  string  ElementName;
  uint8   CopySnapshotConfiguration;
  boolean CopyVmRuntimeInformation;
  boolean CopyVmStorage;
  boolean CreateVmExportSubdirectory;
  string  SnapshotVirtualSystem;
  uint8   BackupIntent;
  boolean ExportForLiveMigration;
  boolean DisableDifferentialOfIgnoredStorage;
  string  ExcludedVirtualHardDisks[];
  string  DifferentialBackupBase;
};
```

## <a name="members"></a>Membros

A classe **Msvm \_ VirtualSystemExportSettingData** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **Msvm \_ VirtualSystemExportSettingData** tem essas propriedades.

<dl> <dt>

**BackupIntent**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint8**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

Indica a intenção de como os conjuntos de backup exportados seriam usados.

> [!Note]  
> Essa propriedade foi adicionada no Windows 10 e no Windows Server 2016.

 

<dt>

<span id="BackupIntentPreserveChain"></span><span id="backupintentpreservechain"></span><span id="BACKUPINTENTPRESERVECHAIN"></span>

<span id="BackupIntentPreserveChain"></span><span id="backupintentpreservechain"></span><span id="BACKUPINTENTPRESERVECHAIN"></span>**BackupIntentPreserveChain** (0)


</dt> <dd>

Todos os conjuntos de backup exportados completos e diferenciais seriam preservados como estão.

</dd> <dt>

<span id="BackupIntentMerge"></span><span id="backupintentmerge"></span><span id="BACKUPINTENTMERGE"></span>

<span id="BackupIntentMerge"></span><span id="backupintentmerge"></span><span id="BACKUPINTENTMERGE"></span>**BackupIntentMerge** (1)


</dt> <dd>

Os conjuntos de backup exportados completos e diferenciais seriam mesclados para sintetizar conjuntos de backup completos.

</dd> </dl>

</dd> <dt>

**Legenda**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **maxlen** (64)
</dt> </dl>

Uma breve descrição do objeto. Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).

</dd> <dt>

**CaptureLiveState**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint8**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

Indica qual estado capturar se o destino da exportação for uma VM em execução.

<dt>

<span id="CaptureCrashConsistentState"></span><span id="capturecrashconsistentstate"></span><span id="CAPTURECRASHCONSISTENTSTATE"></span>

<span id="CaptureCrashConsistentState"></span><span id="capturecrashconsistentstate"></span><span id="CAPTURECRASHCONSISTENTSTATE"></span>**CaptureCrashConsistentState** (0)


</dt> <dd>

Nenhum arquivo de estado salvo será exportado para a VM em execução, colocando-o em um estado consistente de falha.

</dd> <dt>

<span id="CaptureSavedState"></span><span id="capturesavedstate"></span><span id="CAPTURESAVEDSTATE"></span>

<span id="CaptureSavedState"></span><span id="capturesavedstate"></span><span id="CAPTURESAVEDSTATE"></span>**CaptureSavedState** (1)


</dt> <dd>

Os arquivos de estado salvos para a VM em execução serão exportados junto com a configuração da VM.

</dd> <dt>

<span id="CaptureAppConsistentState"></span><span id="captureappconsistentstate"></span><span id="CAPTUREAPPCONSISTENTSTATE"></span>

<span id="CaptureAppConsistentState"></span><span id="captureappconsistentstate"></span><span id="CAPTUREAPPCONSISTENTSTATE"></span>**CaptureAppConsistentState** (2)


</dt> <dd>

O estado consistente com o aplicativo da VM em execução será exportado.

> [!Note]  
> Adicionado ao Windows 10 e ao Windows Server 2016.

 

</dd> </dl>

</dd> <dt>

**CopySnapshotConfiguration**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint8**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

Indica quais instantâneos devem ser exportados com a máquina virtual.

<dt>

<span id="ExportAllSnapshots"></span><span id="exportallsnapshots"></span><span id="EXPORTALLSNAPSHOTS"></span>

<span id="ExportAllSnapshots"></span><span id="exportallsnapshots"></span><span id="EXPORTALLSNAPSHOTS"></span>**ExportAllSnapshots** (0)


</dt> <dd>

Todos os instantâneos serão exportados com a máquina virtual.

</dd> <dt>

<span id="ExportNoSnapshots"></span><span id="exportnosnapshots"></span><span id="EXPORTNOSNAPSHOTS"></span>

<span id="ExportNoSnapshots"></span><span id="exportnosnapshots"></span><span id="EXPORTNOSNAPSHOTS"></span>**ExportNoSnapshots** (1)


</dt> <dd>

Nenhum instantâneo será exportado com a máquina virtual.

</dd> <dt>

<span id="ExportOneSnapshot"></span><span id="exportonesnapshot"></span><span id="EXPORTONESNAPSHOT"></span>

<span id="ExportOneSnapshot"></span><span id="exportonesnapshot"></span><span id="EXPORTONESNAPSHOT"></span>**ExportOneSnapshot** (2)


</dt> <dd>

Os instantâneos identificados pela propriedade **SnapshotVirtualSystem** serão exportados com a máquina virtual. As propriedades **CopyVmStorage** e **CopyVmRuntimeInformation** são ignoradas, as informações de armazenamento e tempo de execução são exportadas com a máquina virtual e todos os discos diferenciais VHD serão mesclados em um novo VHD.

</dd> <dt>

<span id="ExportOneSnapshotForBackup"></span><span id="exportonesnapshotforbackup"></span><span id="EXPORTONESNAPSHOTFORBACKUP"></span>

<span id="ExportOneSnapshotForBackup"></span><span id="exportonesnapshotforbackup"></span><span id="EXPORTONESNAPSHOTFORBACKUP"></span>**ExportOneSnapshotForBackup** (3)


</dt> <dd>

O instantâneo identificado pela propriedade **SnapshotVirtualSystem** será exportado para fins de backup da VM. A configuração exportada usará a ID da VM.

> [!Note]  
> Adicionado ao Windows 10 e ao Windows Server 2016.

 

</dd> </dl>

</dd> <dt>

**CopyVmRuntimeInformation**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

Indica se as informações de tempo de execução da máquina virtual serão copiadas quando a máquina virtual for exportada.



| Valor                                                                                | Significado                                                                 |
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| <dl> <dt>**True**</dt> </dl>  | As informações de tempo de execução da máquina virtual serão copiadas.<br/>     |
| <dl> <dt>**For**</dt> </dl> | As informações de tempo de execução da máquina virtual não serão copiadas.<br/> |



 

</dd> <dt>

**CopyVmStorage**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

Indica se o armazenamento da máquina virtual será copiado quando a máquina virtual for exportada.



| Valor                                                                                | Significado                                                    |
|--------------------------------------------------------------------------------------|------------------------------------------------------------|
| <dl> <dt>**True**</dt> </dl>  | O armazenamento da máquina virtual será copiado.<br/>     |
| <dl> <dt>**For**</dt> </dl> | O armazenamento da máquina virtual não será copiado.<br/> |



 

</dd> <dt>

**CreateVmExportSubdirectory**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

Indica se um subdiretório com o nome da máquina virtual será criado quando a máquina virtual for exportada.



| Valor                                                                                | Significado                                        |
|--------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <dt>**True**</dt> </dl>  | Um subdiretório será criado.<br/>     |
| <dl> <dt>**For**</dt> </dl> | Um subdiretório não será criado.<br/> |



 

</dd> <dt>

**Descrição**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Uma descrição do objeto . Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).

</dd> <dt>

**DifferentialBackupBase**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

Base para exportação diferencial. Esse é o caminho para uma instância [**Msvm \_ VirtualSystemReferencePoint**](msvm-virtualsystemreferencepoint.md) que representa o ponto de referência ou o caminho para uma instância [**\_ VirtualSystemSettingData Msvm**](msvm-virtualsystemsettingdata.md) que representa o instantâneo a ser usado como base para a exportação diferencial. Se a propriedade **CopySnapshotConfiguration** não estiver definida como 3 (**ExportOneSnapshotForBackup**), essa propriedade será ignorada.

> [!Note]  
> Adicionado ao Windows 10 e ao Windows Server 2016.

 

</dd> <dt>

**DisableDifferentialOfIgnoredStorage**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

Indica se os discos diferenciais serão criados ou não para armazenamento ignorado durante a exportação. Por padrão, isso é definido como false, o que significa que os discos diferenciais são criados para o armazenamento que não será copiado para o destino de exportação.

> [!Note]  
> Adicionado no Windows 10, versão 1709.

 

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

O nome de exibição desta instância. Além disso, o nome de exibição pode ser usado como uma propriedade de índice para uma pesquisa ou consulta. Essa propriedade é herdada do [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85)).

</dd> <dt>

**ExcludedVirtualHardDisks**
</dt> <dd> <dl> <dt>

Tipo de dados: matriz de **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

Matriz de IDs de instância de RASD ( [**Msvm \_ StorageAllocationSettingData**](msvm-storageallocationsettingdata.md) ) que representam os discos rígidos virtuais que são solicitados a serem excluídos da operação de exportação. Se pelo menos uma das IDs fornecidas não for um disco rígido virtual anexado válido, a operação falhará.

Os discos rígidos virtuais referenciados por essa propriedade podem ser da VM e/ou de qualquer um de seus instantâneos. Não há suporte para a exclusão de discos rígidos virtuais quando a propriedade **CopySnapshotConfiguration** está definida como 0 (ExportAllSnapshots).

Observe que a ID da instância do RASD para discos rígidos virtuais representa o local ao qual eles estão anexados e a exclusão por meio dessa ID exclui todos os discos rígidos virtuais anexados nesse local na árvore de instantâneo da máquina virtual, independentemente de serem realmente uma cadeia de disco rígido virtual válida.

> [!Note]  
> Adicionado no Windows 10, versão 1709.

 

</dd> <dt>

**ExportForLiveMigration**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

Indica se a VM exportada deve ser usada na migração dinâmica.

> [!Note]  
> Adicionado no Windows 10, versão 1703 e Windows Server 2016.

 

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **chave**
</dt> </dl>

Dentro do escopo do namespace de instanciação, ele identifica de forma opaca e exclusiva uma instância dessa classe. Essa propriedade é herdada do [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85)).

</dd> <dt>

**SnapshotVirtualSystem**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

Caminho para uma instância de [**\_ VirtualSystemSettingData Msvm**](msvm-virtualsystemsettingdata.md) que representa o instantâneo a ser exportado com a máquina virtual. Se a propriedade **CopySnapshotConfiguration** não estiver definida como 2 (ExportOneSnapshot), essa propriedade será ignorada.

</dd> </dl>

## <a name="remarks"></a>Comentários

O acesso à classe **Msvm \_ VirtualSystemExportSettingData** pode ser restringido pela filtragem do UAC. Para obter mais informações, consulte [controle de conta de usuário e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

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

[**CIM \_ SettingData**](cim-settingdata.md)
</dt> <dt>

[Classes de gerenciamento do sistema virtual](virtual-system-management-classes.md)
</dt> <dt>

[**ExportSystemDefinition**](exportsystemdefinition-msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

