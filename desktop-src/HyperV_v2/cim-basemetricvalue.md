---
description: Representa o valor da instância de uma métrica.
ms.assetid: 6b272ae8-7684-45bb-bff8-6559680cc8b6
title: Classe CIM_BaseMetricValue
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_BaseMetricValue
- CIM_BaseMetricValue.InstanceID
- CIM_BaseMetricValue.MetricDefinitionId
- CIM_BaseMetricValue.MeasuredElementName
- CIM_BaseMetricValue.TimeStamp
- CIM_BaseMetricValue.Duration
- CIM_BaseMetricValue.MetricValue
- CIM_BaseMetricValue.BreakdownDimension
- CIM_BaseMetricValue.BreakdownValue
- CIM_BaseMetricValue.Volatile
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 107dc3721ee32ca7f51efd563cdd6af14af483a69a5990e0b107a153b79b9351
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119014694"
---
# <a name="cim_basemetricvalue-class"></a>\_Classe CIM BaseMetricValue

Representa o valor da instância de uma métrica.

## <a name="syntax"></a>Sintaxe

``` syntax
[Abstract, Version("2.19.0"), UMLPackagePath("CIM::Metrics::BaseMetric"), AMENDMENT]
class CIM_BaseMetricValue : CIM_ManagedElement
{
  string   InstanceID;
  string   MetricDefinitionId;
  string   MeasuredElementName;
  datetime TimeStamp;
  datetime Duration;
  string   MetricValue;
  string   BreakdownDimension;
  string   BreakdownValue;
  boolean  Volatile;
};
```

## <a name="members"></a>Membros

A classe **CIM \_ BaseMetricValue** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **CIM \_ BaseMetricValue** tem essas propriedades.

<dl> <dt>

**BreakdownDimension**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

A dimensão para a qual esse conjunto de valores de métrica é dividido com base na propriedade **BreakdownDimensions** do objeto [**CIM \_ BaseMetricDefinition**](cim-basemetricdefinition.md) associado.

</dd> <dt>

**Divisãovalue**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

O valor da propriedade **BreakdownDimension** definida para esse valor de instância. Por exemplo, se **BreakdownDimension** contiver "transactionName", essa propriedade poderá nomear a transação real à qual esse valor de métrica específico se aplica.

</dd> <dt>

**Duration**
</dt> <dd> <dl> <dt>

Tipo de dados: **DateTime**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ BaseMetricDefinition**](cim-basemetricdefinition.md).**Timescope**","**CIM \_ BaseMetricValue**.**TimeStamp**")
</dt> </dl>

O tempo durante o qual esse valor de métrica é válido. Essa propriedade não deve existir para carimbos de data/hora que se aplicam somente a um ponto no tempo, mas devem ser definidas para valores que são considerados válidos por um determinado período de tempo (por exemplo, amostragem). Se a propriedade **Duration** existir e não for nula, o valor de **timestamp** deverá ser o final do intervalo.

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**chave**](/windows/desktop/WmiSdk/key-qualifier), [**substituição**](/windows/desktop/WmiSdk/standard-qualifiers) ("InstanceId")
</dt> </dl>

Identifica exclusivamente uma instância dessa classe dentro do escopo do namespace que a contém.

> [!IMPORTANT]
>
> Para garantir a exclusividade no namespace, o valor da propriedade **InstanceId** deve ser construído no seguinte padrão: *OrgID*:*LocalId*
>
> *OrgID* deve incluir um nome de direitos autorais, com marca registrada ou exclusivo que pertença à entidade de negócios que define a **InstanceId** ou ser uma ID registrada que é atribuída por uma autoridade global reconhecida. Esse padrão é semelhante à estrutura de nomes de classe de esquema. Além disso, para garantir a exclusividade, os primeiros dois-pontos em **InstanceId** devem estar entre *OrgID* e *LocalId*. Portanto, o *OrgID* não deve conter dois-pontos (': ').
>
> A *LocalId* é escolhida pela entidade de negócios e não deve ser reutilizada para identificar elementos do mundo real subjacentes diferentes.
>
> Se o padrão acima não for usado, a entidade de definição deverá garantir que o valor de **InstanceId** resultante não seja reutilizado em todas as propriedades **InstanceId** produzidas por este provedor ou por outros provedores para esse namespace.
>
> Para instâncias definidas pela DMTF (Distributed Management Task Force), o padrão deve ser usado com o *OrgID* definido como CIM.

 

</dd> <dt>

**MeasuredElementName**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Um nome descritivo para o elemento que é medido pela métrica.

Essa propriedade será necessária se a definição da métrica não estiver associada a um objeto [**\_ managedelement CIM**](cim-managedelement.md) e poderá ser usada em outros casos para fornecer informações complementares. Isso permite que as métricas sejam capturadas independentemente de qualquer objeto **CIM \_ managedelement** .

Se houver vários objetos [**\_ gerenciados CIM**](cim-managedelement.md) associados ao valor de métrica, você poderá escolher um dos elementos gerenciados para criar as informações complementares para a métrica. A propriedade não deve ser usada como uma chave estrangeira para consultar o elemento medido. Em vez disso, a associação ao **CIM \_ managedelement** deve ser usada.

</dd> <dt>

**MetricDefinitionId**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**Required**](/windows/desktop/WmiSdk/standard-qualifiers), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ BaseMetricDefinition**](cim-basemetricdefinition.md).**ID**")
</dt> </dl>

A chave da instância [**\_ BaseMetricDefinition do CIM**](cim-basemetricdefinition.md) que está associada a esse valor de instância.

</dd> <dt>

**Metricvalue**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [ **obrigatório**](/windows/desktop/WmiSdk/standard-qualifiers)
</dt> </dl>

Uma representação de cadeia de caracteres do valor da métrica. O tipo de dados original do valor da métrica é especificado no objeto [**CIM \_ BaseMetricDefinition**](cim-basemetricdefinition.md) associado.

</dd> <dt>

**Estampa**
</dt> <dd> <dl> <dt>

Tipo de dados: **DateTime**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ BaseMetricDefinition**](cim-basemetricdefinition.md).**Timescope**","**CIM \_ BaseMetricValue**.**Duração**")
</dt> </dl>

A hora em que o valor de uma instância de métrica é computada. Isso é diferente da hora em que a instância é criada. Se a propriedade **volátil** for true, esse valor será alterado sempre que um novo instantâneo de medida for obtido.

Um aplicativo de gerenciamento pode estabelecer uma série temporal de dados de métrica recuperando as instâncias do **CIM \_ BaseMetricValue** e classificando-as de acordo com o valor do **carimbo de data/hora** .

</dd> <dt>

**Volátil**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

True se o valor do **carimbo de data/hora** for alterado sempre que o valor da instância de métrica for alterado. False se esse objeto deve permanecer inalterado e um novo objeto criado para o novo valor de **carimbo de data/hora** .

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

[**\_Managedelement do CIM**](cim-managedelement.md)
</dt> </dl>

 

