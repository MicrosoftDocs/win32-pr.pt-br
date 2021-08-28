---
description: Destrói um instantâneo existente da coleção do sistema virtual. Esse método pode, como um efeito colateral, destruir outros instantâneos que dependem do instantâneo afetado.
ms.assetid: 79a529d5-35bb-4e63-a1b7-8943de9580e8
title: Método DestroySnapshot da classe Msvm_CollectionSnapshotService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionSnapshotService.DestroySnapshot
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: bacdb760580057516b6663bf53f5cd02a83f76148fa782ab875ca7385c053cb4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119431486"
---
# <a name="destroysnapshot-method-of-the-msvm_collectionsnapshotservice-class"></a>Método DestroySnapshot da \_ classe CollectionSnapshotService Msvm

Destrói um instantâneo existente da coleção do sistema virtual. Esse método pode, como um efeito colateral, destruir outros instantâneos que dependem do instantâneo afetado.

## <a name="syntax"></a>Sintaxe


```mof
uint32 DestroySnapshot(
  [in]  CIM_Collection  REF AffectedSnapshotCollection,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*AffectedSnapshotCollection* \[ no\]
</dt> <dd>

Referência a uma [**\_ coleção CIM**](cim-collection.md) que descreve a coleção de instantâneos do sistema virtual afetada.

</dd> <dt>

*Trabalho* \[ do fora\]
</dt> <dd>

Uma referência opcional que será retornada se a operação for executada de forma assíncrona. Se estiver presente, a referência retornada a uma instância de [**CIM \_ ConcreteJob**](cim-concretejob.md) poderá ser usada para monitorar o progresso e obter o resultado do método.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Em caso de sucesso, retorna 0 (completo) ou 4096 (trabalho iniciado); caso contrário, retornará um erro.

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
| Cliente mínimo com suporte<br/> | Windows 10 \[ somente aplicativos da área de trabalho\]<br/>                                                             |
| Servidor mínimo com suporte<br/> | Windows Server 2016<br/>                                                                          |
| Namespace<br/>                | \\Virtualização \\ v2 de raiz<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Msvm \_ CollectionSnapshotService**](msvm-collectionsnapshotservice.md)
</dt> </dl>

 

 




