---
description: Representa as configurações para a alocação da porta Ethernet, além das configurações fornecidas pela \_ classe CIM EthernetPort. Essas configurações são usadas para fornecer informações específicas ao próprio recurso.
ms.assetid: f59ebaf1-60dd-49bd-b48e-d7a6c2650909
title: Classe CIM_EthernetPortAllocationSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_EthernetPortAllocationSettingData
- CIM_EthernetPortAllocationSettingData.DesiredVLANEndpointMode
- CIM_EthernetPortAllocationSettingData.OtherEndpointMode
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 7e77b4387f77e88ceaff273b8be72a354c989e7e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105770227"
---
# <a name="cim_ethernetportallocationsettingdata-class"></a>\_Classe CIM EthernetPortAllocationSettingData

Representa as configurações para a alocação da porta Ethernet, além das configurações fornecidas pela classe [**CIM \_ EthernetPort**](cim-ethernetport.md) . Essas configurações são usadas para fornecer informações específicas ao próprio recurso.

## <a name="syntax"></a>Sintaxe

``` syntax
[Abstract, Version("2.26.0"), UMLPackagePath("CIM::Core::Resource"), AMENDMENT]
class CIM_EthernetPortAllocationSettingData : CIM_ResourceAllocationSettingData
{
  uint16 DesiredVLANEndpointMode;
  string OtherEndpointMode;
};
```

## <a name="members"></a>Membros

A classe **CIM \_ EthernetPortAllocationSettingData** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **CIM \_ EthernetPortAllocationSettingData** tem essas propriedades.

<dl> <dt>

**DesiredVLANEndpointMode**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ VLANEndpoint**](cim-vlanendpoint.md).**OperationalEndpointMode**","**CIM \_ VLANEndpoint**.**DesiredEndpointMode**","**CIM \_ EthernetPortAllocationSettingData**.**OtherEndpointMode**")
</dt> </dl>

O modo de VLAN solicitado. Essa propriedade é usada para definir o valor da propriedade **OperationalEndpointMode** inicial na instância do **CIM \_ VLANEndpoint** associada à porta Ethernet.

<dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

**DMTF reservado** (0)


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Outro** (1)


</dt> <dd></dd> <dt>

<span id="Access"></span><span id="access"></span><span id="ACCESS"></span>

**Acesso** (2)


</dt> <dd></dd> <dt>

<span id="Dynamic_Auto"></span><span id="dynamic_auto"></span><span id="DYNAMIC_AUTO"></span>

**Automático dinâmico** (3)


</dt> <dd></dd> <dt>

<span id="Dynamic_Desirable"></span><span id="dynamic_desirable"></span><span id="DYNAMIC_DESIRABLE"></span>

**Dinâmico desejável** (4)


</dt> <dd></dd> <dt>

<span id="Trunk"></span><span id="trunk"></span><span id="TRUNK"></span>

**Tronco** (5)


</dt> <dd></dd> <dt>

<span id="Dot1Q_Tunnel"></span><span id="dot1q_tunnel"></span><span id="DOT1Q_TUNNEL"></span>

**Túnel Dot1Q** (6)


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

**DMTF reservado** (..)


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

**Fornecedor reservado** (0x8000.. 0xFFFF


</dt> <dd></dd> </dl>

</dd> <dt>

**OtherEndpointMode**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ EthernetPortAllocationSettingData**.**DesiredVLANEndpointMode**")
</dt> </dl>

O tipo de modelo de ponto de extremidade de VLAN com suporte por esse ponto de extremidade de VLAN, quando o valor da propriedade de modo é definido como "1" (outro). Essa propriedade deve ser definida como **NULL** quando a propriedade Mode for qualquer valor diferente de "1".

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

[**\_RESOURCEALLOCATIONSETTINGDATA CIM**](cim-resourceallocationsettingdata.md)
</dt> </dl>

 

