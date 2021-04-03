---
description: Altera as configurações de recurso de pool pai para recursos atribuídos a um pool filho.
ms.assetid: 419fca70-5f15-4593-80ac-ef2af2c3dde5
title: Método ModifyPoolResources da classe Msvm_ResourcePoolConfigurationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ResourcePoolConfigurationService.ModifyPoolResources
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 2efffdbcc34577f675556874c4153eea2670768c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829365"
---
# <a name="modifypoolresources-method-of-the-msvm_resourcepoolconfigurationservice-class"></a>Método ModifyPoolResources da \_ classe ResourcePoolConfigurationService Msvm

Altera as configurações de recurso de pool pai para recursos atribuídos a um pool filho.

## <a name="syntax"></a>Sintaxe


```mof
uint32 ModifyPoolResources(
  [in]  CIM_ResourcePool REF ChildPool,
  [in]  CIM_ResourcePool REF ParentPools[],
  [in]  string               AllocationSettings[],
  [out] CIM_ConcreteJob  REF Job
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ChildPool* \[ no\]
</dt> <dd>

Uma referência a uma instância da classe [**CIM \_ ResourcePool**](cim-resourcepool.md) que representa o pool filho a ser modificado.

</dd> <dt>

*ParentPools* \[ no\]
</dt> <dd>

Uma matriz de referências do [**CIM \_ ResourcePool**](cim-resourcepool.md) que representam os novos pools pai a serem atribuídos ao pool filho.

</dd> <dt>

*AllocationSettings* \[ no\]
</dt> <dd>

Uma matriz opcional de uma ou mais instâncias inseridas da classe [**Msvm \_ ResourceAllocationSettingData**](msvm-resourceallocationsettingdata.md) que são usadas para especificar as configurações relacionadas à alocação de pool.

</dd> <dt>

*Trabalho* \[ do fora\]
</dt> <dd>

Se a operação for executada de forma assíncrona, esse método retornará 4096, e esse parâmetro conterá uma referência a um objeto derivado de [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método retorna um dos valores a seguir.

<dl> <dt>

**Trabalho concluído sem erro** (0)
</dt> <dt>

**DMTF reservado** (..)
</dt> <dt>

**Parâmetros de método marcados-trabalho iniciado** (4096)
</dt> <dt>

**Método reservado** (4097.. 32767)
</dt> <dt>

**Falha** (32768)
</dt> <dt>

**Acesso negado** (32769)
</dt> <dt>

**Sem suporte** (32770)
</dt> <dt>

**Desconhecido** (32771)
</dt> <dt>

**Tempo limite** (32772)
</dt> <dt>

**Parâmetro inválido** (32773)
</dt> <dt>

**Em uso** (32774)
</dt> <dt>

**Estado inválido** (32775)
</dt> <dt>

**Tipo de recurso incorreto para o pool** (32776)
</dt> <dt>

**Não disponível** (32777)
</dt> <dt>

**Memória insuficiente** (32778)
</dt> <dt>

**Fornecedor reservado** (32779)
</dt> <dt>

**Recursos insuficientes** (32780)
</dt> <dt>

**Objeto não encontrado** (32781.. 32787)
</dt> <dt>

O **objeto existe** (32788)
</dt> <dt>

**Específico do fornecedor** (32768.. 65535)
</dt> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 8\]<br/>                                                              |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2012\]<br/>                                                    |
| Namespace<br/>                | \\Virtualização \\ v2 de raiz<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Msvm \_ ResourcePoolConfigurationService**](msvm-resourcepoolconfigurationservice.md)
</dt> </dl>

 

