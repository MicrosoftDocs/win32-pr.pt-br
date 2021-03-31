---
description: Descreve um conjunto de classes com propriedades e métodos necessários, necessários para gerenciar uma entidade do mundo real ou para dar suporte a um cenário de uso de maneira interoperável.
ms.assetid: 75644856-3B47-43B8-835C-783A6BEE7251
title: Classe Msvm_RegisteredProfile
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_RegisteredProfile
- Msvm_RegisteredProfile.InstanceID
- Msvm_RegisteredProfile.Caption
- Msvm_RegisteredProfile.Description
- Msvm_RegisteredProfile.ElementName
- Msvm_RegisteredProfile.RegisteredOrganization
- Msvm_RegisteredProfile.OtherRegisteredOrganization
- Msvm_RegisteredProfile.RegisteredName
- Msvm_RegisteredProfile.RegisteredVersion
- Msvm_RegisteredProfile.AdvertiseTypes
- Msvm_RegisteredProfile.AdvertiseTypeDescriptions
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: a7014687355524fbe10ff01869cac6c3fd35a894
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011087"
---
# <a name="msvm_registeredprofile-class"></a>\_Classe Msvm RegisteredProfile

Descreve um conjunto de classes com propriedades e métodos necessários, necessários para gerenciar uma entidade do mundo real ou para dar suporte a um cenário de uso de maneira interoperável.

A sintaxe a seguir é simplificada formato MOF código (MOF) e inclui todas as propriedades herdadas.

## <a name="syntax"></a>Sintaxe

``` syntax
class Msvm_RegisteredProfile : CIM_RegisteredProfile
{
  string InstanceID;
  string Caption;
  string Description;
  string ElementName;
  uint16 RegisteredOrganization;
  string OtherRegisteredOrganization;
  string RegisteredName;
  string RegisteredVersion;
  uint16 AdvertiseTypes[];
  string AdvertiseTypeDescriptions[];
};
```

## <a name="members"></a>Membros

A classe **Msvm \_ RegisteredProfile** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **Msvm \_ RegisteredProfile** tem essas propriedades.

<dl> <dt>

**AdvertiseTypeDescriptions**
</dt> <dd> <dl> <dt>

Tipo de dados: matriz de **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Uma matriz de cadeias de caracteres que fornece informações adicionais relacionadas à propriedade **advertisetype** . Uma descrição deve ser fornecida quando **advertisetype** for 1 (Other). Uma entrada nessa matriz corresponde ao mesmo índice na matriz **AdvertiseTypes** . Essa propriedade é herdada do [**CIM \_ RegisteredProfile**](/previous-versions//ee309375(v=vs.85)).

</dd> <dt>

**AdvertiseTypes**
</dt> <dd> <dl> <dt>

Tipo de dados: a matriz **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Especifica o anúncio das informações de perfil. Ele é usado pelos serviços de anúncio da infraestrutura do WBEM para determinar o que deve ser anunciado, por meio de quais mecanismos. A propriedade é uma matriz para que o perfil possa ser anunciado usando vários mecanismos. Se essa propriedade for **nula**, isso será equivalente a especificar o valor 2 (não anunciado). Essa propriedade é herdada do [**CIM \_ RegisteredProfile**](/previous-versions//ee309375(v=vs.85)).

<dl> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outro** (1)
</dt> <dt>

<span id="Not_Advertised"></span><span id="not_advertised"></span><span id="NOT_ADVERTISED"></span>**Não anunciado** (2)
</dt> <dt>

<span id="SLP_"></span><span id="slp_"></span>**SLP** (3)
</dt> </dl>

</dd> <dt>

**Legenda**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Uma breve descrição do objeto. Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).

</dd> <dt>

**Descrição**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Uma descrição do objeto . Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Um nome de exibição para o objeto. Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **chave**, **substituição**
</dt> </dl>

Uma cadeia de caracteres que identifica exclusivamente uma instância dessa classe. Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).

</dd> <dt>

**OtherRegisteredOrganization**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **maxlen** (256)
</dt> </dl>

