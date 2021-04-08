---
description: Uma classe base abstrata para as classes de dados preinstaladas e calculadas.
ms.assetid: 4eb6ad42-0f68-44f4-be19-095c51b4b1b6
ms.tgt_platform: multiple
title: Classe Win32_PerfFormattedData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PerfFormattedData
- Win32_PerfFormattedData.Caption
- Win32_PerfFormattedData.Description
- Win32_PerfFormattedData.Name
- Win32_PerfFormattedData.Frequency_Object
- Win32_PerfFormattedData.Frequency_PerfTime
- Win32_PerfFormattedData.Frequency_Sys100NS
- Win32_PerfFormattedData.Timestamp_Object
- Win32_PerfFormattedData.Timestamp_PerfTime
- Win32_PerfFormattedData.Timestamp_Sys100NS
api_type:
- DllExport
api_location:
- WmiPerfInst.dll
ms.openlocfilehash: c28d0366c80e8838b36e17cd0fa1074b6ad33629
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920519"
---
# <a name="win32_perfformatteddata-class"></a><span data-ttu-id="671e0-103">\_Classe Win32 PerfFormattedData</span><span class="sxs-lookup"><span data-stu-id="671e0-103">Win32\_PerfFormattedData class</span></span>

<span data-ttu-id="671e0-104">Uma classe base abstrata para as classes de dados preinstaladas e calculadas.</span><span class="sxs-lookup"><span data-stu-id="671e0-104">An abstract base class for the preinstalled, calculated data classes.</span></span> <span data-ttu-id="671e0-105">Um exemplo dessa classe é o [**Win32 \_ PerfFormattedData \_ perfdisk \_ LogicalDisk**](../wmisdk/retrieving-raw-and-formatted-performance-data.md).</span><span class="sxs-lookup"><span data-stu-id="671e0-105">An example of such a class is [**Win32\_PerfFormattedData\_PerfDisk\_LogicalDisk**](../wmisdk/retrieving-raw-and-formatted-performance-data.md).</span></span> <span data-ttu-id="671e0-106">Essas classes contêm valores calculados fornecidos pelo [provedor de dados de desempenho formatado](../wmisdk/formatted-performance-data-provider.md)de alto desempenho.</span><span class="sxs-lookup"><span data-stu-id="671e0-106">These classes contain calculated values provided by the high-performance [Formatted Performance Data Provider](../wmisdk/formatted-performance-data-provider.md).</span></span>

<span data-ttu-id="671e0-107">A sintaxe a seguir é simplificada do código MOF e mostra todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="671e0-107">The following syntax is simplified from MOF code and shows all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="671e0-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="671e0-108">Syntax</span></span>

``` syntax
[abstract, AMENDMENT]
class Win32_PerfFormattedData : Win32_Perf
{
  string Caption;
  string Description;
  string Name;
  uint64 Frequency_Object;
  uint64 Frequency_PerfTime;
  uint64 Frequency_Sys100NS;
  uint64 Timestamp_Object;
  uint64 Timestamp_PerfTime;
  uint64 Timestamp_Sys100NS;
};
```

## <a name="members"></a><span data-ttu-id="671e0-109">Membros</span><span class="sxs-lookup"><span data-stu-id="671e0-109">Members</span></span>

<span data-ttu-id="671e0-110">A classe **Win32 \_ PerfFormattedData** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="671e0-110">The **Win32\_PerfFormattedData** class has these types of members:</span></span>

