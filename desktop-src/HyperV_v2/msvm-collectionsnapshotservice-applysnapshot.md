---
description: Aplica uma coleção de instantâneos à coleção do sistema de computador virtual.
ms.assetid: c76c552a-ae07-4dab-a938-740d77447a53
title: Método ApplySnapshot da classe Msvm_CollectionSnapshotService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionSnapshotService.ApplySnapshot
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 1fa5b664b39541b9d697dfbbfd0493f7a6f7cf96
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105782810"
---
# <a name="applysnapshot-method-of-the-msvm_collectionsnapshotservice-class"></a>Método ApplySnapshot da \_ classe CollectionSnapshotService Msvm

Aplica uma coleção de instantâneos à coleção do sistema de computador virtual.

## <a name="syntax"></a>Sintaxe


```mof
uint32 ApplySnapshot(
  [in]  CIM_Collection  REF SnapshotCollection,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Instantâneocollection* \[ no\]
</dt> <dd>

Uma referência a uma [**\_ coleção CIM**](cim-collection.md) que representa a coleção de instantâneos a ser aplicada.

</dd> <dt>

*Trabalho* \[ do fora\]
</dt> <dd>

Uma referência opcional que será retornada se a operação for executada de forma assíncrona. Se estiver presente, a referência retornada a uma instância de [**CIM \_ ConcreteJob**](cim-concretejob.md) poderá ser usada para monitorar o progresso e obter o resultado do método.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Em caso de sucesso, retorna um 0; caso contrário, retornará um erro.

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

**Tipo inválido** (6)
</dt> <dt>

**DMTF reservado** (..)
</dt> <dt>

**Parâmetros de método marcados-trabalho iniciado** (4096)
</dt> <dt>

**Método reservado** (4097.. 32767)
</dt> <dt>

**Específico do fornecedor** (32768.. 65535)
</dt> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows 10, versão 1703\]<br/>                                               |
| Servidor mínimo com suporte<br/> | Windows Server 2016<br/>                                                                          |
| Namespace<br/>                | \\Virtualização \\ v2 de raiz<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Msvm \_ CollectionSnapshotService**](msvm-collectionsnapshotservice.md)
</dt> </dl>

 

 




