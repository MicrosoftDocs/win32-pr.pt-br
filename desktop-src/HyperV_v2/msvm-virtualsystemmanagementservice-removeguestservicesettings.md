---
description: Remove as configurações de serviço de convidado de uma configuração de sistema virtual.
ms.assetid: 33e55d74-adfd-4174-8f05-14e797a33806
title: Método RemoveGuestServiceSettings da classe Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.RemoveGuestServiceSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 0aee1f8f9d729c093bff2a580e054d93fa7fc033
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105782349"
---
# <a name="removeguestservicesettings-method-of-the-msvm_virtualsystemmanagementservice-class"></a>Método RemoveGuestServiceSettings da \_ classe VirtualSystemManagementService Msvm

Remove as configurações de serviço de convidado de uma configuração de sistema virtual.

Quando aplicado a partes de uma configuração de sistema virtual "atual", como um efeito colateral, os serviços convidados do sistema virtual ativo podem ser modificados.

## <a name="syntax"></a>Sintaxe


```mof
uint32 RemoveGuestServiceSettings(
  [in]  CIM_SettingData REF GuestServiceSettings[],
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*GuestServiceSettings* \[ no\]
</dt> <dd>

Referência a uma matriz de [**CIM \_ SettingData**](cim-settingdata.md) que descreve a configuração do serviço de convidado a ser removida.

</dd> <dt>

*Trabalho* \[ do fora\]
</dt> <dd>

Se a operação for executada de forma assíncrona, esse método retornará 4096, e esse parâmetro conterá uma referência a um objeto derivado de [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).

</dd> </dl>

## <a name="return-value"></a>Retornar valor

Esse método retorna um dos seguintes valores:

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

**Estado inválido** (5)
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
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows 10\]<br/>                                                             |
| Servidor mínimo com suporte<br/> | Windows Server 2016<br/>                                                                          |
| Namespace<br/>                | \\Virtualização \\ v2 de raiz<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

