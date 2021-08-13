---
description: A \_ Associação de encaixe CIM representa a relação entre dois chassis. Por exemplo, um laptop (um tipo de chassi) pode ser encaixado em uma estação de encaixe (outro tipo de chassi). Essa relação típica é descrita explicitamente.
ms.assetid: 72cb36bb-f79e-4d1a-a859-4024031e4ebc
ms.tgt_platform: multiple
title: Classe CIM_Docked
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Docked
- CIM_Docked.Dependent
- CIM_Docked.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 6988606cc419c2a5340b4a964a8fa8328b989f286fe544153452fcce48fa7c8d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119438836"
---
# <a name="cim_docked-class"></a>\_Classe encaixada CIM

A associação de **\_ encaixe CIM** representa a relação entre dois chassis. Por exemplo, um laptop (um tipo de chassi) pode ser encaixado em uma estação de encaixe (outro tipo de chassi). Essa relação típica é descrita explicitamente.

> [!IMPORTANT]
> As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas. Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades herdadas.

## <a name="syntax"></a>Sintaxe

``` syntax
[Abstract, MappingStrings("MIF.DMTF|Dynamic States|001.2"), UUID("{FAF76B75-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_Docked : CIM_Dependency
{
  CIM_Chassis REF Dependent;
  CIM_Chassis REF Antecedent;
};
```

## <a name="members"></a>Membros

A **classe \_ encaixada CIM** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A **classe \_ encaixada CIM** tem essas propriedades.

<dl> <dt>

**Antecedent**
</dt> <dd> <dl> <dt>

Tipo de dados **: \_ chassi CIM**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)
</dt> </dl>

Um [**\_ chassi CIM**](cim-chassis.md) que descreve a estação de encaixe.

</dd> <dt>

**Depende**
</dt> <dd> <dl> <dt>

Tipo de dados **: \_ chassi CIM**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependente"), [**máx**](/windows/desktop/WmiSdk/standard-qualifiers) . (1)
</dt> </dl>

Um [**\_ chassi CIM**](cim-chassis.md) que descreve o laptop encaixado.

</dd> </dl>

## <a name="remarks"></a>Comentários

A **classe \_ encaixada CIM** é derivada [**da \_ dependência CIM**](cim-dependency.md).

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



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_Dependência CIM**](cim-dependency.md)
</dt> </dl>

 

