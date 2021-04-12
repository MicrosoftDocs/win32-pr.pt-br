---
description: A \_ classe CIM ElementCapacity associa um \_ objeto CIM PhysicalCapacity a um ou mais elementos físicos. Ele associa uma descrição dos requisitos mínimos e máximos de hardware (ou recursos) aos elementos físicos descritos.
ms.assetid: 368c31e8-d56b-4b90-ba3f-20d9b0de8730
ms.tgt_platform: multiple
title: Classe CIM_ElementCapacity
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ElementCapacity
- CIM_ElementCapacity.Capacity
- CIM_ElementCapacity.Element
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 7c6ecac913f6d4affcd9784a30d85fa08dfe0486
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104457038"
---
# <a name="cim_elementcapacity-class"></a>\_Classe CIM ElementCapacity

A classe **CIM \_ ElementCapacity** associa um objeto [**CIM \_ PhysicalCapacity**](cim-physicalcapacity.md) a um ou mais elementos físicos. Ele associa uma descrição dos requisitos mínimos e máximos de hardware (ou recursos) aos elementos físicos descritos.

> [!IMPORTANT]
> As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas. Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas. As propriedades são listadas em ordem alfabética, não em ordem MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
[Abstract, Association, UUID("{FAF76B6A-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_ElementCapacity
{
  CIM_PhysicalCapacity REF Capacity;
  CIM_PhysicalElement  REF Element;
};
```

## <a name="members"></a>Membros

A classe **CIM \_ ElementCapacity** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **CIM \_ ElementCapacity** tem essas propriedades.

<dl> <dt>

**Capacidade**
</dt> <dd> <dl> <dt>

Tipo de dados: **CIM \_ PhysicalCapacity**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Referência à classe [**CIM \_ PhysicalCapacity**](cim-physicalcapacity.md) que descreve os requisitos mínimo e máximo e a capacidade de dar suporte a diferentes tipos de hardware para um elemento físico.

</dd> <dt>

**Element**
</dt> <dd> <dl> <dt>

Tipo de dados: **CIM \_ físicoelement**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**mín**](/windows/desktop/WmiSdk/standard-qualifiers) . (1)
</dt> </dl>

Referência ao elemento físico que está sendo descrito.

</dd> </dl>

## <a name="remarks"></a>Comentários

O WMI não implementa essa classe.

Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF. A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | Raiz \\ cimv2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



 

