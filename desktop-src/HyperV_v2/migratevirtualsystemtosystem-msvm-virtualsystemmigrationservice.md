---
description: Move, migra ou realoca um sistema virtual para um sistema de destino.
ms.assetid: 3a0be791-4514-4ce2-b4e8-3735bd6ea1d7
title: Método MigrateVirtualSystemToSystem da classe Msvm_VirtualSystemMigrationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemMigrationService.MigrateVirtualSystemToSystem
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 398c4ae9d9d8ad89f7188ecbfe19e1b687bd694f7e716e88bd5231e79a38a665
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119694267"
---
# <a name="migratevirtualsystemtosystem-method-of-the-msvm_virtualsystemmigrationservice-class"></a>Método MigrateVirtualSystemToSystem da classe Msvm \_ VirtualSystemMigrationService

Move, migra ou realoca um sistema virtual para um sistema de destino.

## <a name="syntax"></a>Sintaxe


```mof
uint32 MigrateVirtualSystemToSystem(
  [in]  CIM_ComputerSystem REF ComputerSystem,
  [in]  CIM_System         REF DestinationSystem,
  [in]  string                 MigrationSettingData,
  [in]  string                 NewSystemSettingData,
  [in]  string                 NewResourceSettingData[],
  [out] CIM_ComputerSystem REF NewComputerSystem,
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ComputerSystem* \[ Em\]
</dt> <dd>

Uma referência a uma instância da [**classe Msvm \_ ComputerSystem**](msvm-computersystem.md) que representa o sistema de computador virtual a ser migrado.

</dd> <dt>

*DestinationSystem* \[ Em\]
</dt> <dd>

Uma referência a uma instância da [**classe Msvm \_ ComputerSystem**](msvm-computersystem.md) que representa o sistema para o que será migrado.

</dd> <dt>

*MigrationSettingData* \[ Em\]
</dt> <dd>

Uma instância inserida da [**classe Msvm \_ VirtualSystemMigrationSettingData**](msvm-virtualsystemmigrationsettingdata.md) que representa as configurações para a operação de migração.

</dd> <dt>

*NewSystemSettingData* \[ Em\]
</dt> <dd>

Uma instância inserida da [**classe Msvm \_ VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) que representa novas propriedades aplicáveis ao sistema virtual depois que ele é migrado.

</dd> <dt>

*NewResourceSettingData* \[ Em\]
</dt> <dd>

Uma matriz de cadeias de caracteres que contém uma instância inserida da classe [**Msvm \_ ResourceAllocationSettingData**](msvm-resourceallocationsettingdata.md) que representa as novas propriedades aplicáveis aos recursos virtuais do sistema virtual depois que ele é migrado.

</dd> <dt>

*NewComputerSystem* \[ out\]
</dt> <dd>

Uma referência a uma instância da [**classe Msvm \_ ComputerSystem**](msvm-computersystem.md) que representa o novo sistema migrado.

</dd> <dt>

*Trabalho* \[ out\]
</dt> <dd>

Se a operação for executada de forma assíncrona, esse método retornará 4096 e esse parâmetro conterá uma referência a um objeto derivado de [**CIM \_ ConcreteJob.**](/previous-versions//cc136808(v=vs.85))

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método retorna um dos valores a seguir.

<dl> <dt>

**Concluído sem erro** (0)
</dt> <dt>

**Sem suporte** (1)
</dt> <dt>

**Falha** (2)
</dt> <dt>

**Tempoout** (3)
</dt> <dt>

**Parâmetro inválido** (4)
</dt> <dt>

**Estado inválido** (5)
</dt> <dt>

**Parâmetros incompatíveis** (6)
</dt> <dt>

**DMTF Reservado** (..)
</dt> <dt>

**Parâmetros de método verificados – Trabalho iniciado** (4096)
</dt> <dt>

**Método Reservado** (4097..32767)
</dt> <dt>

**Específico do** fornecedor (32768..65535 )
</dt> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Windows 8 somente aplicativos da área de trabalho\]<br/>                                                              |
| Servidor mínimo com suporte<br/> | \[Windows Server 2012 somente aplicativos da área de trabalho\]<br/>                                                    |
| Namespace<br/>                | Virtualização \\ raiz \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Msvm \_ VirtualSystemMigrationService**](msvm-virtualsystemmigrationservice.md)
</dt> </dl>

 

