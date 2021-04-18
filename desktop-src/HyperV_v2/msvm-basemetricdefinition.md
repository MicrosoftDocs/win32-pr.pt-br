---
description: Representa os aspectos de definição de uma métrica.
ms.assetid: 861a69f6-a3bf-4e18-a9c2-931632e3cccc
title: Classe Msvm_BaseMetricDefinition
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_BaseMetricDefinition
- Msvm_BaseMetricDefinition.InstanceID
- Msvm_BaseMetricDefinition.Caption
- Msvm_BaseMetricDefinition.Description
- Msvm_BaseMetricDefinition.ElementName
- Msvm_BaseMetricDefinition.Id
- Msvm_BaseMetricDefinition.Name
- Msvm_BaseMetricDefinition.DataType
- Msvm_BaseMetricDefinition.Calculable
- Msvm_BaseMetricDefinition.Units
- Msvm_BaseMetricDefinition.BreakdownDimensions
- Msvm_BaseMetricDefinition.IsContinuous
- Msvm_BaseMetricDefinition.ChangeType
- Msvm_BaseMetricDefinition.TimeScope
- Msvm_BaseMetricDefinition.GatheringType
- Msvm_BaseMetricDefinition.ProgrammaticUnits
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 8d1edbd722e3bf87631371b5650576917a7cfb39
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105767642"
---
# <a name="msvm_basemetricdefinition-class"></a>\_Classe Msvm BaseMetricDefinition

Representa os aspectos de definição de uma métrica. A classe **Msvm \_ BaseMetricDefinition** deve ser associada ao [**\_ ManagedElements CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) ao qual se aplica.

A sintaxe a seguir é simplificada formato MOF código (MOF) e inclui todas as propriedades herdadas.

