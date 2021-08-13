---
description: Representa uma associação entre um sistema e um dos elementos que o compõem.
ms.assetid: 728f25bf-3d52-4b1c-bf72-51e8ed0a4e72
title: CIM_SystemComponent classe (gerenciamento do Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SystemComponent
- CIM_SystemComponent.GroupComponent
- CIM_SystemComponent.PartComponent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 6ca4212f1501fe73981a810e697745a61609ea374f46ab2884c8124fd2b00202
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118646714"
---
# <a name="cim_systemcomponent-class-hyper-v-management"></a>CIM_SystemComponent classe (gerenciamento do Hyper-V)

Representa uma associação entre um sistema e um dos elementos que o compõem.

## <a name="syntax"></a>Sintaxe

``` syntax
[Association, Aggregation, Abstract, Version("2.10.0"), UMLPackagePath("CIM::Core::CoreElements"), AMENDMENT]
class CIM_SystemComponent : CIM_Component
{
  CIM_System               REF GroupComponent;
  CIM_ManagedSystemElement REF PartComponent;
};
```

## <a name="members"></a>Membros

A **classe Cim \_ SystemComponent** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A **classe \_ Cim SystemComponent** tem essas propriedades.

<dl> <dt>

**Groupcomponent**
</dt> <dd> <dl> <dt>

Tipo de dados: **Sistema CIM \_**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")
</dt> </dl>

O [**Sistema CIM \_ que**](cim-system.md) contém **o PartComponent.**

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

Tipo de dados: **Cim \_ ManagedSystemElement**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**substituir**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")
</dt> </dl>

O [**\_ ManagedSystemElement cim**](cim-managedsystemelement.md) filho que é um componente do sistema.

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

[**Componente \_ CIM**](cim-component.md)
</dt> </dl>

 

