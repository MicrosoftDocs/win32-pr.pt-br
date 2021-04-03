---
description: Conecta uma porta de comutador ao ponto de extremidade da LAN ao qual a porta está conectada.
ms.assetid: 963EC004-6A67-4F75-BD93-1BCD17F32490
title: Classe Msvm_ActiveConnection
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ActiveConnection
- Msvm_ActiveConnection.Antecedent
- Msvm_ActiveConnection.Dependent
- Msvm_ActiveConnection.TrafficType
- Msvm_ActiveConnection.OtherTrafficDescription
- Msvm_ActiveConnection.IsUnidirectional
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: cf682fac419658785cfe7594aa6fc17e4b2dd28e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103829483"
---
# <a name="msvm_activeconnection-class"></a>\_Classe Msvm ActiveConnection

Conecta uma porta de comutador ao ponto de extremidade da LAN ao qual a porta está conectada. A existência desse objeto significa que a porta do comutador e o ponto de extremidade da LAN estão ativamente conectados e a porta Ethernet associada ao ponto de extremidade da LAN pode se comunicar com a rede por meio da porta do comutador.

A sintaxe a seguir é simplificada formato MOF código (MOF) e inclui todas as propriedades herdadas.

## <a name="syntax"></a>Sintaxe

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ActiveConnection : CIM_ActiveConnection
{
  Msvm_LANEndpoint REF Antecedent;
  CIM_LANEndpoint  REF Dependent;
  uint16               TrafficType;
  string               OtherTrafficDescription;
  boolean              IsUnidirectional;
};
```

## <a name="members"></a>Membros

A classe **Msvm \_ ActiveConnection** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **Msvm \_ ActiveConnection** tem essas propriedades.

<dl> <dt>

**Antecedent**
</dt> <dd> <dl> <dt>

Tipo de dados: **[ **Msvm \_ LANEndpoint**](msvm-lanendpoint.md)**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")
</dt> </dl>

Uma referência a uma instância da classe [**Msvm \_ LANEndpoint**](msvm-lanendpoint.md) que representa o SAP (ponto de acesso a serviços) configurado para comunicação ou que está se comunicando ativamente com o SAP dependente. Em uma conexão unidirecional, esse SAP é aquele que está transmitindo.

</dd> <dt>

**Depende**
</dt> <dd> <dl> <dt>

Tipo de dados: **[ **CIM \_ LANEndpoint**](cim-lanendpoint.md)**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependente")
</dt> </dl>

Uma referência a uma instância da classe [**Msvm \_ LANEndpoint**](cim-lanendpoint.md) que representa o SAP que está configurado para se comunicar ou que está se comunicando ativamente com o SAP Antecedent. Em uma conexão unidirecional, esse SAP é aquele que está recebendo.

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

## <a name="remarks"></a>Comentários

O acesso à classe **Msvm \_ ActiveConnection** pode ser restringido pela filtragem UAC. Para obter mais informações, consulte [controle de conta de usuário e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

## <a name="examples"></a>Exemplos

Consulte [consultando objetos de rede](querying-networking-objects.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 8\]<br/>                                                              |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2012\]<br/>                                                    |
| Namespace<br/>                | \\Virtualização \\ v2 de raiz<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ActiveConnection do CIM \_**](cim-activeconnection.md)
</dt> <dt>

[**ActiveConnection do CIM \_**](/previous-versions//cc136779(v=vs.85))
</dt> </dl>

 

