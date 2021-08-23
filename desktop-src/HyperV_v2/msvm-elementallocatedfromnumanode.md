---
description: Associa uma instância de um recurso alocado com o nó NUMA físico do qual ele foi alocado.
ms.assetid: 811ed19f-9084-4e30-8604-860d2bf722c7
title: Classe Msvm_ElementAllocatedFromNumaNode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ElementAllocatedFromNumaNode
- Msvm_ElementAllocatedFromNumaNode.Antecedent
- Msvm_ElementAllocatedFromNumaNode.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 0683ba63a76d64950f48dc9787347c4f08dd433653cef3a6f0388f97420d3ed6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119681716"
---
# <a name="msvm_elementallocatedfromnumanode-class"></a>\_Classe Msvm ElementAllocatedFromNumaNode

Associa uma instância de um recurso alocado com o nó NUMA físico do qual ele foi alocado.

A sintaxe a seguir é simplificada formato MOF código (MOF) e inclui todas as propriedades herdadas.

## <a name="syntax"></a>Sintaxe

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ElementAllocatedFromNumaNode : CIM_Dependency
{
  Msvm_NumaNode      REF Antecedent;
  CIM_LogicalElement REF Dependent;
};
```

## <a name="members"></a>Membros

A classe **Msvm \_ ElementAllocatedFromNumaNode** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **Msvm \_ ElementAllocatedFromNumaNode** tem essas propriedades.

<dl> <dt>

**Antecedent**
</dt> <dd> <dl> <dt>

Tipo de dados: **[ **Msvm \_ NumaNode**](msvm-numanode.md)**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)
</dt> </dl>

O nó físico NUMA.

</dd> <dt>

**Depende**
</dt> <dd> <dl> <dt>

Tipo de dados: **[ **CIM \_ LogicalElement**](/windows/desktop/CIMWin32Prov/cim-logicalelement)**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependente")
</dt> </dl>

O recurso alocado.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8 \[ somente aplicativos da área de trabalho\]<br/>                                                              |
| Servidor mínimo com suporte<br/> | Windows Server 2012 \[ somente aplicativos da área de trabalho\]<br/>                                                    |
| Namespace<br/>                | \\Virtualização \\ v2 de raiz<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