-   [<span data-ttu-id="671e0-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="671e0-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="671e0-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="671e0-112">Properties</span></span>

<span data-ttu-id="671e0-113">A classe **Win32 \_ PerfFormattedData** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="671e0-113">The **Win32\_PerfFormattedData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="671e0-114">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="671e0-114">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="671e0-115">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="671e0-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="671e0-116">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="671e0-116">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="671e0-117">Qualificadores: [**maxlen**](../wmisdk/standard-qualifiers.md) (64)</span><span class="sxs-lookup"><span data-stu-id="671e0-117">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="671e0-118">Breve descrição textual para a estatística ou métrica.</span><span class="sxs-lookup"><span data-stu-id="671e0-118">Short textual description for the statistic or metric.</span></span>

<span data-ttu-id="671e0-119">Essa propriedade é herdada do [**CIM \_ StatisticalInformation**](cim-statisticalinformation.md).</span><span class="sxs-lookup"><span data-stu-id="671e0-119">This property is inherited from [**CIM\_StatisticalInformation**](cim-statisticalinformation.md).</span></span>

</dd> <dt>

<span data-ttu-id="671e0-120">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="671e0-120">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="671e0-121">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="671e0-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="671e0-122">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="671e0-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="671e0-123">Descrição textual da estatística ou métrica.</span><span class="sxs-lookup"><span data-stu-id="671e0-123">Textual description of the statistic or metric.</span></span>

<span data-ttu-id="671e0-124">Essa propriedade é herdada do [**CIM \_ StatisticalInformation**](cim-statisticalinformation.md).</span><span class="sxs-lookup"><span data-stu-id="671e0-124">This property is inherited from [**CIM\_StatisticalInformation**](cim-statisticalinformation.md).</span></span>

</dd> <dt>

<span data-ttu-id="671e0-125">**\_Objeto Frequency**</span><span class="sxs-lookup"><span data-stu-id="671e0-125">**Frequency\_Object**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="671e0-126">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="671e0-126">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="671e0-127">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="671e0-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="671e0-128">Frequência em tiques por segundo da propriedade **do \_ objeto timestamp** .</span><span class="sxs-lookup"><span data-stu-id="671e0-128">Frequency in ticks per second of the **Timestamp\_Object** property.</span></span> <span data-ttu-id="671e0-129">Quando em subclasse, o provedor define essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="671e0-129">When sub-classed, the provider defines this property.</span></span>

<span data-ttu-id="671e0-130">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="671e0-130">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

<span data-ttu-id="671e0-131">Essa propriedade é herdada [**do \_ desempenho do Win32**](win32-perf.md).</span><span class="sxs-lookup"><span data-stu-id="671e0-131">This property is inherited from [**Win32\_Perf**](win32-perf.md).</span></span>

</dd> <dt>

<span data-ttu-id="671e0-132">**Frequência \_ PerfTime**</span><span class="sxs-lookup"><span data-stu-id="671e0-132">**Frequency\_PerfTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="671e0-133">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="671e0-133">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="671e0-134">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="671e0-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="671e0-135">Frequência em tiques por segundo da propriedade **de \_ PerfTime de frequência** .</span><span class="sxs-lookup"><span data-stu-id="671e0-135">Frequency in ticks per second of the **Frequency\_PerfTime** property.</span></span> <span data-ttu-id="671e0-136">Um valor pode ser obtido chamando a função do Windows [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter).</span><span class="sxs-lookup"><span data-stu-id="671e0-136">A value can be obtained by calling the Windows function [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter).</span></span>

<span data-ttu-id="671e0-137">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="671e0-137">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

<span data-ttu-id="671e0-138">Essa propriedade é herdada [**do \_ desempenho do Win32**](win32-perf.md).</span><span class="sxs-lookup"><span data-stu-id="671e0-138">This property is inherited from [**Win32\_Perf**](win32-perf.md).</span></span>

</dd> <dt>

<span data-ttu-id="671e0-139">**Frequência \_ Sys100NS**</span><span class="sxs-lookup"><span data-stu-id="671e0-139">**Frequency\_Sys100NS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="671e0-140">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="671e0-140">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="671e0-141">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="671e0-141">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="671e0-142">Frequência em tiques por segundo da propriedade **timestamp \_ Sys100NS** (10 milhões).</span><span class="sxs-lookup"><span data-stu-id="671e0-142">Frequency in ticks per second of the **Timestamp\_Sys100NS** property (10000000).</span></span>

<span data-ttu-id="671e0-143">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="671e0-143">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

<span data-ttu-id="671e0-144">Essa propriedade é herdada [**do \_ desempenho do Win32**](win32-perf.md).</span><span class="sxs-lookup"><span data-stu-id="671e0-144">This property is inherited from [**Win32\_Perf**](win32-perf.md).</span></span>

</dd> <dt>

<span data-ttu-id="671e0-145">**Nome**</span><span class="sxs-lookup"><span data-stu-id="671e0-145">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="671e0-146">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="671e0-146">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="671e0-147">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="671e0-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="671e0-148">Qualificadores: [**maxlen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="671e0-148">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="671e0-149">Rótulo pelo qual a estatística ou métrica é conhecida.</span><span class="sxs-lookup"><span data-stu-id="671e0-149">Label by which the statistic or metric is known.</span></span> <span data-ttu-id="671e0-150">Quando em uma subclasse, essa propriedade pode ser substituída como uma propriedade de chave.</span><span class="sxs-lookup"><span data-stu-id="671e0-150">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="671e0-151">Essa propriedade é herdada do [**CIM \_ StatisticalInformation**](cim-statisticalinformation.md).</span><span class="sxs-lookup"><span data-stu-id="671e0-151">This property is inherited from [**CIM\_StatisticalInformation**](cim-statisticalinformation.md).</span></span>

</dd> <dt>

<span data-ttu-id="671e0-152">**\_Objeto timestamp**</span><span class="sxs-lookup"><span data-stu-id="671e0-152">**Timestamp\_Object**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="671e0-153">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="671e0-153">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="671e0-154">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="671e0-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="671e0-155">Carimbo de data/hora definido pelo objeto.</span><span class="sxs-lookup"><span data-stu-id="671e0-155">Object-defined timestamp.</span></span> <span data-ttu-id="671e0-156">O provedor define sua propriedade.</span><span class="sxs-lookup"><span data-stu-id="671e0-156">The provider defines his property.</span></span>

<span data-ttu-id="671e0-157">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="671e0-157">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

<span data-ttu-id="671e0-158">Essa propriedade é herdada [**do \_ desempenho do Win32**](win32-perf.md).</span><span class="sxs-lookup"><span data-stu-id="671e0-158">This property is inherited from [**Win32\_Perf**](win32-perf.md).</span></span>

</dd> <dt>

<span data-ttu-id="671e0-159">**Carimbo de data/hora \_ PerfTime**</span><span class="sxs-lookup"><span data-stu-id="671e0-159">**Timestamp\_PerfTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="671e0-160">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="671e0-160">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="671e0-161">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="671e0-161">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="671e0-162">Carimbo de data/hora do contador de alto desempenho.</span><span class="sxs-lookup"><span data-stu-id="671e0-162">High Performance counter timestamp.</span></span> <span data-ttu-id="671e0-163">Um valor pode ser obtido chamando a função do Windows [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter).</span><span class="sxs-lookup"><span data-stu-id="671e0-163">A value can be obtained by calling the Windows function [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter).</span></span>

<span data-ttu-id="671e0-164">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="671e0-164">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

<span data-ttu-id="671e0-165">Essa propriedade é herdada [**do \_ desempenho do Win32**](win32-perf.md).</span><span class="sxs-lookup"><span data-stu-id="671e0-165">This property is inherited from [**Win32\_Perf**](win32-perf.md).</span></span>

</dd> <dt>

<span data-ttu-id="671e0-166">**\_Sys100NS timestamp**</span><span class="sxs-lookup"><span data-stu-id="671e0-166">**Timestamp\_Sys100NS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="671e0-167">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="671e0-167">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="671e0-168">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="671e0-168">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="671e0-169">Valor de carimbo de data/hora em unidades de 100 nanossegundos.</span><span class="sxs-lookup"><span data-stu-id="671e0-169">Timestamp value in 100 nanosecond units.</span></span>

<span data-ttu-id="671e0-170">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="671e0-170">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

<span data-ttu-id="671e0-171">Essa propriedade é herdada [**do \_ desempenho do Win32**](win32-perf.md).</span><span class="sxs-lookup"><span data-stu-id="671e0-171">This property is inherited from [**Win32\_Perf**](win32-perf.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="671e0-172">Comentários</span><span class="sxs-lookup"><span data-stu-id="671e0-172">Remarks</span></span>

<span data-ttu-id="671e0-173">A classe **Win32 \_ PerfFormattedData** é derivada do [**\_ desempenho do Win32**](win32-perf.md), que é derivado de [**CIM \_ StatisticalInformation**](cim-statisticalinformation.md).</span><span class="sxs-lookup"><span data-stu-id="671e0-173">The **Win32\_PerfFormattedData** class is derived from [**Win32\_Perf**](win32-perf.md), which is derived from [**CIM\_StatisticalInformation**](cim-statisticalinformation.md).</span></span> <span data-ttu-id="671e0-174">A classe é encontrada no namespace **raiz \\ cimv2** .</span><span class="sxs-lookup"><span data-stu-id="671e0-174">The class is found in the **root\\cimv2** namespace.</span></span>

## <a name="requirements"></a><span data-ttu-id="671e0-175">Requisitos</span><span class="sxs-lookup"><span data-stu-id="671e0-175">Requirements</span></span>



| <span data-ttu-id="671e0-176">Requisito</span><span class="sxs-lookup"><span data-stu-id="671e0-176">Requirement</span></span> | <span data-ttu-id="671e0-177">Valor</span><span class="sxs-lookup"><span data-stu-id="671e0-177">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="671e0-178">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="671e0-178">Minimum supported client</span></span><br/> | <span data-ttu-id="671e0-179">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="671e0-179">Windows Vista</span></span><br/>                                                                   |
| <span data-ttu-id="671e0-180">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="671e0-180">Minimum supported server</span></span><br/> | <span data-ttu-id="671e0-181">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="671e0-181">Windows Server 2008</span></span><br/>                                                             |
| <span data-ttu-id="671e0-182">Namespace</span><span class="sxs-lookup"><span data-stu-id="671e0-182">Namespace</span></span><br/>                | <span data-ttu-id="671e0-183">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="671e0-183">Root\\CIMV2</span></span><br/>                                                                     |
| <span data-ttu-id="671e0-184">MOF</span><span class="sxs-lookup"><span data-stu-id="671e0-184">MOF</span></span><br/>                      | <dl> <span data-ttu-id="671e0-185"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="671e0-185"><dt>CIMWin32.mof</dt></span></span> </dl>    |
| <span data-ttu-id="671e0-186">DLL</span><span class="sxs-lookup"><span data-stu-id="671e0-186">DLL</span></span><br/>                      | <dl> <span data-ttu-id="671e0-187"><dt>WmiPerfInst.dll</dt></span><span class="sxs-lookup"><span data-stu-id="671e0-187"><dt>WmiPerfInst.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="671e0-188">Confira também</span><span class="sxs-lookup"><span data-stu-id="671e0-188">See also</span></span>

<dl> <dt>

[<span data-ttu-id="671e0-189">**Desempenho do Win32 \_**</span><span class="sxs-lookup"><span data-stu-id="671e0-189">**Win32\_Perf**</span></span>](win32-perf.md)
</dt> <dt>

[<span data-ttu-id="671e0-190">Classes de contador de desempenho</span><span class="sxs-lookup"><span data-stu-id="671e0-190">Performance Counter Classes</span></span>](performance-counter-classes.md)
</dt> <dt>

[<span data-ttu-id="671e0-191">Acessando classes de desempenho de WMI pré-instalado</span><span class="sxs-lookup"><span data-stu-id="671e0-191">Accessing WMI Preinstalled Performance Classes</span></span>](../wmisdk/accessing-wmi-preinstalled-performance-classes.md)
</dt> <dt>

[<span data-ttu-id="671e0-192">Tarefas do WMI: monitoramento de desempenho</span><span class="sxs-lookup"><span data-stu-id="671e0-192">WMI Tasks: Performance Monitoring</span></span>](../wmisdk/wmi-tasks--performance-monitoring.md)
</dt> <dt>

[<span data-ttu-id="671e0-193">Acessando dados de desempenho no script</span><span class="sxs-lookup"><span data-stu-id="671e0-193">Accessing Performance Data in Script</span></span>](../wmisdk/accessing-performance-data-in-script.md)
</dt> </dl>

 

 
