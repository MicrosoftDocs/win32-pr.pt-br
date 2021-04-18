---
description: Representa uma associação genérica entre um elemento gerenciado pai e um elemento gerenciado filho em que o filho representa um componente ou parte do pai.
ms.assetid: b5cef452-2d00-483c-8e70-f804f1e3536b
title: Classe CIM_Component (gerenciamento do Hyper-V)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Component
- CIM_Component.GroupComponent
- CIM_Component.PartComponent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 56ff83a4da51ba18205a8d8ab5e6e57ea1a7794b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105761722"
---
# <a name="cim_component-class-hyper-v-management"></a>Classe CIM_Component (gerenciamento do Hyper-V)

Representa uma associação genérica entre um elemento gerenciado pai e um elemento gerenciado filho em que o filho representa um componente ou parte do pai.

## <a name="syntax"></a>Sintaxe

``` syntax
[Association, Abstract, Aggregation, Version("2.7.0"), UMLPackagePath("CIM::Core::CoreElements"), AMENDMENT]
class CIM_Component
{
  CIM_ManagedElement REF GroupComponent;
  CIM_ManagedElement REF PartComponent;
};
```

## <a name="members"></a>Membros

A classe de **\_ componente CIM** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe de **\_ componente CIM** tem essas propriedades.

<dl> <dt>

**GroupComponent**
</dt> <dd> <dl> <dt>

Tipo de dados: **CIM \_ managedelement**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**chave**](/windows/desktop/WmiSdk/key-qualifier), [**agregação**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

O elemento pai na associação.

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

Tipo de dados: **CIM \_ managedelement**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

O elemento filho na associação.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8<br/>                                                                                    |
| Servidor mínimo com suporte<br/> | Windows Server 2012<br/>                                                                          |
| Namespace<br/>                | \\Virtualização \\ v2 de raiz<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

