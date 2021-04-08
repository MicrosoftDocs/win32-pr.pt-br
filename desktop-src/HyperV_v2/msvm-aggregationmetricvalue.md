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
# <a name="msvm_aggregationmetricvalue-class"></a><span data-ttu-id="a8b1c-103">\_Classe Msvm AggregationMetricValue</span><span class="sxs-lookup"><span data-stu-id="a8b1c-103">Msvm\_AggregationMetricValue class</span></span>

<span data-ttu-id="a8b1c-104">Representa o valor da instância de uma métrica definida por uma instância da classe [**Msvm \_ AggregationMetricDefinition**](msvm-aggregationmetricdefinition.md) .</span><span class="sxs-lookup"><span data-stu-id="a8b1c-104">Represents the instance value of a metric defined by an instance of the [**Msvm\_AggregationMetricDefinition**](msvm-aggregationmetricdefinition.md) class.</span></span> <span data-ttu-id="a8b1c-105">As propriedades herdadas de [**Msvm \_ BaseMetricValue**](msvm-basemetricvalue.md) fornecem o valor de métrica real.</span><span class="sxs-lookup"><span data-stu-id="a8b1c-105">The properties inherited from [**Msvm\_BaseMetricValue**](msvm-basemetricvalue.md) provide the actual metric value.</span></span> <span data-ttu-id="a8b1c-106">As propriedades definidas por essa classe fornecem informações sobre o intervalo sobre o qual a função de agregação foi aplicada.</span><span class="sxs-lookup"><span data-stu-id="a8b1c-106">The properties defined by this class provide information about the interval over which the aggregation function was applied.</span></span>

<span data-ttu-id="a8b1c-107">A sintaxe a seguir é simplificada formato MOF código (MOF) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="a8b1c-107">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="a8b1c-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a8b1c-108">Syntax</span></span>

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

## <a name="members"></a><span data-ttu-id="a8b1c-109">Membros</span><span class="sxs-lookup"><span data-stu-id="a8b1c-109">Members</span></span>

<span data-ttu-id="a8b1c-110">A classe **Msvm \_ AggregationMetricValue** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="a8b1c-110">The **Msvm\_AggregationMetricValue** class has these types of members:</span></span>

