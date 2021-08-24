---
description: Adiciona configurações genéricas a uma configuração do sistema virtual.
ms.assetid: ae04be39-0401-43e9-b19b-3539ca1786ec
title: Método AddSystemComponentSettings da classe Msvm_VirtualSystemManagementService dados
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.AddSystemComponentSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 43bc224a0ab81732c24c581bbb0142d2121c93f0dbe5f6b80da0efb02227340a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119789186"
---
# <a name="addsystemcomponentsettings-method-of-the-msvm_virtualsystemmanagementservice-class"></a>Método AddSystemComponentSettings da classe Msvm \_ VirtualSystemManagementService

Adiciona configurações genéricas a uma configuração do sistema virtual.

## <a name="syntax"></a>Sintaxe


```mof
uint32 AddSystemComponentSettings(
  [in]  Msvm_VirtualSystemSettingData   REF AffectedConfiguration,
  [in]  string                              ComponentSettings[],
  [out] Msvm_SystemComponentSettingData REF ResultingComponentSettings[],
  [out] CIM_ConcreteJob                 REF Job
);
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*AffectedConfiguration* \[ Em\]
</dt> <dd></dd> <dt>

*ComponentSettings* \[ Em\]
</dt> <dd>

As configurações do componente a adicionar.

</dd> <dt>

*ResultingComponentSettings* \[ out\]
</dt> <dd>

Em caso de sucesso, faz referência a [**um \_ SystemComponentSettingData da Msvm**](msvm-systemcomponentsettingdata.md) que contém as configurações de componente resultantes.

</dd> <dt>

*Trabalho* \[ out\]
</dt> <dd>

Se a operação for executada de forma assíncrona, esse método retornará 4096 e esse parâmetro conterá uma referência a um objeto derivado de [**CIM \_ ConcreteJob.**](/previous-versions//cc136808(v=vs.85))

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
| Cliente mínimo com suporte<br/> | Windows 10, versão 1703 somente \[ para aplicativos da área de trabalho\]<br/>                                               |
| Servidor mínimo com suporte<br/> | Windows Server 2016<br/>                                                                          |
| Namespace<br/>                | Virtualização \\ raiz \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

