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
ms.openlocfilehash: ca6c90a4b6b3ef3e690c13612f69480ec5f008be
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103922338"
---
# <a name="cim_basemetricvalue-class"></a><span data-ttu-id="2e31a-103">\_Classe CIM BaseMetricValue</span><span class="sxs-lookup"><span data-stu-id="2e31a-103">CIM\_BaseMetricValue class</span></span>

<span data-ttu-id="2e31a-104">Representa o valor da instância de uma métrica.</span><span class="sxs-lookup"><span data-stu-id="2e31a-104">Represents the instance value of a metric.</span></span>

## <a name="syntax"></a><span data-ttu-id="2e31a-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2e31a-105">Syntax</span></span>

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

## <a name="members"></a><span data-ttu-id="2e31a-106">Membros</span><span class="sxs-lookup"><span data-stu-id="2e31a-106">Members</span></span>

<span data-ttu-id="2e31a-107">A classe **CIM \_ BaseMetricValue** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="2e31a-107">The **CIM\_BaseMetricValue** class has these types of members:</span></span>

-   [<span data-ttu-id="2e31a-108">Propriedades</span><span class="sxs-lookup"><span data-stu-id="2e31a-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="2e31a-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="2e31a-109">Properties</span></span>

<span data-ttu-id="2e31a-110">A classe **CIM \_ BaseMetricValue** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="2e31a-110">The **CIM\_BaseMetricValue** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="2e31a-111">**BreakdownDimension**</span><span class="sxs-lookup"><span data-stu-id="2e31a-111">**BreakdownDimension**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e31a-112">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="2e31a-112">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2e31a-113">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2e31a-113">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2e31a-114">A dimensão para a qual esse conjunto de valores de métrica é dividido com base na propriedade **BreakdownDimensions** do objeto [**CIM \_ BaseMetricDefinition**](cim-basemetricdefinition.md) associado.</span><span class="sxs-lookup"><span data-stu-id="2e31a-114">The dimension for which this set of metric values is broken down based on **BreakdownDimensions** property of the associated [**CIM\_BaseMetricDefinition**](cim-basemetricdefinition.md) object.</span></span>

</dd> <dt>

<span data-ttu-id="2e31a-115">**Divisãovalue**</span><span class="sxs-lookup"><span data-stu-id="2e31a-115">**BreakdownValue**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e31a-116">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="2e31a-116">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2e31a-117">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2e31a-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2e31a-118">O valor da propriedade **BreakdownDimension** definida para esse valor de instância.</span><span class="sxs-lookup"><span data-stu-id="2e31a-118">The value of the **BreakdownDimension** property defined for this instance value.</span></span> <span data-ttu-id="2e31a-119">Por exemplo, se **BreakdownDimension** contiver "transactionName", essa propriedade poderá nomear a transação real à qual esse valor de métrica específico se aplica.</span><span class="sxs-lookup"><span data-stu-id="2e31a-119">For example, if **BreakdownDimension** contains "TransactionName", this property could name the actual transaction to which this particular metric value applies.</span></span>

</dd> <dt>

<span data-ttu-id="2e31a-120">**Duration**</span><span class="sxs-lookup"><span data-stu-id="2e31a-120">**Duration**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e31a-121">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="2e31a-121">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="2e31a-122">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2e31a-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2e31a-123">Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ BaseMetricDefinition**](cim-basemetricdefinition.md).**Timescope**","**CIM \_ BaseMetricValue**.**TimeStamp**")</span><span class="sxs-lookup"><span data-stu-id="2e31a-123">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_BaseMetricDefinition**](cim-basemetricdefinition.md).**TimeScope**", "**CIM\_BaseMetricValue**.**TimeStamp**")</span></span>
</dt> </dl>

<span data-ttu-id="2e31a-124">O tempo durante o qual esse valor de métrica é válido.</span><span class="sxs-lookup"><span data-stu-id="2e31a-124">The time duration over which this metric value is valid.</span></span> <span data-ttu-id="2e31a-125">Essa propriedade não deve existir para carimbos de data/hora que se aplicam somente a um ponto no tempo, mas devem ser definidas para valores que são considerados válidos por um determinado período de tempo (por exemplo,</span><span class="sxs-lookup"><span data-stu-id="2e31a-125">This property should not exist for time stamps that only apply to a point in time, but should be defined for values that are considered valid for a certain time period (ex.</span></span> <span data-ttu-id="2e31a-126">amostragem).</span><span class="sxs-lookup"><span data-stu-id="2e31a-126">sampling).</span></span> <span data-ttu-id="2e31a-127">Se a propriedade **Duration** existir e não for nula, o valor de **timestamp** deverá ser o final do intervalo.</span><span class="sxs-lookup"><span data-stu-id="2e31a-127">If the **Duration** property exists and is non-Null, the **TimeStamp** value should be the end of the interval.</span></span>