## <a name="syntax"></a>Sintaxe

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_BaseMetricDefinition : CIM_BaseMetricDefinition
{
  string  InstanceID;
  string  Caption;
  string  Description;
  string  ElementName;
  string  Id;
  string  Name;
  uint16  DataType;
  uint16  Calculable;
  string  Units;
  string  BreakdownDimensions[];
  boolean IsContinuous;
  uint16  ChangeType;
  uint16  TimeScope;
  uint16  GatheringType;
  string  ProgrammaticUnits;
};
```

## <a name="members"></a>Membros

A classe **Msvm \_ BaseMetricDefinition** tem estes tipos de membros:

-   [Propriedades](#properties)

### <a name="properties"></a>Propriedades

A classe **Msvm \_ BaseMetricDefinition** tem essas propriedades.

<dl> <dt>

**BreakdownDimensions**
</dt> <dd> <dl> <dt>

Tipo de dados: matriz de **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Define uma ou mais cadeias de caracteres que podem ser usadas para refinar (dividir) consultas em relação aos valores de métrica em uma determinada dimensão. Um exemplo é um nome de transação, permitindo a interrupção do valor total de todas as transações em um conjunto de valores, uma para cada nome de transação. Outros exemplos podem ser o nome do grupo de usuários ou do sistema de aplicativos. As cadeias de caracteres são de formato livre e devem ser significativas para os usuários finais dos dados da métrica. As cadeias de caracteres indicam quais dimensões de divisão são suportadas para essa definição de métrica, pela Instrumentação subjacente. Essa propriedade é herdada do **CIM \_ BaseMetricDefinition**.

</dd> <dt>

**Calculável**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Descreve as características da métrica para fins de execução de cálculos. Essa propriedade é herdada do **CIM \_ BaseMetricDefinition**. Isso pode ser **nulo** ou um dos valores a seguir.



| Valor                                                                                                                                                                                                                                                   | Significado                                                                                                                                                                                                                                                                                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Non-calculable"></span><span id="non-calculable"></span><span id="NON-CALCULABLE"></span><dl> <dt>**Não calculável**</dt> <dt>1</dt> </dl> | O valor não pode ser calculado. Por exemplo, uma cadeia de caracteres.<br/>                                                                                                                                                                                                                                                                                                         |
| <span id="Summable"></span><span id="summable"></span><span id="SUMMABLE"></span><dl> <dt>**Res**</dt> . <dt>2</dt> </dl>                         | O valor pode ser somado em várias instâncias. Por exemplo, se cada trabalho de backup é uma unidade de trabalho e cada trabalho faz backup de 27.000 arquivos em média, 100 os trabalhos de backup processaram 2,7 milhões arquivos.<br/>                                                                                                                                                                 |
| <span id="Non-summable_"></span><span id="non-summable_"></span><span id="NON-SUMMABLE_"></span><dl> <dt> **Não resumible**</dt> <dt>3</dt> </dl>    | Esse valor não pode ser somado em várias instâncias. Um exemplo seria uma métrica que mede o comprimento da fila quando um trabalho chega a um servidor. Se cada trabalho é uma unidade de trabalho e o comprimento médio da fila quando cada trabalho chega é 33, não faz sentido dizer que o comprimento da fila para 100 trabalhos é 3300. Faz sentido dizer que a média é de 33.<br/> |



 

</dd> <dt>

**Legenda**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Uma breve descrição do objeto. Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).

</dd> <dt>

**ChangeType**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Indica como o valor da métrica é alterado, na forma de combinações típicas de atributos de detalhamento mais detalhados, como alteração de direção, valores mínimos e máximos e semântica de encapsulamento. Essa propriedade é herdada do **CIM \_ BaseMetricDefinition**.



| Valor                                                                                                                                                                                                                                                                       | Significado                                                                                                                                                                                          |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <dt></dt> <dt>0</dt> desconhecido </dl>                                                 | O designer de métrica não qualificou o **ChangeType.**.<br/>                                                                                                                              |
| <span id="N_A"></span><span id="n_a"></span><dl> <dt>**N/A**</dt> <dt>2</dt> </dl>                                                                                       | Se a propriedade **Iscontinuous** for "false", **altertype** não faz sentido e deve ser definida como "N/A".<br/>                                                                             |
| <span id="Counter"></span><span id="counter"></span><span id="COUNTER"></span><dl> <dt>**Contador**</dt> <dt>3</dt> </dl>                                                 | A métrica é uma métrica de contador. Eles têm valores inteiros não negativos que aumentam até atingir o número máximo reapresentável e, em seguida, encapsular e começar a aumentar de 0.<br/> |
| <span id="Gauge"></span><span id="gauge"></span><span id="GAUGE"></span><dl> <dt>**Indicador**</dt> <dt>4</dt> </dl>                                                         | A métrica é uma métrica de medidor. Eles têm valores inteiros ou flutuantes que podem aumentar e diminuir arbitrariamente.<br/>                                                                          |
| <span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span><dl> <dt>**DMTF reservado**</dt> <dt>5.. 32767</dt> </dl>                  |                                                                                                                                                                                                  |
| <span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span><dl> 32768 <dt> **reservado para fornecedor**</dt> <dt>.. 65535</dt> </dl> | Os fornecedores podem estender a propriedade **altertype** no intervalo reservado do fornecedor.<br/>                                                                                                          |



 

</dd> <dt>

**DataType**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

O tipo de dados da métrica. Essa propriedade é herdada do **CIM \_ BaseMetricDefinition**.

<dl> <dt>

<span id="boolean"></span><span id="BOOLEAN"></span>**booliano** (1)
</dt> <dt>

<span id="char16"></span><span id="CHAR16"></span>**char16** (2)
</dt> <dt>

<span id="datetime"></span><span id="DATETIME"></span>**data e hora** (3)
</dt> <dt>

<span id="real32"></span><span id="REAL32"></span>**real32** (4)
</dt> <dt>

<span id="real64"></span><span id="REAL64"></span>**real64** (5)
</dt> <dt>

<span id="sint16"></span><span id="SINT16"></span>**sint16** (6)
</dt> <dt>

<span id="sint32"></span><span id="SINT32"></span>**sint32** (7)
</dt> <dt>

<span id="sint64"></span><span id="SINT64"></span>**sint64** (8)
</dt> <dt>

<span id="sint8"></span><span id="SINT8"></span>**sint8** (9)
</dt> <dt>

<span id="string"></span><span id="STRING"></span>**cadeia de caracteres** (10)
</dt> <dt>

<span id="uint16"></span><span id="UINT16"></span>**UInt16** (11)
</dt> <dt>

<span id="uint32"></span><span id="UINT32"></span>**UInt32** (12)
</dt> <dt>

<span id="uint64"></span><span id="UINT64"></span>**UInt64** (13)
</dt> <dt>

<span id="uint8_"></span><span id="UINT8_"></span>**uint8** (14)
</dt> </dl>

</dd> <dt>

**Descrição**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Uma descrição do objeto . Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Um nome de exibição para o objeto. Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).

</dd> <dt>

**Gathertype**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Indica como os valores de métrica são coletados pela Instrumentação subjacente. Isso permite que o aplicativo cliente escolha a métrica certa para a finalidade. Essa propriedade é herdada do **CIM \_ BaseMetricDefinition**. Isso pode ser **nulo** ou um dos valores a seguir.



| Valor                                                                                                                                                                                                                                                                       | Significado                                                                                                                                                                                                                                                                   |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <dt></dt> <dt>0</dt> desconhecido </dl>                                                 | O tipo de coleta não é conhecido.<br/>                                                                                                                                                                                                                               |
| <span id="OnChange"></span><span id="onchange"></span><span id="ONCHANGE"></span><dl> <dt>**OnChange**</dt> <dt>2</dt> </dl>                                             | Os valores de métrica são atualizados imediatamente quando os valores dentro do recurso medido são alterados.<br/>                                                                                                                                                              |
| <span id="Periodic"></span><span id="periodic"></span><span id="PERIODIC"></span><dl> <dt>**Atividades periódicas**</dt> <dt>3</dt> </dl>                                             | Os valores de métrica são atualizados periodicamente. Por exemplo, para um aplicativo cliente, um valor de métrica que se aplica à hora atual aparecerá constante durante cada intervalo de coleta e, em seguida, salta para o novo valor no final de cada intervalo de coleta.<br/> |
| <span id="OnRequest"></span><span id="onrequest"></span><span id="ONREQUEST"></span><dl> <dt>**OnRequest**</dt> <dt>4</dt> </dl>                                         | O valor da métrica é determinado sempre que um aplicativo cliente lê-lo.<br/>                                                                                                                                                                                        |
| <span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span><dl> <dt>**DMTF reservado**</dt> <dt>5.. 32767</dt> </dl>                  |                                                                                                                                                                                                                                                                           |
| <span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span><dl> 32768 <dt> **reservado para fornecedor**</dt> <dt>.. 65535</dt> </dl> |                                                                                                                                                                                                                                                                           |



 

</dd> <dt>

**Id**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> <dt>

Qualificadores: **chave**
</dt> </dl>

Uma cadeia de caracteres que identifica exclusivamente a definição da métrica. Essa propriedade é herdada do **CIM \_ BaseMetricDefinition**.

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

**IsContinuous**
</dt> <dd> <dl> <dt>

Tipo de dados: **booliano**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Indica se o valor da métrica é contínuo ou escalar. As métricas de desempenho são um exemplo de uma métrica contínua. Exemplos de métricas escalares incluem códigos de erro ou Estados operacionais. Métricas contínuas podem ser comparadas usando a relação "maior que". Essa propriedade é herdada do **CIM \_ BaseMetricDefinition**.

</dd> <dt>

**Nome**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

O nome da métrica. Essa propriedade é herdada do **CIM \_ BaseMetricDefinition**.

</dd> <dt>

**ProgrammaticUnits**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Identifica as unidades específicas de um valor. O valor dessa propriedade será um valor válido do qualificador de unidades programáticas, conforme definido no Apêndice C. 1 de [DSP0004 v 2.4](https://www.dmtf.org/sites/default/files/standards/documents/DSP0004_2.5.0.pdf) ou posterior. Essa propriedade é herdada do **CIM \_ BaseMetricDefinition**.

</dd> <dt>

**Timescope**
</dt> <dd> <dl> <dt>

Tipo de dados: **UInt16**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Indica o escopo de tempo ao qual o valor de métrica se aplica. Essa propriedade é herdada do **CIM \_ BaseMetricDefinition**.



| Valor                                                                                                                                                                                                                                                                       | Significado                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <dt></dt> <dt>0</dt> desconhecido </dl>                                                 | O escopo de tempo não foi qualificado pelo designer de métrica ou é desconhecido para o provedor.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="Point"></span><span id="point"></span><span id="POINT"></span><dl> <dt>**Ponto**</dt> <dt>2</dt> </dl>                                                         | A métrica se aplica a um ponto no tempo. Nas instâncias [**Msvm \_ BaseMetricValue**](msvm-basemetricvalue.md) correspondentes, a propriedade **timestamp** especifica o ponto no tempo e a propriedade **Duration** é sempre 0.<br/>                                                                                                                                                                                                                                                                                              |
| <span id="Interval"></span><span id="interval"></span><span id="INTERVAL"></span><dl> <dt>**Intervalo**</dt> <dt>3</dt> </dl>                                             | A métrica se aplica a um intervalo de tempo. Nas instâncias [**Msvm \_ BaseMetricValue**](msvm-basemetricvalue.md) correspondentes, a propriedade **timestamp** especifica o final do intervalo de tempo e a propriedade **Duration** especifica sua duração.<br/>                                                                                                                                                                                                                                                                        |
| <span id="StartupInterval"></span><span id="startupinterval"></span><span id="STARTUPINTERVAL"></span><dl> <dt>**StartupInterval**</dt> <dt>4</dt> </dl>                 | A métrica se aplica a um intervalo de tempo que começou na inicialização do recurso medido (ou seja, o Managedelement associado por MetricDefForMe). Nas instâncias [**Msvm \_ BaseMetricValue**](msvm-basemetricvalue.md) correspondentes, a propriedade **timestamp** especifica o final do intervalo de tempo. Se a propriedade **Duration** for 0, isso indica que o tempo de inicialização do recurso medido é desconhecido. Caso contrário, **Duration** especificará a duração entre a inicialização do recurso e o **carimbo de data/hora**.<br/> |
| <span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span><dl> <dt>**DMTF reservado**</dt> <dt>5.. 32767</dt> </dl>                  |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span><dl> 32768 <dt> **reservado para fornecedor**</dt> <dt>.. 65535</dt> </dl> |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |



 

</dd> <dt>

**Unidades**
</dt> <dd> <dl> <dt>

Tipo de dados: **cadeia de caracteres**
</dt> <dt>

Tipo de acesso: Somente leitura
</dt> </dl>

Identifica as unidades específicas de um valor, por exemplo, "megabytes". Essa propriedade é herdada do **CIM \_ BaseMetricDefinition**.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 8\]<br/>                                                              |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2012\]<br/>                                                    |
| Namespace<br/>                | \\Virtualização \\ v2 de raiz<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

