---
description: A \_ associação CIM ActionSequence define uma série de operações que fazem a transição do elemento software (referenciado pela \_ Associação SOFTWAREELEMENTACTIONS do CIM) para seu próximo estado ou remove o elemento software de seu estado atual.
ms.assetid: b539c424-bc2a-414b-b56c-72550004720f
ms.tgt_platform: multiple
title: Classe CIM_ActionSequence
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ActionSequence
- CIM_ActionSequence.Next
- CIM_ActionSequence.Prior
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: a199671dd9f88cd81be50af537e156892e8cab653c70677de27c6e5df02f1d3d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119801076"
---
# <a name="cim_actionsequence-class"></a>\_Classe CIM ActionSequence

A associação **CIM \_ ActionSequence** define uma série de operações que fazem a transição do elemento software (referenciado pela Associação [**\_ SoftwareElementActions do CIM**](cim-softwareelementactions.md) ) para seu próximo estado ou remove o elemento software de seu estado atual.

As ações de estado seguinte e as ações de desinstalação associadas a um elemento de software específico devem ser uma sequência contínua. Como o **CIM \_ ActionSequence** é uma associação, o loops na classe de [**\_ ação CIM**](cim-action.md) , com funções para a ação "anterior" e a ação "Avançar", formam uma sequência.

A necessidade de uma sequência contínua implica:

-   Dentro do conjunto de ações de próximo estado ou de desinstalação, há apenas uma ação que não tem uma instância da Associação **\_ ActionSequence do CIM** que a referencia na função "Next". Essa é a primeira ação na sequência.
-   Dentro do conjunto de ações de próximo estado ou de desinstalação, há apenas uma ação que não tem uma instância da Associação **\_ ActionSequence do CIM** fazendo referência a ela na função "anterior". Esta é a última ação na sequência.
-   Todas as outras ações dentro do conjunto de ações de próximo estado e desinstalação devem participar de duas instâncias da Associação de **\_ ActionSequence do CIM** , uma em uma função "anterior" e outra na função "Next".

> [!IMPORTANT]
> As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas. Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas. As propriedades são listadas em ordem alfabética, não em ordem MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
[Abstract, Association, UUID("{F127E50E-E3E0-11d2-8601-0000F8102E5F}"), AMENDMENT]
class CIM_ActionSequence
{
  CIM_Action REF Next;
  CIM_Action REF Prior;
};
```

## <a name="members"></a>Membros

A classe **CIM \_ ActionSequence** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **CIM \_ ActionSequence** tem essas propriedades.

<dl> <dt>

**Próximo**
</dt> <dd> <dl> <dt>

Tipo de dados **: \_ ação CIM**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (0)
</dt> </dl>

Referência à próxima ação.

</dd> <dt>

**Prior**
</dt> <dd> <dl> <dt>

Tipo de dados **: \_ ação CIM**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (0)
</dt> </dl>

Referência à ação anterior.

</dd> </dl>

## <a name="remarks"></a>Comentários

As classes de [**\_ ação CIM**](cim-action.md) que participam dessa associação devem ter o mesmo valor para a propriedade **Direction** .

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

[Classes CIM](/windows/desktop/WmiSdk/cimclas)
</dt> </dl>

 

