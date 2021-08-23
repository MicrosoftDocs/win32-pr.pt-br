---
description: 'Saiba mais sobre: Método CheckVirtualSystemIsMigratableToSystem da classe CIM_VirtualSystemMigrationService'
ms.assetid: d3f7c926-804f-4c7c-8964-a8e464155417
title: Método CheckVirtualSystemIsMigratableToSystem da classe CIM_VirtualSystemMigrationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VirtualSystemMigrationService.CheckVirtualSystemIsMigratableToSystem
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 4f2f543cff29464d76f1b2729efa9bca1a0c677d3cd7173975f59d2007aafb7e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119682706"
---
# <a name="checkvirtualsystemismigratabletosystem-method-of-the-cim_virtualsystemmigrationservice-class"></a>Método CheckVirtualSystemIsMigratableToSystem da classe CIM \_ VirtualSystemMigrationService

Método para executar uma pré-verificação para determinar se um sistema virtual provavelmente será migrado com êxito para um sistema de destino. Esse método não garante que uma migração subsequente sempre terá êxito, devido à disponibilidade dinâmica de recursos. Descrição do código de retorno:

## <a name="syntax"></a>Sintaxe


```mof
uint32 CheckVirtualSystemIsMigratableToSystem(
  [in]  CIM_ComputerSystem REF ComputerSystem,
  [in]  CIM_System         REF DestinationSystem,
  [in]  string                 MigrationSettingData,
  [in]  string                 NewSystemSettingData,
  [in]  string                 NewResourceSettingData[],
  [out] boolean                IsMigratable
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ComputerSystem* \[ Em\]
</dt> <dd>

[**CIM \_ Instância do ComputerSystem**](cim-computersystem.md) que referencia o sistema de computador virtual de origem a ser migrado.

</dd> <dt>

*DestinationSystem* \[ Em\]
</dt> <dd>

[**CIM \_ Instância**](cim-system.md) do sistema que faz referência ao sistema de destino para o qual migrar o sistema virtual.

</dd> <dt>

*MigrationSettingData* \[ Em\]
</dt> <dd>

Cadeia de caracteres que contém uma instância inserida da [**classe CIM \_ VirtualSystemMigrationSettingData**](cim-virtualsystemmigrationsettingdata.md) que representa as configurações de migração aplicáveis à operação de migração.

</dd> <dt>

*NewSystemSettingData* \[ Em\]
</dt> <dd>

Cadeia de caracteres que contém uma instância inserida da classe [**CIM \_ VirtualSystemSettingData**](cim-virtualsystemsettingdata.md) que representa novas propriedades aplicáveis ao sistema virtual depois que ela é migrada.

</dd> <dt>

*NewResourceSettingData* \[ Em\]
</dt> <dd>

Matriz de cadeias de caracteres que contêm uma instância inserida da classe [**CIM \_ ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md) que representa novas propriedades aplicáveis aos recursos virtuais no escopo do sistema virtual depois que ele é migrado.

</dd> <dt>

*IsMigratable* \[ out\]
</dt> <dd>

O resultado da verificação de migração que indica se o sistema virtual pode ou não ser migrado com êxito.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um 0 em caso de êxito; caso contrário, retornará um erro.



| Valor/código de retorno                                                                                                                                                | Descrição                                                                                                                                                                                                                                                                                                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**Concluído sem erro**</dt> <dt>0</dt> </dl>    | Verificação executada; resultado relatado por meio do valor do \[ parâmetro \] *Out IsMigratable.*<br/>                                                                                                                                                                                                                                                                          |
| <dl> <dt>**Sem suporte**</dt> <dt>1</dt> </dl>              | Método sem suporte pela implementação. Nenhum resultado relatado por meio do valor do \[ parâmetro \] *Out IsMigratable.*<br/>                                                                                                                                                                                                                                                |
| <dl> <dt>**Falha**</dt> <dt>2</dt> </dl>                     | Falha na verificação por motivos não especificados. Nenhum resultado relatado por meio do valor do \[ parâmetro \] *Out IsMigratable.*<br/>                                                                                                                                                                                                                                                  |
| <dl> <dt>**Tempoout**</dt> <dt>3</dt> </dl>                    | Verifique o tempo de saída. Nenhum resultado relatado por meio do valor do \[ parâmetro \] *Out IsMigratable.*<br/>                                                                                                                                                                                                                                                                       |
| <dl> <dt>**Parâmetro inválido**</dt> <dt>4</dt> </dl>          | Um ou mais parâmetros são formalmente inválidos. Por exemplo, o valor do parâmetro *DestinationSystem* não inclui um caminho de objeto válido. Nenhum resultado relatado por meio do valor do \[ parâmetro \] *Out IsMigratable.*<br/>                                                                                                                                        |
| <dl> <dt>**Estado inválido**</dt> <dt>5</dt> </dl>              | O sistema virtual de origem, o sistema de host de origem ou o sistema de host de destino estão em um estado que permite o início da migração do sistema virtual solicitada; essa pode ser uma condição temporária. Nenhum resultado relatado por meio do valor do \[ parâmetro \] *Out IsMigratable.*<br/>                                                                                    |
| <dl> <dt>**Parâmetros incompatíveis**</dt> <dt>6</dt> </dl>    | Um ou mais parâmetros de entrada são incompatíveis como um conjunto ou em relação ao host de destino. Por exemplo, o valor do *parâmetro NewSettingData* contém propriedades que não têm suporte pelo sistema de host de destino identificado pelo valor do *parâmetro DestinationSystem.* Nenhum resultado relatado por meio do valor do \[ parâmetro \] *Out IsMigratable.*<br/> |
| <dl> <dt>**DMTF Reservado**</dt> <dt>..</dt> </dl>             |                                                                                                                                                                                                                                                                                                                                                                                 |
| <dl> <dt>**Método Reservado**</dt> <dt>4097..32767</dt> </dl>  |                                                                                                                                                                                                                                                                                                                                                                                 |
| <dl> <dt>**Fornecedor específico**</dt> <dt>32768..65535</dt> </dl> |                                                                                                                                                                                                                                                                                                                                                                                 |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8.1<br/>                                                                                  |
| Servidor mínimo com suporte<br/> | Windows Server 2012 R2<br/>                                                                       |
| Namespace<br/>                | Virtualização \\ raiz \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**CIM \_ VirtualSystemMigrationService**](cim-virtualsystemmigrationservice.md)
</dt> </dl>

 

 




