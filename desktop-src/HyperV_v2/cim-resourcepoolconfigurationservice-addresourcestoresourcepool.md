---
description: Inicia um trabalho para adicionar recursos a um pool de recursos.
ms.assetid: b163619a-19bd-43d7-ba35-ec4bd8192100
title: Método AddResourcesToResourcePool da classe CIM_ResourcePoolConfigurationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ResourcePoolConfigurationService.AddResourcesToResourcePool
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 55191f3ddce5672d1b76987b8a7c2ce1f87b9cca330a7ba14aa4ae10bacc5b67
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119980926"
---
# <a name="addresourcestoresourcepool-method-of-the-cim_resourcepoolconfigurationservice-class"></a>Método AddResourcesToResourcePool da \_ classe RESOURCEPOOLCONFIGURATIONSERVICE CIM

Inicia um trabalho para adicionar recursos a um pool de recursos.

## <a name="syntax"></a>Sintaxe


```mof
uint32 AddResourcesToResourcePool(
  [in]  CIM_LogicalDevice REF HostResources[],
  [in]  CIM_ResourcePool  REF Pool,
  [out] CIM_ConcreteJob   REF Job
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Recursos* \[ no\]
</dt> <dd>

Matriz de instâncias de [**\_ LogicalDevice CIM**](cim-logicaldevice.md) a serem adicionadas ao pool.

</dd> <dt>

*Pool* \[ de no\]
</dt> <dd>

Um [**\_ ResourcePool CIM**](cim-resourcepool.md) que representa o pool no qual os recursos são adicionados.

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

**Tamanho sem suporte** (4097)
</dt> <dt>

**Método reservado** (4098.. 32767)
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

 

 




