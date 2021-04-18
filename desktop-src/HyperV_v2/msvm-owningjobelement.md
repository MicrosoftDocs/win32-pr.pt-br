---
description: Representa uma associação entre um trabalho e o elemento gerenciado responsável pela criação do trabalho.
ms.assetid: 1a100c7e-7e17-47dd-b730-c05c5e4dccda
title: Classe Msvm_OwningJobElement
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_OwningJobElement
- Msvm_OwningJobElement.OwningElement
- Msvm_OwningJobElement.OwnedElement
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 34aa6f390d21a37421e09f30f9a775784717be9e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105768748"
---
# <a name="msvm_owningjobelement-class"></a>\_Classe Msvm OwningJobElement

Representa uma associação entre um trabalho e o elemento gerenciado responsável pela criação do trabalho.

A sintaxe a seguir é simplificada formato MOF código (MOF) e inclui todas as propriedades herdadas.

## <a name="syntax"></a>Sintaxe

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_OwningJobElement : CIM_OwningJobElement
{
  CIM_ManagedElement REF OwningElement;
  Msvm_ConcreteJob   REF OwnedElement;
};
```

## <a name="members"></a>Membros

A classe **Msvm \_ OwningJobElement** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **Msvm \_ OwningJobElement** tem essas propriedades.

<dl> <dt>

**Propriedade**
</dt> <dd> <dl> <dt>

Tipo de dados: **[ **Msvm \_ ConcreteJob**](msvm-concretejob.md)**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

O trabalho criado pelo elemento gerenciado.

</dd> <dt>

**Propriedade proprietária**
</dt> <dd> <dl> <dt>

Tipo de dados: **[ **CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

O elemento gerenciado responsável pela criação do trabalho.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 8\]<br/>                                                              |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2012\]<br/>                                                    |
| Namespace<br/>                | \\Virtualização \\ v2 de raiz<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