Uma cadeia de caracteres que fornece uma descrição da organização quando **RegisteredOrganization** contém 1 (outro). Essa propriedade é herdada do [**CIM \_ RegisteredProfile**](/previous-versions//ee309375(v=vs.85)).

</dd> <dt>

**Registeredname**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **maxlen** (256)
</dt> </dl>

O nome deste perfil registrado. Como várias versões podem existir para o mesmo **registeredname**, a combinação de **registeredname**, **RegisteredOrganization** e **RegisteredVersion** deve identificar exclusivamente o perfil registrado no escopo da organização. Essa propriedade é herdada do [**CIM \_ RegisteredProfile**](/previous-versions//ee309375(v=vs.85)).

</dd> <dt>

**RegisteredOrganization**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

A organização que define esse perfil. Essa propriedade é herdada do [**CIM \_ RegisteredProfile**](/previous-versions//ee309375(v=vs.85)).

<dl> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outro** (1)
</dt> <dt>

<span id="DMTF"></span><span id="dmtf"></span>**DMTF** (2)
</dt> <dt>

<span id="CompTIA"></span><span id="comptia"></span><span id="COMPTIA"></span>**CompTIA** (3)
</dt> <dt>

<span id="Consortium_for_Service_Innovation"></span><span id="consortium_for_service_innovation"></span><span id="CONSORTIUM_FOR_SERVICE_INNOVATION"></span>**Consórcio para inovação de serviço** (4)
</dt> <dt>

<span id="FAST"></span><span id="fast"></span>**Rápido** (5)
</dt> <dt>

<span id="GGF"></span><span id="ggf"></span>**GGF** (6)
</dt> <dt>

<span id="INTAP"></span><span id="intap"></span>**INTAP** (7)
</dt> <dt>

<span id="itSMF"></span><span id="itsmf"></span><span id="ITSMF"></span>**itSMF** (8)
</dt> <dt>

<span id="NAC"></span><span id="nac"></span>**NAC** (9)
</dt> <dt>

<span id="__10___________Northwest_Energy_Efficiency_Alliance"></span><span id="__10___________northwest_energy_efficiency_alliance"></span><span id="__10___________NORTHWEST_ENERGY_EFFICIENCY_ALLIANCE"></span>**10-aliança de eficiência de energia do noroeste** (10)
</dt> <dt>

<span id="SNIA"></span><span id="snia"></span>**SNIA** (11)
</dt> <dt>

<span id="TM_Forum"></span><span id="tm_forum"></span><span id="TM_FORUM"></span>**Fórum TM** (12)
</dt> <dt>

<span id="The_Open_Group"></span><span id="the_open_group"></span><span id="THE_OPEN_GROUP"></span>**O grupo aberto** (13)
</dt> <dt>

<span id="ANSI"></span><span id="ansi"></span>**ANSI** (14)
</dt> <dt>

<span id="IEEE"></span><span id="ieee"></span>**IEEE** (15)
</dt> <dt>

<span id="IETF"></span><span id="ietf"></span>**IETF** (16)
</dt> <dt>

<span id="INCITS"></span><span id="incits"></span>**INCITS** (17)
</dt> <dt>

<span id="ISO"></span><span id="iso"></span>**ISO** (18)
</dt> <dt>

<span id="W3C"></span><span id="w3c"></span>**W3C** (19)
</dt> <dt>

<span id="__20___________OGF"></span><span id="__20___________ogf"></span>**20 OGF** (20)
</dt> <dt>

<span id="The_Green_Grid"></span><span id="the_green_grid"></span><span id="THE_GREEN_GRID"></span>**A grade verde** (21)
</dt> <dt>

<span id="DMTF_Reserved_"></span><span id="dmtf_reserved_"></span><span id="DMTF_RESERVED_"></span>**DMTF reservado** (.. )
</dt> </dl>

</dd> <dt>

**RegisteredVersion**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

A versão deste perfil. A cadeia de caracteres deve estar no formato: "*M*. *N*. *U*"onde:

-   *M* é a versão principal (em formato numérico) que descreve a criação ou a última modificação do perfil.
-   *N* é a versão secundária (em formato numérico) que descreve a criação ou a última modificação do perfil.
-   *U* é a atualização (em formato numérico) que descreve a criação ou a última modificação do perfil.

Essa propriedade é herdada do [**CIM \_ RegisteredProfile**](/previous-versions//ee309375(v=vs.85)).

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8.1 \[ apenas aplicativos de área de trabalho\]<br/>                                                            |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2012 R2\]<br/>                                                 |
| Namespace<br/>                | \\Interoperabilidade raiz<br/>                                                                                |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

