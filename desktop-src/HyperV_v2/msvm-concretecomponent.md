---
description: Uma associação genérica usada para estabelecer parte das relações entre elementos gerenciados.
ms.assetid: 4D237D68-0A63-4A19-B6AD-E3C781090994
title: Msvm_ConcreteComponent classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ConcreteComponent
- Msvm_ConcreteComponent.GroupComponent
- Msvm_ConcreteComponent.PartComponent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 24b813e7b8460f3de24207ed91b2e113f0d6b9633e17263806ef8447c166bdf7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119531746"
---
# <a name="msvm_concretecomponent-class"></a>Classe Msvm \_ ConcreteComponent

Uma associação genérica usada para estabelecer relações 'parte de' entre elementos gerenciados. [**CIM \_ ConcreteComponent**](/previous-versions//cc150665(v=vs.85)) é definido como uma subclasse concreta da classe de componente [**CIM \_**](/windows/desktop/CIMWin32Prov/cim-component) abstrata, a ser usada no lugar de muitas subclasses específicas do componente que não adicionam semântica (ou seja, subclasses que não esclarecem o tipo de composição, atualiza cardinalidades ou adicionam ou removem qualificadores).)

A sintaxe a seguir é simplificada Managed Object Format código MOF e inclui todas as propriedades herdadas.

## <a name="syntax"></a>Sintaxe

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ConcreteComponent : CIM_ConcreteComponent
{
  CIM_ManagedElement REF GroupComponent;
  CIM_ManagedElement REF PartComponent;
};
```

## <a name="members"></a>Membros

A **classe Msvm \_ ConcreteComponent** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A **classe Msvm \_ ConcreteComponent** tem essas propriedades.

<dl> <dt>

**Groupcomponent**
</dt> <dd> <dl> <dt>

Tipo de dados: **[ **\_ ManagedElement do CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

O elemento pai na associação. Essa propriedade é herdada [**de CIM \_ ConcreteComponent.**](/previous-versions//cc150665(v=vs.85))

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

Tipo de dados: **[ **\_ ManagedElement do CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

O elemento filho na associação. Essa propriedade é herdada [**de CIM \_ ConcreteComponent.**](/previous-versions//cc150665(v=vs.85))

</dd> </dl>

## <a name="remarks"></a>Comentários

O acesso à **classe Msvm \_ ConcreteComponent** pode ser restrito pela Filtragem de UAC. Para obter mais informações, consulte [Controle de conta de usuário e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Windows 8 somente aplicativos da área de trabalho\]<br/>                                                              |
| Servidor mínimo com suporte<br/> | \[Windows Server 2012 somente aplicativos da área de trabalho\]<br/>                                                    |
| Namespace<br/>                | Virtualização \\ raiz \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**CIM \_ ConcreteComponent**](cim-concretecomponent.md)
</dt> <dt>

[**CIM \_ ConcreteComponent**](/previous-versions//cc150665(v=vs.85))
</dt> <dt>

[Classes do sistema virtual](virtual-system-classes.md)
</dt> </dl>

 

