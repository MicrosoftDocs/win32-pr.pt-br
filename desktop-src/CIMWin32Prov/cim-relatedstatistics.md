---
description: A associação \_ Cim RelatedStatistics representa hierarquias e dependências de classes \_ StatisticalInformation cim relacionadas.
ms.assetid: f5cea01d-7854-4ad4-a89e-db0ce9f4a83f
ms.tgt_platform: multiple
title: CIM_RelatedStatistics classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_RelatedStatistics
- CIM_RelatedStatistics.RelatedStats
- CIM_RelatedStatistics.Stats
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 3b45a1224114664196b5e21c6c7016e96fd49935adc370158133ec6c119695ce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119920586"
---
# <a name="cim_relatedstatistics-class"></a>Classe Cim \_ RelatedStatistics

A **associação \_ Cim RelatedStatistics** representa hierarquias e dependências de classes [**\_ StatisticalInformation cim**](cim-statisticalinformation.md) relacionadas.

> [!IMPORTANT]
> As classes CIM (Distributed Management Task Force) do DMTF (Distributed Management Task Force) modelo CIM são as classes pai nas quais as classes WMI são criadas. Atualmente, o WMI dá suporte apenas aos esquemas de versão [do CIM 2.x.](https://dmtf.org/standards/cim/schemas)

 

A sintaxe a seguir é simplificada Managed Object Format código (MOF) e inclui todas as suas propriedades herdadas. As propriedades são listadas em ordem alfabética, não em ordem MOF.

## <a name="syntax"></a>Sintaxe

``` syntax
[Abstract, Association, UUID("{956597A4-7D80-11D2-AAD3-006008C78BC7}"), AMENDMENT]
class CIM_RelatedStatistics
{
  CIM_StatisticalInformation REF RelatedStats;
  CIM_StatisticalInformation REF Stats;
};
```

## <a name="members"></a>Membros

A **classe \_ CIM RelatedStatistics** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A **classe \_ CIM RelatedStatistics** tem essas propriedades.

<dl> <dt>

**RelatedStats**
</dt> <dd> <dl> <dt>

Tipo de dados: **Cim \_ StatisticalInformation**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Referência às estatísticas ou métricas relacionadas.

</dd> <dt>

**Estatísticas**
</dt> <dd> <dl> <dt>

Tipo de dados: **Cim \_ StatisticalInformation**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Referência às informações de estatística ou objeto .

</dd> </dl>

## <a name="remarks"></a>Comentários

O WMI não implementa essa classe.

Esta documentação é derivada das descrições da classe CIM publicadas pelo DMTF. A Microsoft pode ter feito alterações para corrigir erros secundários, estar em conformidade com os padrões de documentação do SDK da Microsoft ou fornecer mais informações.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo com suporte<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | RAIZ \\ CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



 

 




