---
description: Representa uma associação em que um objeto Cim \_ ServiceAccessPoint ou Cim ProtocolEndpoint depende de um objeto \_ CIM LANEndpoint subjacente no mesmo \_ sistema.
ms.assetid: 3c015fbd-0611-41e8-a79a-01c980eedfd3
title: CIM_BindsToLANEndpoint classe
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
ms.openlocfilehash: 53418dd9f2e259ac2b5f109dac4c783682657a7a9c5ac5e0548e23cbe0fd6be1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119765606"
---
# <a name="cim_bindstolanendpoint-class"></a>Classe CIM \_ BindsToLANEndpoint

Representa uma associação em que um [**objeto Cim \_ ServiceAccessPoint**](cim-serviceaccesspoint.md) ou [**Cim \_ ProtocolEndpoint**](cim-protocolendpoint.md) depende de um objeto [**CIM \_ LANEndpoint**](cim-lanendpoint.md) subjacente no mesmo sistema.

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

A **classe \_ CIM BindsToLANEndpoint** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A **classe \_ CIM BindsToLANEndpoint** tem essas propriedades.

<dl> <dt>

**Antecedente**
</dt> <dd> <dl> <dt>

Tipo de dados: **CIM \_ LANEndpoint**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**substituir**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecessor")
</dt> </dl>

O objeto [**CIM \_ LANEndpoint**](cim-lanendpoint.md) subjacente.

</dd> <dt>

**Dependente**
</dt> <dd> <dl> <dt>

Tipo de dados: **\_ Serviço CIMAccessPoint**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**Substituir**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependente")
</dt> </dl>

O [**objeto \_ CIM ServiceAccessPoint**](cim-serviceaccesspoint.md) ou [**CIM \_ ProtocolEndpoint**](cim-protocolendpoint.md) que depende do [**\_ LANEndpoint do CIM.**](cim-lanendpoint.md)

</dd> <dt>

**FrameType**
</dt> <dd> <dl> <dt>

Tipo de dados: **uint16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

O método de enquadramento para o ponto de acesso do serviço de camada superior ou o ponto de extremidade de protocolo.

> [!Note]  
> Raw802.3 é conhecido apenas por ser usado com o protocolo IPX.

 

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Desconhecido** (0)


</dt> <dd></dd> <dt>

<span id="Ethernet"></span><span id="ethernet"></span><span id="ETHERNET"></span>

**Ethernet** (1)


</dt> <dd></dd> <dt>

<span id="802.2"></span>

**802.2** (2)


</dt> <dd></dd> <dt>

<span id="SNAP"></span><span id="snap"></span>

**SNAP** (3)


</dt> <dd></dd> <dt>

<span id="Raw802.3"></span><span id="raw802.3"></span><span id="RAW802.3"></span>

**Raw802.3** (4)


</dt> <dd></dd> </dl>

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8<br/>                                                                                    |
| Servidor mínimo com suporte<br/> | Windows Server 2012<br/>                                                                          |
| Namespace<br/>                | Virtualização \\ raiz \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**CIM \_ BindsTo**](cim-bindsto.md)
</dt> </dl>

 

