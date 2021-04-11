---
description: A \_ classe CIM conectadoto representa uma associação que indica que dois ou mais conectores físicos estão conectados.
ms.assetid: fedd9227-8a3b-461a-995b-08cbceb81181
ms.tgt_platform: multiple
title: Classe CIM_ConnectedTo
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ConnectedTo
- CIM_ConnectedTo.Dependent
- CIM_ConnectedTo.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1f1a507cb529f2040607024e1a6167ddcd5dc7c0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010222"
---
# <a name="cim_connectedto-class"></a>\_Classe conectada CIM

A classe **CIM \_ conectadoto** representa uma associação que indica que dois ou mais conectores físicos estão conectados.

> [!IMPORTANT]
> As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas. Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas. As propriedades são listadas em ordem alfabética, não em ordem MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
[Abstract, UUID("{FAF76B85-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_ConnectedTo : CIM_Dependency
{
  CIM_PhysicalConnector REF Dependent;
  CIM_PhysicalConnector REF Antecedent;
};
```

## <a name="members"></a>Membros

A classe **CIM \_ conectadoto** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **CIM \_ conectadoto** tem essas propriedades.

<dl> <dt>

**Antecedent**
</dt> <dd> <dl> <dt>

Tipo de dados: **CIM \_ PhysicalConnector**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")
</dt> </dl>

Um [**\_ PhysicalConnector CIM**](cim-physicalconnector.md) que representa um conector físico que serve como uma extremidade da conexão.

</dd> <dt>

**Depende**
</dt> <dd> <dl> <dt>

Tipo de dados: **CIM \_ PhysicalConnector**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependente")
</dt> </dl>

Um [**\_ PhysicalConnector CIM**](cim-physicalconnector.md) que representa outro conector físico que serve como a outra extremidade da conexão.

</dd> </dl>

## <a name="remarks"></a>Comentários

A **classe \_ conectada ao CIM** é herdada da [**\_ dependência CIM**](cim-dependency.md).

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

 

