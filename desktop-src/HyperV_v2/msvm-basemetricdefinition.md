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
# <a name="msvm_basemetricdefinition-class"></a><span data-ttu-id="9d58f-103">\_Classe Msvm BaseMetricDefinition</span><span class="sxs-lookup"><span data-stu-id="9d58f-103">Msvm\_BaseMetricDefinition class</span></span>

<span data-ttu-id="9d58f-104">Representa os aspectos de definição de uma métrica.</span><span class="sxs-lookup"><span data-stu-id="9d58f-104">Represents the definition aspects of a metric.</span></span> <span data-ttu-id="9d58f-105">A classe **Msvm \_ BaseMetricDefinition** deve ser associada ao [**\_ ManagedElements CIM**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) ao qual se aplica.</span><span class="sxs-lookup"><span data-stu-id="9d58f-105">The **Msvm\_BaseMetricDefinition** class should be associated with the [**CIM\_ManagedElements**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) to which it applies.</span></span>

<span data-ttu-id="9d58f-106">A sintaxe a seguir é simplificada formato MOF código (MOF) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="9d58f-106">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="9d58f-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9d58f-107">Syntax</span></span>

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

## <a name="members"></a><span data-ttu-id="9d58f-108">Membros</span><span class="sxs-lookup"><span data-stu-id="9d58f-108">Members</span></span>

<span data-ttu-id="9d58f-109">A classe **Msvm \_ BaseMetricDefinition** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="9d58f-109">The **Msvm\_BaseMetricDefinition** class has these types of members:</span></span>

