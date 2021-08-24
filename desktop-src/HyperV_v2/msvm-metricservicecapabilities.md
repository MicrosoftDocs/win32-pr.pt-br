---
description: Descreve os recursos da instância do Msvm \_ MetricService associada.
ms.assetid: 4E24D675-8265-4B5E-9551-550510B138FE
title: Msvm_MetricServiceCapabilities classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_MetricServiceCapabilities
- Msvm_MetricServiceCapabilities.InstanceID
- Msvm_MetricServiceCapabilities.Caption
- Msvm_MetricServiceCapabilities.Description
- Msvm_MetricServiceCapabilities.ElementName
- Msvm_MetricServiceCapabilities.ElementNameEditSupported
- Msvm_MetricServiceCapabilities.MaxElementNameLen
- Msvm_MetricServiceCapabilities.RequestedStatesSupported
- Msvm_MetricServiceCapabilities.ElementNameMask
- Msvm_MetricServiceCapabilities.ControllableMetrics
- Msvm_MetricServiceCapabilities.MetricsControlTypes
- Msvm_MetricServiceCapabilities.ControllableManagedElements
- Msvm_MetricServiceCapabilities.ManagedElementControlTypes
- Msvm_MetricServiceCapabilities.SupportedMethods
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 37fed3fead642ecfc5370d55c9f8b954477406b4b276cac392d9776a0cefb338
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119521326"
---
# <a name="msvm_metricservicecapabilities-class"></a>Classe Msvm \_ MetricServiceCapabilities

Descreve os recursos da instância do [**Msvm \_ MetricService**](msvm-metricservice.md) associada.

A sintaxe a seguir é simplificada Managed Object Format código MOF e inclui todas as propriedades herdadas.