</dd> <dt>

<span data-ttu-id="2e31a-128">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="2e31a-128">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e31a-129">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="2e31a-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2e31a-130">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2e31a-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2e31a-131">Qualificadores: [**chave**](/windows/desktop/WmiSdk/key-qualifier), [**substituição**](/windows/desktop/WmiSdk/standard-qualifiers) ("InstanceId")</span><span class="sxs-lookup"><span data-stu-id="2e31a-131">Qualifiers: [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("InstanceID")</span></span>
</dt> </dl>

<span data-ttu-id="2e31a-132">Identifica exclusivamente uma instância dessa classe dentro do escopo do namespace que a contém.</span><span class="sxs-lookup"><span data-stu-id="2e31a-132">Uniquely identifies an instance of this class within the scope of the containing namespace.</span></span>

> [!IMPORTANT]
>
> <span data-ttu-id="2e31a-133">Para garantir a exclusividade no namespace, o valor da propriedade **InstanceId** deve ser construído no seguinte padrão: *OrgID*:*LocalId*</span><span class="sxs-lookup"><span data-stu-id="2e31a-133">In order to ensure uniqueness within the namespace, the value of the **InstanceID** property should be constructed in the following pattern: *OrgID*:*LocalID*</span></span>
>
> <span data-ttu-id="2e31a-134">*OrgID* deve incluir um nome de direitos autorais, com marca registrada ou exclusivo que pertença à entidade de negócios que define a **InstanceId** ou ser uma ID registrada que é atribuída por uma autoridade global reconhecida.</span><span class="sxs-lookup"><span data-stu-id="2e31a-134">*OrgID* must include a copyrighted, trademarked or otherwise unique name that is owned by the business entity that defines the **InstanceID**, or be a registered ID that is assigned by a recognized global authority.</span></span> <span data-ttu-id="2e31a-135">Esse padrão é semelhante à estrutura de nomes de classe de esquema.</span><span class="sxs-lookup"><span data-stu-id="2e31a-135">This pattern is similar to the structure of schema class names.</span></span> <span data-ttu-id="2e31a-136">Além disso, para garantir a exclusividade, os primeiros dois-pontos em **InstanceId** devem estar entre *OrgID* e *LocalId*.</span><span class="sxs-lookup"><span data-stu-id="2e31a-136">In addition, to ensure uniqueness, the first colon in **InstanceID** must be between the *OrgID* and *LocalID*.</span></span> <span data-ttu-id="2e31a-137">Portanto, o *OrgID* não deve conter dois-pontos (': ').</span><span class="sxs-lookup"><span data-stu-id="2e31a-137">Therefore the *OrgID* must not contain a colon (':').</span></span>
>
> <span data-ttu-id="2e31a-138">A *LocalId* é escolhida pela entidade de negócios e não deve ser reutilizada para identificar elementos do mundo real subjacentes diferentes.</span><span class="sxs-lookup"><span data-stu-id="2e31a-138">*LocalID* is chosen by the business entity and should not be re-used to identify different underlying real-world elements.</span></span>
>
> <span data-ttu-id="2e31a-139">Se o padrão acima não for usado, a entidade de definição deverá garantir que o valor de **InstanceId** resultante não seja reutilizado em todas as propriedades **InstanceId** produzidas por este provedor ou por outros provedores para esse namespace.</span><span class="sxs-lookup"><span data-stu-id="2e31a-139">If the above pattern is not used, the defining entity must assure that the resultant **InstanceID** value is not re-used across any **InstanceID** properties that are produced by this provider or other providers for this namespace.</span></span>
>
> <span data-ttu-id="2e31a-140">Para instâncias definidas pela DMTF (Distributed Management Task Force), o padrão deve ser usado com o *OrgID* definido como CIM.</span><span class="sxs-lookup"><span data-stu-id="2e31a-140">For Distributed Management Task Force (DMTF) defined instances, the pattern must be used with the *OrgID* set to CIM.</span></span>

 

</dd> <dt>

<span data-ttu-id="2e31a-141">**MeasuredElementName**</span><span class="sxs-lookup"><span data-stu-id="2e31a-141">**MeasuredElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e31a-142">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="2e31a-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2e31a-143">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2e31a-143">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2e31a-144">Um nome descritivo para o elemento que é medido pela métrica.</span><span class="sxs-lookup"><span data-stu-id="2e31a-144">A descriptive name for the element that is measure by the metric.</span></span>

<span data-ttu-id="2e31a-145">Essa propriedade será necessária se a definição da métrica não estiver associada a um objeto [**\_ managedelement CIM**](cim-managedelement.md) e poderá ser usada em outros casos para fornecer informações complementares.</span><span class="sxs-lookup"><span data-stu-id="2e31a-145">This property is required if the metric definition is not associated with a [**CIM\_ManagedElement**](cim-managedelement.md) object, and may be used in other cases to provide supplemental information.</span></span> <span data-ttu-id="2e31a-146">Isso permite que as métricas sejam capturadas independentemente de qualquer objeto **CIM \_ managedelement** .</span><span class="sxs-lookup"><span data-stu-id="2e31a-146">This allows metrics to be captured independent of any **CIM\_ManagedElement** object.</span></span>

<span data-ttu-id="2e31a-147">Se houver vários objetos [**\_ gerenciados CIM**](cim-managedelement.md) associados ao valor de métrica, você poderá escolher um dos elementos gerenciados para criar as informações complementares para a métrica.</span><span class="sxs-lookup"><span data-stu-id="2e31a-147">If there are multiple [**CIM\_ManagedElement**](cim-managedelement.md) objects associated with the metric value, then you can choose one of the managed elements to create the supplemental information for the metric.</span></span> <span data-ttu-id="2e31a-148">A propriedade não deve ser usada como uma chave estrangeira para consultar o elemento medido.</span><span class="sxs-lookup"><span data-stu-id="2e31a-148">The property is not meant to be used as a foreign key to query the measured element.</span></span> <span data-ttu-id="2e31a-149">Em vez disso, a associação ao **CIM \_ managedelement** deve ser usada.</span><span class="sxs-lookup"><span data-stu-id="2e31a-149">Instead, the association to the **CIM\_ManagedElement** should be used.</span></span>

</dd> <dt>

<span data-ttu-id="2e31a-150">**MetricDefinitionId**</span><span class="sxs-lookup"><span data-stu-id="2e31a-150">**MetricDefinitionId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e31a-151">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="2e31a-151">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2e31a-152">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2e31a-152">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2e31a-153">Qualificadores: [**Required**](/windows/desktop/WmiSdk/standard-qualifiers), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ BaseMetricDefinition**](cim-basemetricdefinition.md).**ID**")</span><span class="sxs-lookup"><span data-stu-id="2e31a-153">Qualifiers: [**Required**](/windows/desktop/WmiSdk/standard-qualifiers), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_BaseMetricDefinition**](cim-basemetricdefinition.md).**Id**")</span></span>
</dt> </dl>