-   [<span data-ttu-id="9d58f-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="9d58f-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="9d58f-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="9d58f-111">Properties</span></span>

<span data-ttu-id="9d58f-112">A classe **Msvm \_ BaseMetricDefinition** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="9d58f-112">The **Msvm\_BaseMetricDefinition** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="9d58f-113">**BreakdownDimensions**</span><span class="sxs-lookup"><span data-stu-id="9d58f-113">**BreakdownDimensions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d58f-114">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="9d58f-114">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="9d58f-115">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9d58f-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9d58f-116">Define uma ou mais cadeias de caracteres que podem ser usadas para refinar (dividir) consultas em relação aos valores de métrica em uma determinada dimensão.</span><span class="sxs-lookup"><span data-stu-id="9d58f-116">Defines one or more strings that can be used to refine (break down) queries against the metric values along a certain dimension.</span></span> <span data-ttu-id="9d58f-117">Um exemplo é um nome de transação, permitindo a interrupção do valor total de todas as transações em um conjunto de valores, uma para cada nome de transação.</span><span class="sxs-lookup"><span data-stu-id="9d58f-117">An example is a transaction name, allowing the break down of the total value for all transactions into a set of values, one for each transaction name.</span></span> <span data-ttu-id="9d58f-118">Outros exemplos podem ser o nome do grupo de usuários ou do sistema de aplicativos.</span><span class="sxs-lookup"><span data-stu-id="9d58f-118">Other examples might be application system or user group name.</span></span> <span data-ttu-id="9d58f-119">As cadeias de caracteres são de formato livre e devem ser significativas para os usuários finais dos dados da métrica.</span><span class="sxs-lookup"><span data-stu-id="9d58f-119">The strings are free format and should be meaningful to the end users of the metric data.</span></span> <span data-ttu-id="9d58f-120">As cadeias de caracteres indicam quais dimensões de divisão são suportadas para essa definição de métrica, pela Instrumentação subjacente.</span><span class="sxs-lookup"><span data-stu-id="9d58f-120">The strings indicate which break down dimensions are supported for this metric definition, by the underlying instrumentation.</span></span> <span data-ttu-id="9d58f-121">Essa propriedade é herdada do **CIM \_ BaseMetricDefinition**.</span><span class="sxs-lookup"><span data-stu-id="9d58f-121">This property is inherited from **CIM\_BaseMetricDefinition**.</span></span>

</dd> <dt>

<span data-ttu-id="9d58f-122">**Calculável**</span><span class="sxs-lookup"><span data-stu-id="9d58f-122">**Calculable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d58f-123">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9d58f-123">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9d58f-124">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9d58f-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9d58f-125">Descreve as características da métrica para fins de execução de cálculos.</span><span class="sxs-lookup"><span data-stu-id="9d58f-125">Describes the characteristics of the metric for purposes of performing calculations.</span></span> <span data-ttu-id="9d58f-126">Essa propriedade é herdada do **CIM \_ BaseMetricDefinition**.</span><span class="sxs-lookup"><span data-stu-id="9d58f-126">This property is inherited from **CIM\_BaseMetricDefinition**.</span></span> <span data-ttu-id="9d58f-127">Isso pode ser **nulo** ou um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="9d58f-127">This may be **Null** or one of the following values.</span></span>



| <span data-ttu-id="9d58f-128">Valor</span><span class="sxs-lookup"><span data-stu-id="9d58f-128">Value</span></span>                                                                                                                                                                                                                                                   | <span data-ttu-id="9d58f-129">Significado</span><span class="sxs-lookup"><span data-stu-id="9d58f-129">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Non-calculable"></span><span id="non-calculable"></span><span id="NON-CALCULABLE"></span><dl> <span data-ttu-id="9d58f-130"><dt>**Não calculável**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="9d58f-130"><dt>**Non-calculable**</dt> <dt>1</dt></span></span> </dl> | <span data-ttu-id="9d58f-131">O valor não pode ser calculado.</span><span class="sxs-lookup"><span data-stu-id="9d58f-131">The value cannot be calculated.</span></span> <span data-ttu-id="9d58f-132">Por exemplo, uma cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="9d58f-132">For example, a string.</span></span><br/>                                                                                                                                                                                                                                                                                                         |
| <span id="Summable"></span><span id="summable"></span><span id="SUMMABLE"></span><dl> <span data-ttu-id="9d58f-133"><dt>**Res**</dt> . <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="9d58f-133"><dt>**Summable**</dt> <dt>2</dt></span></span> </dl>                         | <span data-ttu-id="9d58f-134">O valor pode ser somado em várias instâncias.</span><span class="sxs-lookup"><span data-stu-id="9d58f-134">The value can be summed over many instances.</span></span> <span data-ttu-id="9d58f-135">Por exemplo, se cada trabalho de backup é uma unidade de trabalho e cada trabalho faz backup de 27.000 arquivos em média, 100 os trabalhos de backup processaram 2,7 milhões arquivos.</span><span class="sxs-lookup"><span data-stu-id="9d58f-135">For example, if each backup job is a unit of work, and each job backs up 27,000 files on average, then 100 backup jobs processed 2,700,000 files.</span></span><br/>                                                                                                                                                                 |
| <span id="Non-summable_"></span><span id="non-summable_"></span><span id="NON-SUMMABLE_"></span><dl> <span data-ttu-id="9d58f-136"><dt> **Não resumible**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="9d58f-136"><dt>**Non-summable** </dt> <dt>3 </dt></span></span> </dl>    | <span data-ttu-id="9d58f-137">Esse valor não pode ser somado em várias instâncias.</span><span class="sxs-lookup"><span data-stu-id="9d58f-137">This value cannot be summed over many instances.</span></span> <span data-ttu-id="9d58f-138">Um exemplo seria uma métrica que mede o comprimento da fila quando um trabalho chega a um servidor.</span><span class="sxs-lookup"><span data-stu-id="9d58f-138">An example would be a metric that measures the queue length when a job arrives at a server.</span></span> <span data-ttu-id="9d58f-139">Se cada trabalho é uma unidade de trabalho e o comprimento médio da fila quando cada trabalho chega é 33, não faz sentido dizer que o comprimento da fila para 100 trabalhos é 3300.</span><span class="sxs-lookup"><span data-stu-id="9d58f-139">If each job is a unit of work, and the average queue length when each job arrives is 33, it does not make sense to say that the queue length for 100 jobs is 3300.</span></span> <span data-ttu-id="9d58f-140">Faz sentido dizer que a média é de 33.</span><span class="sxs-lookup"><span data-stu-id="9d58f-140">It does make sense to say that the mean is 33.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="9d58f-141">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="9d58f-141">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d58f-142">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="9d58f-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9d58f-143">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9d58f-143">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9d58f-144">Uma breve descrição do objeto.</span><span class="sxs-lookup"><span data-stu-id="9d58f-144">A short description of the object.</span></span> <span data-ttu-id="9d58f-145">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="9d58f-145">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="9d58f-146">**ChangeType**</span><span class="sxs-lookup"><span data-stu-id="9d58f-146">**ChangeType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d58f-147">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9d58f-147">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9d58f-148">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9d58f-148">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9d58f-149">Indica como o valor da métrica é alterado, na forma de combinações típicas de atributos de detalhamento mais detalhados, como alteração de direção, valores mínimos e máximos e semântica de encapsulamento.</span><span class="sxs-lookup"><span data-stu-id="9d58f-149">Indicates how the metric value changes, in the form of typical combinations of finer grain attributes such as direction change, minimum and maximum values, and wrapping semantics.</span></span> <span data-ttu-id="9d58f-150">Essa propriedade é herdada do **CIM \_ BaseMetricDefinition**.</span><span class="sxs-lookup"><span data-stu-id="9d58f-150">This property is inherited from **CIM\_BaseMetricDefinition**.</span></span>



| <span data-ttu-id="9d58f-151">Valor</span><span class="sxs-lookup"><span data-stu-id="9d58f-151">Value</span></span>                                                                                                                                                                                                                                                                       | <span data-ttu-id="9d58f-152">Significado</span><span class="sxs-lookup"><span data-stu-id="9d58f-152">Meaning</span></span>                                                                                                                                                                                          |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <span data-ttu-id="9d58f-153"><dt></dt> <dt>0</dt> desconhecido</span><span class="sxs-lookup"><span data-stu-id="9d58f-153"><dt>**Unknown**</dt> <dt>0</dt></span></span> </dl>                                                 | <span data-ttu-id="9d58f-154">O designer de métrica não qualificou o **ChangeType.**.</span><span class="sxs-lookup"><span data-stu-id="9d58f-154">The metric designer did not qualify the **ChangeType.**.</span></span><br/>                                                                                                                              |
| <span id="N_A"></span><span id="n_a"></span><dl> <span data-ttu-id="9d58f-155"><dt>**N/A**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="9d58f-155"><dt>**N/A**</dt> <dt>2</dt></span></span> </dl>                                                                                       | <span data-ttu-id="9d58f-156">Se a propriedade **Iscontinuous** for "false", **altertype** não faz sentido e deve ser definida como "N/A".</span><span class="sxs-lookup"><span data-stu-id="9d58f-156">If the **IsContinuous** property is "false", **ChangeType** does not make sense and must be set to "N/A".</span></span><br/>                                                                             |
| <span id="Counter"></span><span id="counter"></span><span id="COUNTER"></span><dl> <span data-ttu-id="9d58f-157"><dt>**Contador**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="9d58f-157"><dt>**Counter**</dt> <dt>3</dt></span></span> </dl>                                                 | <span data-ttu-id="9d58f-158">A métrica é uma métrica de contador.</span><span class="sxs-lookup"><span data-stu-id="9d58f-158">The metric is a counter metric.</span></span> <span data-ttu-id="9d58f-159">Eles têm valores inteiros não negativos que aumentam até atingir o número máximo reapresentável e, em seguida, encapsular e começar a aumentar de 0.</span><span class="sxs-lookup"><span data-stu-id="9d58f-159">These have nonnegative integer values that increase until reaching the maximum representable number and then wrap around and start increasing from 0.</span></span><br/> |
| <span id="Gauge"></span><span id="gauge"></span><span id="GAUGE"></span><dl> <span data-ttu-id="9d58f-160"><dt>**Indicador**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="9d58f-160"><dt>**Gauge**</dt> <dt>4</dt></span></span> </dl>                                                         | <span data-ttu-id="9d58f-161">A métrica é uma métrica de medidor.</span><span class="sxs-lookup"><span data-stu-id="9d58f-161">The metric is a gauge metric.</span></span> <span data-ttu-id="9d58f-162">Eles têm valores inteiros ou flutuantes que podem aumentar e diminuir arbitrariamente.</span><span class="sxs-lookup"><span data-stu-id="9d58f-162">These have integer or float values that can increase and decrease arbitrarily.</span></span><br/>                                                                          |
| <span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span><dl> <span data-ttu-id="9d58f-163"><dt>**DMTF reservado**</dt> <dt>5.. 32767</dt></span><span class="sxs-lookup"><span data-stu-id="9d58f-163"><dt>**DMTF Reserved**</dt> <dt>5..32767</dt></span></span> </dl>                  |                                                                                                                                                                                                  |
| <span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span><dl> <span data-ttu-id="9d58f-164">32768 <dt> **reservado para fornecedor**</dt> <dt>.. 65535</dt></span><span class="sxs-lookup"><span data-stu-id="9d58f-164"><dt>**Vendor Reserved** </dt> <dt>32768..65535 </dt></span></span> </dl> | <span data-ttu-id="9d58f-165">Os fornecedores podem estender a propriedade **altertype** no intervalo reservado do fornecedor.</span><span class="sxs-lookup"><span data-stu-id="9d58f-165">Vendors may extend the **ChangeType** property in the vendor reserved range.</span></span><br/>                                                                                                          |



 

</dd> <dt>

<span data-ttu-id="9d58f-166">**DataType**</span><span class="sxs-lookup"><span data-stu-id="9d58f-166">**DataType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d58f-167">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9d58f-167">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9d58f-168">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9d58f-168">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9d58f-169">O tipo de dados da métrica.</span><span class="sxs-lookup"><span data-stu-id="9d58f-169">The data type of the metric.</span></span> <span data-ttu-id="9d58f-170">Essa propriedade é herdada do **CIM \_ BaseMetricDefinition**.</span><span class="sxs-lookup"><span data-stu-id="9d58f-170">This property is inherited from **CIM\_BaseMetricDefinition**.</span></span>

<dl> <dt>

<span data-ttu-id="9d58f-171"><span id="boolean"></span><span id="BOOLEAN"></span>**booliano** (1)</span><span class="sxs-lookup"><span data-stu-id="9d58f-171"><span id="boolean"></span><span id="BOOLEAN"></span>**boolean** (1)</span></span>
</dt> <dt>

<span data-ttu-id="9d58f-172"><span id="char16"></span><span id="CHAR16"></span>**char16** (2)</span><span class="sxs-lookup"><span data-stu-id="9d58f-172"><span id="char16"></span><span id="CHAR16"></span>**char16** (2)</span></span>
</dt> <dt>

<span data-ttu-id="9d58f-173"><span id="datetime"></span><span id="DATETIME"></span>**data e hora** (3)</span><span class="sxs-lookup"><span data-stu-id="9d58f-173"><span id="datetime"></span><span id="DATETIME"></span>**datetime** (3)</span></span>
</dt> <dt>

<span data-ttu-id="9d58f-174"><span id="real32"></span><span id="REAL32"></span>**real32** (4)</span><span class="sxs-lookup"><span data-stu-id="9d58f-174"><span id="real32"></span><span id="REAL32"></span>**real32** (4)</span></span>
</dt> <dt>

<span data-ttu-id="9d58f-175"><span id="real64"></span><span id="REAL64"></span>**real64** (5)</span><span class="sxs-lookup"><span data-stu-id="9d58f-175"><span id="real64"></span><span id="REAL64"></span>**real64** (5)</span></span>
</dt> <dt>

<span data-ttu-id="9d58f-176"><span id="sint16"></span><span id="SINT16"></span>**sint16** (6)</span><span class="sxs-lookup"><span data-stu-id="9d58f-176"><span id="sint16"></span><span id="SINT16"></span>**sint16** (6)</span></span>
</dt> <dt>

<span data-ttu-id="9d58f-177"><span id="sint32"></span><span id="SINT32"></span>**sint32** (7)</span><span class="sxs-lookup"><span data-stu-id="9d58f-177"><span id="sint32"></span><span id="SINT32"></span>**sint32** (7)</span></span>
</dt> <dt>

<span data-ttu-id="9d58f-178"><span id="sint64"></span><span id="SINT64"></span>**sint64** (8)</span><span class="sxs-lookup"><span data-stu-id="9d58f-178"><span id="sint64"></span><span id="SINT64"></span>**sint64** (8)</span></span>
</dt> <dt>

<span data-ttu-id="9d58f-179"><span id="sint8"></span><span id="SINT8"></span>**sint8** (9)</span><span class="sxs-lookup"><span data-stu-id="9d58f-179"><span id="sint8"></span><span id="SINT8"></span>**sint8** (9)</span></span>
</dt> <dt>

<span data-ttu-id="9d58f-180"><span id="string"></span><span id="STRING"></span>**cadeia de caracteres** (10)</span><span class="sxs-lookup"><span data-stu-id="9d58f-180"><span id="string"></span><span id="STRING"></span>**string** (10)</span></span>
</dt> <dt>

<span data-ttu-id="9d58f-181"><span id="uint16"></span><span id="UINT16"></span>**UInt16** (11)</span><span class="sxs-lookup"><span data-stu-id="9d58f-181"><span id="uint16"></span><span id="UINT16"></span>**uint16** (11)</span></span>
</dt> <dt>

<span data-ttu-id="9d58f-182"><span id="uint32"></span><span id="UINT32"></span>**UInt32** (12)</span><span class="sxs-lookup"><span data-stu-id="9d58f-182"><span id="uint32"></span><span id="UINT32"></span>**uint32** (12)</span></span>
</dt> <dt>

<span data-ttu-id="9d58f-183"><span id="uint64"></span><span id="UINT64"></span>**UInt64** (13)</span><span class="sxs-lookup"><span data-stu-id="9d58f-183"><span id="uint64"></span><span id="UINT64"></span>**uint64** (13)</span></span>
</dt> <dt>

<span data-ttu-id="9d58f-184"><span id="uint8_"></span><span id="UINT8_"></span>**uint8** (14)</span><span class="sxs-lookup"><span data-stu-id="9d58f-184"><span id="uint8_"></span><span id="UINT8_"></span>**uint8** (14 )</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="9d58f-185">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="9d58f-185">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d58f-186">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="9d58f-186">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9d58f-187">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9d58f-187">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9d58f-188">Uma descrição do objeto .</span><span class="sxs-lookup"><span data-stu-id="9d58f-188">A description of the object.</span></span> <span data-ttu-id="9d58f-189">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="9d58f-189">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="9d58f-190">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="9d58f-190">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d58f-191">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="9d58f-191">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9d58f-192">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9d58f-192">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9d58f-193">Um nome de exibição para o objeto.</span><span class="sxs-lookup"><span data-stu-id="9d58f-193">A display name for the object.</span></span> <span data-ttu-id="9d58f-194">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="9d58f-194">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="9d58f-195">**Gathertype**</span><span class="sxs-lookup"><span data-stu-id="9d58f-195">**GatheringType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d58f-196">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9d58f-196">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9d58f-197">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9d58f-197">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9d58f-198">Indica como os valores de métrica são coletados pela Instrumentação subjacente.</span><span class="sxs-lookup"><span data-stu-id="9d58f-198">Indicates how the metric values are gathered by the underlying instrumentation.</span></span> <span data-ttu-id="9d58f-199">Isso permite que o aplicativo cliente escolha a métrica certa para a finalidade.</span><span class="sxs-lookup"><span data-stu-id="9d58f-199">This allows the client application to choose the right metric for the purpose.</span></span> <span data-ttu-id="9d58f-200">Essa propriedade é herdada do **CIM \_ BaseMetricDefinition**.</span><span class="sxs-lookup"><span data-stu-id="9d58f-200">This property is inherited from **CIM\_BaseMetricDefinition**.</span></span> <span data-ttu-id="9d58f-201">Isso pode ser **nulo** ou um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="9d58f-201">This may be **Null** or one of the following values.</span></span>



| <span data-ttu-id="9d58f-202">Valor</span><span class="sxs-lookup"><span data-stu-id="9d58f-202">Value</span></span>                                                                                                                                                                                                                                                                       | <span data-ttu-id="9d58f-203">Significado</span><span class="sxs-lookup"><span data-stu-id="9d58f-203">Meaning</span></span>                                                                                                                                                                                                                                                                   |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <span data-ttu-id="9d58f-204"><dt></dt> <dt>0</dt> desconhecido</span><span class="sxs-lookup"><span data-stu-id="9d58f-204"><dt>**Unknown**</dt> <dt>0</dt></span></span> </dl>                                                 | <span data-ttu-id="9d58f-205">O tipo de coleta não é conhecido.</span><span class="sxs-lookup"><span data-stu-id="9d58f-205">The gathering type is not known.</span></span><br/>                                                                                                                                                                                                                               |
| <span id="OnChange"></span><span id="onchange"></span><span id="ONCHANGE"></span><dl> <span data-ttu-id="9d58f-206"><dt>**OnChange**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="9d58f-206"><dt>**OnChange**</dt> <dt>2</dt></span></span> </dl>                                             | <span data-ttu-id="9d58f-207">Os valores de métrica são atualizados imediatamente quando os valores dentro do recurso medido são alterados.</span><span class="sxs-lookup"><span data-stu-id="9d58f-207">The metric values get updated immediately when the values inside of the measured resource change.</span></span><br/>                                                                                                                                                              |
| <span id="Periodic"></span><span id="periodic"></span><span id="PERIODIC"></span><dl> <span data-ttu-id="9d58f-208"><dt>**Atividades periódicas**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="9d58f-208"><dt>**Periodic**</dt> <dt>3</dt></span></span> </dl>                                             | <span data-ttu-id="9d58f-209">Os valores de métrica são atualizados periodicamente.</span><span class="sxs-lookup"><span data-stu-id="9d58f-209">The metric values get updated periodically.</span></span> <span data-ttu-id="9d58f-210">Por exemplo, para um aplicativo cliente, um valor de métrica que se aplica à hora atual aparecerá constante durante cada intervalo de coleta e, em seguida, salta para o novo valor no final de cada intervalo de coleta.</span><span class="sxs-lookup"><span data-stu-id="9d58f-210">For instance, to a client application, a metric value that applies to the current time will appear constant during each gathering interval, and then jumps to the new value at the end of each gathering interval.</span></span><br/> |
| <span id="OnRequest"></span><span id="onrequest"></span><span id="ONREQUEST"></span><dl> <span data-ttu-id="9d58f-211"><dt>**OnRequest**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="9d58f-211"><dt>**OnRequest**</dt> <dt>4</dt></span></span> </dl>                                         | <span data-ttu-id="9d58f-212">O valor da métrica é determinado sempre que um aplicativo cliente lê-lo.</span><span class="sxs-lookup"><span data-stu-id="9d58f-212">The metric value is determined each time a client application reads it.</span></span><br/>                                                                                                                                                                                        |
| <span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span><dl> <span data-ttu-id="9d58f-213"><dt>**DMTF reservado**</dt> <dt>5.. 32767</dt></span><span class="sxs-lookup"><span data-stu-id="9d58f-213"><dt>**DMTF Reserved**</dt> <dt>5..32767</dt></span></span> </dl>                  |                                                                                                                                                                                                                                                                           |
| <span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span><dl> <span data-ttu-id="9d58f-214">32768 <dt> **reservado para fornecedor**</dt> <dt>.. 65535</dt></span><span class="sxs-lookup"><span data-stu-id="9d58f-214"><dt>**Vendor Reserved** </dt> <dt>32768..65535 </dt></span></span> </dl> |                                                                                                                                                                                                                                                                           |



 

</dd> <dt>

<span data-ttu-id="9d58f-215">**Id**</span><span class="sxs-lookup"><span data-stu-id="9d58f-215">**Id**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d58f-216">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="9d58f-216">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9d58f-217">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9d58f-217">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9d58f-218">Qualificadores: **chave**</span><span class="sxs-lookup"><span data-stu-id="9d58f-218">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="9d58f-219">Uma cadeia de caracteres que identifica exclusivamente a definição da métrica.</span><span class="sxs-lookup"><span data-stu-id="9d58f-219">A string that uniquely identifies the metric definition.</span></span> <span data-ttu-id="9d58f-220">Essa propriedade é herdada do **CIM \_ BaseMetricDefinition**.</span><span class="sxs-lookup"><span data-stu-id="9d58f-220">This property is inherited from **CIM\_BaseMetricDefinition**.</span></span>

</dd> <dt>

<span data-ttu-id="9d58f-221">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="9d58f-221">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d58f-222">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="9d58f-222">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9d58f-223">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9d58f-223">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9d58f-224">Qualificadores: **chave**</span><span class="sxs-lookup"><span data-stu-id="9d58f-224">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="9d58f-225">Uma cadeia de caracteres que identifica exclusivamente uma instância dessa classe.</span><span class="sxs-lookup"><span data-stu-id="9d58f-225">A string that uniquely identifies an instance of this class.</span></span> <span data-ttu-id="9d58f-226">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="9d58f-226">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="9d58f-227">**IsContinuous**</span><span class="sxs-lookup"><span data-stu-id="9d58f-227">**IsContinuous**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d58f-228">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="9d58f-228">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="9d58f-229">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9d58f-229">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9d58f-230">Indica se o valor da métrica é contínuo ou escalar.</span><span class="sxs-lookup"><span data-stu-id="9d58f-230">Indicates whether the metric value is continuous or scalar.</span></span> <span data-ttu-id="9d58f-231">As métricas de desempenho são um exemplo de uma métrica contínua.</span><span class="sxs-lookup"><span data-stu-id="9d58f-231">Performance metrics are an example of a continuous metric.</span></span> <span data-ttu-id="9d58f-232">Exemplos de métricas escalares incluem códigos de erro ou Estados operacionais.</span><span class="sxs-lookup"><span data-stu-id="9d58f-232">Examples of scalar metrics include error codes or operational states.</span></span> <span data-ttu-id="9d58f-233">Métricas contínuas podem ser comparadas usando a relação "maior que".</span><span class="sxs-lookup"><span data-stu-id="9d58f-233">Continuous metrics can be compared by using the "greater than" relation.</span></span> <span data-ttu-id="9d58f-234">Essa propriedade é herdada do **CIM \_ BaseMetricDefinition**.</span><span class="sxs-lookup"><span data-stu-id="9d58f-234">This property is inherited from **CIM\_BaseMetricDefinition**.</span></span>

</dd> <dt>

<span data-ttu-id="9d58f-235">**Nome**</span><span class="sxs-lookup"><span data-stu-id="9d58f-235">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d58f-236">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="9d58f-236">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9d58f-237">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9d58f-237">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9d58f-238">O nome da métrica.</span><span class="sxs-lookup"><span data-stu-id="9d58f-238">The name of the metric.</span></span> <span data-ttu-id="9d58f-239">Essa propriedade é herdada do **CIM \_ BaseMetricDefinition**.</span><span class="sxs-lookup"><span data-stu-id="9d58f-239">This property is inherited from **CIM\_BaseMetricDefinition**.</span></span>

</dd> <dt>

<span data-ttu-id="9d58f-240">**ProgrammaticUnits**</span><span class="sxs-lookup"><span data-stu-id="9d58f-240">**ProgrammaticUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d58f-241">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="9d58f-241">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9d58f-242">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9d58f-242">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9d58f-243">Identifica as unidades específicas de um valor.</span><span class="sxs-lookup"><span data-stu-id="9d58f-243">Identifies the specific units of a value.</span></span> <span data-ttu-id="9d58f-244">O valor dessa propriedade será um valor válido do qualificador de unidades programáticas, conforme definido no Apêndice C. 1 de [DSP0004 v 2.4](https://www.dmtf.org/sites/default/files/standards/documents/DSP0004_2.5.0.pdf) ou posterior.</span><span class="sxs-lookup"><span data-stu-id="9d58f-244">The value of this property will be a legal value of the Programmatic Units qualifier as defined in Appendix C.1 of [DSP0004 V2.4](https://www.dmtf.org/sites/default/files/standards/documents/DSP0004_2.5.0.pdf) or later.</span></span> <span data-ttu-id="9d58f-245">Essa propriedade é herdada do **CIM \_ BaseMetricDefinition**.</span><span class="sxs-lookup"><span data-stu-id="9d58f-245">This property is inherited from **CIM\_BaseMetricDefinition**.</span></span>

</dd> <dt>

<span data-ttu-id="9d58f-246">**Timescope**</span><span class="sxs-lookup"><span data-stu-id="9d58f-246">**TimeScope**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d58f-247">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="9d58f-247">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="9d58f-248">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9d58f-248">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9d58f-249">Indica o escopo de tempo ao qual o valor de métrica se aplica.</span><span class="sxs-lookup"><span data-stu-id="9d58f-249">Indicates the time scope to which the metric value applies.</span></span> <span data-ttu-id="9d58f-250">Essa propriedade é herdada do **CIM \_ BaseMetricDefinition**.</span><span class="sxs-lookup"><span data-stu-id="9d58f-250">This property is inherited from **CIM\_BaseMetricDefinition**.</span></span>



| <span data-ttu-id="9d58f-251">Valor</span><span class="sxs-lookup"><span data-stu-id="9d58f-251">Value</span></span>                                                                                                                                                                                                                                                                       | <span data-ttu-id="9d58f-252">Significado</span><span class="sxs-lookup"><span data-stu-id="9d58f-252">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span><dl> <span data-ttu-id="9d58f-253"><dt></dt> <dt>0</dt> desconhecido</span><span class="sxs-lookup"><span data-stu-id="9d58f-253"><dt>**Unknown**</dt> <dt>0</dt></span></span> </dl>                                                 | <span data-ttu-id="9d58f-254">O escopo de tempo não foi qualificado pelo designer de métrica ou é desconhecido para o provedor.</span><span class="sxs-lookup"><span data-stu-id="9d58f-254">The time scope was not qualified by the metric designer or is unknown to the provider.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="Point"></span><span id="point"></span><span id="POINT"></span><dl> <span data-ttu-id="9d58f-255"><dt>**Ponto**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="9d58f-255"><dt>**Point**</dt> <dt>2</dt></span></span> </dl>                                                         | <span data-ttu-id="9d58f-256">A métrica se aplica a um ponto no tempo.</span><span class="sxs-lookup"><span data-stu-id="9d58f-256">The metric applies to a point in time.</span></span> <span data-ttu-id="9d58f-257">Nas instâncias [**Msvm \_ BaseMetricValue**](msvm-basemetricvalue.md) correspondentes, a propriedade **timestamp** especifica o ponto no tempo e a propriedade **Duration** é sempre 0.</span><span class="sxs-lookup"><span data-stu-id="9d58f-257">On the corresponding [**Msvm\_BaseMetricValue**](msvm-basemetricvalue.md) instances, the **TimeStamp** property specifies the point in time, and the **Duration** property is always 0.</span></span><br/>                                                                                                                                                                                                                                                                                              |
| <span id="Interval"></span><span id="interval"></span><span id="INTERVAL"></span><dl> <span data-ttu-id="9d58f-258"><dt>**Intervalo**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="9d58f-258"><dt>**Interval**</dt> <dt>3</dt></span></span> </dl>                                             | <span data-ttu-id="9d58f-259">A métrica se aplica a um intervalo de tempo.</span><span class="sxs-lookup"><span data-stu-id="9d58f-259">The metric applies to a time interval.</span></span> <span data-ttu-id="9d58f-260">Nas instâncias [**Msvm \_ BaseMetricValue**](msvm-basemetricvalue.md) correspondentes, a propriedade **timestamp** especifica o final do intervalo de tempo e a propriedade **Duration** especifica sua duração.</span><span class="sxs-lookup"><span data-stu-id="9d58f-260">On the corresponding [**Msvm\_BaseMetricValue**](msvm-basemetricvalue.md) instances, the **TimeStamp** property specifies the end of the time interval, and the **Duration** property specifies its duration.</span></span><br/>                                                                                                                                                                                                                                                                        |
| <span id="StartupInterval"></span><span id="startupinterval"></span><span id="STARTUPINTERVAL"></span><dl> <span data-ttu-id="9d58f-261"><dt>**StartupInterval**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="9d58f-261"><dt>**StartupInterval**</dt> <dt>4</dt></span></span> </dl>                 | <span data-ttu-id="9d58f-262">A métrica se aplica a um intervalo de tempo que começou na inicialização do recurso medido (ou seja, o Managedelement associado por MetricDefForMe).</span><span class="sxs-lookup"><span data-stu-id="9d58f-262">The metric applies to a time interval that began at the startup of the measured resource (that is, the ManagedElement associated by MetricDefForMe).</span></span> <span data-ttu-id="9d58f-263">Nas instâncias [**Msvm \_ BaseMetricValue**](msvm-basemetricvalue.md) correspondentes, a propriedade **timestamp** especifica o final do intervalo de tempo.</span><span class="sxs-lookup"><span data-stu-id="9d58f-263">On the corresponding [**Msvm\_BaseMetricValue**](msvm-basemetricvalue.md) instances, the **TimeStamp** property specifies the end of the time interval.</span></span> <span data-ttu-id="9d58f-264">Se a propriedade **Duration** for 0, isso indica que o tempo de inicialização do recurso medido é desconhecido.</span><span class="sxs-lookup"><span data-stu-id="9d58f-264">If the **Duration** property is 0, this indicates that the startup time of the measured resource is unknown.</span></span> <span data-ttu-id="9d58f-265">Caso contrário, **Duration** especificará a duração entre a inicialização do recurso e o **carimbo de data/hora**.</span><span class="sxs-lookup"><span data-stu-id="9d58f-265">Otherwise, **Duration** specifies the duration between startup of the resource and **TimeStamp**.</span></span><br/> |
| <span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span><dl> <span data-ttu-id="9d58f-266"><dt>**DMTF reservado**</dt> <dt>5.. 32767</dt></span><span class="sxs-lookup"><span data-stu-id="9d58f-266"><dt>**DMTF Reserved**</dt> <dt>5..32767</dt></span></span> </dl>                  |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span id="Vendor_Reserved_"></span><span id="vendor_reserved_"></span><span id="VENDOR_RESERVED_"></span><dl> <span data-ttu-id="9d58f-267">32768 <dt> **reservado para fornecedor**</dt> <dt>.. 65535</dt></span><span class="sxs-lookup"><span data-stu-id="9d58f-267"><dt>**Vendor Reserved** </dt> <dt>32768..65535 </dt></span></span> </dl> |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |



 

</dd> <dt>

<span data-ttu-id="9d58f-268">**Unidades**</span><span class="sxs-lookup"><span data-stu-id="9d58f-268">**Units**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9d58f-269">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="9d58f-269">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9d58f-270">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9d58f-270">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9d58f-271">Identifica as unidades específicas de um valor, por exemplo, "megabytes".</span><span class="sxs-lookup"><span data-stu-id="9d58f-271">Identifies the specific units of a value, for example, "megabytes".</span></span> <span data-ttu-id="9d58f-272">Essa propriedade é herdada do **CIM \_ BaseMetricDefinition**.</span><span class="sxs-lookup"><span data-stu-id="9d58f-272">This property is inherited from **CIM\_BaseMetricDefinition**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="9d58f-273">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9d58f-273">Requirements</span></span>



| <span data-ttu-id="9d58f-274">Requisito</span><span class="sxs-lookup"><span data-stu-id="9d58f-274">Requirement</span></span> | <span data-ttu-id="9d58f-275">Valor</span><span class="sxs-lookup"><span data-stu-id="9d58f-275">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9d58f-276">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9d58f-276">Minimum supported client</span></span><br/> | <span data-ttu-id="9d58f-277">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="9d58f-277">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="9d58f-278">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9d58f-278">Minimum supported server</span></span><br/> | <span data-ttu-id="9d58f-279">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="9d58f-279">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="9d58f-280">Namespace</span><span class="sxs-lookup"><span data-stu-id="9d58f-280">Namespace</span></span><br/>                | <span data-ttu-id="9d58f-281">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="9d58f-281">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="9d58f-282">MOF</span><span class="sxs-lookup"><span data-stu-id="9d58f-282">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9d58f-283"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9d58f-283"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="9d58f-284">DLL</span><span class="sxs-lookup"><span data-stu-id="9d58f-284">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9d58f-285"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="9d58f-285"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

