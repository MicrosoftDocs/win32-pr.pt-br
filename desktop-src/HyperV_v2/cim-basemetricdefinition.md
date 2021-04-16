---
description: Representa uma definição de métrica que contém os metadados para um \_ objeto CIM MetricInstance.
ms.assetid: 6abfb0dc-e80b-4ca6-89d9-2e43283d0abe
title: Classe CIM_BaseMetricDefinition
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_BaseMetricDefinition
- CIM_BaseMetricDefinition.Id
- CIM_BaseMetricDefinition.Name
- CIM_BaseMetricDefinition.DataType
- CIM_BaseMetricDefinition.Calculable
- CIM_BaseMetricDefinition.Units
- CIM_BaseMetricDefinition.BreakdownDimensions
- CIM_BaseMetricDefinition.IsContinuous
- CIM_BaseMetricDefinition.ChangeType
- CIM_BaseMetricDefinition.TimeScope
- CIM_BaseMetricDefinition.GatheringType
- CIM_BaseMetricDefinition.ProgrammaticUnits
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: cac965ed1eae59f1c269d897a12e9aa116183eb4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105757552"
---
# <a name="cim_basemetricdefinition-class"></a><span data-ttu-id="b0f25-103">\_Classe CIM BaseMetricDefinition</span><span class="sxs-lookup"><span data-stu-id="b0f25-103">CIM\_BaseMetricDefinition class</span></span>

<span data-ttu-id="b0f25-104">Representa uma definição de métrica que contém os metadados para um objeto **CIM \_ MetricInstance** .</span><span class="sxs-lookup"><span data-stu-id="b0f25-104">Represents a metric definition that contains the meta data for a **CIM\_MetricInstance** object.</span></span>

