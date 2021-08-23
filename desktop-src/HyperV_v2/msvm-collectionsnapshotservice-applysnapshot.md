---
description: Aplica uma coleção de instantâneos à coleção do sistema de computador virtual.
ms.assetid: c76c552a-ae07-4dab-a938-740d77447a53
title: Método ApplySnapshot da Msvm_CollectionSnapshotService classe
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
ms.openlocfilehash: f4dd36db457099aaa9c134593fa385f21480e036e15629d10c32e716e604a462
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119426926"
---
# <a name="applysnapshot-method-of-the-msvm_collectionsnapshotservice-class"></a>Método ApplySnapshot da classe Msvm \_ CollectionSnapshotService

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

*SnapshotCollection* \[ Em\]
</dt> <dd>

Uma referência a uma [**Coleção CIM \_**](cim-collection.md) que representa a coleção de instantâneos a ser aplicada.

</dd> <dt>

*Trabalho* \[ out\]
</dt> <dd>

Uma referência opcional que será retornada se a operação for executada de forma assíncrona. Se presente, a referência retornada a uma instância de [**CIM \_ ConcreteJob**](cim-concretejob.md) pode ser usada para monitorar o progresso e obter o resultado do método.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Em caso de sucesso, retorna um 0; caso contrário, retornará um erro.

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

**Tipo inválido** (6)
</dt> <dt>

**DMTF Reservado** (..)
</dt> <dt>

**Parâmetros de método verificados – Trabalho iniciado** (4096)
</dt> <dt>

**Método Reservado** (4097..32767)
</dt> <dt>

**Específico do** fornecedor (32768..65535)
</dt> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 10, versão 1703 somente \[ aplicativos da área de trabalho\]<br/>                                               |
| Servidor mínimo com suporte<br/> | Windows Server 2016<br/>                                                                          |
| Namespace<br/>                | Virtualização \\ raiz \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Coleção \_ MsvmSnapshotService**](msvm-collectionsnapshotservice.md)
</dt> </dl>

 

 




