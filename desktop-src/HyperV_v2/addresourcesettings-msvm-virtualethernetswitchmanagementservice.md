---
description: Adiciona recursos a uma configuração de com switch virtual.
ms.assetid: aad5fac1-3884-4a95-abe3-bf192f23ea41
title: Método AddResourceSettings da classe Msvm_VirtualEthernetSwitchManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualEthernetSwitchManagementService.AddResourceSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 2e13b9a9738b830f5b9dfcce5f37efa23c1014c735a5cb0a9cc0e09afa7b0038
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119914146"
---
# <a name="addresourcesettings-method-of-the-msvm_virtualethernetswitchmanagementservice-class"></a>Método AddResourceSettings da classe \_ Msvm VirtualEthernetSwitchManagementService

Adiciona recursos a uma configuração de com switch virtual. Quando aplicado a uma configuração de máquina virtual de "estado", como um efeito colateral, os recursos são adicionados à máquina virtual ativa.

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

*AffectedConfiguration* \[ Em\]
</dt> <dd>

Uma referência a um [**objeto CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)) que representa a configuração do com switch virtual afetado.

</dd> <dt>

*ResourceSettings* \[ Em\]
</dt> <dd>

Uma matriz de cadeias de caracteres que contém uma instância inserida da classe [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) que descreve os aspectos virtuais de um recurso virtual a ser adicionado ao computação virtual.

</dd> <dt>

*ResultingResourceSettings* \[ out\]
</dt> <dd>

Uma matriz de referências a instâncias da classe [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) que representa aspectos virtuais dos recursos virtuais adicionados.

</dd> <dt>

*Trabalho* \[ out\]
</dt> <dd>

Se a operação for executada de forma assíncrona, esse método retornará 4096 e esse parâmetro conterá uma referência a um objeto derivado de [**CIM \_ ConcreteJob.**](/previous-versions//cc136808(v=vs.85))

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

**Tempoout** (3)
</dt> <dt>

**Parâmetro inválido** (4)
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
| Cliente mínimo com suporte<br/> | \[Windows 8 somente aplicativos da área de trabalho\]<br/>                                                              |
| Servidor mínimo com suporte<br/> | \[Windows Server 2012 somente aplicativos da área de trabalho\]<br/>                                                    |
| Namespace<br/>                | Virtualização \\ raiz \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ModifyResourceSettings**](modifyresourcesettings-msvm-virtualethernetswitchmanagementservice.md)
</dt> <dt>

[**RemoveResourceSettings**](removeresourcesettings-msvm-virtualethernetswitchmanagementservice.md)
</dt> <dt>

[**Msvm \_ VirtualEthernetSwitchManagementService**](msvm-virtualethernetswitchmanagementservice.md)
</dt> </dl>

 

