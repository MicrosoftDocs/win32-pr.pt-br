---
description: Descreve dados de configurações para um comutador Ethernet virtual.
ms.assetid: 462cff06-5ba6-410a-b091-5c6abab13f03
title: Classe CIM_VirtualEthernetSwitchSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VirtualEthernetSwitchSettingData
- CIM_VirtualEthernetSwitchSettingData.VLANConnection
- CIM_VirtualEthernetSwitchSettingData.AssociatedResourcePool
- CIM_VirtualEthernetSwitchSettingData.MaxNumMACAddress
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 64d7053364aebe1fab5739cd75389b1a9343efe0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105769346"
---
# <a name="cim_virtualethernetswitchsettingdata-class"></a>\_Classe CIM VirtualEthernetSwitchSettingData

Descreve dados de configurações para um comutador Ethernet virtual.

## <a name="syntax"></a>Sintaxe

``` syntax
[Abstract, Version("2.26.0"), UMLPackagePath("CIM::Core::Virtualization"), AMENDMENT]
class CIM_VirtualEthernetSwitchSettingData : CIM_VirtualSystemSettingData
{
  string VLANConnection[];
  string AssociatedResourcePool[];
  uint32 MaxNumMACAddress;
};
```

## <a name="members"></a>Membros

A classe **CIM \_ VirtualEthernetSwitchSettingData** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **CIM \_ VirtualEthernetSwitchSettingData** tem essas propriedades.

<dl> <dt>

**AssociatedResourcePool**
</dt> <dd> <dl> <dt>

Tipo de dados: matriz de **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Uma matriz que contém os pools de recursos de host que estão associados atualmente ou para associar ao comutador Ethernet, a fim de alocar conexões Ethernet entre o comutador Ethernet e uma máquina virtual. Cada valor não nulo dessa propriedade deve estar de acordo com **o \_ \_ UntypedInstancePath do URI WBEM** , conforme definido na especificação "DSP0207" de DMTF.

</dd> <dt>

**MaxNumMACAddress**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

O número de endereços MAC exclusivos que o comutador pode aprender para o aprendizado de endereço MAC, conforme definido no padrão IEEE 802,1.

</dd> <dt>

**VLANConnection**
</dt> <dd> <dl> <dt>

Tipo de dados: matriz de **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Uma matriz que contém as IDs de VLAN que o comutador pode acessar.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8<br/>                                                                                    |
| Servidor mínimo com suporte<br/> | Windows Server 2012<br/>                                                                          |
| Namespace<br/>                | \\Virtualização \\ v2 de raiz<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_VIRTUALSYSTEMSETTINGDATA CIM**](cim-virtualsystemsettingdata.md)
</dt> </dl>

 

 




