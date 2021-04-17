---
description: Representa uma associação entre um trabalho e o elemento gerenciado que criou o trabalho.
ms.assetid: 08c33a81-0a3f-4545-9812-96a854a7509e
title: Classe CIM_OwningJobElement
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_OwningJobElement
- CIM_OwningJobElement.OwningElement
- CIM_OwningJobElement.OwnedElement
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 9d3879104a8f7406ff24dc2f63b79b51eb2fa58c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105758343"
---
# <a name="cim_owningjobelement-class"></a>\_Classe CIM OwningJobElement

Representa uma associação entre um trabalho e o elemento gerenciado que criou o trabalho. Como um trabalho pode ser movido entre sistemas, e o elemento gerenciado pode não existir durante toda a duração do trabalho, em alguns casos, essa associação pode não ser possível ou só pode existir para uma parte da existência do trabalho.

## <a name="syntax"></a>Sintaxe

``` syntax
[Association, Abstract, Version("2.7.0"), UMLPackagePath("CIM::System::Processing"), ModelCorrespondence("CIM_Job.Owner"), AMENDMENT]
class CIM_OwningJobElement
{
  CIM_ManagedElement REF OwningElement;
  CIM_Job            REF OwnedElement;
};
```

## <a name="members"></a>Membros

A classe **CIM \_ OwningJobElement** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **CIM \_ OwningJobElement** tem essas propriedades.

<dl> <dt>

**Propriedade**
</dt> <dd> <dl> <dt>

Tipo de dados **: \_ trabalho do CIM**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Uma referência ao trabalho criado pelo elemento gerenciado.

</dd> <dt>

**Propriedade proprietária**
</dt> <dd> <dl> <dt>

Tipo de dados: **CIM \_ managedelement**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**chave**](/windows/desktop/WmiSdk/key-qualifier), [**máx**](/windows/desktop/WmiSdk/standard-qualifiers) . (1)
</dt> </dl>

Uma referência ao elemento gerenciado que criou o trabalho.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8<br/>                                                                                    |
| Servidor mínimo com suporte<br/> | Windows Server 2012<br/>                                                                          |
| Namespace<br/>                | \\Virtualização \\ v2 de raiz<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

