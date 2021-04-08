---
description: A \_ classe CIM ProductFRU representa uma associação entre o produto e uma unidade de substituição de campo (FRU), que fornece informações sobre os componentes do produto que foram ou estão sendo substituídos.
ms.assetid: 15d682e5-cd90-4fc4-8fff-e3fe1d2a0ac4
ms.tgt_platform: multiple
title: Classe CIM_ProductFRU
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ProductFRU
- CIM_ProductFRU.FRU
- CIM_ProductFRU.Product
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: b141d16adb50c5bc3f8d6be682a90aa4921061ef
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089040"
---
# <a name="cim_productfru-class"></a>\_Classe CIM ProductFRU

A classe **CIM \_ ProductFRU** representa uma associação entre o produto e uma unidade de substituição de campo (FRU), que fornece informações sobre os componentes do produto que foram ou estão sendo substituídos.

> [!IMPORTANT]
> As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas. Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

A sintaxe a seguir é simplificada do código formato MOF (MOF) e inclui todas as suas propriedades herdadas. As propriedades são listadas em ordem alfabética, não em ordem MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
[Abstract, UUID("{EB98A1B2-DB36-11d2-85FC-0000F8102E5F}"), Association, AMENDMENT]
class CIM_ProductFRU
{
  CIM_FRU     REF FRU;
  CIM_Product REF Product;
};
```

## <a name="members"></a>Membros

A classe **CIM \_ ProductFRU** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **CIM \_ ProductFRU** tem essas propriedades.

<dl> <dt>

**FRU**
</dt> <dd> <dl> <dt>

Tipo de dados **: \_ FRU do CIM**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Referência à FRU.

</dd> <dt>

**Product**
</dt> <dd> <dl> <dt>

Tipo de dados **: \_ produto CIM**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)
</dt> </dl>

Referência ao produto ao qual a FRU é aplicada.

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



 

