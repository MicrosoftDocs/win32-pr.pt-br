---
description: A \_ classe CIM FRUIncludesProduct indica que uma FRU (unidade substituível de campo) pode ser composta por outros produtos.
ms.assetid: e57dc7f5-4c5b-4ec4-9300-e080053955cb
ms.tgt_platform: multiple
title: Classe CIM_FRUIncludesProduct
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_FRUIncludesProduct
- CIM_FRUIncludesProduct.Component
- CIM_FRUIncludesProduct.FRU
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 196f0cc1f2e81312e5e695c34e0a492ac7c05389
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "104172487"
---
# <a name="cim_fruincludesproduct-class"></a>\_Classe CIM FRUIncludesProduct

A classe **CIM \_ FRUIncludesProduct** indica que uma FRU (unidade substituível de campo) pode ser composta por outros produtos.

> [!IMPORTANT]
> As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas. Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas. As propriedades são listadas em ordem alfabética, não em ordem MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
[Abstract, UUID("{87FEEDCA-DB2A-11d2-85FC-0000F8102E5F}"), Aggregation, Association, AMENDMENT]
class CIM_FRUIncludesProduct
{
  CIM_Product REF Component;
  CIM_FRU     REF FRU;
};
```

## <a name="members"></a>Membros

A classe **CIM \_ FRUIncludesProduct** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **CIM \_ FRUIncludesProduct** tem essas propriedades.

<dl> <dt>

**Componente**
</dt> <dd> <dl> <dt>

Tipo de dados **: \_ produto CIM**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Referência ao produto que faz parte da FRU.

</dd> <dt>

**FRU**
</dt> <dd> <dl> <dt>

Tipo de dados **: \_ FRU do CIM**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)
</dt> </dl>

Referência à FRU.

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



 

