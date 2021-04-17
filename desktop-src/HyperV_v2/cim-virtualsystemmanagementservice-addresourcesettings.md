---
description: Adiciona recursos a uma configuração de sistema virtual.
ms.assetid: c2541571-74f0-48f8-997c-56c152980eea
title: Método AddResourceSettings da classe CIM_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VirtualSystemManagementService.AddResourceSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 9563b1e8421dfa6724971450b117780435f6f39e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105789807"
---
# <a name="addresourcesettings-method-of-the-cim_virtualsystemmanagementservice-class"></a>Método AddResourceSettings da \_ classe VIRTUALSYSTEMMANAGEMENTSERVICE CIM

Adiciona recursos a uma configuração de sistema virtual.

Quando aplicado a uma configuração de sistema virtual "State", como os recursos de efeito colateral são adicionados ao sistema virtual ativo.

## <a name="syntax"></a>Sintaxe


```mof
uint32 AddResourceSettings(
  [in]  CIM_VirtualSystemSettingData      REF AffectedConfiguration,
  [in]  string                                ResourceSettings[],
  [out] CIM_ResourceAllocationSettingData REF ResultingResourceSettings[],
  [out] CIM_ConcreteJob                   REF Job
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*AffectedConfiguration* \[ no\]
</dt> <dd>

Uma referência do [**CIM \_ VirtualSystemSettingData**](cim-virtualsystemsettingdata.md) à configuração do sistema virtual afetada.

</dd> <dt>

*ResourceSettings* \[ no\]
</dt> <dd>

Matriz de cadeias de caracteres que contém uma instância inserida da classe [**CIM \_ ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md) que descreve os aspectos virtuais de um recurso virtual a ser adicionado ao sistema virtual.

</dd> <dt>

*ResultingResourceSettings* \[ fora\]
</dt> <dd>

Matriz de referências a instâncias da classe [**CIM \_ ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md) que representa aspectos virtuais dos recursos virtuais adicionados.

</dd> <dt>

*Trabalho* \[ do fora\]
</dt> <dd>

Se a operação for de longa execução, opcionalmente, um trabalho poderá ser retornado. Nesse caso, as instâncias da classe [**CIM \_ ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md) que representa as configurações de recurso adicionadas estão disponíveis por meio da **\_ ConreteComponent de CIM** de associação da instância da classe [**CIM \_ VirtualSystemSettingData**](cim-virtualsystemsettingdata.md) que representa a configuração do sistema virtual afetado.

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Retorna um 0 em caso de êxito; caso contrário, retornará um erro.

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

[**\_VIRTUALSYSTEMMANAGEMENTSERVICE CIM**](cim-virtualsystemmanagementservice.md)
</dt> </dl>

 

 




