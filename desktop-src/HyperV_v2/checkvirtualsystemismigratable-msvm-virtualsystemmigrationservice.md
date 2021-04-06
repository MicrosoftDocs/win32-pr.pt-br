---
description: Determina se o sistema virtual especificado pode ser migrado.
ms.assetid: 1bf1b385-162e-41c9-a408-f7ee755a9646
title: Método CheckVirtualSystemIsMigratable da classe Msvm_VirtualSystemMigrationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemMigrationService.CheckVirtualSystemIsMigratable
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 1aed843f3f0f4c6c30eb6125cdd5859cdba902d0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826869"
---
# <a name="checkvirtualsystemismigratable-method-of-the-msvm_virtualsystemmigrationservice-class"></a>Método CheckVirtualSystemIsMigratable da \_ classe VirtualSystemMigrationService Msvm

Determina se o sistema virtual especificado pode ser migrado.

## <a name="syntax"></a>Sintaxe


```mof
uint32 CheckVirtualSystemIsMigratable(
  [in]  CIM_ComputerSystem REF ComputerSystem,
  [in]  string                 DestinationHost,
  [in]  string                 MigrationSettingData,
  [in]  string                 NewSystemSettingData,
  [in]  string                 NewResourceSettingData[],
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ComputerSystem* \[ no\]
</dt> <dd>

Uma referência a uma instância da classe [**de \_ ComputerSystem do CIM**](cim-computersystem.md) que representa a máquina virtual para testar a capacidade de migração do.

</dd> <dt>

*DestinationHost* \[ no\]
</dt> <dd>

O nome do sistema host para a migração. O formato desse nome é especificado pela propriedade **DestinationHostFormatsSupported** da classe [**Msvm \_ VirtualSystemMigrationCapabilities**](msvm-virtualsystemmigrationcapabilities.md) associada a essa classe.

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

*Trabalho* \[ do fora\]
</dt> <dd>

Se a operação for executada de forma assíncrona, esse método retornará 4096, e esse parâmetro conterá uma referência a um objeto derivado de [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método retorna um dos valores a seguir.

<dl> <dt>

**Parâmetros de método marcados-trabalho iniciado** (4096)
</dt> <dt>

**Falha** (32768)
</dt> <dt>

**Acesso negado** (32769)
</dt> <dt>

**Sem suporte** (32770)
</dt> <dt>

O **status é desconhecido** (32771)
</dt> <dt>

**Tempo limite** (32772)
</dt> <dt>

**Parâmetro inválido** (32773)
</dt> <dt>

O **sistema está em uso** (32774)
</dt> <dt>

**Estado inválido para esta operação** (32775)
</dt> <dt>

**Tipo de dados incorreto** (32776)
</dt> <dt>

O **sistema não está disponível** (32777)
</dt> <dt>

**Memória insuficiente** (32778)
</dt> </dl>

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

[**Msvm \_ VirtualSystemMigrationService**](msvm-virtualsystemmigrationservice.md)
</dt> </dl>

 

