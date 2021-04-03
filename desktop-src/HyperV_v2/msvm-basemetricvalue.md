---
description: Representa um valor de métrica definido por uma instância da \_ classe Msvm BaseMetricDefinition.
ms.assetid: bd872f21-ab71-4ab7-88d3-b26dd2fbdbe5
title: Classe Msvm_BaseMetricValue
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_BaseMetricValue
- Msvm_BaseMetricValue.InstanceID
- Msvm_BaseMetricValue.Caption
- Msvm_BaseMetricValue.Description
- Msvm_BaseMetricValue.ElementName
- Msvm_BaseMetricValue.MetricDefinitionId
- Msvm_BaseMetricValue.MeasuredElementName
- Msvm_BaseMetricValue.TimeStamp
- Msvm_BaseMetricValue.Duration
- Msvm_BaseMetricValue.MetricValue
- Msvm_BaseMetricValue.BreakdownDimension
- Msvm_BaseMetricValue.BreakdownValue
- Msvm_BaseMetricValue.Volatile
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: f0e566de4822b271dcd4633c3dba35f7c88495bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103836867"
---
# <a name="msvm_basemetricvalue-class"></a><span data-ttu-id="93c05-103">\_Classe Msvm BaseMetricValue</span><span class="sxs-lookup"><span data-stu-id="93c05-103">Msvm\_BaseMetricValue class</span></span>

<span data-ttu-id="93c05-104">Representa um valor de métrica definido por uma instância da classe [**Msvm \_ BaseMetricDefinition**](msvm-basemetricdefinition.md) .</span><span class="sxs-lookup"><span data-stu-id="93c05-104">Represents a metric value defined by an instance of the [**Msvm\_BaseMetricDefinition**](msvm-basemetricdefinition.md) class.</span></span>

