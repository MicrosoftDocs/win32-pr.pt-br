---
description: Representa os dados de configuração de isolamento.
ms.assetid: f6bf5fcf-61c4-4e69-8ba0-fff4c4873368
title: Msvm_EthernetSwitchPortIsolationSettingData classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetSwitchPortIsolationSettingData
- Msvm_EthernetSwitchPortIsolationSettingData.IsolationMode
- Msvm_EthernetSwitchPortIsolationSettingData.AllowUntaggedTraffic
- Msvm_EthernetSwitchPortIsolationSettingData.DefaultIsolationId
- Msvm_EthernetSwitchPortIsolationSettingData.EnableMultiTenantStack
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 33ddf01fb7df5787fc35c073472987aa9a170e62086cd6c127f874cb2360b38d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119681526"
---
# <a name="msvm_ethernetswitchportisolationsettingdata-class"></a>Classe Msvm \_ EthernetSwitchPortIsolationSettingData

Representa os dados de configuração de isolamento.

A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.

## <a name="syntax"></a>Sintaxe

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), UUID("83AF2CCB-72C9-4479-A285-94E58A98CAA6"), ExtensionId("11EC6134-128A-4A23-B12F-164184B48348"), InterfaceVersion("1"), InterfaceRevision("0"), DisplayName("Ethernet Switch Port Isolation Settings"), AMENDMENT]
class Msvm_EthernetSwitchPortIsolationSettingData : Msvm_EthernetSwitchPortFeatureSettingData
{
  uint32  IsolationMode = 0;
  boolean AllowUntaggedTraffic = FALSE;
  uint32  DefaultIsolationId = 0;
  Boolean EnableMultiTenantStack = FALSE;
};
```

## <a name="members"></a>Membros

A **classe Msvm \_ EthernetSwitchPortIsolationSettingData** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A **classe Msvm \_ EthernetSwitchPortIsolationSettingData** tem essas propriedades.

<dl> <dt>

**AllowUntaggedTraffic**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliana**
</dt> <dt>

Tipo de acesso: Leitura/gravação
</dt> <dt>

Qualificadores: **WmiDataId** (2), [**Versão**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Revisão**](/windows/desktop/WmiSdk/standard-qualifiers) (0)
</dt> </dl>

Se a porta tem permissão para enviar/receber tráfego não marcado.

</dd> <dt>

**DefaultIsolationId**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Leitura/gravação
</dt> <dt>

Qualificadores: **WmiDataId** (3), [**Versão**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Revisão**](/windows/desktop/WmiSdk/standard-qualifiers) (0)
</dt> </dl>

O VirtualSubnetId padrão ou VLAN que será definido em todo o tráfego de envio/recebimento se **AllowedUntaggedTraffic** for **true.**

</dd> <dt>

**EnableMultiTenantStack**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliana**
</dt> <dt>

Tipo de acesso: Leitura/gravação
</dt> <dt>

Qualificadores: **WmiDataId** (4), [**Versão**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Revisão**](/windows/desktop/WmiSdk/standard-qualifiers) (0)
</dt> </dl>

Se **true**, a pilha de rede na VM poderá acessar a configuração de isolamento. O valor padrão é **false**.

</dd> <dt>

**IsolationMode**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint32**
</dt> <dt>

Tipo de acesso: Leitura/gravação
</dt> <dt>

Qualificadores: **WmiDataId** (1), [**Versão**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Revisão**](/windows/desktop/WmiSdk/standard-qualifiers) (0)
</dt> </dl>

Se a porta está usando **VLAN** ou **VirtualSubnetId** para isolamento. **NativeVirtualSubnetId** é usado para redes baseadas em WNV VirtualSubnetId.

<dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

**Nenhum** (0)


</dt> <dd></dd> <dt>

<span id="NativeVirtualSubnetId"></span><span id="nativevirtualsubnetid"></span><span id="NATIVEVIRTUALSUBNETID"></span>

**NativeVirtualSubnetId** (1)


</dt> <dd></dd> <dt>

<span id="ExternalVirtualSubnetId"></span><span id="externalvirtualsubnetid"></span><span id="EXTERNALVIRTUALSUBNETID"></span>

**ExternalVirtualSubnetId** (2)


</dt> <dd></dd> <dt>

<span id="VLAN"></span><span id="vlan"></span>

**VLAN** (3)


</dt> <dd></dd> </dl>

</dd> </dl>

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

[**Msvm \_ EthernetSwitchPortFeatureSettingData**](msvm-ethernetswitchportfeaturesettingdata.md)
</dt> </dl>

 

