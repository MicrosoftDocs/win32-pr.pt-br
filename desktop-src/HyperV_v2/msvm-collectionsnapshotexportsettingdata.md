---
description: Exportar dados de configuração a serem passados para o método ExportSnapshot da classe Msvm \_ CollectionSnapshotService.
ms.assetid: 03b448ed-72bc-485e-bb31-4445c53baa1c
title: Msvm_CollectionSnapshotExportSettingData classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionSnapshotExportSettingData
- Msvm_CollectionSnapshotExportSettingData.CopyVmStorage
- Msvm_CollectionSnapshotExportSettingData.DifferentialBackupBase
- Msvm_CollectionSnapshotExportSettingData.BackupIntent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: bd148b7ea73bf7c2eaff7f648c7084c37a8669779515749611c675e7f5564d1c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120130626"
---
# <a name="msvm_collectionsnapshotexportsettingdata-class"></a>Classe Msvm \_ CollectionSnapshotExportSettingData

Exportar dados de configuração a serem passados para o método ExportSnapshot da [**classe Msvm \_ CollectionSnapshotService.**](msvm-collectionsnapshotservice.md)

A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.

## <a name="syntax"></a>Sintaxe

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_CollectionSnapshotExportSettingData : CIM_SettingData
{
  boolean CopyVmStorage;
  string  DifferentialBackupBase;
  uint16  BackupIntent;
};
```

## <a name="members"></a>Membros

A **classe Msvm \_ CollectionSnapshotExportSettingData** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A **classe Msvm \_ CollectionSnapshotExportSettingData** tem essas propriedades.

<dl> <dt>

**BackupIntent**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint16**
</dt> <dt>

Tipo de acesso: Leitura/gravação
</dt> </dl>

Indica a intenção de como os conjuntos de backup exportados seriam usados:

<dt>

<span id="BackupIntentPreserveChain"></span><span id="backupintentpreservechain"></span><span id="BACKUPINTENTPRESERVECHAIN"></span>

<span id="BackupIntentPreserveChain"></span><span id="backupintentpreservechain"></span><span id="BACKUPINTENTPRESERVECHAIN"></span>**BackupIntentPreserveChain** (1)


</dt> <dd>

Todos os conjuntos de backup completos e diferenciais exportados seriam preservados como estão.

</dd> <dt>

<span id="BackupIntentMerge"></span><span id="backupintentmerge"></span><span id="BACKUPINTENTMERGE"></span>

<span id="BackupIntentMerge"></span><span id="backupintentmerge"></span><span id="BACKUPINTENTMERGE"></span>**BackupIntentMerge** (2)


</dt> <dd>

Os conjuntos de backup completos e diferenciais exportados seriam mesclados para sintetizar conjuntos de backup completos.

</dd> </dl>

</dd> <dt>

**CopyVmStorage**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliana**
</dt> <dt>

Tipo de acesso: Leitura/gravação
</dt> </dl>

se **true**, o armazenamento de VM será copiado quando a VM for exportada. Caso contrário, **false.**

</dd> <dt>

**DifferentialBackupBase**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Leitura/gravação
</dt> </dl>

Base para exportação diferencial. Esse é o caminho para uma instância [**Msvm \_ ReferencePointCollection**](msvm-referencepointcollection.md) que representa o ponto de referência ou o caminho para uma instância [**de \_ SnapshotCollection Msvm**](msvm-snapshotcollection.md) que representa o instantâneo a ser usado como base para exportação diferencial.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Windows 10 somente aplicativos da área de trabalho\]<br/>                                                             |
| Servidor mínimo com suporte<br/> | Windows Server 2016<br/>                                                                          |
| Namespace<br/>                | Virtualização \\ raiz \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Configuração \_ cimData**](cim-settingdata.md)
</dt> </dl>

 

 