<span data-ttu-id="93c05-105">A sintaxe a seguir é simplificada formato MOF código (MOF) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="93c05-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="93c05-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="93c05-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_BaseMetricValue : CIM_BaseMetricValue
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
};
```

## <a name="members"></a><span data-ttu-id="93c05-107">Membros</span><span class="sxs-lookup"><span data-stu-id="93c05-107">Members</span></span>

<span data-ttu-id="93c05-108">A classe **Msvm \_ BaseMetricValue** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="93c05-108">The **Msvm\_BaseMetricValue** class has these types of members:</span></span>

-   [<span data-ttu-id="93c05-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="93c05-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="93c05-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="93c05-110">Properties</span></span>

<span data-ttu-id="93c05-111">A classe **Msvm \_ BaseMetricValue** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="93c05-111">The **Msvm\_BaseMetricValue** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="93c05-112">**BreakdownDimension**</span><span class="sxs-lookup"><span data-stu-id="93c05-112">**BreakdownDimension**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93c05-113">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="93c05-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="93c05-114">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="93c05-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="93c05-115">Especifica uma dimensão de divisão da matriz **BreakdownDimensions** definida no [**\_ BaseMetricDefinition Msvm**](msvm-basemetricdefinition.md)associado.</span><span class="sxs-lookup"><span data-stu-id="93c05-115">Specifies one breakdown dimension from the **BreakdownDimensions** array defined in the associated [**Msvm\_BaseMetricDefinition**](msvm-basemetricdefinition.md).</span></span> <span data-ttu-id="93c05-116">Essa é a dimensão na qual esse conjunto de valores de métrica é dividido.</span><span class="sxs-lookup"><span data-stu-id="93c05-116">This is the dimension along which this set of metric values is broken down.</span></span> <span data-ttu-id="93c05-117">Essa propriedade é herdada do [**CIM \_ BaseMetricDefinition**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="93c05-117">This property is inherited from [**CIM\_BaseMetricDefinition**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="93c05-118">**Divisãovalue**</span><span class="sxs-lookup"><span data-stu-id="93c05-118">**BreakdownValue**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93c05-119">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="93c05-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="93c05-120">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="93c05-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="93c05-121">Define um valor da propriedade **BreakdownDimension** definida para essa instância de valor de métrica.</span><span class="sxs-lookup"><span data-stu-id="93c05-121">Defines a value of the **BreakdownDimension** property defined for this metric value instance.</span></span> <span data-ttu-id="93c05-122">Por exemplo, se **BreakdownDimension** for "transactionName", essa propriedade poderá nomear a transação real à qual esse valor de métrica específico se aplica.</span><span class="sxs-lookup"><span data-stu-id="93c05-122">For example, if the **BreakdownDimension** is "TransactionName", this property could name the actual transaction to which this particular metric value applies.</span></span> <span data-ttu-id="93c05-123">Essa propriedade é herdada do [**CIM \_ BaseMetricDefinition**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="93c05-123">This property is inherited from [**CIM\_BaseMetricDefinition**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="93c05-124">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="93c05-124">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93c05-125">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="93c05-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="93c05-126">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="93c05-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="93c05-127">Uma breve descrição do objeto.</span><span class="sxs-lookup"><span data-stu-id="93c05-127">A short description of the object.</span></span> <span data-ttu-id="93c05-128">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="93c05-128">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="93c05-129">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="93c05-129">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93c05-130">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="93c05-130">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="93c05-131">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="93c05-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="93c05-132">Uma descrição do objeto .</span><span class="sxs-lookup"><span data-stu-id="93c05-132">A description of the object.</span></span> <span data-ttu-id="93c05-133">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="93c05-133">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="93c05-134">**Duration**</span><span class="sxs-lookup"><span data-stu-id="93c05-134">**Duration**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93c05-135">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="93c05-135">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="93c05-136">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="93c05-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="93c05-137">Especifica o tempo durante o qual esse valor de métrica é válido.</span><span class="sxs-lookup"><span data-stu-id="93c05-137">Specifies the time duration over which this metric value is valid.</span></span> <span data-ttu-id="93c05-138">Essa propriedade não deve existir para carimbos de data/hora que se aplicam somente a um ponto no tempo, mas devem ser especificadas para valores que são considerados válidos por um determinado período de tempo (por exemplo, amostragem).</span><span class="sxs-lookup"><span data-stu-id="93c05-138">This property should not exist for time stamps that apply only to a point in time, but should be specified for values that are considered valid for a certain time period (for example, sampling).</span></span> <span data-ttu-id="93c05-139">Se a propriedade **Duration** existir e não for **NULL**, a propriedade **timestamp** especificará o final do intervalo.</span><span class="sxs-lookup"><span data-stu-id="93c05-139">If the **Duration** property exists and is not **Null**, the **TimeStamp** property specifies the end of the interval.</span></span> <span data-ttu-id="93c05-140">Essa propriedade é herdada do [**CIM \_ BaseMetricDefinition**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="93c05-140">This property is inherited from [**CIM\_BaseMetricDefinition**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="93c05-141">**ElementName**</span><span class="sxs-lookup"><span data-stu-id="93c05-141">**ElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93c05-142">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="93c05-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="93c05-143">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="93c05-143">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="93c05-144">Um nome de exibição para o objeto.</span><span class="sxs-lookup"><span data-stu-id="93c05-144">A display name for the object.</span></span> <span data-ttu-id="93c05-145">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="93c05-145">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="93c05-146">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="93c05-146">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93c05-147">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="93c05-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="93c05-148">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="93c05-148">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="93c05-149">Qualificadores: **chave**</span><span class="sxs-lookup"><span data-stu-id="93c05-149">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="93c05-150">Uma cadeia de caracteres que identifica exclusivamente uma instância dessa classe.</span><span class="sxs-lookup"><span data-stu-id="93c05-150">A string that uniquely identifies an instance of this class.</span></span> <span data-ttu-id="93c05-151">Essa propriedade é herdada de [**CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="93c05-151">This property is inherited from [**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="93c05-152">**MeasuredElementName**</span><span class="sxs-lookup"><span data-stu-id="93c05-152">**MeasuredElementName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93c05-153">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="93c05-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="93c05-154">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="93c05-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="93c05-155">Um nome descritivo para o elemento ao qual o valor de métrica pertence (o elemento medido).</span><span class="sxs-lookup"><span data-stu-id="93c05-155">A descriptive name for the element to which the metric value belongs (the measured element).</span></span> <span data-ttu-id="93c05-156">Essa propriedade é herdada do [**CIM \_ BaseMetricDefinition**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="93c05-156">This property is inherited from [**CIM\_BaseMetricDefinition**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="93c05-157">**MetricDefinitionId**</span><span class="sxs-lookup"><span data-stu-id="93c05-157">**MetricDefinitionId**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93c05-158">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="93c05-158">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="93c05-159">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="93c05-159">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="93c05-160">A chave da instância [**de \_ BaseMetricDefinition do Msvm**](msvm-basemetricdefinition.md) para esse valor.</span><span class="sxs-lookup"><span data-stu-id="93c05-160">The key of the [**Msvm\_BaseMetricDefinition**](msvm-basemetricdefinition.md) instance for this value.</span></span> <span data-ttu-id="93c05-161">Essa propriedade é herdada do [**CIM \_ BaseMetricDefinition**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="93c05-161">This property is inherited from [**CIM\_BaseMetricDefinition**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="93c05-162">**Metricvalue**</span><span class="sxs-lookup"><span data-stu-id="93c05-162">**MetricValue**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93c05-163">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="93c05-163">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="93c05-164">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="93c05-164">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="93c05-165">O valor da métrica que é representada como uma cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="93c05-165">The value of the metric that is represented as a string.</span></span> <span data-ttu-id="93c05-166">Essa propriedade é herdada do [**CIM \_ BaseMetricDefinition**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="93c05-166">This property is inherited from [**CIM\_BaseMetricDefinition**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="93c05-167">**Estampa**</span><span class="sxs-lookup"><span data-stu-id="93c05-167">**TimeStamp**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93c05-168">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="93c05-168">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="93c05-169">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="93c05-169">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="93c05-170">Especifica a hora em que o valor da métrica foi capturado ou computado.</span><span class="sxs-lookup"><span data-stu-id="93c05-170">Specifies the time when the metric value was captured or computed.</span></span> <span data-ttu-id="93c05-171">Lembre-se de que isso é diferente da hora em que a instância foi criada.</span><span class="sxs-lookup"><span data-stu-id="93c05-171">Be aware that this is different from the time when the instance was created.</span></span> <span data-ttu-id="93c05-172">Essa propriedade é herdada do [**CIM \_ BaseMetricDefinition**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="93c05-172">This property is inherited from [**CIM\_BaseMetricDefinition**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> <dt>

<span data-ttu-id="93c05-173">**Volátil**</span><span class="sxs-lookup"><span data-stu-id="93c05-173">**Volatile**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="93c05-174">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="93c05-174">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="93c05-175">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="93c05-175">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="93c05-176">**True** se o valor para o próximo ponto no tempo usar a mesma instância de classe e apenas alterar os valores de propriedade (como o **valor** ou **carimbo de data/hora**).</span><span class="sxs-lookup"><span data-stu-id="93c05-176">**True** if the value for the next point in time will use the same class instance and just change the property values (such as the **Value** or **TimeStamp**).</span></span> <span data-ttu-id="93c05-177">Se for **true**, a instância será reutilizada.</span><span class="sxs-lookup"><span data-stu-id="93c05-177">If **True**, the instance is reused.</span></span> <span data-ttu-id="93c05-178">Se **for false**, as instâncias existentes permanecerão inalteradas e uma nova instância será criada para o novo ponto no tempo.</span><span class="sxs-lookup"><span data-stu-id="93c05-178">If **False**, the existing instances remain unchanged and a new instance is created for the new point in time.</span></span> <span data-ttu-id="93c05-179">Essa propriedade é herdada do [**CIM \_ BaseMetricDefinition**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span><span class="sxs-lookup"><span data-stu-id="93c05-179">This property is inherited from [**CIM\_BaseMetricDefinition**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="93c05-180">Requisitos</span><span class="sxs-lookup"><span data-stu-id="93c05-180">Requirements</span></span>



| <span data-ttu-id="93c05-181">Requisito</span><span class="sxs-lookup"><span data-stu-id="93c05-181">Requirement</span></span> | <span data-ttu-id="93c05-182">Valor</span><span class="sxs-lookup"><span data-stu-id="93c05-182">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="93c05-183">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="93c05-183">Minimum supported client</span></span><br/> | <span data-ttu-id="93c05-184">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="93c05-184">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="93c05-185">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="93c05-185">Minimum supported server</span></span><br/> | <span data-ttu-id="93c05-186">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="93c05-186">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="93c05-187">Namespace</span><span class="sxs-lookup"><span data-stu-id="93c05-187">Namespace</span></span><br/>                | <span data-ttu-id="93c05-188">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="93c05-188">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="93c05-189">MOF</span><span class="sxs-lookup"><span data-stu-id="93c05-189">MOF</span></span><br/>                      | <dl> <span data-ttu-id="93c05-190"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="93c05-190"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="93c05-191">DLL</span><span class="sxs-lookup"><span data-stu-id="93c05-191">DLL</span></span><br/>                      | <dl> <span data-ttu-id="93c05-192"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="93c05-192"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

