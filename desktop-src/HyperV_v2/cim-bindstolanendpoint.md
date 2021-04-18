---
description: Representa uma associação em que um \_ objeto CIM ServiceAccessPoint ou CIM é \_ dependente de um \_ objeto LANEndpoint CIM subjacente no mesmo sistema.
ms.assetid: 3c015fbd-0611-41e8-a79a-01c980eedfd3
title: Classe CIM_BindsToLANEndpoint
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_BindsToLANEndpoint
- CIM_BindsToLANEndpoint.Antecedent
- CIM_BindsToLANEndpoint.Dependent
- CIM_BindsToLANEndpoint.FrameType
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: dff1cf243b54739509343d6d8958aa2a54f464b8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105811883"
---
# <a name="cim_bindstolanendpoint-class"></a>\_Classe CIM BindsToLANEndpoint

Representa uma associação em que um objeto [**CIM \_ ServiceAccessPoint**](cim-serviceaccesspoint.md) ou CIM é dependente de um [**objeto \_ LANEndpoint CIM**](cim-lanendpoint.md) subjacente no mesmo sistema. [**\_**](cim-protocolendpoint.md)

## <a name="syntax"></a>Sintaxe

``` syntax
[Association, Abstract, Version("2.6.0"), UMLPackagePath("CIM::Network::ProtocolEndpoints"), AMENDMENT]
class CIM_BindsToLANEndpoint : CIM_BindsTo
{
  CIM_LANEndpoint        REF Antecedent;
  CIM_ServiceAccessPoint REF Dependent;
  uint16                     FrameType;
};
```

## <a name="members"></a>Membros

A classe **CIM \_ BindsToLANEndpoint** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **CIM \_ BindsToLANEndpoint** tem essas propriedades.

<dl> <dt>

**Antecedent**
</dt> <dd> <dl> <dt>

Tipo de dados: **CIM \_ LANEndpoint**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")
</dt> </dl>

O objeto [**CIM \_ LANEndpoint**](cim-lanendpoint.md) subjacente.

</dd> <dt>

**Depende**
</dt> <dd> <dl> <dt>

Tipo de dados: **CIM \_ ServiceAccessPoint**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependente")
</dt> </dl>

O objeto [**CIM \_ ServiceAccessPoint**](cim-serviceaccesspoint.md) ou [**CIM \_ ProtocolEndpoint**](cim-protocolendpoint.md) que é dependente do [**\_ LANEndpoint do CIM**](cim-lanendpoint.md).

</dd> <dt>

**Conjunto de quadros**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

O método de enquadramento para o ponto de acesso do serviço de camada superior ou o EndPoint do protocolo.

> [!Note]  
> O 802.3 bruto só é conhecido por ser usado com o protocolo IPX.

 

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Desconhecido** (0)


</dt> <dd></dd> <dt>

<span id="Ethernet"></span><span id="ethernet"></span><span id="ETHERNET"></span>

**Ethernet** (1)


</dt> <dd></dd> <dt>

<span id="802.2"></span>

**802,2** (2)


</dt> <dd></dd> <dt>

<span id="SNAP"></span><span id="snap"></span>

**Snap** (3)


</dt> <dd></dd> <dt>

<span id="Raw802.3"></span><span id="raw802.3"></span><span id="RAW802.3"></span>

**802.3 bruto** (4)


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

[**\_BINDSTO CIM**](cim-bindsto.md)
</dt> </dl>

 

