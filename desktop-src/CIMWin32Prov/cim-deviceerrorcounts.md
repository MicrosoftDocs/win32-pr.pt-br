---
description: A \_ classe CIM DeviceErrorCounts é uma classe estatística que contém contadores relacionados a erros para um dispositivo lógico. Os tipos de erros são definidos por CCITT (REC X. 733) e ISO (IEC 10164-4).
ms.assetid: d65cbc78-40f2-4846-bd47-76e04b2f588b
ms.tgt_platform: multiple
title: Classe CIM_DeviceErrorCounts
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DeviceErrorCounts
- CIM_DeviceErrorCounts.Caption
- CIM_DeviceErrorCounts.Description
- CIM_DeviceErrorCounts.CriticalErrorCount
- CIM_DeviceErrorCounts.DeviceCreationClassName
- CIM_DeviceErrorCounts.DeviceID
- CIM_DeviceErrorCounts.Name
- CIM_DeviceErrorCounts.IndeterminateErrorCount
- CIM_DeviceErrorCounts.MajorErrorCount
- CIM_DeviceErrorCounts.MinorErrorCount
- CIM_DeviceErrorCounts.SystemCreationClassName
- CIM_DeviceErrorCounts.SystemName
- CIM_DeviceErrorCounts.WarningCount
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1602e68b7254811ba8c09726feda8baa7bf23d29
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920460"
---
# <a name="cim_deviceerrorcounts-class"></a><span data-ttu-id="2590e-104">\_Classe CIM DeviceErrorCounts</span><span class="sxs-lookup"><span data-stu-id="2590e-104">CIM\_DeviceErrorCounts class</span></span>

