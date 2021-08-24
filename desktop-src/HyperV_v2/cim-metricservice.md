---
description: Gerencia métricas para elementos gerenciados.
ms.assetid: df249d0c-960b-47d6-9590-f0fd08ddec18
title: Classe CIM_MetricService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_MetricService
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: e5fd976abf5bce91ffbc5581e73f93c2a8422fcdcbe69fd70745511362e504d9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119694936"
---
# <a name="cim_metricservice-class"></a>\_Classe CIM MetricService

Gerencia métricas para elementos gerenciados.

## <a name="syntax"></a>Sintaxe

``` syntax
[Abstract, Version("2.23.0"), UMLPackagePath("CIM::Metrics::BaseMetric"), AMENDMENT]
class CIM_MetricService : CIM_Service
{
};
```

## <a name="members"></a>Membros

A classe **CIM \_ MetricService** tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A classe **CIM \_ MetricService** tem esses métodos.



| Método                                                                   | Descrição                                                                                                                                                                         |
|:-------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ControlMetrics**](cim-metricservice-controlmetrics.md)               | Habilita e desabilita a coleção de métricas.<br/>                                                                                                                          |
| [**ControlMetricsByClass**](cim-metricservice-controlmetricsbyclass.md) | Habilita e desabilita a coleção de métricas para uma classe.<br/>                                                                                                              |
| [**ControlSampleTimes**](cim-metricservice-controlsampletimes.md)       | Especifica quando as métricas são coletadas.<br/>                                                                                                                                     |
| [**GetMetricValues**](cim-metricservice-getmetricvalues.md)             | Recupera uma lista filtrada de valores de métrica.<br/>                                                                                                                              |
| [**Permétricas**](cim-metricservice-showmetrics.md)                     | Indica se a coleta de métrica está habilitada para os elementos gerenciados especificados e indica as métricas que estão disponíveis para coleta para cada elemento gerenciado.<br/> |
| [**ShowMetricsByClass**](cim-metricservice-showmetricsbyclass.md)       | Indica quais métricas estão disponíveis para coleta para todas as instâncias de uma classe CIM.<br/>                                                                                   |



 

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

[**\_Serviço CIM**](cim-service.md)
</dt> </dl>

 

 