## <a name="syntax"></a><span data-ttu-id="b0f25-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b0f25-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.22.0"), UMLPackagePath("CIM::Metrics::BaseMetric"), AMENDMENT]
class CIM_BaseMetricDefinition : CIM_ManagedElement
{
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

## <a name="members"></a><span data-ttu-id="b0f25-106">Membros</span><span class="sxs-lookup"><span data-stu-id="b0f25-106">Members</span></span>

<span data-ttu-id="b0f25-107">A classe **CIM \_ BaseMetricDefinition** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="b0f25-107">The **CIM\_BaseMetricDefinition** class has these types of members:</span></span>

-   [<span data-ttu-id="b0f25-108">Propriedades</span><span class="sxs-lookup"><span data-stu-id="b0f25-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b0f25-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="b0f25-109">Properties</span></span>

<span data-ttu-id="b0f25-110">A classe **CIM \_ BaseMetricDefinition** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="b0f25-110">The **CIM\_BaseMetricDefinition** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b0f25-111">**BreakdownDimensions**</span><span class="sxs-lookup"><span data-stu-id="b0f25-111">**BreakdownDimensions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0f25-112">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="b0f25-112">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="b0f25-113">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b0f25-113">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b0f25-114">Uma matriz que contém cadeias de caracteres de formato livre que podem ser usadas para dividir consultas de objetos [**CIM \_ BaseMetricValue**](cim-basemetricvalue.md) ao longo de uma determinada dimensão.</span><span class="sxs-lookup"><span data-stu-id="b0f25-114">An array that contains free format strings that can be used to break down queries of [**CIM\_BaseMetricValue**](cim-basemetricvalue.md) objects along a certain dimension.</span></span> <span data-ttu-id="b0f25-115">As cadeias de caracteres devem ser significativas para os usuários finais dos dados da métrica.</span><span class="sxs-lookup"><span data-stu-id="b0f25-115">The strings should be meaningful to the end users of the metric data.</span></span> <span data-ttu-id="b0f25-116">Além disso, as cadeias de caracteres devem indicar quais dimensões de interrupção têm suporte para a definição de métrica, pela Instrumentação subjacente.</span><span class="sxs-lookup"><span data-stu-id="b0f25-116">In addition, the strings should indicate which break down dimensions are supported for the metric definition, by the underlying instrumentation.</span></span>

<span data-ttu-id="b0f25-117">Um exemplo é um nome de transação que permite a divisão do valor total de todas as transações em um conjunto de valores, um para cada nome de transação.</span><span class="sxs-lookup"><span data-stu-id="b0f25-117">An example is a transaction name that allows the break down of the total value for all transactions into a set of values, one for each transaction name.</span></span> <span data-ttu-id="b0f25-118">Outros exemplos são um sistema de aplicativos ou um nome de grupo de usuários.</span><span class="sxs-lookup"><span data-stu-id="b0f25-118">Other examples are an application system, or a user group name.</span></span>

</dd> <dt>

<span data-ttu-id="b0f25-119">**Calculável**</span><span class="sxs-lookup"><span data-stu-id="b0f25-119">**Calculable**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0f25-120">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b0f25-120">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b0f25-121">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b0f25-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b0f25-122">As características da métrica usada para executar cálculos.</span><span class="sxs-lookup"><span data-stu-id="b0f25-122">The characteristics of the metric used to perform calculations.</span></span>

<dt>

<span id="Non-calculable"></span><span id="non-calculable"></span><span id="NON-CALCULABLE"></span>

<span data-ttu-id="b0f25-123"><span id="Non-calculable"></span><span id="non-calculable"></span><span id="NON-CALCULABLE"></span>**Não calculável** (1)</span><span class="sxs-lookup"><span data-stu-id="b0f25-123"><span id="Non-calculable"></span><span id="non-calculable"></span><span id="NON-CALCULABLE"></span>**Non-calculable** (1)</span></span>


</dt> <dd>

<span data-ttu-id="b0f25-124">Uma cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="b0f25-124">A string.</span></span> <span data-ttu-id="b0f25-125">A aritmética não faz sentido.</span><span class="sxs-lookup"><span data-stu-id="b0f25-125">Arithmetic makes no sense.</span></span>

</dd> <dt>

<span id="Summable"></span><span id="summable"></span><span id="SUMMABLE"></span>

<span data-ttu-id="b0f25-126"><span id="Summable"></span><span id="summable"></span><span id="SUMMABLE"></span>**Res** . (2)</span><span class="sxs-lookup"><span data-stu-id="b0f25-126"><span id="Summable"></span><span id="summable"></span><span id="SUMMABLE"></span>**Summable** (2)</span></span>


</dt> <dd>

<span data-ttu-id="b0f25-127">É razoável somar esse valor em várias instâncias de, por exemplo, UnitOfWork, como o número de arquivos processados em um trabalho de backup.</span><span class="sxs-lookup"><span data-stu-id="b0f25-127">It is reasonable to sum this value over many instances of e.g., UnitOfWork, such as the number of files processed in a backup job.</span></span> <span data-ttu-id="b0f25-128">Por exemplo, se cada trabalho de backup for um UnitOfWork e cada trabalho fizer backup de 27.000 arquivos em média, faz sentido dizer que 100 os trabalhos de backup processaram 2,7 milhões arquivos.</span><span class="sxs-lookup"><span data-stu-id="b0f25-128">For example, if each backup job is a UnitOfWork, and each job backs up 27,000 files on average, then it makes sense to say that 100 backup jobs processed 2,700,000 files.</span></span>

</dd> <dt>

<span id="Non-summable"></span><span id="non-summable"></span><span id="NON-SUMMABLE"></span>

<span data-ttu-id="b0f25-129"><span id="Non-summable"></span><span id="non-summable"></span><span id="NON-SUMMABLE"></span>**Não somable** (3)</span><span class="sxs-lookup"><span data-stu-id="b0f25-129"><span id="Non-summable"></span><span id="non-summable"></span><span id="NON-SUMMABLE"></span>**Non-summable** (3)</span></span>


</dt> <dd>

<span data-ttu-id="b0f25-130">Não faz sentido somar esse valor em várias instâncias de UnitOfWork.</span><span class="sxs-lookup"><span data-stu-id="b0f25-130">It does not make sense to sum this value over many instances of UnitOfWork.</span></span> <span data-ttu-id="b0f25-131">Um exemplo seria uma métrica que mede o comprimento da fila quando um trabalho chega a um servidor.</span><span class="sxs-lookup"><span data-stu-id="b0f25-131">An example would be a metric that measures the queue length when a job arrives at a server.</span></span> <span data-ttu-id="b0f25-132">Se cada trabalho for um UnitOfWork e o comprimento médio da fila quando cada trabalho chega for 33, não faz sentido dizer que o comprimento da fila para 100 trabalhos é 3300.</span><span class="sxs-lookup"><span data-stu-id="b0f25-132">If each job is a UnitOfWork, and the average queue length when each job arrives is 33, it does not make sense to say that the queue length for 100 jobs is 3300.</span></span> <span data-ttu-id="b0f25-133">Faz sentido dizer que a média é de 33.</span><span class="sxs-lookup"><span data-stu-id="b0f25-133">It does make sense to say that the mean is 33.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="b0f25-134">**ChangeType**</span><span class="sxs-lookup"><span data-stu-id="b0f25-134">**ChangeType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0f25-135">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b0f25-135">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b0f25-136">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b0f25-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b0f25-137">Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ BaseMetricDefinition**.**Iscontinuous**")</span><span class="sxs-lookup"><span data-stu-id="b0f25-137">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_BaseMetricDefinition**.**IsContinuous**")</span></span>
</dt> </dl>

<span data-ttu-id="b0f25-138">Indica como o valor da métrica muda usando atributos comuns, como alteração de direção, valores mínimos e máximos e semântica de encapsulamento.</span><span class="sxs-lookup"><span data-stu-id="b0f25-138">Indicates how the metric value changes using common attributes such as direction change, minimum and maximum values, and wrapping semantics.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="b0f25-139"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="b0f25-139"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="b0f25-140">O designer de métrica não qualificou o ChangeType.</span><span class="sxs-lookup"><span data-stu-id="b0f25-140">The metric designer did not qualify the ChangeType.</span></span>

</dd> <dt>

<span id="N_A"></span><span id="n_a"></span>

<span data-ttu-id="b0f25-141"><span id="N_A"></span><span id="n_a"></span>**N/A** (2)</span><span class="sxs-lookup"><span data-stu-id="b0f25-141"><span id="N_A"></span><span id="n_a"></span>**N/A** (2)</span></span>


</dt> <dd>

<span data-ttu-id="b0f25-142">Se a propriedade "iscontinuous" for "false", Altertype não faz sentido e deve ser definida como "N/A".</span><span class="sxs-lookup"><span data-stu-id="b0f25-142">If the "IsContinuous" property is "false", ChangeType does not make sense and MUST be is set to "N/A".</span></span>

</dd> <dt>

<span id="Counter"></span><span id="counter"></span><span id="COUNTER"></span>

<span data-ttu-id="b0f25-143"><span id="Counter"></span><span id="counter"></span><span id="COUNTER"></span>**Contador** (3)</span><span class="sxs-lookup"><span data-stu-id="b0f25-143"><span id="Counter"></span><span id="counter"></span><span id="COUNTER"></span>**Counter** (3)</span></span>


</dt> <dd>

<span data-ttu-id="b0f25-144">A métrica é uma métrica de contador.</span><span class="sxs-lookup"><span data-stu-id="b0f25-144">The metric is a counter metric.</span></span> <span data-ttu-id="b0f25-145">Eles têm valores inteiros não negativos que aumentam de forma monotônico até atingir o número máximo reapresentável e, em seguida, encapsular e começar a aumentar de 0.</span><span class="sxs-lookup"><span data-stu-id="b0f25-145">These have non-negative integer values which increase monotonically until reaching the maximum representable number and then wrap around and start increasing from 0.</span></span> <span data-ttu-id="b0f25-146">Esses contadores, também conhecidos como contadores de sobreposição, podem ser usados por instância para contar o número de erros de rede ou o número de transações processadas.</span><span class="sxs-lookup"><span data-stu-id="b0f25-146">Such counters, also known as rollover counters, can be used for instance to count the number of network errors or the number of transactions processed.</span></span> <span data-ttu-id="b0f25-147">A única maneira de um aplicativo cliente controlar o encapsule é recuperar o valor do contador em intervalos adequadamente curtos.</span><span class="sxs-lookup"><span data-stu-id="b0f25-147">The only way for a client application to keep track of wrap arounds is to retrieve the value of the counter in appropriately short intervals.</span></span>

</dd> <dt>

<span id="Gauge"></span><span id="gauge"></span><span id="GAUGE"></span>

<span data-ttu-id="b0f25-148"><span id="Gauge"></span><span id="gauge"></span><span id="GAUGE"></span>**Medidor** (4)</span><span class="sxs-lookup"><span data-stu-id="b0f25-148"><span id="Gauge"></span><span id="gauge"></span><span id="GAUGE"></span>**Gauge** (4)</span></span>


</dt> <dd>

<span data-ttu-id="b0f25-149">A métrica é uma métrica de medidor.</span><span class="sxs-lookup"><span data-stu-id="b0f25-149">The metric is a gauge metric.</span></span> <span data-ttu-id="b0f25-150">Eles têm valores inteiros ou flutuantes que podem aumentar e diminuir arbitrariamente.</span><span class="sxs-lookup"><span data-stu-id="b0f25-150">These have integer or float values that can increase and decrease arbitrarily.</span></span> <span data-ttu-id="b0f25-151">Um medidor não deve encapsular ao atingir o número mínimo ou máximo representeble, em vez disso, o valor "pente" nesse número.</span><span class="sxs-lookup"><span data-stu-id="b0f25-151">A gauge MUST NOT wrap when reaching the minimum or maximum representable number, instead, the value "sticks" at that number.</span></span> <span data-ttu-id="b0f25-152">Os valores mínimo ou máximo dentro do intervalo de valores representáveis no qual o valor de métrica "pente", pode ou não ser definido.</span><span class="sxs-lookup"><span data-stu-id="b0f25-152">Minimum or maximum values inside of the representable value range at which the metric value "sticks", may or may not be defined.</span></span>

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="b0f25-153"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (5.. 32767)</span><span class="sxs-lookup"><span data-stu-id="b0f25-153"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (5..32767)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="b0f25-154"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Fornecedor reservado** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="b0f25-154"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Vendor Reserved** (32768..65535)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="b0f25-155">**DataType**</span><span class="sxs-lookup"><span data-stu-id="b0f25-155">**DataType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0f25-156">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b0f25-156">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b0f25-157">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b0f25-157">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b0f25-158">O tipo de dados da métrica.</span><span class="sxs-lookup"><span data-stu-id="b0f25-158">The data type of the metric.</span></span>

<dt>

<span id="boolean"></span><span id="BOOLEAN"></span>

<span data-ttu-id="b0f25-159">**booliano** (1)</span><span class="sxs-lookup"><span data-stu-id="b0f25-159">**boolean** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="char16"></span><span id="CHAR16"></span>

<span data-ttu-id="b0f25-160">**char16** (2)</span><span class="sxs-lookup"><span data-stu-id="b0f25-160">**char16** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="datetime"></span><span id="DATETIME"></span>

<span data-ttu-id="b0f25-161">**data e hora** (3)</span><span class="sxs-lookup"><span data-stu-id="b0f25-161">**datetime** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="real32"></span><span id="REAL32"></span>

<span data-ttu-id="b0f25-162">**real32** (4)</span><span class="sxs-lookup"><span data-stu-id="b0f25-162">**real32** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="real64"></span><span id="REAL64"></span>

<span data-ttu-id="b0f25-163">**real64** (5)</span><span class="sxs-lookup"><span data-stu-id="b0f25-163">**real64** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="sint16"></span><span id="SINT16"></span>

<span data-ttu-id="b0f25-164">**sint16** (6)</span><span class="sxs-lookup"><span data-stu-id="b0f25-164">**sint16** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="sint32"></span><span id="SINT32"></span>

<span data-ttu-id="b0f25-165">**sint32** (7)</span><span class="sxs-lookup"><span data-stu-id="b0f25-165">**sint32** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="sint64"></span><span id="SINT64"></span>

<span data-ttu-id="b0f25-166">**sint64** (8)</span><span class="sxs-lookup"><span data-stu-id="b0f25-166">**sint64** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="sint8"></span><span id="SINT8"></span>

<span data-ttu-id="b0f25-167">**sint8** (9)</span><span class="sxs-lookup"><span data-stu-id="b0f25-167">**sint8** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="string"></span><span id="STRING"></span>

<span data-ttu-id="b0f25-168">**cadeia de caracteres** (10)</span><span class="sxs-lookup"><span data-stu-id="b0f25-168">**string** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="uint16"></span><span id="UINT16"></span>

<span data-ttu-id="b0f25-169">**UInt16** (11)</span><span class="sxs-lookup"><span data-stu-id="b0f25-169">**uint16** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="uint32"></span><span id="UINT32"></span>

<span data-ttu-id="b0f25-170">**UInt32** (12)</span><span class="sxs-lookup"><span data-stu-id="b0f25-170">**uint32** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="uint64"></span><span id="UINT64"></span>

<span data-ttu-id="b0f25-171">**UInt64** (13)</span><span class="sxs-lookup"><span data-stu-id="b0f25-171">**uint64** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="uint8"></span><span id="UINT8"></span>

<span data-ttu-id="b0f25-172">**uint8** (14)</span><span class="sxs-lookup"><span data-stu-id="b0f25-172">**uint8** (14)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="b0f25-173">**Gathertype**</span><span class="sxs-lookup"><span data-stu-id="b0f25-173">**GatheringType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0f25-174">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b0f25-174">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b0f25-175">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b0f25-175">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b0f25-176">Indica como os valores de métrica são coletados pela Instrumentação subjacente.</span><span class="sxs-lookup"><span data-stu-id="b0f25-176">Indicates how the metric values are gathered by the underlying instrumentation.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="b0f25-177"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="b0f25-177"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="b0f25-178">Indica que o Gathertype não é conhecido.</span><span class="sxs-lookup"><span data-stu-id="b0f25-178">Indicates that the GatheringType is not known.</span></span>

</dd> <dt>

<span id="OnChange"></span><span id="onchange"></span><span id="ONCHANGE"></span>

<span data-ttu-id="b0f25-179"><span id="OnChange"></span><span id="onchange"></span><span id="ONCHANGE"></span>**OnChange** (2)</span><span class="sxs-lookup"><span data-stu-id="b0f25-179"><span id="OnChange"></span><span id="onchange"></span><span id="ONCHANGE"></span>**OnChange** (2)</span></span>


</dt> <dd>

<span data-ttu-id="b0f25-180">Indica que os valores de métrica CIM são atualizados imediatamente quando os valores dentro do recurso medido são alterados.</span><span class="sxs-lookup"><span data-stu-id="b0f25-180">Indicates that the CIM metric values get updated immediately when the values inside of the measured resource change.</span></span> <span data-ttu-id="b0f25-181">Os valores das métricas de OnChange realmente refletem a situação atual no recurso a qualquer momento.</span><span class="sxs-lookup"><span data-stu-id="b0f25-181">The values of OnChange metrics truly reflect the current situation within the resource at any time.</span></span> <span data-ttu-id="b0f25-182">Um exemplo é o número de usuários conectados que são atualizados imediatamente à medida que os usuários fazem logon e logoff.</span><span class="sxs-lookup"><span data-stu-id="b0f25-182">An example is the number of logged on users that gets updated immediately as users log on and off.</span></span>

</dd> <dt>

<span id="Periodic"></span><span id="periodic"></span><span id="PERIODIC"></span>

<span data-ttu-id="b0f25-183"><span id="Periodic"></span><span id="periodic"></span><span id="PERIODIC"></span>**Periódico** (3)</span><span class="sxs-lookup"><span data-stu-id="b0f25-183"><span id="Periodic"></span><span id="periodic"></span><span id="PERIODIC"></span>**Periodic** (3)</span></span>


</dt> <dd>

<span data-ttu-id="b0f25-184">": Indica que os valores de métrica CIM são atualizados periodicamente.</span><span class="sxs-lookup"><span data-stu-id="b0f25-184">": Indicates that the CIM metric values get updated periodically.</span></span> <span data-ttu-id="b0f25-185">Por exemplo, para um aplicativo cliente, um valor de métrica aplicável à hora atual aparecerá constante durante cada intervalo de coleta e, em seguida, salta para o novo valor no final de cada intervalo de coleta.</span><span class="sxs-lookup"><span data-stu-id="b0f25-185">For instance, to a client application, a metric value applying to the current time will appear constant during each gathering interval, and then jumps to the new value at the end of each gathering interval.</span></span>

</dd> <dt>

<span id="OnRequest"></span><span id="onrequest"></span><span id="ONREQUEST"></span>

<span data-ttu-id="b0f25-186"><span id="OnRequest"></span><span id="onrequest"></span><span id="ONREQUEST"></span>**OnRequest** (4)</span><span class="sxs-lookup"><span data-stu-id="b0f25-186"><span id="OnRequest"></span><span id="onrequest"></span><span id="ONREQUEST"></span>**OnRequest** (4)</span></span>


</dt> <dd>

<span data-ttu-id="b0f25-187">Indica que o valor da métrica CIM é determinado sempre que um aplicativo cliente lê-lo.</span><span class="sxs-lookup"><span data-stu-id="b0f25-187">Indicates that the CIM metric value is determined each time a client application reads it.</span></span> <span data-ttu-id="b0f25-188">Os valores de métrica OnRequest retornam realmente a situação atual dentro do recurso se alguém solicitar.</span><span class="sxs-lookup"><span data-stu-id="b0f25-188">The values of OnRequest metrics truly return the current situation within the resource if somebody asks for it.</span></span> <span data-ttu-id="b0f25-189">No entanto, eles não mudam de "não observado" e, portanto, a assinatura para alterações de valor de métricas de OnRequest não é recomendada.</span><span class="sxs-lookup"><span data-stu-id="b0f25-189">However, they do not change "unobserved", and therefore subscribing for value changes of OnRequest metrics is NOT RECOMMENDED.</span></span>

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="b0f25-190"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (5.. 32767)</span><span class="sxs-lookup"><span data-stu-id="b0f25-190"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (5..32767)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="b0f25-191"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Fornecedor reservado** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="b0f25-191"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Vendor Reserved** (32768..65535)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="b0f25-192">**Id**</span><span class="sxs-lookup"><span data-stu-id="b0f25-192">**Id**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0f25-193">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="b0f25-193">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b0f25-194">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b0f25-194">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b0f25-195">Qualificadores: [ **chave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="b0f25-195">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="b0f25-196">A ID exclusiva da definição da métrica.</span><span class="sxs-lookup"><span data-stu-id="b0f25-196">The unique ID of the metric definition.</span></span> <span data-ttu-id="b0f25-197">Os GUIDs/UUID do Open Software Foundation (uso) são recomendados.</span><span class="sxs-lookup"><span data-stu-id="b0f25-197">Open Software Foundation (OSF) UUID/GUIDs are recommended.</span></span>

</dd> <dt>

<span data-ttu-id="b0f25-198">**IsContinuous**</span><span class="sxs-lookup"><span data-stu-id="b0f25-198">**IsContinuous**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0f25-199">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="b0f25-199">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="b0f25-200">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b0f25-200">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b0f25-201">True se o valor da métrica for contínuo; caso contrário, false.</span><span class="sxs-lookup"><span data-stu-id="b0f25-201">True if the metric value is continuous; otherwise, false.</span></span>

</dd> <dt>

<span data-ttu-id="b0f25-202">**Nome**</span><span class="sxs-lookup"><span data-stu-id="b0f25-202">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0f25-203">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="b0f25-203">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b0f25-204">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b0f25-204">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b0f25-205">O nome da métrica.</span><span class="sxs-lookup"><span data-stu-id="b0f25-205">The name of the metric.</span></span> <span data-ttu-id="b0f25-206">Esse nome não precisa ser exclusivo, mas deve ser descritivo e pode conter espaços em branco.</span><span class="sxs-lookup"><span data-stu-id="b0f25-206">This name does not have to be unique, but should be descriptive and may contain blank spaces.</span></span>

</dd> <dt>

<span data-ttu-id="b0f25-207">**ProgrammaticUnits**</span><span class="sxs-lookup"><span data-stu-id="b0f25-207">**ProgrammaticUnits**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0f25-208">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="b0f25-208">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b0f25-209">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b0f25-209">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b0f25-210">As unidades específicas de um valor.</span><span class="sxs-lookup"><span data-stu-id="b0f25-210">The specific units of a value.</span></span> <span data-ttu-id="b0f25-211">O valor dessa propriedade deve ser um valor válido do qualificador de unidades programáticas, conforme definido no Apêndice C. 1 de DSP0004 V 2.4 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="b0f25-211">The value of this property should be a legal value of the Programmatic Units qualifier as defined in Appendix C.1 of DSP0004 V2.4 or later.</span></span>

</dd> <dt>

<span data-ttu-id="b0f25-212">**Timescope**</span><span class="sxs-lookup"><span data-stu-id="b0f25-212">**TimeScope**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0f25-213">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="b0f25-213">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="b0f25-214">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b0f25-214">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b0f25-215">Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ BaseMetricValue**](cim-basemetricvalue.md).**TimeStamp**","**CIM \_ BaseMetricValue**.**Duração**")</span><span class="sxs-lookup"><span data-stu-id="b0f25-215">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_BaseMetricValue**](cim-basemetricvalue.md).**TimeStamp**", "**CIM\_BaseMetricValue**.**Duration**")</span></span>
</dt> </dl>

