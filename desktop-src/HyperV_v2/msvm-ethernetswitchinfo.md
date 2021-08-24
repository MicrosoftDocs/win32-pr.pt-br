---
description: Define a associação entre um comutador Ethernet e um recurso de comutador.
ms.assetid: fb29f4cb-50c4-4865-b267-21ff99bb4a8b
title: Classe Msvm_EthernetSwitchInfo
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetSwitchInfo
- Msvm_EthernetSwitchInfo.Antecedent
- Msvm_EthernetSwitchInfo.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: aea2d0f2c1f139b6953f165c9482f28c770d1384bc71f885378fedcb586a8ac1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119524556"
---
# <a name="msvm_ethernetswitchinfo-class"></a>\_Classe Msvm EthernetSwitchInfo

Define a associação entre um comutador Ethernet e um recurso de comutador.

A sintaxe a seguir é simplificada formato MOF código (MOF) e inclui todas as propriedades herdadas.

## <a name="syntax"></a>Sintaxe

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_EthernetSwitchInfo : CIM_Dependency
{
  Msvm_VirtualEthernetSwitch REF Antecedent;
  Msvm_EthernetSwitchData    REF Dependent;
};
```

## <a name="members"></a>Membros

A classe **Msvm \_ EthernetSwitchInfo** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **Msvm \_ EthernetSwitchInfo** tem essas propriedades.

<dl> <dt>

**Antecedent**
</dt> <dd> <dl> <dt>

Tipo de dados: **Msvm \_ VirtualEthernetSwitch**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")
</dt> </dl>

Uma referência à classe [**Msvm \_ VirtualEthernetSwitch**](msvm-virtualethernetswitch.md) que representa o sistema de hospedagem. Essa propriedade é derivada da [**\_ dependência CIM**](/windows/desktop/CIMWin32Prov/cim-dependency).

</dd> <dt>

**Depende**
</dt> <dd> <dl> <dt>

Tipo de dados: **Msvm \_ EthernetSwitchData**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependente")
</dt> </dl>

Uma referência à classe [**Msvm \_ EthernetSwitchData**](msvm-ethernetswitchdata.md) que representa o recurso de opção. Essa propriedade é derivada da [**\_ dependência CIM**](/windows/desktop/CIMWin32Prov/cim-dependency).

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8 \[ somente aplicativos da área de trabalho\]<br/>                                                              |
| Servidor mínimo com suporte<br/> | Windows Server 2012 \[ somente aplicativos da área de trabalho\]<br/>                                                    |
| Namespace<br/>                | \\Virtualização \\ v2 de raiz<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