## <a name="syntax"></a>Sintaxe

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_MetricServiceCapabilities : CIM_MetricServiceCapabilities
{
  string  InstanceID;
  string  Caption = "Hyper-V Metric Service Capabilities";
  string  Description = "Defines Hyper-V Metric Service Capabilities";
  string  ElementName = "Hyper-V Metric Service Capabilities";
  boolean ElementNameEditSupported;
  unit16  MaxElementNameLen;
  unit16  RequestedStatesSupported[];
  string  ElementNameMask;
  string  ControllableMetrics[];
  uint16  MetricsControlTypes[];
  string  ControllableManagedElements[];
  uint16  ManagedElementControlTypes[];
  uint16  SupportedMethods[];
};
```

## <a name="members"></a>Membros

A **classe Msvm \_ MetricServiceCapabilities** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A **classe Msvm \_ MetricServiceCapabilities** tem essas propriedades.

<dl> <dt>

**Legenda**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Uma breve descrição do objeto . Essa propriedade é herdada de [**\_ ManagedElement do CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)e sempre é definida como "Funcionalidades do Serviço de Métrica do Hyper-V".

</dd> <dt>

**ControllableManagedElements**
</dt> <dd> <dl> <dt>

Tipo de dados: matriz **de cadeia de** caracteres
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **ArrayType** ("Indexado")
</dt> </dl>

Identifica as instâncias do [**\_ ManagedElement cim**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) que podem ser controladas pela instância **cim \_ metricService** associada. Se essa propriedade for **Null,** todos os elementos poderão ser controlados. Essa propriedade é herdada de **\_ MetricServiceCapabilities do CIM.**

</dd> <dt>

**ControllableMetrics**
</dt> <dd> <dl> <dt>

Tipo de dados: matriz **de cadeia de** caracteres
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **ArrayType** ("Indexado")
</dt> </dl>

Identifica as instâncias do **CIM \_ BaseMetricDefinition** que podem ser controladas pela instância **cim \_ metricService** associada. Se essa propriedade for **Null,** todas as métricas poderão ser controladas. Essa propriedade é herdada de **\_ MetricServiceCapabilities do CIM.**

</dd> <dt>

**Descrição**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Uma descrição do objeto . Essa propriedade é herdada de [**\_ ManagedElement do CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)e sempre é definida como "Define funcionalidades de serviço de métrica do Hyper-V".

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Um nome de exibição para o objeto . Essa propriedade é herdada de [**\_ ManagedElement do CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)e sempre é definida como "Funcionalidades do Serviço de Métrica do Hyper-V".

</dd> <dt>

**ElementNameEditSupported**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliana**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Indica se a **propriedade ElementName** pode ser modificada. Essa propriedade é herdada de **CIM \_ EnabledLogicalElementCapabilities.**

</dd> <dt>

**ElementNameMask**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Especifica as restrições em **ElementName**, expressas como uma expressão regular. Essa propriedade é herdada de **CIM \_ EnabledLogicalElementCapabilities.**

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **Chave**
</dt> </dl>

Identifica exclusivamente uma instância dessa classe. Essa propriedade é herdada de [**\_ ManagedElement do CIM.**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)

</dd> <dt>

**ManagedElementControlTypes**
</dt> <dd> <dl> <dt>

Tipo de dados: **matriz uint16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **ArrayType** ("Indexado")
</dt> </dl>

Identifica o tipo de controle com suporte da instância **cim \_ metricservice** associada para o objeto [**\_ ManagedElement CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) identificado pelo valor no mesmo índice de matriz na propriedade **ControllableManagedElements.** Se essa propriedade for **Null,** todos os tipos de controle serão suportados. Essa propriedade é herdada de **\_ MetricServiceCapabilities do CIM.**



| Valor                                                                                   | Significado                    |
|-----------------------------------------------------------------------------------------|----------------------------|
| <dl> <dt>0</dt> </dl>            | Unknown<br/>         |
| <dl> <dt>2</dt> </dl>            | Discreto<br/>        |
| <dl> <dt>3</dt> </dl>            | Em massa<br/>            |
| <dl> <dt>4</dt> </dl>            | Ambos<br/>            |
| <dl> <dt>5..32767</dt> </dl>     | DMTF reservado<br/>   |
| <dl> <dt>32768..65535</dt> </dl> | Específico do fornecedor<br/> |



 

</dd> <dt>

**MaxElementNameLen**
</dt> <dd> <dl> <dt>

Tipo de dados: **unit16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **MaxValue** (256)
</dt> </dl>

Especifica o comprimento máximo com suporte da **propriedade ElementName.** Essa propriedade é herdada de **CIM \_ EnabledLogicalElementCapabilities.**

</dd> <dt>

**MetricsControlTypes**
</dt> <dd> <dl> <dt>

Tipo de dados: **matriz uint16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **ArrayType** ("Indexado")
</dt> </dl>

Identifica o tipo de controle com suporte da instância **cim \_ metricService** associada para **o \_ BaseMetricDefinition CIM** identificado pelo valor no mesmo índice de matriz na propriedade **ControllableMetrics.** Se essa propriedade for **Null,** todos os tipos de controle serão suportados. Essa propriedade é herdada de **\_ MetricServiceCapabilities do CIM.**



| Valor                                                                                   | Significado                    |
|-----------------------------------------------------------------------------------------|----------------------------|
| <dl> <dt>0</dt> </dl>            | Unknown<br/>         |
| <dl> <dt>2</dt> </dl>            | Discreto<br/>        |
| <dl> <dt>3</dt> </dl>            | Em massa<br/>            |
| <dl> <dt>4</dt> </dl>            | Ambos<br/>            |
| <dl> <dt>5.. 32767</dt> </dl>     | DMTF reservado<br/>   |
| <dl> <dt>32768.. 65535</dt> </dl> | Específico do fornecedor<br/> |



 

</dd> <dt>

**RequestedStatesSupported**
</dt> <dd> <dl> <dt>

Tipo de dados: matriz **unit16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Indica os possíveis Estados que podem ser solicitados ao usar o método **RequestStateChange** no elemento lógico habilitado. Essa propriedade é herdada do **CIM \_ EnabledLogicalElementCapabilities**.



| Valor                                                                         | Significado              |
|-------------------------------------------------------------------------------|----------------------|
| <dl> <dt>2</dt> </dl>  | habilitado<br/>   |
| <dl> <dt>3</dt> </dl>  | Desabilita<br/>  |
| <dl> <dt>4</dt> </dl>  | Desligar<br/> |
| <dl> <dt>6</dt> </dl>  | Offline<br/>   |
| <dl> <dt>7</dt> </dl>  | Teste<br/>      |
| <dl> <dt>8</dt> </dl>  | Ferida<br/>     |
| <dl> <dt>9</dt> </dl>  | Fechar<br/>   |
| <dl> <dt>10</dt> </dl> | Reinicialização<br/>    |
| <dl> <dt>11</dt> </dl> | Redefinir<br/>     |



 

</dd> <dt>

**SupportedMethods**
</dt> <dd> <dl> <dt>

Tipo de dados: a matriz **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Especifica os métodos com suporte pelo serviço de métrica. Essa propriedade é herdada do **CIM \_ MetricServiceCapabilities**.



| Valor                                                                                   | Significado                                                                                         |
|-----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <dt>2</dt> </dl>            | Há suporte para o método [**ControlMetrics**](controlmetrics-msvm-metricservice.md) .<br/> |
| <dl> <dt>3</dt> </dl>            | Há suporte para o método **ControlMetricsByClass** .<br/>                                   |
| <dl> <dt>4</dt> </dl>            | Há suporte para o método não há **métricas** .<br/>                                             |
| <dl> <dt>5</dt> </dl>            | Há suporte para o método **ShowMetricsByClass** .<br/>                                      |
| <dl> <dt>6</dt> </dl>            | Há suporte para o método **GetMetricValues** .<br/>                                         |
| <dl> <dt>7</dt> </dl>            | Há suporte para o método **ControlSampleTimes** .<br/>                                      |
| <dl> <dt>8.. 32767</dt> </dl>     | DMTF reservado<br/>                                                                        |
| <dl> <dt>32768.. 65535</dt> </dl> | Específico do fornecedor<br/>                                                                      |



 

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 8 \[ somente aplicativos da área de trabalho\]<br/>                                                              |
| Servidor mínimo com suporte<br/> | Windows Server 2012 \[ somente aplicativos da área de trabalho\]<br/>                                                    |
| Namespace<br/>                | \\Virtualização \\ v2 de raiz<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**\_METRICSERVICECAPABILITIES CIM**](cim-metricservicecapabilities.md)
</dt> <dt>

[**Msvm \_ MetricService**](msvm-metricservice.md)
</dt> </dl>

 