-   [<span data-ttu-id="a8b1c-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="a8b1c-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a8b1c-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="a8b1c-112">Properties</span></span>

<span data-ttu-id="a8b1c-113">A classe **Msvm \_ AggregationMetricValue** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="a8b1c-113">The **Msvm\_AggregationMetricValue** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a8b1c-114">**AggregationDuration**</span><span class="sxs-lookup"><span data-stu-id="a8b1c-114">**AggregationDuration**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a8b1c-115">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="a8b1c-115">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="a8b1c-116">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a8b1c-116">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a8b1c-117">Representa a duração da hora em que a agregação foi computada.</span><span class="sxs-lookup"><span data-stu-id="a8b1c-117">Represents the time duration over which the aggregation was computed.</span></span> <span data-ttu-id="a8b1c-118">O início de um intervalo de monitoramento sobre o qual a função de agregação é aplicada é determinado pela subtração do **AggregationDuration** do **AggregationTimeStamp**.</span><span class="sxs-lookup"><span data-stu-id="a8b1c-118">The start of a monitoring interval over which the aggregation function is applied is determined by subtracting the **AggregationDuration** from the **AggregationTimeStamp**.</span></span> <span data-ttu-id="a8b1c-119">Essa propriedade é herdada do **CIM \_ AggregationMetricValue**.</span><span class="sxs-lookup"><span data-stu-id="a8b1c-119">This property is inherited from **CIM\_AggregationMetricValue**.</span></span>

</dd> <dt>

<span data-ttu-id="a8b1c-120">**AggregationTimeStamp**</span><span class="sxs-lookup"><span data-stu-id="a8b1c-120">**AggregationTimeStamp**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a8b1c-121">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="a8b1c-121">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="a8b1c-122">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a8b1c-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a8b1c-123">Identifica a hora em que a função de agregação foi aplicada para determinar o valor da instância de métrica.</span><span class="sxs-lookup"><span data-stu-id="a8b1c-123">Identifies the time when the aggregation function was applied to determine the value of the metric instance.</span></span> <span data-ttu-id="a8b1c-124">Isso não é o mesmo que a hora em que a instância foi criada.</span><span class="sxs-lookup"><span data-stu-id="a8b1c-124">This is not the same as the time when the instance was created.</span></span> <span data-ttu-id="a8b1c-125">Para uma determinada instância de **\_ AggregationMetricValue do CIM** , o **AggregationTimeStamp** é alterado sempre que a função de agregação é aplicada para calcular o valor.</span><span class="sxs-lookup"><span data-stu-id="a8b1c-125">For a given **CIM\_AggregationMetricValue** instance, the **AggregationTimeStamp** changes whenever the aggregation function is applied to calculate the value.</span></span> <span data-ttu-id="a8b1c-126">Essa propriedade é herdada do **CIM \_ AggregationMetricValue**.</span><span class="sxs-lookup"><span data-stu-id="a8b1c-126">This property is inherited from **CIM\_AggregationMetricValue**.</span></span>

</dd> <dt>

<span data-ttu-id="a8b1c-127">**BreakdownDimension**</span><span class="sxs-lookup"><span data-stu-id="a8b1c-127">**BreakdownDimension**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a8b1c-128">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="a8b1c-128">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a8b1c-129">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a8b1c-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a8b1c-130">Especifica uma dimensão de divisão da matriz **BreakdownDimensions** definida no [**\_ BaseMetricDefinition Msvm**](msvm-basemetricdefinition.md)associado.</span><span class="sxs-lookup"><span data-stu-id="a8b1c-130">Specifies one breakdown dimension from the **BreakdownDimensions** array defined in the associated [**Msvm\_BaseMetricDefinition**](msvm-basemetricdefinition.md).</span></span> <span data-ttu-id="a8b1c-131">Essa é a dimensão na qual esse conjunto de valores de métrica é dividido.</span><span class="sxs-lookup"><span data-stu-id="a8b1c-131">This is the dimension along which this set of metric values is broken down.</span></span> <span data-ttu-id="a8b1c-132">Essa propriedade é herdada do [**CIM \_ BaseMetricDefinition**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="a8b1c-132">This property is inherited from [**CIM\_BaseMetricDefinition**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="a8b1c-133">**Divisãovalue**</span><span class="sxs-lookup"><span data-stu-id="a8b1c-133">**BreakdownValue**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a8b1c-134">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="a8b1c-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a8b1c-135">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a8b1c-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a8b1c-136">Define um valor da propriedade **BreakdownDimension** definida para essa instância de valor de métrica.</span><span class="sxs-lookup"><span data-stu-id="a8b1c-136">Defines a value of the **BreakdownDimension** property defined for this metric value instance.</span></span> <span data-ttu-id="a8b1c-137">Por exemplo, se **BreakdownDimension** for "transactionName", essa propriedade poderá nomear a transação real à qual esse valor de métrica específico se aplica.</span><span class="sxs-lookup"><span data-stu-id="a8b1c-137">For example, if the **BreakdownDimension** is "TransactionName", this property could name the actual transaction to which this particular metric value applies.</span></span> <span data-ttu-id="a8b1c-138">Essa propriedade é herdada do [**CIM \_ BaseMetricDefinition**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="a8b1c-138">This property is inherited from [**CIM\_BaseMetricDefinition**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="a8b1c-139">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="a8b1c-139">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a8b1c-140">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="a8b1c-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a8b1c-141">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a8b1c-141">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a8b1c-142">Uma breve descrição do objeto.</span><span class="sxs-lookup"><span data-stu-id="a8b1c-142">A short description of the object.</span></span> <span data-ttu-id="a8b1c-143">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="a8b1c-143">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="a8b1c-144">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="a8b1c-144">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a8b1c-145">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="a8b1c-145">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a8b1c-146">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a8b1c-146">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a8b1c-147">Uma descrição do objeto .</span><span class="sxs-lookup"><span data-stu-id="a8b1c-147">A description of the object.</span></span> <span data-ttu-id="a8b1c-148">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="a8b1c-148">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="a8b1c-149">**Duration**</span><span class="sxs-lookup"><span data-stu-id="a8b1c-149">**Duration**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a8b1c-150">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="a8b1c-150">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="a8b1c-151">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a8b1c-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a8b1c-152">Especifica o tempo durante o qual esse valor de métrica é válido.</span><span class="sxs-lookup"><span data-stu-id="a8b1c-152">Specifies the time duration over which this metric value is valid.</span></span> <span data-ttu-id="a8b1c-153">Essa propriedade não deve existir para carimbos de data/hora que se aplicam somente a um ponto no tempo, mas devem ser especificadas para valores que são considerados válidos por um determinado período de tempo (por exemplo, amostragem).</span><span class="sxs-lookup"><span data-stu-id="a8b1c-153">This property should not exist for time stamps that apply only to a point in time, but should be specified for values that are considered valid for a certain time period (for example, sampling).</span></span> <span data-ttu-id="a8b1c-154">Se a propriedade **Duration** existir e não for **NULL**, a propriedade **timestamp** especificará o final do intervalo.</span><span class="sxs-lookup"><span data-stu-id="a8b1c-154">If the **Duration** property exists and is not **Null**, the **TimeStamp** property specifies the end of the interval.</span></span> <span data-ttu-id="a8b1c-155">Essa propriedade é herdada do [**CIM \_ BaseMetricDefinition**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="a8b1c-155">This property is inherited from [**CIM\_BaseMetricDefinition**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="a8b1c-156">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="a8b1c-156">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a8b1c-157">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="a8b1c-157">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a8b1c-158">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a8b1c-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a8b1c-159">Um nome de exibição para o objeto.</span><span class="sxs-lookup"><span data-stu-id="a8b1c-159">A display name for the object.</span></span> <span data-ttu-id="a8b1c-160">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="a8b1c-160">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="a8b1c-161">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="a8b1c-161">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a8b1c-162">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="a8b1c-162">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a8b1c-163">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a8b1c-163">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a8b1c-164">Qualificadores: **chave**</span><span class="sxs-lookup"><span data-stu-id="a8b1c-164">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="a8b1c-165">Uma cadeia de caracteres que identifica exclusivamente uma instância dessa classe.</span><span class="sxs-lookup"><span data-stu-id="a8b1c-165">A string that uniquely identifies an instance of this class.</span></span> <span data-ttu-id="a8b1c-166">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="a8b1c-166">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="a8b1c-167">**MeasuredElementName**</span><span class="sxs-lookup"><span data-stu-id="a8b1c-167">**MeasuredElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a8b1c-168">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="a8b1c-168">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a8b1c-169">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a8b1c-169">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a8b1c-170">Um nome descritivo para o elemento ao qual o valor de métrica pertence (o elemento medido).</span><span class="sxs-lookup"><span data-stu-id="a8b1c-170">A descriptive name for the element to which the metric value belongs (the measured element).</span></span> <span data-ttu-id="a8b1c-171">Essa propriedade é herdada do [**CIM \_ BaseMetricDefinition**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="a8b1c-171">This property is inherited from [**CIM\_BaseMetricDefinition**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="a8b1c-172">**MetricDefinitionId**</span><span class="sxs-lookup"><span data-stu-id="a8b1c-172">**MetricDefinitionId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a8b1c-173">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="a8b1c-173">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a8b1c-174">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a8b1c-174">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a8b1c-175">A chave da instância [**de \_ BaseMetricDefinition do Msvm**](msvm-basemetricdefinition.md) para esse valor.</span><span class="sxs-lookup"><span data-stu-id="a8b1c-175">The key of the [**Msvm\_BaseMetricDefinition**](msvm-basemetricdefinition.md) instance for this value.</span></span> <span data-ttu-id="a8b1c-176">Essa propriedade é herdada do [**CIM \_ BaseMetricDefinition**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="a8b1c-176">This property is inherited from [**CIM\_BaseMetricDefinition**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="a8b1c-177">**Metricvalue**</span><span class="sxs-lookup"><span data-stu-id="a8b1c-177">**MetricValue**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a8b1c-178">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="a8b1c-178">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a8b1c-179">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a8b1c-179">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a8b1c-180">O valor da métrica que é representada como uma cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="a8b1c-180">The value of the metric that is represented as a string.</span></span> <span data-ttu-id="a8b1c-181">Essa propriedade é herdada do [**CIM \_ BaseMetricDefinition**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="a8b1c-181">This property is inherited from [**CIM\_BaseMetricDefinition**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="a8b1c-182">**Estampa**</span><span class="sxs-lookup"><span data-stu-id="a8b1c-182">**TimeStamp**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a8b1c-183">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="a8b1c-183">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="a8b1c-184">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a8b1c-184">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a8b1c-185">Especifica a hora em que o valor da métrica foi capturado ou computado.</span><span class="sxs-lookup"><span data-stu-id="a8b1c-185">Specifies the time when the metric value was captured or computed.</span></span> <span data-ttu-id="a8b1c-186">Lembre-se de que isso é diferente da hora em que a instância foi criada.</span><span class="sxs-lookup"><span data-stu-id="a8b1c-186">Be aware that this is different from the time when the instance was created.</span></span> <span data-ttu-id="a8b1c-187">Essa propriedade é herdada do [**CIM \_ BaseMetricDefinition**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="a8b1c-187">This property is inherited from [**CIM\_BaseMetricDefinition**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="a8b1c-188">**Volátil**</span><span class="sxs-lookup"><span data-stu-id="a8b1c-188">**Volatile**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a8b1c-189">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="a8b1c-189">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a8b1c-190">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a8b1c-190">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a8b1c-191">**True** se o valor para o próximo ponto no tempo usar a mesma instância de classe e apenas alterar os valores de propriedade (como o **valor** ou **carimbo de data/hora**).</span><span class="sxs-lookup"><span data-stu-id="a8b1c-191">**True** if the value for the next point in time will use the same class instance and just change the property values (such as the **Value** or **TimeStamp**).</span></span> <span data-ttu-id="a8b1c-192">Se for **true**, a instância será reutilizada.</span><span class="sxs-lookup"><span data-stu-id="a8b1c-192">If **True**, the instance is reused.</span></span> <span data-ttu-id="a8b1c-193">Se **for false**, as instâncias existentes permanecerão inalteradas e uma nova instância será criada para o novo ponto no tempo.</span><span class="sxs-lookup"><span data-stu-id="a8b1c-193">If **False**, the existing instances remain unchanged and a new instance is created for the new point in time.</span></span> <span data-ttu-id="a8b1c-194">Essa propriedade é herdada do [**CIM \_ BaseMetricDefinition**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="a8b1c-194">This property is inherited from [**CIM\_BaseMetricDefinition**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a8b1c-195">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a8b1c-195">Requirements</span></span>



| <span data-ttu-id="a8b1c-196">Requisito</span><span class="sxs-lookup"><span data-stu-id="a8b1c-196">Requirement</span></span> | <span data-ttu-id="a8b1c-197">Valor</span><span class="sxs-lookup"><span data-stu-id="a8b1c-197">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a8b1c-198">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a8b1c-198">Minimum supported client</span></span><br/> | <span data-ttu-id="a8b1c-199">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="a8b1c-199">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="a8b1c-200">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a8b1c-200">Minimum supported server</span></span><br/> | <span data-ttu-id="a8b1c-201">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="a8b1c-201">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="a8b1c-202">Namespace</span><span class="sxs-lookup"><span data-stu-id="a8b1c-202">Namespace</span></span><br/>                | <span data-ttu-id="a8b1c-203">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="a8b1c-203">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="a8b1c-204">MOF</span><span class="sxs-lookup"><span data-stu-id="a8b1c-204">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a8b1c-205"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a8b1c-205"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="a8b1c-206">DLL</span><span class="sxs-lookup"><span data-stu-id="a8b1c-206">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a8b1c-207"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="a8b1c-207"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

