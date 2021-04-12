---
description: A \_ associação CIM ProductParentChild define uma hierarquia pai-filho entre os produtos. Por exemplo, um produto pode ser agrupado com outros produtos.
ms.assetid: 244576fd-8dae-4554-b80b-0cac58c93037
ms.tgt_platform: multiple
title: Classe CIM_ProductParentChild
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ProductParentChild
- CIM_ProductParentChild.Child
- CIM_ProductParentChild.Parent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 3a5fd34cc3dffc6d5c8df7f7a76d9cada7856d57
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104500840"
---
# <a name="cim_productparentchild-class"></a>\_Classe CIM ProductParentChild

A associação **CIM \_ ProductParentChild** define uma hierarquia pai-filho entre os produtos. Por exemplo, um produto pode ser agrupado com outros produtos.

> [!IMPORTANT]
> As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas. Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

A sintaxe a seguir é simplificada do código formato MOF (MOF) e inclui todas as suas propriedades herdadas. As propriedades são listadas em ordem alfabética, não em ordem MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
[Abstract, UUID("{3E24D5A6-DB2B-11d2-85FC-0000F8102E5F}"), Aggregation, Association, AMENDMENT]
class CIM_ProductParentChild
{
  CIM_Product REF Child;
  CIM_Product REF Parent;
};
```

## <a name="members"></a>Membros

A classe **CIM \_ ProductParentChild** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **CIM \_ ProductParentChild** tem essas propriedades.

<dl> <dt>

**Filho**
</dt> <dd> <dl> <dt>

Tipo de dados **: \_ produto CIM**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Referência ao produto filho na associação.

</dd> <dt>

**Pai**
</dt> <dd> <dl> <dt>

Tipo de dados **: \_ produto CIM**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [ **agregação**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

Referência ao produto pai na associação.

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



 

