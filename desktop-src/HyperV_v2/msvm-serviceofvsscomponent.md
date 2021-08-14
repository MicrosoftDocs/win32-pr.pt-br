---
description: Uma associação entre uma instância de Msvm \_ VssComponent e uma instância de Msvm \_ VssService que representa um serviço para executar operações no componente do VSS.
ms.assetid: 19fdf2e3-48c4-452b-89d0-ec0b8681fca2
title: Classe Msvm_ServiceOfVssComponent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ServiceOfVssComponent
- Msvm_ServiceOfVssComponent.Antecedent
- Msvm_ServiceOfVssComponent.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: a96c59a2e483080293ece2281ddb64fc9a7b43b425e5b508fe7ec209d1144dc0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118950535"
---
# <a name="msvm_serviceofvsscomponent-class"></a>\_Classe Msvm ServiceOfVssComponent

Uma associação entre uma instância de [**Msvm \_ VssComponent**](msvm-vsscomponent.md) e uma instância de [**Msvm \_ VssService**](msvm-vssservice.md) que representa um serviço para executar operações no componente do VSS.

A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.

## <a name="syntax"></a>Sintaxe

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ServiceOfVssComponent : CIM_Dependency
{
  Msvm_VssComponent REF Antecedent;
  Msvm_VssService   REF Dependent;
};
```

## <a name="members"></a>Membros

A classe **Msvm \_ ServiceOfVssComponent** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **Msvm \_ ServiceOfVssComponent** tem essas propriedades.

<dl> <dt>

**Antecedent**
</dt> <dd> <dl> <dt>

Tipo de dados: **Msvm \_ VssComponent**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**substituir**](/windows/desktop/WmiSdk/standard-qualifiers) (" \_ dependência CIM. Antecedent")
</dt> </dl>

A, [**Msvm \_ VssComponent**](msvm-vsscomponent.md) que representa o componente do VSS.

</dd> <dt>

**Depende**
</dt> <dd> <dl> <dt>

Tipo de dados: **Msvm \_ VssService**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) (" \_ dependência CIM. dependent")
</dt> </dl>

Um [**\_ VssService Msvm**](msvm-vssservice.md) que representa o serviço VSS IC.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 10 \[ somente aplicativos da área de trabalho\]<br/>                                                             |
| Servidor mínimo com suporte<br/> | Windows Server 2016<br/>                                                                          |
| Namespace<br/>                | \\Virtualização \\ v2 de raiz<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_Dependência CIM**](cim-dependency.md)
</dt> </dl>

 

