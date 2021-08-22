---
description: Inicie um trabalho para excluir um pool de recursos.
ms.assetid: af3d9c7c-a825-4568-822d-044b3d92d144
title: Método DeleteResourcePool da classe CIM_ResourcePoolConfigurationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ResourcePoolConfigurationService.DeleteResourcePool
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: a5fb895eb76a503d6199bf1057a9f9eaff0c72e4af59460c63551a7c581ff0cd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118648085"
---
# <a name="deleteresourcepool-method-of-the-cim_resourcepoolconfigurationservice-class"></a>Método DeleteResourcePool da \_ classe RESOURCEPOOLCONFIGURATIONSERVICE CIM

Inicie um trabalho para excluir um pool de recursos. Nenhuma alocação pode estar pendente ou a exclusão falhará com "em uso". Se o pool de recursos for um pool de recursos raiz, todos os recursos do host serão retornados para o sistema subjacente.

## <a name="syntax"></a>Sintaxe


```mof
uint32 DeleteResourcePool(
  [in]  CIM_ResourcePool REF Pool,
  [out] CIM_ConcreteJob  REF Job
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Pool* \[ de no\]
</dt> <dd>

Um [**\_ ResourcePool CIM**](cim-resourcepool.md) que faz referência ao pool a ser excluído.

</dd> <dt>

*Trabalho* \[ do fora\]
</dt> <dd>

Um [**\_ ConcreteJob CIM**](cim-concretejob.md) que referencia o trabalho (pode ser **nulo** se o trabalho for concluído).

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um 0 em caso de êxito; caso contrário, retornará um erro.

<dl> <dt>

**Trabalho concluído sem erro** (0)
</dt> <dt>

**Sem suporte** (1)
</dt> <dt>

**Desconhecido** (2)
</dt> <dt>

**Tempo limite** (3)
</dt> <dt>

**Com falha** (4)
</dt> <dt>

**Parâmetro inválido** (5)
</dt> <dt>

**Em uso** (6)
</dt> <dt>

**ResourceType incorreto para o pool** (7)
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
| Cliente mínimo com suporte<br/> | Windows 8.1<br/>                                                                                  |
| Servidor mínimo com suporte<br/> | Windows Server 2012 R2<br/>                                                                       |
| Namespace<br/>                | \\Virtualização \\ v2 de raiz<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_RESOURCEPOOLCONFIGURATIONSERVICE CIM**](cim-resourcepoolconfigurationservice.md)
</dt> </dl>

 

 




