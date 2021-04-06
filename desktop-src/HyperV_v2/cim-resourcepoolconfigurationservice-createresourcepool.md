---
description: Inicia um trabalho para criar um ResourcePool raiz. O ResourcePool será definido como escopo para o mesmo sistema que esse serviço.
ms.assetid: 357880dc-125a-452c-89f5-44cd17684436
title: Método CreateResourcePool da classe CIM_ResourcePoolConfigurationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ResourcePoolConfigurationService.CreateResourcePool
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: ca339eb2e2a4ec0fb441c5ed1a657608d71248bc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103647336"
---
# <a name="createresourcepool-method-of-the-cim_resourcepoolconfigurationservice-class"></a>Método CreateResourcePool da \_ classe RESOURCEPOOLCONFIGURATIONSERVICE CIM

Inicia um trabalho para criar um ResourcePool raiz. O ResourcePool será definido como escopo para o mesmo sistema que esse serviço.

## <a name="syntax"></a>Sintaxe


```mof
uint32 CreateResourcePool(
  [in]  string                ElementName,
  [in]  CIM_LogicalDevice REF HostResources[],
  [in]  string                ResourceType,
  [out] CIM_ResourcePool  REF Pool,
  [out] CIM_ConcreteJob   REF Job
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ElementName* \[ no\]
</dt> <dd>

Um nome relevante do usuário final para o pool que está sendo criado. Se for **NULL**, um nome padrão fornecido pelo sistema poderá ser usado. O valor será armazenado na propriedade **ElementName** do pool criado.

</dd> <dt>

*Recursos* \[ no\]
</dt> <dd>

Matriz de zero ou mais dispositivos [**CIM \_ LogicalDevice**](cim-logicaldevice.md) que são usados para criar o pool ou modificar as extensões de origem. Todos os elementos na matriz devem ser do mesmo tipo.

</dd> <dt>

*ResourceType* \[ no\]
</dt> <dd>

O tipo de recursos que o pool criado irá gerenciar. Se *recursos* contiver elementos, essa propriedade deverá Mach seu tipo.

</dd> <dt>

*Pool* \[ de fora\]
</dt> <dd>

Em caso de sucesso, retorna uma referência para [**o \_ ResourcePool CIM**](cim-resourcepool.md)resultante. Quando um trabalho é retornado, isso pode ser **nulo**; nesse caso, o cliente deve usar o trabalho para localizar o ResourcePool resultante quando o trabalho for concluído.

</dd> <dt>

*Trabalho* \[ do fora\]
</dt> <dd>

Referência a um [**\_ ConcreteJob CIM**](cim-concretejob.md) que representa o trabalho (pode ser NULL se o trabalho for concluído).

</dd> </dl>

## <a name="return-value"></a>Retornar valor

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

 

 