<span data-ttu-id="2e31a-154">A chave da instância [**\_ BaseMetricDefinition do CIM**](cim-basemetricdefinition.md) que está associada a esse valor de instância.</span><span class="sxs-lookup"><span data-stu-id="2e31a-154">The key of the [**CIM\_BaseMetricDefinition**](cim-basemetricdefinition.md) instance that is associated with this instance value.</span></span>

</dd> <dt>

<span data-ttu-id="2e31a-155">**Metricvalue**</span><span class="sxs-lookup"><span data-stu-id="2e31a-155">**MetricValue**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e31a-156">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="2e31a-156">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2e31a-157">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2e31a-157">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2e31a-158">Qualificadores: [ **obrigatório**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="2e31a-158">Qualifiers: [**Required**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="2e31a-159">Uma representação de cadeia de caracteres do valor da métrica.</span><span class="sxs-lookup"><span data-stu-id="2e31a-159">A string representation of the metric value.</span></span> <span data-ttu-id="2e31a-160">O tipo de dados original do valor da métrica é especificado no objeto [**CIM \_ BaseMetricDefinition**](cim-basemetricdefinition.md) associado.</span><span class="sxs-lookup"><span data-stu-id="2e31a-160">The original data type of the metric value is specified in the associated [**CIM\_BaseMetricDefinition**](cim-basemetricdefinition.md) object.</span></span>

</dd> <dt>

<span data-ttu-id="2e31a-161">**Estampa**</span><span class="sxs-lookup"><span data-stu-id="2e31a-161">**TimeStamp**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e31a-162">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="2e31a-162">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="2e31a-163">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2e31a-163">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2e31a-164">Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ BaseMetricDefinition**](cim-basemetricdefinition.md).**Timescope**","**CIM \_ BaseMetricValue**.**Duração**")</span><span class="sxs-lookup"><span data-stu-id="2e31a-164">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_BaseMetricDefinition**](cim-basemetricdefinition.md).**TimeScope**", "**CIM\_BaseMetricValue**.**Duration**")</span></span>
</dt> </dl>

