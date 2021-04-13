---
description: Representa uma porta Ethernet.
ms.assetid: c9a148c2-cf02-466f-b8ca-b1bf616d75dc
title: Classe CIM_EthernetPort
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_EthernetPort
- CIM_EthernetPort.PortType
- CIM_EthernetPort.NetworkAddresses
- CIM_EthernetPort.MaxDataSize
- CIM_EthernetPort.Capabilities
- CIM_EthernetPort.CapabilityDescriptions
- CIM_EthernetPort.EnabledCapabilities
- CIM_EthernetPort.OtherEnabledCapabilities
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: a44e93f84178fa2714d3c823735b3d90922e04be
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501279"
---
# <a name="cim_ethernetport-class"></a>\_Classe CIM EthernetPort

Representa uma porta Ethernet.

## <a name="syntax"></a>Sintaxe

``` syntax
[Abstract, Version("2.10.0"), UMLPackagePath("CIM::Device::Ports"), AMENDMENT]
class CIM_EthernetPort : CIM_NetworkPort
{
  uint16 PortType;
  string NetworkAddresses[];
  uint32 MaxDataSize;
  uint16 Capabilities[];
  string CapabilityDescriptions[];
  uint16 EnabledCapabilities[];
  string OtherEnabledCapabilities[];
};
```

## <a name="members"></a>Membros

A classe **CIM \_ EthernetPort** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **CIM \_ EthernetPort** tem essas propriedades.

<dl> <dt>

**Funcionalidades**
</dt> <dd> <dl> <dt>

Tipo de dados: a matriz **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) (**" \_ CIM EthernetPort**.**CapabilityDescriptions**")
</dt> </dl>

Os recursos da porta Ethernet.

> [!Note]  
> Se os recursos de failover ou balanceamento de carga estiverem habilitados, um objeto de [**\_ reserva**](/windows/desktop/CIMWin32Prov/cim-sparegroup) (failover) CIM ou [**CIM \_ ExtraCapacityGroup**](/windows/desktop/CIMWin32Prov/cim-extracapacitygroup) (balanceamento de carga) também deverá ser definido para descrever completamente o recurso.

 

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Desconhecido** (0)


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Outro** (1)


</dt> <dd></dd> <dt>

<span id="AlertOnLan"></span><span id="alertonlan"></span><span id="ALERTONLAN"></span>

**AlertOnLan** (2)


</dt> <dd></dd> <dt>

<span id="WakeOnLan"></span><span id="wakeonlan"></span><span id="WAKEONLAN"></span>

**WakeOnLan** (3)


</dt> <dd></dd> <dt>

<span id="FailOver"></span><span id="failover"></span><span id="FAILOVER"></span>

**Failover** (4)


</dt> <dd></dd> <dt>

<span id="LoadBalancing"></span><span id="loadbalancing"></span><span id="LOADBALANCING"></span>

**Balanceamento de carga** (5)


</dt> <dd></dd> </dl>

</dd> <dt>

**CapabilityDescriptions**
</dt> <dd> <dl> <dt>

Tipo de dados: matriz de **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) (**" \_ CIM EthernetPort**.**Recursos**")
</dt> </dl>

Uma matriz de cadeias de caracteres de forma livre que fornece explicações mais detalhadas para qualquer um dos recursos indicados na matriz Capabilities. Os itens nessa matriz correspondem aos itens na matriz de recursos.

</dd> <dt>

**EnabledCapabilities**
</dt> <dd> <dl> <dt>

Tipo de dados: a matriz **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) (**" \_ CIM EthernetPort**.**Recursos**","**CIM \_ EthernetPort**.**OtherEnabledCapabilities**")
</dt> </dl>

Indica quais funcionalidades estão habilitadas na matriz Capabilities. Os itens nessa matriz correspondem aos itens na matriz de recursos.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Desconhecido** (0)


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Outro** (1)


</dt> <dd></dd> <dt>

<span id="AlertOnLan"></span><span id="alertonlan"></span><span id="ALERTONLAN"></span>

**AlertOnLan** (2)


</dt> <dd></dd> <dt>

<span id="WakeOnLan"></span><span id="wakeonlan"></span><span id="WAKEONLAN"></span>

**WakeOnLan** (3)


</dt> <dd></dd> <dt>

<span id="FailOver"></span><span id="failover"></span><span id="FAILOVER"></span>

**Failover** (4)


</dt> <dd></dd> <dt>

<span id="LoadBalancing"></span><span id="loadbalancing"></span><span id="LOADBALANCING"></span>

**Balanceamento de carga** (5)


</dt> <dd></dd> </dl>

</dd> <dt>

**MaxDataSize**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt32**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| Bridge-MIB. dot1dTpPortMaxInfo ")
</dt> </dl>

O tamanho máximo do campo de informações (não MAC) que será recebido ou transmitido.

