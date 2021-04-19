---
description: Determina se o sistema virtual especificado pode ser migrado para um sistema de destino.
ms.assetid: 2E340737-DEE9-4853-ACD8-BEE2A8C69D6D
title: Método CheckVirtualSystemIsMigratableToSystem da classe Msvm_VirtualSystemMigrationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemMigrationService.CheckVirtualSystemIsMigratableToSystem
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 3e8f294f7e30740e3afab8987c734dbbdbd12acf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105785446"
---
# <a name="checkvirtualsystemismigratabletosystem-method-of-the-msvm_virtualsystemmigrationservice-class"></a>Método CheckVirtualSystemIsMigratableToSystem da \_ classe VirtualSystemMigrationService Msvm

Determina se o sistema virtual especificado pode ser migrado para um sistema de destino.

## <a name="syntax"></a>Sintaxe


```mof
uint32 CheckVirtualSystemIsMigratableToSystem(
  [in]  Msvm_ComputerSystem REF ComputerSystem,
  [in]  Msvm_ComputerSystem REF DestinationSystem,
  [in]  string                  MigrationSettingData,
  [in]  string                  NewSystemSettingData,
  [in]  string                  NewResourceSettingData[],
  [out] boolean                 IsMigratable
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ComputerSystem* \[ no\]
</dt> <dd>

Uma referência a uma instância da classe [**Msvm \_ ComputerSystem**](msvm-computersystem.md) que representa a máquina virtual para testar a capacidade de migração do.

</dd> <dt>

*DestinationSystem* \[ no\]
</dt> <dd>

Uma referência a uma instância da classe [**Msvm \_ ComputerSystem**](msvm-computersystem.md) que representa a máquina virtual para testar a capacidade de migração para o.

</dd> <dt>

*MigrationSettingData* \[ no\]
</dt> <dd>

Uma instância inserida da classe [**Msvm \_ VirtualSystemMigrationSettingData**](msvm-virtualsystemmigrationsettingdata.md) que representa as configurações da operação de migração.

</dd> <dt>

*NewSystemSettingData* \[ no\]
</dt> <dd>

Uma instância inserida da classe [**Msvm \_ VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) que representa as novas propriedades aplicáveis ao sistema virtual depois que ele é migrado.

</dd> <dt>

*NewResourceSettingData* \[ no\]
</dt> <dd>

Uma matriz de cadeias de caracteres que contém uma instância incorporada da classe [**Msvm \_ ResourceAllocationSettingData**](msvm-resourceallocationsettingdata.md) que representa as novas propriedades aplicáveis aos recursos virtuais do sistema virtual depois que ele é migrado.

</dd> <dt>

*IsMigratable* \[ fora\]
</dt> <dd>

Recebe o resultado da verificação de migração que indica se o sistema virtual pode ser migrado com êxito.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método retorna um dos valores a seguir.

<dl> <dt>

**Concluído sem erro** (0)
</dt> <dt>

**Sem suporte** (1)
</dt> <dt>

**Falha** (2)
</dt> <dt>

**Tempo limite** (3)
</dt> <dt>

**Parâmetro inválido** (4)
</dt> <dt>

**Estado inválido** (5)
</dt> <dt>

**Parâmetros incompatíveis** (6)
</dt> <dt>

**DMTF reservado** (..)
</dt> <dt>

**Método reservado** (4097.. 32767)
</dt> <dt>

**Específico do fornecedor** (32768.. 65535)
</dt> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows 10\]<br/>                                                             |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2016\]<br/>                                                    |
| Namespace<br/>                | \\Virtualização \\ v2 de raiz<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Msvm \_ VirtualSystemMigrationService**](msvm-virtualsystemmigrationservice.md)
</dt> </dl>

 

 