<span data-ttu-id="2e31a-165">A hora em que o valor de uma instância de métrica é computada.</span><span class="sxs-lookup"><span data-stu-id="2e31a-165">The time when the value of a metric instance is computed.</span></span> <span data-ttu-id="2e31a-166">Isso é diferente da hora em que a instância é criada.</span><span class="sxs-lookup"><span data-stu-id="2e31a-166">This is different from the time when the instance is created.</span></span> <span data-ttu-id="2e31a-167">Se a propriedade **volátil** for true, esse valor será alterado sempre que um novo instantâneo de medida for obtido.</span><span class="sxs-lookup"><span data-stu-id="2e31a-167">If the **Volatile** property is true, this value changes whenever a new measurement snapshot is taken.</span></span>

<span data-ttu-id="2e31a-168">Um aplicativo de gerenciamento pode estabelecer uma série temporal de dados de métrica recuperando as instâncias do **CIM \_ BaseMetricValue** e classificando-as de acordo com o valor do **carimbo de data/hora** .</span><span class="sxs-lookup"><span data-stu-id="2e31a-168">A management application may establish a time series of metric data by retrieving the instances of **CIM\_BaseMetricValue** and sorting them according to their **TimeStamp** value.</span></span>

</dd> <dt>

<span data-ttu-id="2e31a-169">**Volátil**</span><span class="sxs-lookup"><span data-stu-id="2e31a-169">**Volatile**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2e31a-170">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="2e31a-170">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2e31a-171">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2e31a-171">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2e31a-172">True se o valor do **carimbo de data/hora** for alterado sempre que o valor da instância de métrica for alterado.</span><span class="sxs-lookup"><span data-stu-id="2e31a-172">True if the **TimeStamp** value changes whenever the value of the metric instance changes.</span></span> <span data-ttu-id="2e31a-173">False se esse objeto deve permanecer inalterado e um novo objeto criado para o novo valor de **carimbo de data/hora** .</span><span class="sxs-lookup"><span data-stu-id="2e31a-173">False if this object must remain unchanged and a new object created for the new **TimeStamp** value.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2e31a-174">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2e31a-174">Requirements</span></span>



| <span data-ttu-id="2e31a-175">Requisito</span><span class="sxs-lookup"><span data-stu-id="2e31a-175">Requirement</span></span> | <span data-ttu-id="2e31a-176">Valor</span><span class="sxs-lookup"><span data-stu-id="2e31a-176">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2e31a-177">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2e31a-177">Minimum supported client</span></span><br/> | <span data-ttu-id="2e31a-178">Windows 8</span><span class="sxs-lookup"><span data-stu-id="2e31a-178">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="2e31a-179">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2e31a-179">Minimum supported server</span></span><br/> | <span data-ttu-id="2e31a-180">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="2e31a-180">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="2e31a-181">Namespace</span><span class="sxs-lookup"><span data-stu-id="2e31a-181">Namespace</span></span><br/>                | <span data-ttu-id="2e31a-182">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="2e31a-182">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="2e31a-183">MOF</span><span class="sxs-lookup"><span data-stu-id="2e31a-183">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2e31a-184"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2e31a-184"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="2e31a-185">DLL</span><span class="sxs-lookup"><span data-stu-id="2e31a-185">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2e31a-186"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="2e31a-186"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="2e31a-187">Confira também</span><span class="sxs-lookup"><span data-stu-id="2e31a-187">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2e31a-188">**\_Managedelement do CIM**</span><span class="sxs-lookup"><span data-stu-id="2e31a-188">**CIM\_ManagedElement**</span></span>](cim-managedelement.md)
</dt> </dl>

 

