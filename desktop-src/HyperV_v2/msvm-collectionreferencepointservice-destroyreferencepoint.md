---
description: Destrói uma coleção de pontos de referência existente. Esse método pode como um efeito colateral destruir outros pontos de referência que dependem da coleção de pontos de referência afetados.
ms.assetid: 72c116f4-f844-494c-96ea-e97c49a2af7e
title: Método DestroyReferencePoint da classe Msvm_CollectionReferencePointService dados
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionReferencePointService.DestroyReferencePoint
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 95745646c410c2752f146fc05042b26215f41ef23d3637701497ad565e06583c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119531986"
---
# <a name="destroyreferencepoint-method-of-the-msvm_collectionreferencepointservice-class"></a>Método DestroyReferencePoint da classe Msvm \_ CollectionReferencePointService

Destrói uma coleção de pontos de referência existente. Esse método pode como um efeito colateral destruir outros pontos de referência que dependem da coleção de pontos de referência afetados.

## <a name="syntax"></a>Sintaxe


```mof
uint32 DestroyReferencePoint(
  [in]  CIM_Collection  REF AffectedReferencePointCollection,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*AffectedReferencePointCollection* \[ Em\]
</dt> <dd>

Referência à coleção de pontos de referência do sistema virtual afetado.

</dd> <dt>

*Trabalho* \[ out\]
</dt> <dd>

Se a operação for de execução longa, opcionalmente, um trabalho poderá ser retornado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Se for bem-sucedido, retornará 0 (sem erro) ou 4096 (trabalho iniciado); caso contrário, retorne um erro.

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
| Cliente mínimo com suporte<br/> | \[Windows 10 somente aplicativos da área de trabalho\]<br/>                                                             |
| Servidor mínimo com suporte<br/> | Windows Server 2016<br/>                                                                          |
| Namespace<br/>                | Virtualização \\ raiz \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Msvm \_ CollectionReferencePointService**](msvm-collectionreferencepointservice.md)
</dt> </dl>

 

 




