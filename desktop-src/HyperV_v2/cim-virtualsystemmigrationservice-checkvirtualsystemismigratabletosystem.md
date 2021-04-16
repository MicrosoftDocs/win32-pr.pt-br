---
description: 'Saiba mais sobre: método CheckVirtualSystemIsMigratableToSystem da classe CIM_VirtualSystemMigrationService'
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
ms.openlocfilehash: be85c51cb507fea3cea14f1706ffa8f67af06c42
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105757421"
---
# <a name="checkvirtualsystemismigratabletosystem-method-of-the-cim_virtualsystemmigrationservice-class"></a>Método CheckVirtualSystemIsMigratableToSystem da \_ classe VIRTUALSYSTEMMIGRATIONSERVICE CIM

Método para executar uma verificação prévia para determinar se um sistema virtual provavelmente será migrado com êxito para um sistema de destino. Esse método não garante que uma migração subsequente sempre terá sucesso, devido à disponibilidade dinâmica de recursos. Descrição do código de retorno:

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

*ComputerSystem* \[ no\]
</dt> <dd>

[**CIM \_**](cim-computersystem.md) Instância de ComputerSystem que faz referência ao sistema de computador virtual de origem a ser migrado.

</dd> <dt>

*DestinationSystem* \[ no\]
</dt> <dd>

[**CIM \_**](cim-system.md) Instância do sistema que faz referência ao sistema de destino para o qual migrar o sistema virtual.

</dd> <dt>

*MigrationSettingData* \[ no\]
</dt> <dd>

Cadeia de caracteres que contém uma instância inserida da classe [**CIM \_ VirtualSystemMigrationSettingData**](cim-virtualsystemmigrationsettingdata.md) que representa as configurações de migração aplicáveis à operação de migração.

</dd> <dt>

*NewSystemSettingData* \[ no\]
</dt> <dd>

Cadeia de caracteres que contém uma instância inserida da classe [**CIM \_ VirtualSystemSettingData**](cim-virtualsystemsettingdata.md) que representa as novas propriedades aplicáveis ao sistema virtual depois que ele é migrado.

</dd> <dt>

*NewResourceSettingData* \[ no\]
</dt> <dd>

Matriz de cadeias de caracteres que contém uma instância incorporada da classe [**CIM \_ ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md) que representa as novas propriedades aplicáveis aos recursos virtuais no escopo do sistema virtual depois que ele é migrado.

</dd> <dt>

*IsMigratable* \[ fora\]
</dt> <dd>

O resultado da verificação de migração que indica se o sistema virtual pode ou não ser migrado com êxito.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna um 0 em caso de êxito; caso contrário, retornará um erro.



| Código/valor de retorno                                                                                                                                                | Descrição                                                                                                                                                                                                                                                                                                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**Concluído sem erro**</dt> <dt>0</dt> </dl>    | Verificação realizada; resultado relatado por meio do valor do \[ parâmetro out \] *IsMigratable* .<br/>                                                                                                                                                                                                                                                                          |
| <dl> <dt>**Sem suporte**</dt> <dt>1</dt> </dl>              | Método sem suporte pela implementação. Nenhum resultado relatado pelo valor do \[ parâmetro out \] *IsMigratable* .<br/>                                                                                                                                                                                                                                                |
| <dl> <dt>**Com falha**</dt> <dt>2</dt> </dl>                     | A verificação falhou por razões não especificadas. Nenhum resultado relatado pelo valor do \[ parâmetro out \] *IsMigratable* .<br/>                                                                                                                                                                                                                                                  |
| <dl> <dt>**Tempo limite**</dt> <dt>3</dt> </dl>                    | A verificação atingiu o tempo limite. Nenhum resultado relatado pelo valor do \[ parâmetro out \] *IsMigratable* .<br/>                                                                                                                                                                                                                                                                       |
| <dl> <dt>**Parâmetro inválido**</dt> <dt>4</dt> </dl>          | Um ou mais parâmetros são formalmente inválidos. Por exemplo, o valor do parâmetro *DestinationSystem* não inclui um caminho de objeto válido. Nenhum resultado relatado pelo valor do \[ parâmetro out \] *IsMigratable* .<br/>                                                                                                                                        |
| <dl> <dt>**Estado inválido**</dt> <dt>5</dt> </dl>              | O sistema virtual de origem, o sistema host de origem ou o sistema host de destino estão em um estado que permite a inicialização da migração de sistema virtual solicitada; Essa pode ser uma condição temporária. Nenhum resultado relatado pelo valor do \[ parâmetro out \] *IsMigratable* .<br/>                                                                                    |
| <dl> <dt>**Parâmetros incompatíveis**</dt> <dt>6</dt> </dl>    | Um ou mais parâmetros de entrada são incompatíveis como um conjunto ou em relação ao host de destino. Por exemplo, o valor do parâmetro *NewSettingData* contém propriedades que não são suportadas pelo sistema host de destino identificado pelo valor do parâmetro *DestinationSystem* . Nenhum resultado relatado pelo valor do \[ parâmetro out \] *IsMigratable* .<br/> |
| <dl> <dt>**DMTF reservado**</dt> <dt>..</dt> </dl>             |                                                                                                                                                                                                                                                                                                                                                                                 |
| <dl> <dt>**Método reservado**</dt> <dt>4097.. 32767</dt> </dl>  |                                                                                                                                                                                                                                                                                                                                                                                 |
| <dl> 32768 <dt>**específicos do fornecedor**</dt> <dt>. 65535</dt> </dl> |                                                                                                                                                                                                                                                                                                                                                                                 |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8.1<br/>                                                                                  |
| Servidor mínimo com suporte<br/> | Windows Server 2012 R2<br/>                                                                       |
| Namespace<br/>                | \\Virtualização \\ v2 de raiz<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_VIRTUALSYSTEMMIGRATIONSERVICE CIM**](cim-virtualsystemmigrationservice.md)
</dt> </dl>

 

 




