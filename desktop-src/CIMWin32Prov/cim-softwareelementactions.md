---
description: A \_ associação CIM SoftwareElementActions identifica as ações para um elemento de software.
ms.assetid: 2f8a584c-dff0-48f8-bc5f-2b833b5c0b18
ms.tgt_platform: multiple
title: Classe CIM_SoftwareElementActions
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SoftwareElementActions
- CIM_SoftwareElementActions.Action
- CIM_SoftwareElementActions.Element
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: f3ee22c018c1bcc3a3850ac2b9c4c3bcba32780ea66927245fcf0b02eae74232
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118421287"
---
# <a name="cim_softwareelementactions-class"></a>\_Classe CIM SoftwareElementActions

A associação **CIM \_ SoftwareElementActions** identifica as ações para um elemento de software.

> [!IMPORTANT]
> As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas. Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

A sintaxe a seguir é simplificada do código formato MOF (MOF) e inclui todas as suas propriedades herdadas. As propriedades são listadas em ordem alfabética, não em ordem MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
[UUID("{4B82D255-E3CD-11d2-8601-0000F8102E5F}"), Association, Aggregation, Abstract, AMENDMENT]
class CIM_SoftwareElementActions
{
  CIM_Action          REF Action;
  CIM_SoftwareElement REF Element;
};
```

## <a name="members"></a>Membros

A classe **CIM \_ SoftwareElementActions** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **CIM \_ SoftwareElementActions** tem essas propriedades.

<dl> <dt>

**Ação**
</dt> <dd> <dl> <dt>

Tipo de dados **: \_ ação CIM**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (false), [**fraco**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

Referência a uma instância de [**\_ ação de CIM**](cim-action.md) .

</dd> <dt>

**Element**
</dt> <dd> <dl> <dt>

Tipo de dados: **CIM \_ softwareelement**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

Referência a uma instância do [**CIM \_ softwareelement**](cim-softwareelement.md) .

</dd> </dl>

## <a name="remarks"></a>Comentários

O WMI não implementa essa classe. Para classes WMI derivadas do **CIM \_ SoftwareElementActions**, consulte [classes Win32](win32-provider.md).

Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF. A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | Raiz \\ cimv2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



 

