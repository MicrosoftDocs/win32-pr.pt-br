---
description: Método para mover, migrar ou realocar um sistema virtual para um sistema de destino.
ms.assetid: 210d31f1-093f-4fd5-afd7-5f028b4cb343
title: Método MigrateVirtualSystemToSystem da classe CIM_VirtualSystemMigrationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VirtualSystemMigrationService.MigrateVirtualSystemToSystem
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 7b60e691f2f873a26a52f59def32b35005d45914f7fe379af14b5260b02a0c43
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118393414"
---
# <a name="migratevirtualsystemtosystem-method-of-the-cim_virtualsystemmigrationservice-class"></a>Método MigrateVirtualSystemToSystem da \_ classe VIRTUALSYSTEMMIGRATIONSERVICE CIM

Método para mover, migrar ou realocar um sistema virtual para um sistema de destino.

Descrição do código de retorno:

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

*ComputerSystem* \[ no\]
</dt> <dd>

Sistema de computador virtual de origem a ser migrado.

</dd> <dt>

*DestinationSystem* \[ no\]
</dt> <dd>

Sistema host de destino ondepara migrar o sistema virtual.

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

*NewComputerSystem* \[ fora\]
</dt> <dd>

Referência a uma instância da classe [**de \_ ComputerSystem do CIM**](cim-computersystem.md) que representa o sistema de computador virtual depois que ele foi migrado.

</dd> <dt>

*Trabalho* \[ do fora\]
</dt> <dd>

Se a operação for de longa execução, opcionalmente, [**um \_ ConcreteJob CIM**](cim-concretejob.md) que representa o trabalho poderá ser retornado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um 0 em caso de êxito; caso contrário, retornará um erro.



| Código/valor de retorno                                                                                                                                                                | Description                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**Concluído sem erro**</dt> <dt>0</dt> </dl>                    | O sistema virtual foi migrado.<br/>                                                                                                                                                                                                                                                                    |
| <dl> <dt>**Sem suporte**</dt> <dt>1</dt> </dl>                              | Método sem suporte pela implementação.<br/>                                                                                                                                                                                                                                                         |
| <dl> <dt>**Com falha**</dt> <dt>2</dt> </dl>                                     | A migração do sistema virtual falhou por motivos não especificados.<br/>                                                                                                                                                                                                                                        |
| <dl> <dt>**Tempo limite**</dt> <dt>3</dt> </dl>                                    | Tempo limite de migração do sistema virtual; o estado do sistema virtual é desconhecido.<br/>                                                                                                                                                                                                                         |
| <dl> <dt>**Parâmetro inválido**</dt> <dt>4</dt> </dl>                          | Um ou mais parâmetros são formalmente inválidos, por exemplo, o valor do parâmetro do sistema de destino não contém um caminho de objeto válido.<br/>                                                                                                                                                    |
| <dl> <dt>**Estado inválido**</dt> <dt>5</dt> </dl>                              | O sistema virtual de origem, o sistema host de origem ou o sistema host de destino estão em um estado que permite a inicialização da migração de sistema virtual solicitada; Essa pode ser uma condição temporária.<br/>                                                                                             |
| <dl> <dt>**Parâmetros incompatíveis**</dt> <dt>6</dt> </dl>                    | Um ou mais parâmetros de entrada são incompatíveis como um conjunto ou em relação ao host de destino. Por exemplo, o valor do parâmetro *MigrationNewSettingData* contém propriedades que não são suportadas pelo sistema host de destino identificado pelo valor do parâmetro *DestinationSystem* .<br/> |
| <dl> <dt>**DMTF reservado**</dt> <dt>..</dt> </dl>                             |                                                                                                                                                                                                                                                                                                            |
| <dl> <dt>**Parâmetros de método verificados-trabalho iniciado**</dt> <dt>4096</dt> </dl> |                                                                                                                                                                                                                                                                                                            |
| <dl> <dt>**Método reservado**</dt> <dt>4097.. 32767</dt> </dl>                  |                                                                                                                                                                                                                                                                                                            |
| <dl> 32768 <dt>**específicos do fornecedor**</dt> <dt>. 65535</dt> </dl>                 |                                                                                                                                                                                                                                                                                                            |



 

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

 

 




