---
description: A \_ classe CIM ProductSupport representa uma associação entre produto e acesso de suporte que transmite como o suporte é obtido para o produto.
ms.assetid: 61c62556-0cf3-438c-b9c7-152505bf7ed6
ms.tgt_platform: multiple
title: Classe CIM_ProductSupport
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ProductSupport
- CIM_ProductSupport.Product
- CIM_ProductSupport.Support
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 8d1b39e1eef8f9686eee66c629120feaea51c778
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105753989"
---
# <a name="cim_productsupport-class"></a>\_Classe CIM ProductSupport

A classe **CIM \_ ProductSupport** representa uma associação entre produto e acesso de suporte que transmite como o suporte é obtido para o produto. Vários tipos de suporte estão disponíveis para um produto; o mesmo objeto de suporte pode fornecer assistência para vários produtos.

> [!IMPORTANT]
> As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas. Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

A sintaxe a seguir é simplificada do código formato MOF (MOF) e inclui todas as suas propriedades herdadas. As propriedades são listadas em ordem alfabética, não em ordem MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
[Abstract, UUID("{8D6D6880-DB2B-11d2-85FC-0000F8102E5F}"), Association, AMENDMENT]
class CIM_ProductSupport
{
  CIM_Product       REF Product;
  CIM_SupportAccess REF Support;
};
```

## <a name="members"></a>Membros

A classe **CIM \_ ProductSupport** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **CIM \_ ProductSupport** tem essas propriedades.

<dl> <dt>

**Product**
</dt> <dd> <dl> <dt>

Tipo de dados **: \_ produto CIM**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Referência ao produto.

</dd> <dt>

**Suporte**
</dt> <dd> <dl> <dt>

Tipo de dados: **CIM \_ SupportAccess**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Referência ao suporte do produto.

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



 

 




