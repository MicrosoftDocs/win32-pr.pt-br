---
description: Representa o valor da instância de uma métrica definida por uma instância de CIM \_ AggregationMetricDefinition.
ms.assetid: 663ef18a-0238-416f-9682-8809b271b4fc
title: Classe CIM_AggregationMetricValue
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_AggregationMetricValue
- CIM_AggregationMetricValue.AggregationTimeStamp
- CIM_AggregationMetricValue.AggregationDuration
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 0af264b66838e7c039ef3f99a4f365ebab55c293
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105758992"
---
# <a name="cim_aggregationmetricvalue-class"></a>\_Classe CIM AggregationMetricValue

Representa o valor da instância de uma métrica definida por uma instância de **CIM \_ AggregationMetricDefinition**.

## <a name="syntax"></a>Sintaxe

``` syntax
[Abstract, Version("2.22.0"), UMLPackagePath("CIM::Metrics::BaseMetric"), AMENDMENT]
class CIM_AggregationMetricValue : CIM_BaseMetricValue
{
  datetime AggregationTimeStamp;
  datetime AggregationDuration;
};
```

## <a name="members"></a>Membros

A classe **CIM \_ AggregationMetricValue** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **CIM \_ AggregationMetricValue** tem essas propriedades.

<dl> <dt>

**AggregationDuration**
</dt> <dd> <dl> <dt>

Tipo de dados: **DateTime**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ AggregationMetricValue**.**AggregationTimeStamp**")
</dt> </dl>

Representa a duração da hora em que a agregação foi computada. O início de um intervalo de monitoramento sobre o qual a função de agregação é aplicada é determinado pela subtração do valor **AggregationDuration** do valor **AggregationTimestamp** .

</dd> <dt>

**AggregationTimeStamp**
</dt> <dd> <dl> <dt>

Tipo de dados: **DateTime**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ AggregationMetricValue**.**Duração**")
</dt> </dl>

A hora em que a função de agregação foi aplicada para determinar o valor da instância de métrica. Isso é diferente da hora em que a instância é criada. O valor **AggregationTimeStamp** é alterado sempre que a função de agregação é aplicada para calcular o valor.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8<br/>                                                                                    |
| Servidor mínimo com suporte<br/> | Windows Server 2012<br/>                                                                          |
| Namespace<br/>                | \\Virtualização \\ v2 de raiz<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_BASEMETRICVALUE CIM**](cim-basemetricvalue.md)
</dt> </dl>

 

