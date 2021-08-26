---
description: A associação CIM \_ RealizesAggregatePExtent representa a relação na qual a classe \_ AggregatePExtent cim é realizada em uma mídia física.
ms.assetid: 420dde1d-daa8-4cd3-b3fd-c2aefdc1e217
ms.tgt_platform: multiple
title: CIM_RealizesAggregatePExtent classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_RealizesAggregatePExtent
- CIM_RealizesAggregatePExtent.Dependent
- CIM_RealizesAggregatePExtent.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1c5eaf7e53fc7972795d0502c156e753bae60c777987e7304ef27a3a3fde54e8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119920936"
---
# <a name="cim_realizesaggregatepextent-class"></a>Classe CIM \_ RealizesAggregatePExtent

A **associação CIM \_ RealizesAggregatePExtent** representa a relação na qual a [**classe \_ AggregatePExtent cim**](cim-aggregatepextent.md) é realizada em uma mídia física.

> [!IMPORTANT]
> As classes CIM (Distributed Management Task Force) do DMTF (Distributed Management Task Force) modelo CIM são as classes pai nas quais as classes WMI são criadas. Atualmente, o WMI dá suporte apenas aos esquemas de versão [do CIM 2.x.](https://dmtf.org/standards/cim/schemas)

 

A sintaxe a seguir é simplificada Managed Object Format código (MOF) e inclui todas as suas propriedades herdadas. As propriedades são listadas em ordem alfabética, não em ordem MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
[Abstract, UUID("{FAF76B81-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_RealizesAggregatePExtent : CIM_Realizes
{
  CIM_AggregatePExtent REF Dependent;
  CIM_PhysicalMedia    REF Antecedent;
};
```

## <a name="members"></a>Membros

A **classe CIM \_ RealizesAggregatePExtent** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A **classe CIM \_ RealizesAggregatePExtent** tem essas propriedades.

<dl> <dt>

**Antecedente**
</dt> <dd> <dl> <dt>

Tipo de dados: **CIM \_ PhysicalMedia**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**Substituir**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecessor"), [**Máx.**](/windows/desktop/WmiSdk/standard-qualifiers) (1)
</dt> </dl>

Um [**Cim \_ PhysicalMedia**](cim-physicalmedia.md) que descreve a mídia física na qual a extensão é realizada.

</dd> <dt>

**Dependente**
</dt> <dd> <dl> <dt>

Tipo de dados: **\_ AggregatePExtent do CIM**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**Substituir**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependente")
</dt> </dl>

O [**\_ AggregatePExtent cim**](cim-aggregatepextent.md) localizado na mídia.

</dd> </dl>

## <a name="remarks"></a>Comentários

A **classe CIM \_ RealizesAggregatePExtent** é derivada de [**CIM \_ Realizes**](cim-realizes.md).

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



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Cim \_ Realiza**](cim-realizes.md)
</dt> </dl>

 