<span data-ttu-id="2590e-105">A classe **CIM \_ DeviceErrorCounts** é uma classe estatística que contém contadores relacionados a erros para um dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="2590e-105">The **CIM\_DeviceErrorCounts** class is a statistical class that contains error-related counters for a logical device.</span></span> <span data-ttu-id="2590e-106">Os tipos de erros são definidos por CCITT (REC X. 733) e ISO (IEC 10164-4).</span><span class="sxs-lookup"><span data-stu-id="2590e-106">The types of errors are defined by CCITT (Rec X.733) and ISO (IEC 10164-4).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="2590e-107">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="2590e-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="2590e-108">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="2590e-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="2590e-109">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="2590e-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="2590e-110">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="2590e-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="2590e-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2590e-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{117FDB8C-D025-11d2-85F5-0000F8102E5F}"), AMENDMENT]
class CIM_DeviceErrorCounts : CIM_StatisticalInformation
{
  string Caption;
  string Description;
  uint64 CriticalErrorCount;
  string DeviceCreationClassName;
  string DeviceID;
  string Name;
  uint64 IndeterminateErrorCount;
  uint64 MajorErrorCount;
  uint64 MinorErrorCount;
  string SystemCreationClassName;
  string SystemName;
  uint64 WarningCount;
};
```

## <a name="members"></a><span data-ttu-id="2590e-112">Membros</span><span class="sxs-lookup"><span data-stu-id="2590e-112">Members</span></span>

<span data-ttu-id="2590e-113">A classe **CIM \_ DeviceErrorCounts** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="2590e-113">The **CIM\_DeviceErrorCounts** class has these types of members:</span></span>

-   [<span data-ttu-id="2590e-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="2590e-114">Methods</span></span>](#methods)
-   [<span data-ttu-id="2590e-115">Propriedades</span><span class="sxs-lookup"><span data-stu-id="2590e-115">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="2590e-116">Métodos</span><span class="sxs-lookup"><span data-stu-id="2590e-116">Methods</span></span>

<span data-ttu-id="2590e-117">A classe **CIM \_ DeviceErrorCounts** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="2590e-117">The **CIM\_DeviceErrorCounts** class has these methods.</span></span>



| <span data-ttu-id="2590e-118">Método</span><span class="sxs-lookup"><span data-stu-id="2590e-118">Method</span></span>                                                                     | <span data-ttu-id="2590e-119">Descrição</span><span class="sxs-lookup"><span data-stu-id="2590e-119">Description</span></span>                                                               |
|:---------------------------------------------------------------------------|:--------------------------------------------------------------------------|
| [<span data-ttu-id="2590e-120">**ResetCounter**</span><span class="sxs-lookup"><span data-stu-id="2590e-120">**ResetCounter**</span></span>](resetcounter-method-in-class-cim-deviceerrorcounts.md) | <span data-ttu-id="2590e-121">Redefine os contadores de erro e de aviso.</span><span class="sxs-lookup"><span data-stu-id="2590e-121">Resets the error and warning counters.</span></span> <span data-ttu-id="2590e-122">Não implementado pelo WMI.</span><span class="sxs-lookup"><span data-stu-id="2590e-122">Not implemented by WMI.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="2590e-123">Propriedades</span><span class="sxs-lookup"><span data-stu-id="2590e-123">Properties</span></span>

<span data-ttu-id="2590e-124">A classe **CIM \_ DeviceErrorCounts** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="2590e-124">The **CIM\_DeviceErrorCounts** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="2590e-125">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="2590e-125">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2590e-126">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="2590e-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2590e-127">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2590e-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2590e-128">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="2590e-128">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="2590e-129">Breve descrição textual para a estatística ou métrica.</span><span class="sxs-lookup"><span data-stu-id="2590e-129">Short textual description for the statistic or metric.</span></span>

<span data-ttu-id="2590e-130">Essa propriedade é herdada do [**CIM \_ StatisticalInformation**](cim-statisticalinformation.md).</span><span class="sxs-lookup"><span data-stu-id="2590e-130">This property is inherited from [**CIM\_StatisticalInformation**](cim-statisticalinformation.md).</span></span>

</dd> <dt>

<span data-ttu-id="2590e-131">**CriticalErrorCount**</span><span class="sxs-lookup"><span data-stu-id="2590e-131">**CriticalErrorCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2590e-132">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="2590e-132">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="2590e-133">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2590e-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2590e-134">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Estado operacional da DMTF \| 3,7 ")</span><span class="sxs-lookup"><span data-stu-id="2590e-134">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.7")</span></span>
</dt> </dl>

<span data-ttu-id="2590e-135">Contagem dos erros críticos.</span><span class="sxs-lookup"><span data-stu-id="2590e-135">Count of the critical errors.</span></span>

<span data-ttu-id="2590e-136">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="2590e-136">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="2590e-137">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="2590e-137">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2590e-138">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="2590e-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2590e-139">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2590e-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2590e-140">Descrição textual da estatística ou métrica.</span><span class="sxs-lookup"><span data-stu-id="2590e-140">Textual description of the statistic or metric.</span></span>

<span data-ttu-id="2590e-141">Essa propriedade é herdada do [**CIM \_ StatisticalInformation**](cim-statisticalinformation.md).</span><span class="sxs-lookup"><span data-stu-id="2590e-141">This property is inherited from [**CIM\_StatisticalInformation**](cim-statisticalinformation.md).</span></span>

</dd> <dt>

<span data-ttu-id="2590e-142">**DeviceCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="2590e-142">**DeviceCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2590e-143">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="2590e-143">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2590e-144">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2590e-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2590e-145">Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ LogicalDevice**](cim-logicaldevice.md).**CreationClassName**"), [**chave**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="2590e-145">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_LogicalDevice**](cim-logicaldevice.md).**CreationClassName**"), [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="2590e-146">A propriedade **CreationClassName** do dispositivo de escopo.</span><span class="sxs-lookup"><span data-stu-id="2590e-146">The scoping device's **CreationClassName** property.</span></span>

</dd> <dt>

<span data-ttu-id="2590e-147">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="2590e-147">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2590e-148">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="2590e-148">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2590e-149">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2590e-149">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2590e-150">Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ LogicalDevice**](cim-logicaldevice.md).**DeviceID**"), [**chave**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="2590e-150">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_LogicalDevice**](cim-logicaldevice.md).**DeviceID**"), [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="2590e-151">O identificador do dispositivo de escopo.</span><span class="sxs-lookup"><span data-stu-id="2590e-151">The scoping device's identifier.</span></span>

</dd> <dt>

<span data-ttu-id="2590e-152">**IndeterminateErrorCount**</span><span class="sxs-lookup"><span data-stu-id="2590e-152">**IndeterminateErrorCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2590e-153">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="2590e-153">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="2590e-154">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2590e-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2590e-155">Contagem dos erros indeterminados.</span><span class="sxs-lookup"><span data-stu-id="2590e-155">Count of the indeterminate errors.</span></span>

<span data-ttu-id="2590e-156">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="2590e-156">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="2590e-157">**MajorErrorCount**</span><span class="sxs-lookup"><span data-stu-id="2590e-157">**MajorErrorCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2590e-158">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="2590e-158">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="2590e-159">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2590e-159">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2590e-160">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Estado operacional da DMTF \| 3,8 ")</span><span class="sxs-lookup"><span data-stu-id="2590e-160">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.8")</span></span>
</dt> </dl>

<span data-ttu-id="2590e-161">Contagem dos principais erros.</span><span class="sxs-lookup"><span data-stu-id="2590e-161">Count of the major errors.</span></span>

<span data-ttu-id="2590e-162">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="2590e-162">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="2590e-163">**MinorErrorCount**</span><span class="sxs-lookup"><span data-stu-id="2590e-163">**MinorErrorCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2590e-164">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="2590e-164">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="2590e-165">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2590e-165">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="2590e-166">Contagem dos erros secundários.</span><span class="sxs-lookup"><span data-stu-id="2590e-166">Count of the minor errors.</span></span>

<span data-ttu-id="2590e-167">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="2590e-167">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> <dt>

<span data-ttu-id="2590e-168">**Nome**</span><span class="sxs-lookup"><span data-stu-id="2590e-168">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2590e-169">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="2590e-169">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2590e-170">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2590e-170">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2590e-171">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="2590e-171">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Name"), [**Key**](/windows/desktop/WmiSdk/key-qualifier), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="2590e-172">A propriedade Name herdada serve como parte da chave para a **instância \_ DeviceErrorCounts do CIM** .</span><span class="sxs-lookup"><span data-stu-id="2590e-172">The inherited Name property serves as part of the key for the **CIM\_DeviceErrorCounts** instance.</span></span> <span data-ttu-id="2590e-173">O escopo do objeto é definido pelo dispositivo lógico ao qual as estatísticas se aplicam.</span><span class="sxs-lookup"><span data-stu-id="2590e-173">The object is scoped by the logical device to which the statistics apply.</span></span>

</dd> <dt>

<span data-ttu-id="2590e-174">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="2590e-174">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2590e-175">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="2590e-175">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2590e-176">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2590e-176">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2590e-177">Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ LogicalDevice**](cim-logicaldevice.md).**SystemCreationClassName**"), [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="2590e-177">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_LogicalDevice**](cim-logicaldevice.md).**SystemCreationClassName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="2590e-178">**CreationClassName** do sistema de escopo.</span><span class="sxs-lookup"><span data-stu-id="2590e-178">Scoping system's **CreationClassName**.</span></span>

</dd> <dt>

<span data-ttu-id="2590e-179">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="2590e-179">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2590e-180">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="2590e-180">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2590e-181">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2590e-181">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2590e-182">Qualificadores: [**propagados**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ LogicalDevice**](cim-logicaldevice.md).**SystemName**"), [**\_ chave CIM**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="2590e-182">Qualifiers: [**Propagated**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_LogicalDevice**](cim-logicaldevice.md).**SystemName**"), [**CIM\_Key**](/windows/desktop/WmiSdk/standard-wmi-qualifiers), [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="2590e-183">Propriedade de **nome** do sistema de escopo.</span><span class="sxs-lookup"><span data-stu-id="2590e-183">Scoping system's **Name** property.</span></span>

</dd> <dt>

<span data-ttu-id="2590e-184">**WarningCount**</span><span class="sxs-lookup"><span data-stu-id="2590e-184">**WarningCount**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2590e-185">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="2590e-185">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="2590e-186">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2590e-186">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2590e-187">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Estado operacional da DMTF \| 3,9 ")</span><span class="sxs-lookup"><span data-stu-id="2590e-187">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Operational State\|003.9")</span></span>
</dt> </dl>

<span data-ttu-id="2590e-188">Contagem dos avisos.</span><span class="sxs-lookup"><span data-stu-id="2590e-188">Count of the warnings.</span></span>

<span data-ttu-id="2590e-189">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span><span class="sxs-lookup"><span data-stu-id="2590e-189">For more information about using **uint64** values in scripts, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2590e-190">Comentários</span><span class="sxs-lookup"><span data-stu-id="2590e-190">Remarks</span></span>

<span data-ttu-id="2590e-191">O WMI não implementa essa classe.</span><span class="sxs-lookup"><span data-stu-id="2590e-191">WMI does not implement this class.</span></span>

<span data-ttu-id="2590e-192">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="2590e-192">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="2590e-193">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="2590e-193">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="2590e-194">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2590e-194">Requirements</span></span>



| <span data-ttu-id="2590e-195">Requisito</span><span class="sxs-lookup"><span data-stu-id="2590e-195">Requirement</span></span> | <span data-ttu-id="2590e-196">Valor</span><span class="sxs-lookup"><span data-stu-id="2590e-196">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2590e-197">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2590e-197">Minimum supported client</span></span><br/> | <span data-ttu-id="2590e-198">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2590e-198">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="2590e-199">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2590e-199">Minimum supported server</span></span><br/> | <span data-ttu-id="2590e-200">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2590e-200">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="2590e-201">Namespace</span><span class="sxs-lookup"><span data-stu-id="2590e-201">Namespace</span></span><br/>                | <span data-ttu-id="2590e-202">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="2590e-202">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="2590e-203">MOF</span><span class="sxs-lookup"><span data-stu-id="2590e-203">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2590e-204"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2590e-204"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="2590e-205">DLL</span><span class="sxs-lookup"><span data-stu-id="2590e-205">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2590e-206"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2590e-206"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2590e-207">Confira também</span><span class="sxs-lookup"><span data-stu-id="2590e-207">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2590e-208">**\_STATISTICALINFORMATION CIM**</span><span class="sxs-lookup"><span data-stu-id="2590e-208">**CIM\_StatisticalInformation**</span></span>](cim-statisticalinformation.md)
</dt> </dl>

 

