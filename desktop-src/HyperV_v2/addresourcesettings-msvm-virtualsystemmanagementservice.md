---
description: Adiciona recursos a uma configuração de máquina virtual.
ms.assetid: e2878b60-dc8c-48fb-b163-29457a96d130
title: Método AddResourceSettings da classe Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.AddResourceSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 0092b19a0fa4bf41492c42db0b3346607bd3b587a2e57e789815424d94a89850
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119900466"
---
# <a name="addresourcesettings-method-of-the-msvm_virtualsystemmanagementservice-class"></a>Método AddResourceSettings da \_ classe VirtualSystemManagementService Msvm

Adiciona recursos a uma configuração de máquina virtual. Quando aplicado a uma configuração de máquina virtual de "estado", como um efeito colateral, os recursos são adicionados à máquina virtual ativa.

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

Uma referência a um objeto [**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)) que representa a configuração de máquina virtual afetada.

</dd> <dt>

*ResourceSettings* \[ no\]
</dt> <dd>

Uma matriz de cadeias de caracteres que contém uma instância inserida da classe [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) que descreve os aspectos virtuais de um recurso virtual a ser adicionado à máquina virtual.

</dd> <dt>

*ResultingResourceSettings* \[ fora\]
</dt> <dd>

Uma matriz de referências a instâncias da classe [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) que representa aspectos virtuais dos recursos virtuais adicionados.

</dd> <dt>

*Trabalho* \[ do fora\]
</dt> <dd>

Se a operação for executada de forma assíncrona, esse método retornará 4096, e esse parâmetro conterá uma referência a um objeto derivado de [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Esse método retorna um dos valores a seguir.

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
| Cliente mínimo com suporte<br/> | Windows 8 \[ somente aplicativos da área de trabalho\]<br/>                                                              |
| Servidor mínimo com suporte<br/> | Windows Server 2012 \[ somente aplicativos da área de trabalho\]<br/>                                                    |
| Namespace<br/>                | \\Virtualização \\ v2 de raiz<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

