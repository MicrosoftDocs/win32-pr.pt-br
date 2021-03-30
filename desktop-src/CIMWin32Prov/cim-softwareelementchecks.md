---
description: A \_ classe de associação CIM SoftwareElementChecks relaciona um elemento de software com informações de condição ou local que um recurso pode exigir.
ms.assetid: ff130fe9-ddb2-4e4f-86d3-53f1d8ed14aa
ms.tgt_platform: multiple
title: Classe CIM_SoftwareElementChecks
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SoftwareElementChecks
- CIM_SoftwareElementChecks.Check
- CIM_SoftwareElementChecks.Element
- CIM_SoftwareElementChecks.Phase
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: ea6fcb02794174e825994f70270745741c9b7713
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826250"
---
# <a name="cim_softwareelementchecks-class"></a>\_Classe CIM SoftwareElementChecks

A classe de associação **CIM \_ SoftwareElementChecks** relaciona um elemento de software com informações de condição ou local que um recurso pode exigir.

Como os elementos de software em um estado pronto para execução não podem fazer a transição para outro Estado, o valor da propriedade **Phase** é restrito a estado de objetos [**CIM \_ softwareelement**](cim-softwareelement.md) em um estado pronto para execução.

> [!IMPORTANT]
> As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas. Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

A sintaxe a seguir é simplificada do código formato MOF (MOF) e inclui todas as suas propriedades herdadas. As propriedades são listadas em ordem alfabética, não em ordem MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
[UUID("{24783E8A-DB31-11d2-85FC-0000F8102E5F}"), Association, Aggregation, Abstract, AMENDMENT]
class CIM_SoftwareElementChecks
{
  CIM_Check           REF Check;
  CIM_SoftwareElement REF Element;
  uint16                  Phase;
};
```

## <a name="members"></a>Membros

A classe **CIM \_ SoftwareElementChecks** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **CIM \_ SoftwareElementChecks** tem essas propriedades.

<dl> <dt>

**Verificação**
</dt> <dd> <dl> <dt>

Tipo de dados **: \_ verificação de CIM**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (false), [**fraco**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

Referência à verificação.

</dd> <dt>

**Element**
</dt> <dd> <dl> <dt>

Tipo de dados: **CIM \_ softwareelement**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

Referência ao elemento.

</dd> <dt>

**Fase**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Indica se a verificação referenciada é uma verificação no estado ou uma verificação de estado seguinte.

<dt>

<span id="In-State"></span><span id="in-state"></span><span id="IN-STATE"></span>

**Em estado** (0)


</dt> <dd></dd> <dt>

<span id="Next-State"></span><span id="next-state"></span><span id="NEXT-STATE"></span>

**Próximo estado** (1)


</dt> <dd></dd> </dl>

</dd> </dl>

## <a name="remarks"></a>Comentários

O WMI não implementa essa classe. Para classes WMI derivadas do **CIM \_ SoftwareElementChecks**, consulte [classes Win32](win32-provider.md).

Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF. A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | Raiz \\ cimv2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



 

