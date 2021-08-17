---
description: A classe \_ ElementCapacity cim associa um objeto Cim \_ PhysicalCapacity a um ou mais elementos físicos. Ele associa uma descrição dos requisitos mínimos e máximos de hardware (ou funcionalidades) aos elementos físicos que estão sendo descritos.
ms.assetid: 368c31e8-d56b-4b90-ba3f-20d9b0de8730
ms.tgt_platform: multiple
title: CIM_ElementCapacity classe
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
ms.openlocfilehash: e108fb959b95148b8eb3be2e56346e41d2b2a5ab4d5b97c81394d583b395e9ac
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119924116"
---
# <a name="cim_elementcapacity-class"></a>Classe \_ ElementCapacity cim

A **classe \_ ElementCapacity** cim associa um objeto [**Cim \_ PhysicalCapacity**](cim-physicalcapacity.md) a um ou mais elementos físicos. Ele associa uma descrição dos requisitos mínimos e máximos de hardware (ou funcionalidades) aos elementos físicos que estão sendo descritos.

> [!IMPORTANT]
> As classes CIM (Distributed Management Task Force) do DMTF (Distributed Management Task Force) modelo CIM são as classes pai nas quais as classes WMI são criadas. Atualmente, o WMI dá suporte apenas aos esquemas de versão [do CIM 2.x.](https://dmtf.org/standards/cim/schemas)

 

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

A **classe \_ ElementCapacity cim** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A **classe \_ ElementCapacity cim** tem essas propriedades.

<dl> <dt>

**Capacidade**
</dt> <dd> <dl> <dt>

Tipo de dados: **Cim \_ PhysicalCapacity**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Referência à classe [**Cim \_ PhysicalCapacity**](cim-physicalcapacity.md) que descreve os requisitos mínimos e máximos e a capacidade de dar suporte a diferentes tipos de hardware para um elemento físico.

</dd> <dt>

**Element**
</dt> <dd> <dl> <dt>

Tipo de dados: **Cim \_ PhysicalElement**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1)
</dt> </dl>

Referência ao elemento físico que está sendo descrito.

</dd> </dl>

## <a name="remarks"></a>Comentários

O WMI não implementa essa classe.

Esta documentação é derivada das descrições da classe CIM publicadas pelo DMTF. A Microsoft pode ter feito alterações para corrigir erros secundários, estar em conformidade com os padrões de documentação do SDK da Microsoft ou fornecer mais informações.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | RAIZ \\ CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



 