<span data-ttu-id="b0f25-216">O escopo de tempo que se aplica ao designer de métrica.</span><span class="sxs-lookup"><span data-stu-id="b0f25-216">The time scope that applies to the metric designer.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="b0f25-217"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="b0f25-217"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd>

<span data-ttu-id="b0f25-218">Indica que o escopo de tempo não foi qualificado pelo designer de métrica ou é desconhecido para o provedor.</span><span class="sxs-lookup"><span data-stu-id="b0f25-218">Indicates the time scope was not qualified by the metric designer, or is unknown to the provider.</span></span>

</dd> <dt>

<span id="Point"></span><span id="point"></span><span id="POINT"></span>

<span data-ttu-id="b0f25-219"><span id="Point"></span><span id="point"></span><span id="POINT"></span>**Ponto** (2)</span><span class="sxs-lookup"><span data-stu-id="b0f25-219"><span id="Point"></span><span id="point"></span><span id="POINT"></span>**Point** (2)</span></span>


</dt> <dd>

<span data-ttu-id="b0f25-220">Indica que a métrica se aplica a um ponto no tempo.</span><span class="sxs-lookup"><span data-stu-id="b0f25-220">Indicates that the metric applies to a point in time.</span></span> <span data-ttu-id="b0f25-221">Nas instâncias BaseMetricValue correspondentes, TimeStamp especifica o ponto no tempo e a duração é sempre 0.</span><span class="sxs-lookup"><span data-stu-id="b0f25-221">On the corresponding BaseMetricValue instances, TimeStamp specifies the point in time and Duration is always 0.</span></span>

