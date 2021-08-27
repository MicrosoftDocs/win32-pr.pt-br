---
description: A \_ Associação de componente CIM representa as partes de uma relação entre MSEs.
ms.assetid: a074e2f7-b092-4d3c-be5e-2069b643431b
ms.tgt_platform: multiple
title: Classe CIM_Component (provedores WMI CIMWin32)
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
- CIMWin32.dll
ms.openlocfilehash: 7b47aa88c7cf1238f74a9cb359ddb5f499c2a77b34de0f89023c83bd67420722
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120065176"
---
# <a name="cim_component-class-cimwin32-wmi-providers"></a>Classe CIM_Component (provedores WMI CIMWin32)

A associação de **\_ componente CIM** representa as partes de uma relação entre MSEs.

> [!IMPORTANT]
> As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas. Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas. As propriedades são listadas em ordem alfabética, não em ordem MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
[Association, Abstract, Aggregation, UUID("{8502C573-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_Component
{
  CIM_ManagedSystemElement REF GroupComponent;
  CIM_ManagedSystemElement REF PartComponent;
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

Tipo de dados: **CIM \_ ManagedSystemElement**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [ **agregação**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

Um [**\_ ManagedSystemElement CIM**](cim-managedsystemelement.md) que descreve o elemento pai na associação.

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

Tipo de dados: **CIM \_ ManagedSystemElement**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Um [**\_ ManagedSystemElement CIM**](cim-managedsystemelement.md) que descreve o elemento filho na associação.

</dd> </dl>

## <a name="remarks"></a>Comentários

O WMI não implementa essa classe. Para obter mais informações sobre classes derivadas **do \_ componente CIM**, consulte [classes Win32](win32-provider.md).

Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF. A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | Raiz \\ cimv2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



 

