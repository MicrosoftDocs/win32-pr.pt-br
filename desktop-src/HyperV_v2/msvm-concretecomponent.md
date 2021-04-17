---
description: Uma associação genérica usada para estabelecer parte de relações entre elementos gerenciados.
ms.assetid: 4D237D68-0A63-4A19-B6AD-E3C781090994
title: Classe Msvm_ConcreteComponent
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
ms.openlocfilehash: 2ef9e286f4c7ca296ee6b3638ffb9511ccea4115
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105754670"
---
# <a name="msvm_concretecomponent-class"></a>\_Classe Msvm ConcreteComponent

Uma associação genérica usada para estabelecer a "parte de" relações entre elementos gerenciados. [**CIM \_ ConcreteComponent**](/previous-versions//cc150665(v=vs.85)) é definido como uma subclasse concreta da classe abstrata de [**\_ componente CIM**](/windows/desktop/CIMWin32Prov/cim-component) , a ser usada em vez de muitas subclasses específicas de componente que não adicionam nenhuma semântica (ou seja, as subclasses que não esclarecem o tipo de composição, atualizam cardinalidade ou adicionam ou removem qualificadores.)

A sintaxe a seguir é simplificada formato MOF código (MOF) e inclui todas as propriedades herdadas.

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

A classe **Msvm \_ ConcreteComponent** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **Msvm \_ ConcreteComponent** tem essas propriedades.

<dl> <dt>

**GroupComponent**
</dt> <dd> <dl> <dt>

Tipo de dados: **[ **CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

O elemento pai na associação. Essa propriedade é herdada do [**CIM \_ ConcreteComponent**](/previous-versions//cc150665(v=vs.85)).

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

Tipo de dados: **[ **CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

O elemento filho na associação. Essa propriedade é herdada do [**CIM \_ ConcreteComponent**](/previous-versions//cc150665(v=vs.85)).

</dd> </dl>

## <a name="remarks"></a>Comentários

O acesso à classe **Msvm \_ ConcreteComponent** pode ser restringido pela filtragem do UAC. Para obter mais informações, consulte [controle de conta de usuário e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

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

[**\_CONCRETECOMPONENT CIM**](cim-concretecomponent.md)
</dt> <dt>

[**\_CONCRETECOMPONENT CIM**](/previous-versions//cc150665(v=vs.85))
</dt> <dt>

[Classes de sistema virtual](virtual-system-classes.md)
</dt> </dl>

 