</dd> <dt>

<span id="Interval"></span><span id="interval"></span><span id="INTERVAL"></span>

<span data-ttu-id="b0f25-222"><span id="Interval"></span><span id="interval"></span><span id="INTERVAL"></span>**Intervalo** (3)</span><span class="sxs-lookup"><span data-stu-id="b0f25-222"><span id="Interval"></span><span id="interval"></span><span id="INTERVAL"></span>**Interval** (3)</span></span>


</dt> <dd>

<span data-ttu-id="b0f25-223">Indica que a métrica se aplica a um intervalo de tempo.</span><span class="sxs-lookup"><span data-stu-id="b0f25-223">Indicates that the metric applies to a time interval.</span></span> <span data-ttu-id="b0f25-224">Nas instâncias BaseMetricValue correspondentes, TimeStamp especifica o final do intervalo de tempo e a duração especifica sua duração</span><span class="sxs-lookup"><span data-stu-id="b0f25-224">On the corresponding BaseMetricValue instances, TimeStamp specifies the end of the time interval and Duration specifies its duration</span></span>

</dd> <dt>

<span id="StartupInterval"></span><span id="startupinterval"></span><span id="STARTUPINTERVAL"></span>

<span data-ttu-id="b0f25-225"><span id="StartupInterval"></span><span id="startupinterval"></span><span id="STARTUPINTERVAL"></span>**StartupInterval** (4)</span><span class="sxs-lookup"><span data-stu-id="b0f25-225"><span id="StartupInterval"></span><span id="startupinterval"></span><span id="STARTUPINTERVAL"></span>**StartupInterval** (4)</span></span>


