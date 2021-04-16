---
description: Conecta uma porta de comutador ao ponto de extremidade de Fibre Channel ao qual a porta está conectada.
ms.assetid: e2762e0c-2f78-4159-a67c-31213e311072
title: Classe Msvm_FcActiveConnection
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_FcActiveConnection
- Msvm_FcActiveConnection.Antecedent
- Msvm_FcActiveConnection.Dependent
- Msvm_FcActiveConnection.TrafficType
- Msvm_FcActiveConnection.OtherTrafficDescription
- Msvm_FcActiveConnection.IsUnidirectional
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 7e29330e073266f2f2a8749ec3c70d9e26b35ff7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105759241"
---
# <a name="msvm_fcactiveconnection-class"></a>\_Classe Msvm FcActiveConnection

Conecta uma porta de comutador ao ponto de extremidade de Fibre Channel ao qual a porta está conectada. A existência desse objeto significa que a porta do comutador e o ponto de extremidade de Fibre Channel estão ativamente conectados, e a porta de Fibre Channel associada ao ponto de extremidade Fibre Channel pode se comunicar com a rede por meio da porta do comutador.

A sintaxe a seguir é simplificada formato MOF código (MOF) e inclui todas as propriedades herdadas.

## <a name="syntax"></a>Sintaxe

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_FcActiveConnection : CIM_ActiveConnection
{
  Msvm_FcEndpoint REF Antecedent;
  Msvm_FcEndpoint REF Dependent;
  uint16              TrafficType;
  string              OtherTrafficDescription;
  boolean             IsUnidirectional;
};
```

## <a name="members"></a>Membros

A classe **Msvm \_ FcActiveConnection** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **Msvm \_ FcActiveConnection** tem essas propriedades.

<dl> <dt>

**Antecedent**
</dt> <dd> <dl> <dt>

Tipo de dados: **Msvm \_ FcEndpoint**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")
</dt> </dl>

Uma referência a uma instância da classe [**Msvm \_ FcEndpoint**](msvm-fcendpoint.md) que representa o SAP (ponto de acesso a serviços) configurado para comunicação ou que está se comunicando ativamente com o SAP dependente. Em uma conexão unidirecional, esse SAP é aquele que está transmitindo.

</dd> <dt>

**Depende**
</dt> <dd> <dl> <dt>

Tipo de dados: **Msvm \_ FcEndpoint**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependente")
</dt> </dl>

Uma referência a uma instância da classe [**Msvm \_ FcEndpoint**](msvm-fcendpoint.md) que representa o SAP que está configurado para se comunicar ou que está se comunicando ativamente com o SAP Antecedent. Em uma conexão unidirecional, esse SAP é aquele que está recebendo.

</dd> <dt>

**Unidirecional**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Se essa propriedade for **true**, essa conexão será unidirecional; caso contrário, essa conexão será bidirecional. Quando uma conexão é unidirecional, o "alto-falante" deve ser definido como referência **antecedente** . Em uma conexão bidirecional, não importa se o ponto de acesso selecionado é o **Antecedent** ou **dependente**. Essa propriedade é herdada do [**CIM \_ ActiveConnection**](/previous-versions//cc136779(v=vs.85)).

</dd> <dt>

**OtherTrafficDescription**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Essa propriedade é herdada do [**CIM \_ ActiveConnection**](/previous-versions//cc136779(v=vs.85)), mas não é usada.

</dd> <dt>

**TrafficType**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Essa propriedade é herdada do [**CIM \_ ActiveConnection**](/previous-versions//cc136779(v=vs.85)), mas não é usada.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 8\]<br/>                                                              |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2012\]<br/>                                                    |
| Namespace<br/>                | \\Virtualização \\ v2 de raiz<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

