---
description: Define uma conexão que está atualmente ativada e configurada para fornecer comunicação entre dois \_ objetos CIM ServiceAccessPoint.
ms.assetid: 03f8e43f-a77b-46e2-bb7d-c29758c65aee
title: Classe CIM_ActiveConnection
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ActiveConnection
- CIM_ActiveConnection.Antecedent
- CIM_ActiveConnection.Dependent
- CIM_ActiveConnection.TrafficType
- CIM_ActiveConnection.OtherTrafficDescription
- CIM_ActiveConnection.IsUnidirectional
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 644e8aaae1368e4164ceca7f7db29e343116c93c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105767649"
---
# <a name="cim_activeconnection-class"></a>\_Classe de ACTIVECONNECTION CIM

Define uma conexão que está atualmente ativada e configurada para fornecer comunicação entre dois objetos **CIM \_ ServiceAccessPoint** . **CIM \_ O ActiveConnection** é usado quando a conexão não é tratada como um objeto **\_ managedelement CIM** . Pontos de acesso de serviço conectados por uma conexão ativa normalmente estão na mesma camada de rede ou de aplicativo.

## <a name="syntax"></a>Sintaxe

``` syntax
[Association, Abstract, Version("2.10.0"), UMLPackagePath("CIM::Core::Service"), AMENDMENT]
class CIM_ActiveConnection : CIM_SAPSAPDependency
{
  CIM_ServiceAccessPoint REF Antecedent;
  CIM_ServiceAccessPoint REF Dependent;
  uint16                     TrafficType;
  string                     OtherTrafficDescription;
  boolean                    IsUnidirectional;
};
```

## <a name="members"></a>Membros

A classe **CIM \_ ActiveConnection** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **CIM \_ ActiveConnection** tem essas propriedades.

<dl> <dt>

**Antecedent**
</dt> <dd> <dl> <dt>

Tipo de dados: **CIM \_ ServiceAccessPoint**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")
</dt> </dl>

O ponto de acesso de serviço que está conectado ao outro ponto de acesso de serviço por meio da conexão ativa. **CIM \_ Objeto ServiceAccessPoint** . Em uma conexão unidirecional, esse ponto de acesso é aquele que está transmitindo dados.

</dd> <dt>

**Depende**
</dt> <dd> <dl> <dt>

Tipo de dados: **CIM \_ ServiceAccessPoint**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependente")
</dt> </dl>

O ponto de acesso de serviço configurado para se comunicar ou está se comunicando ativamente com o ponto de acesso de serviço especificado na propriedade **Antecedent** . Em uma conexão unidirecional, esse ponto de acesso é aquele que está recebendo dados.

</dd> <dt>

**Unidirecional**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

True se a conexão for unidirecional; false se a conexão for bidirecional. Quando a conexão é unidirecional, a propriedade **Antecedent** especifica o ponto de acesso que está transmitindo dados. Em uma conexão bidirecional, o **Antecedent** pode especificar o ponto de acesso atribuído à conexão.

</dd> <dt>

**OtherTrafficDescription**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**preteridos**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("sem valor"), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ ActiveConnection**.**Traffictype**")
</dt> </dl>

> [!Note]  
> Essa propriedade é preterida. Em vez disso, recomendamos que você especifique essas informações no endereçamento, protocolo e funcionalidade básica dos pontos de extremidade.

 

Uma descrição do tipo de tráfego que é especificado quando a propriedade **traffictype** é definida como "1" (outro).

</dd> <dt>

**TrafficType**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**preteridos**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("no value"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ ActiveConnection**.**OtherTrafficDescription**")
</dt> </dl>

> [!Note]  
> Essa propriedade é preterida. Em vez disso, recomendamos que você especifique essas informações no endereçamento, protocolo e funcionalidade básica dos pontos de extremidade.

 

O tipo de tráfego transmitido por essa conexão.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Desconhecido** (0)


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Outro** (1)


</dt> <dd></dd> <dt>

<span id="Unicast"></span><span id="unicast"></span><span id="UNICAST"></span>

**Unicast** (2)


</dt> <dd></dd> <dt>

<span id="Broadcast"></span><span id="broadcast"></span><span id="BROADCAST"></span>

**Difusão** (3)


</dt> <dd></dd> <dt>

<span id="Multicast"></span><span id="multicast"></span><span id="MULTICAST"></span>

**Multicast** (4)


</dt> <dd></dd> <dt>

<span id="Anycast"></span><span id="anycast"></span><span id="ANYCAST"></span>

**Anycast** (5)


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

[**\_SAPSAPDEPENDENCY CIM**](cim-sapsapdependency.md)
</dt> </dl>

 

