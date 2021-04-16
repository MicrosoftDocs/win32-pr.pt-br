---
description: Descreve os recursos de um \_ objeto CIM MetricService.
ms.assetid: 3b4da02f-5298-46d4-876c-404baca38c03
title: Classe CIM_MetricServiceCapabilities
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_MetricServiceCapabilities
- CIM_MetricServiceCapabilities.ControllableMetrics
- CIM_MetricServiceCapabilities.MetricsControlTypes
- CIM_MetricServiceCapabilities.ControllableManagedElements
- CIM_MetricServiceCapabilities.ManagedElementControlTypes
- CIM_MetricServiceCapabilities.SupportedMethods
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: f878cb0e616cb710a33d350df866160fc0eebb83
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105759414"
---
# <a name="cim_metricservicecapabilities-class"></a>\_Classe CIM MetricServiceCapabilities

Descreve os recursos de um objeto [**CIM \_ MetricService**](cim-metricservice.md) .

## <a name="syntax"></a>Sintaxe

``` syntax
[Abstract, Version("2.22.0"), UMLPackagePath("CIM::Metrics::BaseMetrics"), AMENDMENT]
class CIM_MetricServiceCapabilities : CIM_EnabledLogicalElementCapabilities
{
  string ControllableMetrics[];
  uint16 MetricsControlTypes[];
  string ControllableManagedElements[];
  uint16 ManagedElementControlTypes[];
  uint16 SupportedMethods[];
};
```

## <a name="members"></a>Membros

A classe **CIM \_ MetricServiceCapabilities** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **CIM \_ MetricServiceCapabilities** tem essas propriedades.

<dl> <dt>

**ControllableManagedElements**
</dt> <dd> <dl> <dt>

Tipo de dados: matriz de **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) (**" \_ CIM MetricServiceCapabilities**.**ManagedElementControlTypes**")
</dt> </dl>

Uma matriz que contém identificadores das instâncias [**\_ gerenciadas CIM**](cim-managedelement.md) que são controladas pelo serviço de métrica. Os identificadores devem ser formatados como URIs WBEM (Web-Based Enterprise Management). Para usar essa propriedade, o serviço de métrica deve dar suporte à habilitação ou desabilitação de pelo menos uma métrica que é definida para a instância de **\_ managedelement CIM** .

</dd> <dt>

**ControllableMetrics**
</dt> <dd> <dl> <dt>

Tipo de dados: matriz de **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) (**" \_ CIM MetricServiceCapabilities**.**MetricControlTypes**")
</dt> </dl>

Uma matriz que contém identificadores do [**\_ BaseMetricDefinition CIM**](cim-basemetricdefinition.md) que define as métricas que são gerenciadas pelo serviço de métrica. Os identificadores devem ser formatados como URIs WBEM (Web-Based Enterprise Management).

Para usar essa propriedade, uma instância de [**\_ BaseMetricDefinition do CIM**](cim-basemetricdefinition.md) deve ser associada a uma instância de [**\_ MetricService do CIM**](cim-metricservice.md) por meio da classe [**CIM \_ imafetable**](cim-serviceaffectselement.md) . Além disso, o serviço de métrica deve dar suporte à habilitação ou desabilitação de pelo menos uma métrica que é definida pela instância **\_ BaseMetricDefinition do CIM** .

</dd> <dt>

**ManagedElementControlTypes**
</dt> <dd> <dl> <dt>

Tipo de dados: a matriz **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) (**" \_ CIM MetricServiceCapabilities**.**ControllableManagedElements**")
</dt> </dl>

Uma matriz que indica os tipos de controle que são suportados pelo serviço de métrica para os elementos gerenciados na matriz **ControllableManagedElements** . Essa matriz corresponde à matriz **ControllableManagedElements** . Os tipos de controle nessa matriz são associados às métricas por meio da matriz **ControllableManagedElements** .

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Desconhecido** (0)


