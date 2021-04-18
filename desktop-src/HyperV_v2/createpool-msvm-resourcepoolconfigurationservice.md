---
description: Cria um pool de recursos filho.
ms.assetid: 30a70231-f1b7-4f0e-ac47-cf5a79ddb8ab
title: Método createpool da classe Msvm_ResourcePoolConfigurationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ResourcePoolConfigurationService.CreatePool
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: fb29a4b5a47d88232a6b0df6a828d482030b3f1a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105778596"
---
# <a name="createpool-method-of-the-msvm_resourcepoolconfigurationservice-class"></a>Método createpool da classe Msvm \_ ResourcePoolConfigurationService

Cria um pool de recursos filho. O pool de recursos será definido como escopo para o mesmo sistema que esse serviço. O pool resultante será um pool filho.

## <a name="syntax"></a>Sintaxe


```mof
uint32 CreatePool(
  [in]  string               PoolSettings,
  [in]  CIM_ResourcePool REF ParentPools[],
  [in]  string               AllocationSettings[],
  [out] CIM_ResourcePool REF Pool,
  [out] CIM_ConcreteJob  REF Job
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*PoolSettings* \[ no\]
</dt> <dd>

Uma instância inserida da classe [**Msvm \_ ResourcePoolSettingData**](msvm-resourcepoolsettingdata.md) que é usada para especificar as configurações de pool que não estão relacionadas à alocação.

</dd> <dt>

*ParentPools* \[ no\]
</dt> <dd>

Uma matriz de referências de [**Msvm \_ ResourcePool**](msvm-resourcepool.md) que representam o pool ou pools dos quais criar o novo pool.

</dd> <dt>

*AllocationSettings* \[ no\]
</dt> <dd>

Uma matriz de uma ou mais instâncias inseridas da classe [**Msvm \_ ResourceAllocationSettingData**](msvm-resourceallocationsettingdata.md) que são usadas para especificar as configurações relacionadas à alocação de pool. Essa matriz deve conter um elemento para cada elemento na matriz *ParentPools* ou exatamente um elemento. Se essa matriz contiver um elemento e *ParentPools* contiver mais de um elemento, *AlllocationSettings* especificará uma alocação de capacidade compartilhada que pode ser satisfeita por qualquer um dos pools pai.

Isso é usado para restringir os recursos que podem ser alocados do filho para o pool a um limite inferior à capacidade agregada fornecida por seus pais. Não há suporte para essa opção em todos os tipos de recurso. Se um tipo de recurso não for compatível com a alocação de capacidade compartilhada, esse método retornará 32770 (sem suporte).

</dd> <dt>

*Pool* \[ de fora\]
</dt> <dd>

Uma referência ao pool resultante.

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

 

