---
description: Representa o valor da instância de uma métrica definida por uma instância da \_ classe Msvm AggregationMetricDefinition.
ms.assetid: 6dfcb711-6137-492a-aff4-82facbd11949
title: Classe Msvm_AggregationMetricValue
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_AggregationMetricValue
- Msvm_AggregationMetricValue.InstanceID
- Msvm_AggregationMetricValue.Caption
- Msvm_AggregationMetricValue.Description
- Msvm_AggregationMetricValue.ElementName
- Msvm_AggregationMetricValue.MetricDefinitionId
- Msvm_AggregationMetricValue.MeasuredElementName
- Msvm_AggregationMetricValue.TimeStamp
- Msvm_AggregationMetricValue.Duration
- Msvm_AggregationMetricValue.MetricValue
- Msvm_AggregationMetricValue.BreakdownDimension
- Msvm_AggregationMetricValue.BreakdownValue
- Msvm_AggregationMetricValue.Volatile
- Msvm_AggregationMetricValue.AggregationTimeStamp
- Msvm_AggregationMetricValue.AggregationDuration
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: f6842e5a23fbbf7cf1d639862cf5b9737bc1ff96
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011469"
---
# <a name="msvm_aggregationmetricvalue-class"></a>\_Classe Msvm AggregationMetricValue

Representa o valor da instância de uma métrica definida por uma instância da classe [**Msvm \_ AggregationMetricDefinition**](msvm-aggregationmetricdefinition.md) . As propriedades herdadas de [**Msvm \_ BaseMetricValue**](msvm-basemetricvalue.md) fornecem o valor de métrica real. As propriedades definidas por essa classe fornecem informações sobre o intervalo sobre o qual a função de agregação foi aplicada.

A sintaxe a seguir é simplificada formato MOF código (MOF) e inclui todas as propriedades herdadas.

## <a name="syntax"></a>Sintaxe

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_AggregationMetricValue : CIM_AggregationMetricValue
{
  string   InstanceID;
  string   Caption;
  string   Description;
  string   ElementName;
  string   MetricDefinitionId;
  string   MeasuredElementName;
  datetime TimeStamp;
  datetime Duration;
  string   MetricValue;
  string   BreakdownDimension;
  string   BreakdownValue;
  boolean  Volatile;
  datetime AggregationTimeStamp;
  datetime AggregationDuration;
};
```

## <a name="members"></a>Membros

A classe **Msvm \_ AggregationMetricValue** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **Msvm \_ AggregationMetricValue** tem essas propriedades.

<dl> <dt>

**AggregationDuration**
</dt> <dd> <dl> <dt>

Tipo de dados: **DateTime**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Representa a duração da hora em que a agregação foi computada. O início de um intervalo de monitoramento sobre o qual a função de agregação é aplicada é determinado pela subtração do **AggregationDuration** do **AggregationTimeStamp**. Essa propriedade é herdada do **CIM \_ AggregationMetricValue**.

</dd> <dt>

**AggregationTimeStamp**
</dt> <dd> <dl> <dt>

Tipo de dados: **DateTime**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Identifica a hora em que a função de agregação foi aplicada para determinar o valor da instância de métrica. Isso não é o mesmo que a hora em que a instância foi criada. Para uma determinada instância de **\_ AggregationMetricValue do CIM** , o **AggregationTimeStamp** é alterado sempre que a função de agregação é aplicada para calcular o valor. Essa propriedade é herdada do **CIM \_ AggregationMetricValue**.

</dd> <dt>

**BreakdownDimension**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Especifica uma dimensão de divisão da matriz **BreakdownDimensions** definida no [**\_ BaseMetricDefinition Msvm**](msvm-basemetricdefinition.md)associado. Essa é a dimensão na qual esse conjunto de valores de métrica é dividido. Essa propriedade é herdada do [**CIM \_ BaseMetricDefinition**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).

</dd> <dt>

**Divisãovalue**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Define um valor da propriedade **BreakdownDimension** definida para essa instância de valor de métrica. Por exemplo, se **BreakdownDimension** for "transactionName", essa propriedade poderá nomear a transação real à qual esse valor de métrica específico se aplica. Essa propriedade é herdada do [**CIM \_ BaseMetricDefinition**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).

</dd> <dt>

**Legenda**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Uma breve descrição do objeto. Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).

</dd> <dt>

**Descrição**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Uma descrição do objeto . Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).

</dd> <dt>

**Duration**
</dt> <dd> <dl> <dt>

Tipo de dados: **DateTime**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Especifica o tempo durante o qual esse valor de métrica é válido. Essa propriedade não deve existir para carimbos de data/hora que se aplicam somente a um ponto no tempo, mas devem ser especificadas para valores que são considerados válidos por um determinado período de tempo (por exemplo, amostragem). Se a propriedade **Duration** existir e não for **NULL**, a propriedade **timestamp** especificará o final do intervalo. Essa propriedade é herdada do [**CIM \_ BaseMetricDefinition**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Um nome de exibição para o objeto. Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **chave**
</dt> </dl>

Uma cadeia de caracteres que identifica exclusivamente uma instância dessa classe. Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).

</dd> <dt>

**MeasuredElementName**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Um nome descritivo para o elemento ao qual o valor de métrica pertence (o elemento medido). Essa propriedade é herdada do [**CIM \_ BaseMetricDefinition**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).

</dd> <dt>

**MetricDefinitionId**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

A chave da instância [**de \_ BaseMetricDefinition do Msvm**](msvm-basemetricdefinition.md) para esse valor. Essa propriedade é herdada do [**CIM \_ BaseMetricDefinition**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).

</dd> <dt>

**Metricvalue**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

O valor da métrica que é representada como uma cadeia de caracteres. Essa propriedade é herdada do [**CIM \_ BaseMetricDefinition**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).

</dd> <dt>

**Estampa**
</dt> <dd> <dl> <dt>

Tipo de dados: **DateTime**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Especifica a hora em que o valor da métrica foi capturado ou computado. Lembre-se de que isso é diferente da hora em que a instância foi criada. Essa propriedade é herdada do [**CIM \_ BaseMetricDefinition**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).

</dd> <dt>

**Volátil**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

**True** se o valor para o próximo ponto no tempo usar a mesma instância de classe e apenas alterar os valores de propriedade (como o **valor** ou **carimbo de data/hora**). Se for **true**, a instância será reutilizada. Se **for false**, as instâncias existentes permanecerão inalteradas e uma nova instância será criada para o novo ponto no tempo. Essa propriedade é herdada do [**CIM \_ BaseMetricDefinition**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 8\]<br/>                                                              |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2012\]<br/>                                                    |
| Namespace<br/>                | \\Virtualização \\ v2 de raiz<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

