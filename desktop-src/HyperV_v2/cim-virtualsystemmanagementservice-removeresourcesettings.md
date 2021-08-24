---
description: Método RemoveResourceSettings da classe CIM_VirtualSystemManagementService - remove as configurações de recurso virtual de uma configuração do sistema virtual.
ms.assetid: 7934a5e4-f54c-43fd-9ec3-d1fc1aad0acd
title: Método RemoveResourceSettings da classe CIM_VirtualSystemManagementService dados
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VirtualSystemManagementService.RemoveResourceSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 4a3b94ff6ecd42ea362cc5caec91bdbd6c7f484acc687dc52d22acf4c1047f09
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119682709"
---
# <a name="removeresourcesettings-method-of-the-cim_virtualsystemmanagementservice-class"></a>Método RemoveResourceSettings da classe CIM \_ VirtualSystemManagementService

Remove as configurações de recurso virtual de uma configuração do sistema virtual.

Quando aplicado a partes de uma configuração de sistema virtual "atual", como um efeito colateral, os recursos do sistema virtual ativo podem ser removidos.

## <a name="syntax"></a>Sintaxe


```mof
uint32 RemoveResourceSettings(
  [in]  CIM_ResourceAllocationSettingData REF ResourceSettings[],
  [out] CIM_ConcreteJob                   REF Job
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*ResourceSettings* \[ Em\]
</dt> <dd>

Matriz de referências a instâncias da classe [**CIM \_ ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md) em que cada instância representa as configurações de um recurso virtual em uma configuração do sistema virtual que deve ser removida.

</dd> <dt>

*Trabalho* \[ out\]
</dt> <dd>

Se a operação for de execução longa, opcionalmente, [**um \_ ConcreteJob CIM**](cim-concretejob.md) que representa o trabalho poderá ser retornado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Retorna um 0 em caso de êxito; caso contrário, retornará um erro.

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
| Cliente mínimo com suporte<br/> | Windows 8.1<br/>                                                                                  |
| Servidor mínimo com suporte<br/> | Windows Server 2012 R2<br/>                                                                       |
| Namespace<br/>                | Virtualização \\ raiz \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**CIM \_ VirtualSystemManagementService**](cim-virtualsystemmanagementservice.md)
</dt> </dl>

 

 