</dd> <dt>

**NetworkAddresses**
</dt> <dd> <dl> <dt>

Tipo de dados: matriz de **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("NetworkAddresses")
</dt> </dl>

Os endereços de rede atribuídos à porta. O endereço é um MAC 802,3 que é formatado como doze dígitos hexadecimais (por exemplo, "010203040506"), onde cada par de dígitos representa um dos seis octetos do endereço MAC na ordem de bits canônica.

</dd> <dt>

**OtherEnabledCapabilities**
</dt> <dd> <dl> <dt>

Tipo de dados: matriz de **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) (**" \_ CIM EthernetPort**.**EnabledCapabilities**")
</dt> </dl>

Uma matriz de cadeias de caracteres de forma livre que fornece explicações mais detalhadas para qualquer um dos itens de matriz **EnabledCapabilities** que são definidos como 1 (outro). Os itens nessa matriz correspondem aos itens na matriz **EnabledCapabilities** .

</dd> <dt>

**PortType**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PortType")
</dt> </dl>

O modo que está habilitado na porta. Quando definido como 1 (outro), a propriedade **OtherPortType** descreve o modo.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Desconhecido** (0)


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Outro** (1)


</dt> <dd></dd> <dt>

<span id="10BaseT"></span><span id="10baset"></span><span id="10BASET"></span>

**10BaseT** (50)


</dt> <dd></dd> <dt>

<span id="10-100BaseT"></span><span id="10-100baset"></span><span id="10-100BASET"></span>

**10-100BaseT** (51)


</dt> <dd></dd> <dt>

<span id="100BaseT"></span><span id="100baset"></span><span id="100BASET"></span>

**100BaseT** (52)


</dt> <dd></dd> <dt>

<span id="1000BaseT"></span><span id="1000baset"></span><span id="1000BASET"></span>

**1000baseT** (53)


</dt> <dd></dd> <dt>

<span id="2500BaseT"></span><span id="2500baset"></span><span id="2500BASET"></span>

**2500BaseT** (54)


</dt> <dd></dd> <dt>

<span id="10GBaseT"></span><span id="10gbaset"></span><span id="10GBASET"></span>

**10GBaseT** (55)


</dt> <dd></dd> <dt>

<span id="10GBase-CX4"></span><span id="10gbase-cx4"></span><span id="10GBASE-CX4"></span>

**10GBASE-CX4** (56)


</dt> <dd></dd> <dt>

<span id="100Base-FX"></span><span id="100base-fx"></span><span id="100BASE-FX"></span>

**100BASE-FX** (100)


</dt> <dd></dd> <dt>

<span id="100Base-SX"></span><span id="100base-sx"></span><span id="100BASE-SX"></span>

**100BASE-SX** (101)


</dt> <dd></dd> <dt>

<span id="1000Base-SX"></span><span id="1000base-sx"></span><span id="1000BASE-SX"></span>

**1000BASE-SX** (102)


</dt> <dd></dd> <dt>

<span id="1000Base-LX"></span><span id="1000base-lx"></span><span id="1000BASE-LX"></span>

**1000BASE-LX** (103)


</dt> <dd></dd> <dt>

<span id="1000Base-CX"></span><span id="1000base-cx"></span><span id="1000BASE-CX"></span>

**1000BASE-CX** (104)


</dt> <dd></dd> <dt>

<span id="10GBase-SR"></span><span id="10gbase-sr"></span><span id="10GBASE-SR"></span>

**10GBASE-Sr** (105)


</dt> <dd></dd> <dt>

<span id="10GBase-SW"></span><span id="10gbase-sw"></span><span id="10GBASE-SW"></span>

**10GBASE-SW** (106)


</dt> <dd></dd> <dt>

<span id="10GBase-LX4"></span><span id="10gbase-lx4"></span><span id="10GBASE-LX4"></span>

**10GBASE-LX4** (107)


</dt> <dd></dd> <dt>

<span id="10GBase-LR"></span><span id="10gbase-lr"></span><span id="10GBASE-LR"></span>

**10GBASE-LR** (108)


</dt> <dd></dd> <dt>

<span id="10GBase-LW"></span><span id="10gbase-lw"></span><span id="10GBASE-LW"></span>

**10GBASE-LW** (109)


</dt> <dd></dd> <dt>

<span id="10GBase-ER"></span><span id="10gbase-er"></span><span id="10GBASE-ER"></span>

**10GBASE-ER** (110)


</dt> <dd></dd> <dt>

<span id="10GBase-EW"></span><span id="10gbase-ew"></span><span id="10GBASE-EW"></span>

**10GBASE-ovo** (111)


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

**Fornecedor reservado** (16000.. 65535)


</dt> <dd></dd> </dl>

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

[**\_NETWORKPORT CIM**](cim-networkport.md)
</dt> </dl>

 

