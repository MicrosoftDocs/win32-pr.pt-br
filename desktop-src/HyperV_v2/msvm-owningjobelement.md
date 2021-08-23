---
description: Representa uma associação entre um trabalho e o elemento gerenciado responsável pela criação do trabalho.
ms.assetid: 1a100c7e-7e17-47dd-b730-c05c5e4dccda
title: Msvm_OwningJobElement classe
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
ms.openlocfilehash: 144a212a98b6f51b731023b5137b01f1e9d77156bddaaae187ce3f6ff2474efb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119520976"
---
# <a name="msvm_owningjobelement-class"></a>Classe Msvm \_ OwningJobElement

Representa uma associação entre um trabalho e o elemento gerenciado responsável pela criação do trabalho.

A sintaxe a seguir é simplificada Managed Object Format código MOF e inclui todas as propriedades herdadas.

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

A **classe Msvm \_ OwningJobElement** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A **classe Msvm \_ OwningJobElement** tem essas propriedades.

<dl> <dt>

**OwnedElement**
</dt> <dd> <dl> <dt>

Tipo de dados: **[ **Msvm \_ ConcreteJob**](msvm-concretejob.md)**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

O trabalho criado pelo elemento gerenciado.

</dd> <dt>

**OwningElement**
</dt> <dd> <dl> <dt>

Tipo de dados: **[ **\_ ManagedElement do CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

O elemento gerenciado responsável pela criação do trabalho.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Windows 8 somente aplicativos da área de trabalho\]<br/>                                                              |
| Servidor mínimo com suporte<br/> | \[Windows Server 2012 somente aplicativos da área de trabalho\]<br/>                                                    |
| Namespace<br/>                | Virtualização \\ raiz \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

