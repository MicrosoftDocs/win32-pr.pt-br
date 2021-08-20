---
description: Exclui o ponto de referência especificado.
ms.assetid: cb5245b6-5984-40ec-a37e-e4a0a62e318a
title: Método DestroyReferencePoint da classe Msvm_VirtualSystemReferencePointService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemReferencePointService.DestroyReferencePoint
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 8b63b383bc44c50049c6ab00bdccb1dd5e2081beeb98a82a0a17c35147b4e436
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118146415"
---
# <a name="destroyreferencepoint-method-of-the-msvm_virtualsystemreferencepointservice-class"></a>Método DestroyReferencePoint da \_ classe VirtualSystemReferencePointService Msvm

Exclui o ponto de referência especificado.

## <a name="syntax"></a>Sintaxe


```mof
uint32 DestroyReferencePoint(
  [in]  Msvm_VirtualSystemReferencePoint REF AffectedReferencePoint,
  [out] CIM_ConcreteJob                  REF Job
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*AffectedReferencePoint* \[ no\]
</dt> <dd>

Uma referência à instância [**de \_ VirtualSystemReferencePoint Msvm**](msvm-virtualsystemreferencepoint.md) que representa o ponto de referência a ser removido.

</dd> <dt>

*Trabalho* \[ do fora\]
</dt> <dd>

Um parâmetro opcional para monitorar o progresso da operação, que é usado se o método não pôde ser executado de forma síncrona. Se a operação estiver sendo executada de forma assíncrona, o valor de retorno será 4096.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Em caso de sucesso, retorna um 0 (completo sem erro) ou 4096 (trabalho iniciado); caso contrário, retorne um erro.

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

[**Msvm \_ VirtualSystemReferencePointService**](msvm-virtualsystemreferencepointservice.md)
</dt> </dl>

 

 