</dt> <dd>

<span data-ttu-id="b0f25-226">Indica que a métrica se aplica a um intervalo de tempo que começou na inicialização do recurso medido (ou seja, o Managedelement associado por MetricDefForMe).</span><span class="sxs-lookup"><span data-stu-id="b0f25-226">Indicates that the metric applies to a time interval that began at the startup of the measured resource (i.e. the ManagedElement associated by MetricDefForMe).</span></span> <span data-ttu-id="b0f25-227">Nas instâncias BaseMetricValue correspondentes, TimeStamp especifica o final do intervalo de tempo.</span><span class="sxs-lookup"><span data-stu-id="b0f25-227">On the corresponding BaseMetricValue instances, TimeStamp specifies the end of the time interval.</span></span> <span data-ttu-id="b0f25-228">Se Duration for 0, isso indica que o tempo de inicialização do recurso medido é desconhecido.</span><span class="sxs-lookup"><span data-stu-id="b0f25-228">If Duration is 0, this indicates that the startup time of the measured resource is unknown.</span></span> <span data-ttu-id="b0f25-229">Caso contrário, a duração especifica a duração entre a inicialização do recurso e o carimbo de data/hora.</span><span class="sxs-lookup"><span data-stu-id="b0f25-229">Else, Duration specifies the duration between startup of the resource and TimeStamp.</span></span>

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="b0f25-230"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reservado** (5.. 32767)</span><span class="sxs-lookup"><span data-stu-id="b0f25-230"><span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF Reserved** (5..32767)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="b0f25-231"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Fornecedor reservado** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="b0f25-231"><span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Vendor Reserved** (32768..65535)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="b0f25-232">**Unidades**</span><span class="sxs-lookup"><span data-stu-id="b0f25-232">**Units**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b0f25-233">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="b0f25-233">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b0f25-234">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b0f25-234">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b0f25-235">As unidades da métrica.</span><span class="sxs-lookup"><span data-stu-id="b0f25-235">The units of the metric.</span></span> <span data-ttu-id="b0f25-236">Os exemplos são bytes, pacotes, trabalhos, arquivos, milissegundos e amps.</span><span class="sxs-lookup"><span data-stu-id="b0f25-236">Examples are bytes, packets, jobs, files, milliseconds, and amps.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b0f25-237">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b0f25-237">Requirements</span></span>



