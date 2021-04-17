---
description: Descreve os recursos do VirtualEthernetSwitchManagementService Msvm associado \_ .
ms.assetid: daed7a02-bae8-4bda-abc6-0657df7dc4f8
title: Classe Msvm_VirtualEthernetSwitchManagementCapabilities
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualEthernetSwitchManagementCapabilities
- Msvm_VirtualEthernetSwitchManagementCapabilities.InstanceID
- Msvm_VirtualEthernetSwitchManagementCapabilities.Caption
- Msvm_VirtualEthernetSwitchManagementCapabilities.Description
- Msvm_VirtualEthernetSwitchManagementCapabilities.ElementName
- Msvm_VirtualEthernetSwitchManagementCapabilities.ElementNameEditSupported
- Msvm_VirtualEthernetSwitchManagementCapabilities.MaxElementNameLen
- Msvm_VirtualEthernetSwitchManagementCapabilities.RequestedStatesSupported
- Msvm_VirtualEthernetSwitchManagementCapabilities.ElementNameMask
- Msvm_VirtualEthernetSwitchManagementCapabilities.VirtualSystemTypesSupported
- Msvm_VirtualEthernetSwitchManagementCapabilities.SynchronousMethodsSupported
- Msvm_VirtualEthernetSwitchManagementCapabilities.AsynchronousMethodsSupported
- Msvm_VirtualEthernetSwitchManagementCapabilities.IndicationsSupported
- Msvm_VirtualEthernetSwitchManagementCapabilities.IOVSupport
- Msvm_VirtualEthernetSwitchManagementCapabilities.IOVSupportReasons
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: d66d73773b956ecbbbf4ca102b18bb6f8ece4190
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105752873"
---
# <a name="msvm_virtualethernetswitchmanagementcapabilities-class"></a>\_Classe Msvm VirtualEthernetSwitchManagementCapabilities

Descreve os recursos do [**\_ VirtualEthernetSwitchManagementService Msvm**](msvm-virtualethernetswitchmanagementservice.md)associado.

A sintaxe a seguir é simplificada formato MOF código (MOF) e inclui todas as propriedades herdadas.

