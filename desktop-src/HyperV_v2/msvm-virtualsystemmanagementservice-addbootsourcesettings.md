---
description: Adiciona fontes de inicialização a uma configuração de sistema virtual quando aplicada a um &\# 0034; state&\# 0034; configuração do sistema virtual.
ms.assetid: 2d091554-73d4-47c6-a0c2-97644fc9abe9
title: Método AddBootSourceSettings da classe Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.AddBootSourceSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: d52333f3118caa1cf437fabb536bb62f84b99dab01b3115e7f6a65c3f182a17e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119148069"
---
# <a name="addbootsourcesettings-method-of-the-msvm_virtualsystemmanagementservice-class"></a>Método AddBootSourceSettings da \_ classe VirtualSystemManagementService Msvm

Adiciona fontes de inicialização a uma configuração de sistema virtual quando aplicada a uma configuração de sistema virtual "State".

## <a name="syntax"></a>Sintaxe


```mof
uint32 AddBootSourceSettings(
  [in]  CIM_VirtualSystemSettingData REF AffectedConfiguration,
  [in]  string                           BootSourceSettings[],
  [out] CIM_SettingData              REF ResultingBootSourceSettings[],
  [out] CIM_ConcreteJob              REF Job
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*AffectedConfiguration* \[ no\]
</dt> <dd>

Um [**\_ VirtualSystemSettingData CIM**](cim-virtualsystemsettingdata.md) que contém a configuração afetada.

</dd> <dt>

*BootSourceSettings* \[ no\]
</dt> <dd>

Uma matriz que contém as configurações de origem da inicialização.

</dd> <dt>

*ResultingBootSourceSettings* \[ fora\]
</dt> <dd>

Em caso de sucesso, retorna um [**CIM \_ SettingData**](cim-settingdata.md) com as configurações de origem de inicialização resultantes.

</dd> <dt>

*Trabalho* \[ do fora\]
</dt> <dd>

Se a operação for executada de forma assíncrona, esse método retornará 4096, e esse parâmetro conterá uma referência a um objeto derivado de [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).

</dd> </dl>

## <a name="return-value"></a>Valor retornado

Em caso de sucesso, retorna 0 ou 4096; caso contrário, retornará um erro.

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
| Cliente mínimo com suporte<br/> | Windows 10 \[ somente aplicativos da área de trabalho\]<br/>                                                             |
| Servidor mínimo com suporte<br/> | Windows Server 2016<br/>                                                                          |
| Namespace<br/>                | \\Virtualização \\ v2 de raiz<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