| <span data-ttu-id="b0f25-238">Requisito</span><span class="sxs-lookup"><span data-stu-id="b0f25-238">Requirement</span></span> | <span data-ttu-id="b0f25-239">Valor</span><span class="sxs-lookup"><span data-stu-id="b0f25-239">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b0f25-240">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b0f25-240">Minimum supported client</span></span><br/> | <span data-ttu-id="b0f25-241">Windows 8</span><span class="sxs-lookup"><span data-stu-id="b0f25-241">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="b0f25-242">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b0f25-242">Minimum supported server</span></span><br/> | <span data-ttu-id="b0f25-243">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="b0f25-243">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="b0f25-244">Namespace</span><span class="sxs-lookup"><span data-stu-id="b0f25-244">Namespace</span></span><br/>                | <span data-ttu-id="b0f25-245">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="b0f25-245">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="b0f25-246">MOF</span><span class="sxs-lookup"><span data-stu-id="b0f25-246">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b0f25-247"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b0f25-247"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="b0f25-248">DLL</span><span class="sxs-lookup"><span data-stu-id="b0f25-248">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b0f25-249"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="b0f25-249"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="b0f25-250">Confira também</span><span class="sxs-lookup"><span data-stu-id="b0f25-250">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b0f25-251">**\_Managedelement do CIM**</span><span class="sxs-lookup"><span data-stu-id="b0f25-251">**CIM\_ManagedElement**</span></span>](cim-managedelement.md)
</dt> </dl>

 