</dt> <dd></dd> <dt>

<span id="Discrete"></span><span id="discrete"></span><span id="DISCRETE"></span>

**Discreto** (2)


</dt> <dd></dd> <dt>

<span id="Bulk"></span><span id="bulk"></span><span id="BULK"></span>

**Em massa** (3)


</dt> <dd></dd> <dt>

<span id="Both"></span><span id="both"></span><span id="BOTH"></span>

**Ambos** (4)


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

**DMTF reservado** (..)


</dt> <dd></dd> <dt>

<span id="Vendor_Specific"></span><span id="vendor_specific"></span><span id="VENDOR_SPECIFIC"></span>

**Específico do fornecedor** (32768.. 65535)


</dt> <dd></dd> </dl>

</dd> <dt>

**MetricsControlTypes**
</dt> <dd> <dl> <dt>

Tipo de dados: a matriz **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) (**" \_ CIM MetricServiceCapabilities**.**ControllableMetrics**")
</dt> </dl>

Uma matriz que indica os tipos de controle que são suportados pelo serviço de métrica. Essa matriz corresponde à matriz **ControllableMetrics** . Os tipos de controle nessa matriz são associados às métricas por meio da matriz **ControllableMetrics** .

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Desconhecido** (0)


</dt> <dd></dd> <dt>

<span id="Discrete"></span><span id="discrete"></span><span id="DISCRETE"></span>

**Discreto** (2)


</dt> <dd></dd> <dt>

<span id="Bulk"></span><span id="bulk"></span><span id="BULK"></span>

**Em massa** (3)


</dt> <dd></dd> <dt>

<span id="Both"></span><span id="both"></span><span id="BOTH"></span>

**Ambos** (4)


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

**DMTF reservado** (..)


</dt> <dd></dd> <dt>

<span id="Vendor_Specific"></span><span id="vendor_specific"></span><span id="VENDOR_SPECIFIC"></span>

**Específico do fornecedor** (32768.. 65535)


</dt> <dd></dd> </dl>

</dd> <dt>

**SupportedMethods**
</dt> <dd> <dl> <dt>

Tipo de dados: a matriz **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Uma matriz que contém nomes de métodos aos quais o serviço de métrica dá suporte.

<dt>

<span id="ControlMetrics"></span><span id="controlmetrics"></span><span id="CONTROLMETRICS"></span>

**ControlMetrics** (2)


</dt> <dd></dd> <dt>

<span id="ControlMetricsByClass"></span><span id="controlmetricsbyclass"></span><span id="CONTROLMETRICSBYCLASS"></span>

**ControlMetricsByClass** (3)


</dt> <dd></dd> <dt>

<span id="ShowMetrics"></span><span id="showmetrics"></span><span id="SHOWMETRICS"></span>

**Permétricas** (4)


</dt> <dd></dd> <dt>

<span id="ShowMetricsByClass"></span><span id="showmetricsbyclass"></span><span id="SHOWMETRICSBYCLASS"></span>

**ShowMetricsByClass** (5)


</dt> <dd></dd> <dt>

<span id="GetMetricValues"></span><span id="getmetricvalues"></span><span id="GETMETRICVALUES"></span>

**GetMetricValues** (6)


</dt> <dd></dd> <dt>

<span id="ControlSampleTimes"></span><span id="controlsampletimes"></span><span id="CONTROLSAMPLETIMES"></span>

**ControlSampleTimes** (7)


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

**DMTF reservado** (..)


</dt> <dd></dd> <dt>

<span id="Vendor_Specific"></span><span id="vendor_specific"></span><span id="VENDOR_SPECIFIC"></span>

**Específico do fornecedor** (0x8000..)


</dt> <dd></dd> </dl>

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

[**\_ENABLEDLOGICALELEMENTCAPABILITIES CIM**](cim-enabledlogicalelementcapabilities.md)
</dt> </dl>

 

