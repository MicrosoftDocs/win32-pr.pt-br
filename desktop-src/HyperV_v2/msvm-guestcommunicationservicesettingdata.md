---
description: Representa as configurações do serviço de comunicação de convidado.
ms.assetid: c36d3002-d43e-4284-b765-2795c941f023
title: Classe Msvm_GuestCommunicationServiceSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_GuestCommunicationServiceSettingData
- Msvm_GuestCommunicationServiceSettingData.Name
- Msvm_GuestCommunicationServiceSettingData.EnabledStatePolicy
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 67026a1dd7e605effb923305c45d329e7a2a502fe0324f00d2ddcf346c899778
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118148045"
---
# <a name="msvm_guestcommunicationservicesettingdata-class"></a>\_Classe Msvm GuestCommunicationServiceSettingData

Representa as configurações do serviço de comunicação de convidado.

A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.

## <a name="syntax"></a>Sintaxe

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_GuestCommunicationServiceSettingData : CIM_SettingData
{
  string Name;
  uint16 EnabledStatePolicy;
};
```

## <a name="members"></a>Membros

A classe **Msvm \_ GuestCommunicationServiceSettingData** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **Msvm \_ GuestCommunicationServiceSettingData** tem essas propriedades.

<dl> <dt>

**EnabledStatePolicy**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: leitura/gravação
</dt> </dl>

EnabledStatePolicy é uma enumeração de inteiro que indica o estado habilitado, desabilitado ou padrão do **Msvm \_ GuestCommunicationServiceSettingData**.

<dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Habilitado** (2)


</dt> <dd>

O serviço de comunicação é definido como o estado habilitado.

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Desabilitado** (3)


</dt> <dd>

O serviço de comunicação é definido como o estado desabilitado.

</dd> <dt>

<span id="Deferred"></span><span id="deferred"></span><span id="DEFERRED"></span>

<span id="Deferred"></span><span id="deferred"></span><span id="DEFERRED"></span>**Adiado** (8)


</dt> <dd>

O estado do serviço de comunicação depende de **DefaultEnabledStatePolicy** em **Msvm \_ GuestCommunicationServiceSettingData**.

</dd> </dl>

</dd> <dt>

**Nome**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

O GUID do serviço.

</dd> </dl>

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

[**CIM \_ SettingData**](cim-settingdata.md)
</dt> </dl>

 

 




