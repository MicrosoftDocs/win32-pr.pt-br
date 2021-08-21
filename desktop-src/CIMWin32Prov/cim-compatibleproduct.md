---
description: A \_ classe CIM CompatibleProduct representa uma associação entre produtos que indica se dois produtos referenciados são interoperáveis, como se eles podem ser instalados juntos ou se um pode ser o contêiner físico para o outro, e assim por diante.
ms.assetid: d822b052-981a-4a66-8404-b4f5f4681502
ms.tgt_platform: multiple
title: Classe CIM_CompatibleProduct
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_CompatibleProduct
- CIM_CompatibleProduct.CompatibilityDescription
- CIM_CompatibleProduct.CompatibleProduct
- CIM_CompatibleProduct.Product
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 5d0d4721d8554723bb9ab808ff55884bb896f59e6050103cf127cc4df77109f4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119080870"
---
# <a name="cim_compatibleproduct-class"></a>\_Classe CIM CompatibleProduct

A classe **CIM \_ CompatibleProduct** representa uma associação entre produtos que indica se dois produtos referenciados são interoperáveis, como se eles podem ser instalados juntos ou se um pode ser o contêiner físico para o outro, e assim por diante.

> [!IMPORTANT]
> As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas. Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas. As propriedades são listadas em ordem alfabética, não em ordem MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
[Abstract, UUID("{2F648FBA-DB22-11d2-85FC-0000F8102E5F}"), Association, AMENDMENT]
class CIM_CompatibleProduct
{
  string          CompatibilityDescription;
  CIM_Product REF CompatibleProduct;
  CIM_Product REF Product;
};
```

## <a name="members"></a>Membros

A classe **CIM \_ CompatibleProduct** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **CIM \_ CompatibleProduct** tem essas propriedades.

<dl> <dt>

**CompatibilityDescription**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Cadeia de caracteres de forma livre que define como os dois produtos referenciados são interoperáveis, compatíveis e se há limitações de compatibilidade.

</dd> <dt>

**CompatibleProduct**
</dt> <dd> <dl> <dt>

Tipo de dados **: \_ produto CIM**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Referência ao produto compatível.

</dd> <dt>

**Product**
</dt> <dd> <dl> <dt>

Tipo de dados **: \_ produto CIM**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Referência ao produto para o qual as ofertas compatíveis são definidas.

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



 

 