## <a name="syntax"></a>Sintaxe

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualEthernetSwitchManagementCapabilities : CIM_VirtualSystemManagementCapabilities
{
  string  InstanceID;
  string  Caption = "Hyper-V Virtual Ethernet Switch Management Service Capabilities";
  string  Description = "Defines Virtual Ethernet Switch Management Service Capabilities";
  string  ElementName = "Hyper-V Virtual Ethernet Switch Management Service Capabilities";
  boolean ElementNameEditSupported;
  unit16  MaxElementNameLen;
  unit16  RequestedStatesSupported[];
  string  ElementNameMask;
  string  VirtualSystemTypesSupported[];
  uint16  SynchronousMethodsSupported[];
  uint16  AsynchronousMethodsSupported[];
  uint16  IndicationsSupported[];
  boolean IOVSupport;
  string  IOVSupportReasons[];
};
```

## <a name="members"></a>Membros

A classe **Msvm \_ VirtualEthernetSwitchManagementCapabilities** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **Msvm \_ VirtualEthernetSwitchManagementCapabilities** tem essas propriedades.

<dl> <dt>

**AsynchronousMethodsSupported**
</dt> <dd> <dl> <dt>

Tipo de dados: a matriz **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ VirtualSystemManagementCapabilities. AsynchronousMethodsSupported")
</dt> </dl>

Uma matriz de identificadores de método, cada um identificando um método da classe [**Msvm \_ VirtualEthernetSwitchManagementService**](msvm-virtualethernetswitchmanagementservice.md) que tem suporte de forma assíncrona pela implementação. Essa propriedade é herdada do **CIM \_ VirtualSystemManagementCapabilities**.

<dt>

<span id="DefineSystem"></span><span id="definesystem"></span><span id="DEFINESYSTEM"></span>

**DefineSystem** (2)


</dt> <dd></dd> <dt>

<span id="DestroySystem"></span><span id="destroysystem"></span><span id="DESTROYSYSTEM"></span>

**DestroySystem** (3)


</dt> <dd></dd> <dt>

<span id="DestroySystemConfiguration"></span><span id="destroysystemconfiguration"></span><span id="DESTROYSYSTEMCONFIGURATION"></span>

**DestroySystemConfiguration** (4)


</dt> <dd></dd> <dt>

<span id="ModifyResourceSettings"></span><span id="modifyresourcesettings"></span><span id="MODIFYRESOURCESETTINGS"></span>

**ModifyResourceSettings** (5)


</dt> <dd></dd> <dt>

<span id="ModifySystemSettings"></span><span id="modifysystemsettings"></span><span id="MODIFYSYSTEMSETTINGS"></span>

**ModifySystemSettings** (6)


</dt> <dd></dd> <dt>

<span id="RemoveResources"></span><span id="removeresources"></span><span id="REMOVERESOURCES"></span>

**RemoveResources** (7)


</dt> <dd></dd> <dt>

<span id="SelectSystemConfiguration"></span><span id="selectsystemconfiguration"></span><span id="SELECTSYSTEMCONFIGURATION"></span>

**SelectSystemConfiguration** (8)


</dt> <dd></dd> <dt>

<span id="SnapshotSystem"></span><span id="snapshotsystem"></span><span id="SNAPSHOTSYSTEM"></span>

**SnapshotSystem** (9)


</dt> <dd></dd> <dt>

<span id="AddResources"></span><span id="addresources"></span><span id="ADDRESOURCES"></span>

**Resources** (10)


</dt> <dd></dd> <dt>

<span id="AddFeatureSettingsSupported"></span><span id="addfeaturesettingssupported"></span><span id="ADDFEATURESETTINGSSUPPORTED"></span>

**AddFeatureSettingsSupported** (32779)


</dt> <dd></dd> <dt>

<span id="ModifyFeatureSettingsSupported"></span><span id="modifyfeaturesettingssupported"></span><span id="MODIFYFEATURESETTINGSSUPPORTED"></span>

**ModifyFeatureSettingsSupported** (32780)


</dt> <dd></dd> <dt>

<span id="RemoveFeatureSettingsSupported"></span><span id="removefeaturesettingssupported"></span><span id="REMOVEFEATURESETTINGSSUPPORTED"></span>

**RemoveFeatureSettingsSupported** (32781)


</dt> <dd></dd> <dt>

<span id="AddFeatureSettingsSupported"></span><span id="addfeaturesettingssupported"></span><span id="ADDFEATURESETTINGSSUPPORTED"></span>

**AddFeatureSettingsSupported** (32779)


</dt> <dd></dd> <dt>

<span id="ModifyFeatureSettingsSupported"></span><span id="modifyfeaturesettingssupported"></span><span id="MODIFYFEATURESETTINGSSUPPORTED"></span>

**ModifyFeatureSettingsSupported** (32780)


</dt> <dd></dd> <dt>

<span id="RemoveFeatureSettingsSupported"></span><span id="removefeaturesettingssupported"></span><span id="REMOVEFEATURESETTINGSSUPPORTED"></span>

**RemoveFeatureSettingsSupported** (32781)


</dt> <dd></dd> </dl>

</dd> <dt>

**Legenda**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Uma breve descrição do objeto. Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)e é sempre definida como "recursos do serviço de gerenciamento do comutador Ethernet virtual do Hyper-V".

</dd> <dt>

**Descrição**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Uma descrição do objeto . Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)e é sempre definida como "define os recursos do serviço de gerenciamento do comutador Ethernet virtual".

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Um nome de exibição para o objeto. Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)e é sempre definida como "recursos do serviço de gerenciamento do comutador Ethernet virtual do Hyper-V".

</dd> <dt>

**ElementNameEditSupported**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Indica se a propriedade **ElementName** pode ser modificada. Essa propriedade é herdada do **CIM \_ EnabledLogicalElementCapabilities**.

</dd> <dt>

**ElementNameMask**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Especifica as restrições em **ElementName**, expressas como uma expressão regular. Essa propriedade é herdada do **CIM \_ EnabledLogicalElementCapabilities**.

</dd> <dt>

**IndicationsSupported**
</dt> <dd> <dl> <dt>

Tipo de dados: a matriz **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Uma matriz de identificadores de indicação, cada um identificando uma indicação com suporte na implementação. Essa propriedade é herdada do **CIM \_ VirtualSystemManagementCapabilities**.



| Valor                                                                                                                                                                                                                                                                                                                                                                                   | Significado                                                                                                                                                                                               |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="VirtualResourceStateChangeIndicationsSupported"></span><span id="virtualresourcestatechangeindicationssupported"></span><span id="VIRTUALRESOURCESTATECHANGEINDICATIONSSUPPORTED"></span><dl> <dt>**VirtualResourceStateChangeIndicationsSupported**</dt> <dt>2</dt> </dl> | Indica se a implementação dá suporte a notificações em alterações de estado de instâncias de [**\_ LogicalDevice CIM**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) que representam recursos de sistemas virtuais.<br/> |
| <span id="ConcreteJobStateChangeIndicationsSupported"></span><span id="concretejobstatechangeindicationssupported"></span><span id="CONCRETEJOBSTATECHANGEINDICATIONSSUPPORTED"></span><dl> <dt>**ConcreteJobStateChangeIndicationsSupported**</dt> <dt>3</dt> </dl>                 | Indica se a implementação dá suporte a notificações em alterações de estado de instâncias de [**\_ ConcreteJob CIM**](/previous-versions//cc136808(v=vs.85)) .<br/>                                                      |
| <span id="VirtualSystemStateChangeIndicationsSupported"></span><span id="virtualsystemstatechangeindicationssupported"></span><span id="VIRTUALSYSTEMSTATECHANGEINDICATIONSSUPPORTED"></span><dl> <dt>**VirtualSystemStateChangeIndicationsSupported**</dt> <dt>4</dt> </dl>         | Indica se a implementação dá suporte a notificações em alterações de estado de instâncias de [**\_ sistema CIM**](/windows/desktop/CIMWin32Prov/cim-computersystem) que representam sistemas virtuais.<br/>            |
| <span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span><dl> <dt>**DMTF reservado**</dt> <dt>..</dt> </dl>                                                                                                                                    |                                                                                                                                                                                                       |
| <span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span><dl> O <dt> **fornecedor reservou**</dt> <dt>32767.. 65535</dt> </dl>                                                                                                             |                                                                                                                                                                                                       |



 

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **chave**
</dt> </dl>

Identifica exclusivamente uma instância dessa classe. Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).

</dd> <dt>

**IOVSupport**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Um valor booliano que indica se o IOV (virtualização de e/s) é suportado pela plataforma. Se o valor for **true**, o IOV terá suporte da plataforma e **IOVSupportReasons** estará vazio. Caso contrário, a propriedade **IOVSupportReasons** terá os motivos pelos quais a IOV não tem suporte.

</dd> <dt>

**IOVSupportReasons**
</dt> <dd> <dl> <dt>

Tipo de dados: matriz de **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Uma matriz de cadeias de caracteres que indica as possíveis razões pelas quais a IOV não tem suporte. Se o valor de **IOVSupport** for **true**, essa matriz estará vazia.

</dd> <dt>

**MaxElementNameLen**
</dt> <dd> <dl> <dt>

Tipo de dados: **unit16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **MaxValue** (256)
</dt> </dl>

Especifica o comprimento máximo com suporte da propriedade **ElementName** . Essa propriedade é herdada do **CIM \_ EnabledLogicalElementCapabilities**.

</dd> <dt>

**RequestedStatesSupported**
</dt> <dd> <dl> <dt>

Tipo de dados: matriz **unit16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Indica os possíveis Estados que podem ser solicitados ao usar o método **RequestStateChange** no elemento lógico habilitado. Essa propriedade é herdada do **CIM \_ EnabledLogicalElementCapabilities** e é sempre **nula**.

</dd> <dt>

**SynchronousMethodsSupported**
</dt> <dd> <dl> <dt>

Tipo de dados: a matriz **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Uma matriz de identificadores de método, cada um identificando um método da classe [**Msvm \_ VirtualEthernetSwitchManagementService**](msvm-virtualethernetswitchmanagementservice.md) que tem suporte de forma síncrona pela implementação. Essa propriedade é herdada do **CIM \_ VirtualSystemManagementCapabilities**.

<dl> <dt>

<span id="DefineSystem"></span><span id="definesystem"></span><span id="DEFINESYSTEM"></span>**DefineSystem** (2)
</dt> <dt>

<span id="DestroySystem"></span><span id="destroysystem"></span><span id="DESTROYSYSTEM"></span>**DestroySystem** (3)
</dt> <dt>

<span id="DestroySystemConfiguration"></span><span id="destroysystemconfiguration"></span><span id="DESTROYSYSTEMCONFIGURATION"></span>**DestroySystemConfiguration** (4)
</dt> <dt>

<span id="ModifyResourceSettings"></span><span id="modifyresourcesettings"></span><span id="MODIFYRESOURCESETTINGS"></span>**ModifyResourceSettings** (5)
</dt> <dt>

<span id="ModifySystemSettings"></span><span id="modifysystemsettings"></span><span id="MODIFYSYSTEMSETTINGS"></span>**ModifySystemSettings** (6)
</dt> <dt>

<span id="RemoveResources"></span><span id="removeresources"></span><span id="REMOVERESOURCES"></span>**RemoveResources** (7)
</dt> <dt>

<span id="SelectSystemConfiguration"></span><span id="selectsystemconfiguration"></span><span id="SELECTSYSTEMCONFIGURATION"></span>**SelectSystemConfiguration** (8)
</dt> <dt>

<span id="SnapshotSystem"></span><span id="snapshotsystem"></span><span id="SNAPSHOTSYSTEM"></span>**SnapshotSystem** (9)
</dt> <dt>

<span id="AddResources"></span><span id="addresources"></span><span id="ADDRESOURCES"></span>**Resources** (10)
</dt> <dt>

<span id="AddFeatureSettings"></span><span id="addfeaturesettings"></span><span id="ADDFEATURESETTINGS"></span>**AddFeatureSettings** (32779)
</dt> <dt>

<span id="ModifyFeatureSettings"></span><span id="modifyfeaturesettings"></span><span id="MODIFYFEATURESETTINGS"></span>**ModifyFeatureSettings** (32780)
</dt> <dt>

<span id="RemoveFeatureSettings"></span><span id="removefeaturesettings"></span><span id="REMOVEFEATURESETTINGS"></span>**RemoveFeatureSettings** (32781)
</dt> </dl>

</dd> <dt>

**VirtualSystemTypesSupported**
</dt> <dd> <dl> <dt>

Tipo de dados: matriz de **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Uma matriz de cadeias de caracteres, cada uma designando um tipo de sistema virtual compatível com a implementação. O valor de cada elemento de matriz não **NULL** deve estar de acordo com o formato definido para a propriedade **VirtualSystemType** da classe [**Msvm \_ VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) . Essa propriedade é herdada do **CIM \_ VirtualSystemManagementCapabilities**.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 8\]<br/>                                                              |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2012\]<br/>                                                    |
| Namespace<br/>                | \\Virtualização \\ v2 de raiz<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

