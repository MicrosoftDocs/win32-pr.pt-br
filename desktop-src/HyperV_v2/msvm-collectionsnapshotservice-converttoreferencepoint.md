---
description: Converta um instantâneo de coleção existente em uma coleção de pontos de referência. A coleção de instantâneos é excluída como um efeito colateral. Somente instantâneos de recuperação podem ser convertidos em pontos de referência.
ms.assetid: 6b304782-9e5e-43b1-af7d-08617d65850c
title: Método ConvertToReferencePoint da classe Msvm_CollectionSnapshotService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionSnapshotService.ConvertToReferencePoint
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 810761b67303ad33ced6fdaef857c96f65365091
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103837422"
---
# <a name="converttoreferencepoint-method-of-the-msvm_collectionsnapshotservice-class"></a>Método ConvertToReferencePoint da \_ classe CollectionSnapshotService Msvm

Converta um instantâneo de coleção existente em uma coleção de pontos de referência. A coleção de instantâneos é excluída como um efeito colateral. Somente instantâneos de recuperação podem ser convertidos em pontos de referência.

## <a name="syntax"></a>Sintaxe


```mof
uint32 ConvertToReferencePoint(
  [in]      Msvm_SnapshotCollection       REF AffectedSnapshotCollection,
  [in, out] Msvm_ReferencePointCollection REF ResultingReferencePointCollection,
  [out]     CIM_ConcreteJob               REF Job
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*AffectedSnapshotCollection* \[ no\]
</dt> <dd>

Referência a um [**Msvm \_ snapshotcollection**](msvm-snapshotcollection.md) que contém a coleção de instantâneos do sistema virtual afetada.

</dd> <dt>

*ResultingReferencePointCollection* \[ entrada, saída\]
</dt> <dd>

Referência a um [**Msvm \_ ReferencePointCollection**](msvm-referencepointcollection.md) que contém a coleção de pontos de referência do sistema virtual resultante

</dd> <dt>

*Trabalho* \[ do fora\]
</dt> <dd>

Se a operação for de longa execução, opcionalmente, um trabalho poderá ser retornado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

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
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows 10\]<br/>                                                             |
| Servidor mínimo com suporte<br/> | Windows Server 2016<br/>                                                                          |
| Namespace<br/>                | \\Virtualização \\ v2 de raiz<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Msvm \_ CollectionSnapshotService**](msvm-collectionsnapshotservice.md)
</dt> </dl>

 

 




