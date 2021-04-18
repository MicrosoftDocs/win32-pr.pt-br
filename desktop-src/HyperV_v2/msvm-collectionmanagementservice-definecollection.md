---
description: Cria um novo \_ objeto CIM CollectionOfMSEs.
ms.assetid: cd2a0cde-d4c6-4ba8-8140-fcc7546c1006
title: Método definocollection da classe Msvm_CollectionManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionManagementService.DefineCollection
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 34ab998f2b742997d588190db80bd342628a07e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105767640"
---
# <a name="definecollection-method-of-the-msvm_collectionmanagementservice-class"></a>Método definocollection da classe Msvm \_ CollectionManagementService

Cria um novo objeto [**CIM \_ CollectionOfMSEs**](cim-collectionofmses.md) .

## <a name="syntax"></a>Sintaxe


```mof
uint32 DefineCollection(
  [in]  string                   Name,
  [in]  string                   Id,
  [in]  uint16                   Type,
  [out] CIM_CollectionOfMSEs REF DefinedCollection,
  [out] CIM_ConcreteJob      REF Job
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Nome* \[ do no\]
</dt> <dd>

O nome da nova coleção.

</dd> <dt>

*ID* \[ em\]
</dt> <dd>

A ID da nova coleção.

</dd> <dt>

*Tipo* \[ de no\]
</dt> <dd>

O tipo da nova coleção.

<dt>

<span id="Collection_of_Virtual_Systems"></span><span id="collection_of_virtual_systems"></span><span id="COLLECTION_OF_VIRTUAL_SYSTEMS"></span>

**Coleção de sistemas virtuais** (0)


</dt> <dd></dd> <dt>

<span id="Collection_of_Collections"></span><span id="collection_of_collections"></span><span id="COLLECTION_OF_COLLECTIONS"></span>

**Coleção de coleções** (1)


</dt> <dd></dd> </dl> </dd> <dt>

*Definedcollection* \[ fora\]
</dt> <dd>

Referência aos objetos que definem a coleção.

</dd> <dt>

*Trabalho* \[ do fora\]
</dt> <dd>

Uma referência ao trabalho (pode ser NULL se a tarefa for concluída).

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Se for bem-sucedido, retornará 0 ou 4096 (trabalho iniciado); caso contrário, retornará um erro.

<dl> <dt>

**Concluído sem erro** (0)
</dt> <dt>

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
</dt> <dt>

**Arquivo não encontrado** (32779)
</dt> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows 10\]<br/>                                                             |
| Servidor mínimo com suporte<br/> | Windows Server 2016<br/>                                                                          |
| Namespace<br/>                | \\Virtualização \\ v2 de raiz<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Msvm \_ CollectionManagementService**](msvm-collectionmanagementservice.md)
</dt> </dl>

 

 




