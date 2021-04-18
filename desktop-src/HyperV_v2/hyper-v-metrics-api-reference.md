---
description: A API de métricas do Hyper-V define os seguintes elementos de programação.
ms.assetid: 00235614-9FCB-4161-B03D-9D557050153B
title: Referência de API de métricas do Hyper-V
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bdd4945bd390d995378c290f846335371fead753
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105810356"
---
# <a name="hyper-v-metrics-api-reference"></a>Referência de API de métricas do Hyper-V

A API de métricas do Hyper-V define os seguintes elementos de programação.

## <a name="in-this-section"></a>Nesta seção



| Tópico                                                                                    | Descrição                                                                                                                                                                                                                                                                                                                     |
|------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Msvm \_ AggregationMetricDefinition**](msvm-aggregationmetricdefinition.md)<br/> | Representa os aspectos de definição de uma métrica que é derivada de outro valor de métrica.<br/>                                                                                                                                                                                                                             |
| [**Msvm \_ AggregationMetricValue**](msvm-aggregationmetricvalue.md)<br/>           | Representa o valor da instância de uma métrica definida por uma instância da classe [**Msvm \_ AggregationMetricDefinition**](msvm-aggregationmetricdefinition.md) .<br/>                                                                                                                                                         |
| [**Msvm \_ BaseMetricDefinition**](msvm-basemetricdefinition.md)<br/>               | Representa os aspectos de definição de uma métrica.<br/>                                                                                                                                                                                                                                                                       |
| [**Msvm \_ BaseMetricValue**](msvm-basemetricvalue.md)<br/>                         | Representa um valor de métrica definido por uma instância da classe [**Msvm \_ BaseMetricDefinition**](msvm-basemetricdefinition.md) .<br/>                                                                                                                                                                                       |
| [**Msvm \_ MetricCollectionDependency**](msvm-metriccollectiondependency.md)<br/>   | Representa a associação entre duas definições de métrica ou dois valores de métrica.<br/>                                                                                                                                                                                                                                      |
| [**Msvm \_ MetricDefForME**](msvm-metricdefforme.md)<br/>                           | Define a associação entre um [**Msvm \_ BaseMetricDefinition**](msvm-basemetricdefinition.md) e um [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) para definir métricas para o último. A definição de métricas recebe o contexto do Managedelement, que é o motivo pelo qual a definição depende do elemento.<br/> |
| [**Msvm \_ MetricForME**](msvm-metricforme.md)<br/>                                 | Essa associação vincula um elemento gerenciado aos valores de métrica que estão sendo mantidos para ele.<br/>                                                                                                                                                                                                                               |
| [**Msvm \_ MetricInstance**](msvm-metricinstance.md)<br/>                           | Representa uma associação de objetos de valor de métrica com suas definições de métricas.<br/>                                                                                                                                                                                                                                    |
| [**Msvm \_ MetricService**](msvm-metricservice.md)<br/>                             | Fornece a capacidade de gerenciar métricas.<br/>                                                                                                                                                                                                                                                                              |
| [**Msvm \_ MetricServiceCapabilities**](msvm-metricservicecapabilities.md)<br/>     | Descreve os recursos da instância [**Msvm \_ MetricService**](msvm-metricservice.md) associada.<br/>                                                                                                                                                                                                             |
| [**Msvm \_ MetricServiceSettingData**](msvm-metricservicesettingdata.md)<br/>       | Representa as configurações para o serviço de métrica. As propriedades desta classe não podem ser modificadas diretamente. O cliente deve chamar o método [**ModifyServiceSettings**](modifyservicesettings-msvm-metricservice.md) para modificar qualquer uma dessas propriedades.<br/>                                                              |



 

 

