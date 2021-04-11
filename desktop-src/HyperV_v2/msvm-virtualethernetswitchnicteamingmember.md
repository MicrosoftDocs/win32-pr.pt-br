---
description: Representa a associação entre um ExternalEthernetPort de equipe e um ExternalEthernetPort de membro.
ms.assetid: e21bea94-d6a8-4788-958e-78ce255837aa
title: Classe Msvm_VirtualEthernetSwitchNicTeamingMember
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualEthernetSwitchNicTeamingMember
- Msvm_VirtualEthernetSwitchNicTeamingMember.Antecedent
- Msvm_VirtualEthernetSwitchNicTeamingMember.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: cbf83f4605d6ab1b7bc9740b14c493393eb93163
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104172344"
---
# <a name="msvm_virtualethernetswitchnicteamingmember-class"></a>\_Classe Msvm VirtualEthernetSwitchNicTeamingMember

Representa a associação entre um ExternalEthernetPort de equipe e um ExternalEthernetPort de membro.

A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.

## <a name="syntax"></a>Sintaxe

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualEthernetSwitchNicTeamingMember : CIM_Dependency
{
  Msvm_ExternalEthernetPort REF Antecedent;
  Msvm_ExternalEthernetPort REF Dependent;
};
```

## <a name="members"></a>Membros

A classe **Msvm \_ VirtualEthernetSwitchNicTeamingMember** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **Msvm \_ VirtualEthernetSwitchNicTeamingMember** tem essas propriedades.

<dl> <dt>

**Antecedent**
</dt> <dd> <dl> <dt>

Tipo de dados: **Msvm \_ ExternalEthernetPort**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")
</dt> </dl>

Um [**\_ ExternalEthernetPort Msvm**](msvm-externalethernetport.md) que faz referência à instância de porta Ethernet externa da equipe.

</dd> <dt>

**Depende**
</dt> <dd> <dl> <dt>

Tipo de dados: **Msvm \_ ExternalEthernetPort**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependente")
</dt> </dl>

Referência à instância do membro [**Msvm \_ ExternalEthernetPort**](msvm-externalethernetport.md) .

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows 10\]<br/>                                                             |
| Servidor mínimo com suporte<br/> | Windows Server 2016<br/>                                                                          |
| Namespace<br/>                | \\Virtualização \\ v2 de raiz<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_Dependência CIM**](cim-dependency.md)
</dt> </dl>

 

