---
description: A classe base para as classes de contador de desempenho Win32 \_ PerfRawData e Win32 \_ PerfFormattedData.
ms.assetid: c754b619-a70f-4a56-8a43-2b36c8f8370b
ms.tgt_platform: multiple
title: Classe Win32_Perf
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Perf
- Root\CIMV2.Win32_Perf.Caption
- Root\CIMV2.Win32_Perf.Description
- Root\CIMV2.Win32_Perf.Name
- Root\CIMV2.Win32_Perf.Frequency_Object
- Root\CIMV2.Win32_Perf.Frequency_PerfTime
- Root\CIMV2.Win32_Perf.Frequency_Sys100NS
- Root\CIMV2.Win32_Perf.Timestamp_Object
- Root\CIMV2.Win32_Perf.Timestamp_PerfTime
- Root\CIMV2.Win32_Perf.Timestamp_Sys100NS
api_type:
- DllExport
api_location:
- WmiPerfInst.dll
ms.openlocfilehash: 13b339e95e175e4d2dff50c0a9674f8002933c1a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105753973"
---
# <a name="win32_perf-class"></a><span data-ttu-id="a9d0d-103">\_Classe perf Win32</span><span class="sxs-lookup"><span data-stu-id="a9d0d-103">Win32\_Perf class</span></span>

<span data-ttu-id="a9d0d-104">A classe base para as classes de contador de desempenho [**Win32 \_ PerfRawData**](win32-perfrawdata.md) e [**Win32 \_ PerfFormattedData**](win32-perfformatteddata.md).</span><span class="sxs-lookup"><span data-stu-id="a9d0d-104">The base class for the performance counter classes [**Win32\_PerfRawData**](win32-perfrawdata.md) and [**Win32\_PerfFormattedData**](win32-perfformatteddata.md).</span></span>

<span data-ttu-id="a9d0d-105">**Win32 \_ Perf** define as propriedades necessárias de carimbo de data/hora e frequência usadas [**nos algoritmos de**](../wmisdk/countertype-qualifier.md) CounterType para as classes de contador de desempenho.</span><span class="sxs-lookup"><span data-stu-id="a9d0d-105">**Win32\_Perf** defines the required timestamp and frequency properties used in the [**CounterType**](../wmisdk/countertype-qualifier.md) algorithms for the performance counter classes.</span></span>

<span data-ttu-id="a9d0d-106">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="a9d0d-106">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="a9d0d-107">As propriedades e os métodos estão em ordem alfabética, não em ordem de MOF.</span><span class="sxs-lookup"><span data-stu-id="a9d0d-107">Properties and methods are in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="a9d0d-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a9d0d-108">Syntax</span></span>

``` syntax
[abstract, AMENDMENT]
class Win32_Perf : CIM_StatisticalInformation
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

## <a name="members"></a><span data-ttu-id="a9d0d-109">Membros</span><span class="sxs-lookup"><span data-stu-id="a9d0d-109">Members</span></span>

<span data-ttu-id="a9d0d-110">A **classe \_ perf do Win32** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="a9d0d-110">The **Win32\_Perf** class has these types of members:</span></span>

-   [<span data-ttu-id="a9d0d-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="a9d0d-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a9d0d-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="a9d0d-112">Properties</span></span>

<span data-ttu-id="a9d0d-113">A **classe \_ perf do Win32** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="a9d0d-113">The **Win32\_Perf** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a9d0d-114">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="a9d0d-114">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9d0d-115">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="a9d0d-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a9d0d-116">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a9d0d-116">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a9d0d-117">Qualificadores: [**maxlen**](../wmisdk/standard-qualifiers.md) (64)</span><span class="sxs-lookup"><span data-stu-id="a9d0d-117">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="a9d0d-118">Breve descrição textual para a estatística ou métrica.</span><span class="sxs-lookup"><span data-stu-id="a9d0d-118">Short textual description for the statistic or metric.</span></span>

<span data-ttu-id="a9d0d-119">Essa propriedade é herdada do [**CIM \_ StatisticalInformation**](cim-statisticalinformation.md).</span><span class="sxs-lookup"><span data-stu-id="a9d0d-119">This property is inherited from [**CIM\_StatisticalInformation**](cim-statisticalinformation.md).</span></span>

</dd> <dt>

<span data-ttu-id="a9d0d-120">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="a9d0d-120">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9d0d-121">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="a9d0d-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a9d0d-122">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a9d0d-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a9d0d-123">Descrição textual da estatística ou métrica.</span><span class="sxs-lookup"><span data-stu-id="a9d0d-123">Textual description of the statistic or metric.</span></span>

<span data-ttu-id="a9d0d-124">Essa propriedade é herdada do [**CIM \_ StatisticalInformation**](cim-statisticalinformation.md).</span><span class="sxs-lookup"><span data-stu-id="a9d0d-124">This property is inherited from [**CIM\_StatisticalInformation**](cim-statisticalinformation.md).</span></span>

</dd> <dt>

<span data-ttu-id="a9d0d-125">**\_Objeto Frequency**</span><span class="sxs-lookup"><span data-stu-id="a9d0d-125">**Frequency\_Object**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9d0d-126">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="a9d0d-126">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="a9d0d-127">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a9d0d-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a9d0d-128">Frequência em tiques por segundo da propriedade **do \_ objeto timestamp** .</span><span class="sxs-lookup"><span data-stu-id="a9d0d-128">Frequency in ticks per second of the **Timestamp\_Object** property.</span></span> <span data-ttu-id="a9d0d-129">Quando em subclasse, o provedor define essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="a9d0d-129">When sub-classed, the provider defines this property.</span></span>

<span data-ttu-id="a9d0d-130">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="a9d0d-130">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="a9d0d-131">**Frequência \_ PerfTime**</span><span class="sxs-lookup"><span data-stu-id="a9d0d-131">**Frequency\_PerfTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9d0d-132">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="a9d0d-132">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="a9d0d-133">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a9d0d-133">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a9d0d-134">Frequência em tiques por segundo da propriedade **de \_ PerfTime de frequência** .</span><span class="sxs-lookup"><span data-stu-id="a9d0d-134">Frequency in ticks per second of the **Frequency\_PerfTime** property.</span></span> <span data-ttu-id="a9d0d-135">Um valor pode ser obtido chamando a função do Windows [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter).</span><span class="sxs-lookup"><span data-stu-id="a9d0d-135">A value can be obtained by calling the Windows function [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter).</span></span>

<span data-ttu-id="a9d0d-136">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="a9d0d-136">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="a9d0d-137">**Frequência \_ Sys100NS**</span><span class="sxs-lookup"><span data-stu-id="a9d0d-137">**Frequency\_Sys100NS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9d0d-138">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="a9d0d-138">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="a9d0d-139">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a9d0d-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a9d0d-140">Frequência em tiques por segundo da propriedade **timestamp \_ Sys100NS** (10 milhões).</span><span class="sxs-lookup"><span data-stu-id="a9d0d-140">Frequency in ticks per second of the **Timestamp\_Sys100NS** property (10000000).</span></span>

<span data-ttu-id="a9d0d-141">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="a9d0d-141">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="a9d0d-142">**Nome**</span><span class="sxs-lookup"><span data-stu-id="a9d0d-142">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9d0d-143">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="a9d0d-143">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a9d0d-144">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a9d0d-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a9d0d-145">Qualificadores: [**maxlen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="a9d0d-145">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="a9d0d-146">Rótulo pelo qual a estatística ou métrica é conhecida.</span><span class="sxs-lookup"><span data-stu-id="a9d0d-146">Label by which the statistic or metric is known.</span></span> <span data-ttu-id="a9d0d-147">Quando em uma subclasse, essa propriedade pode ser substituída como uma propriedade de chave.</span><span class="sxs-lookup"><span data-stu-id="a9d0d-147">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="a9d0d-148">Essa propriedade é herdada do [**CIM \_ StatisticalInformation**](cim-statisticalinformation.md).</span><span class="sxs-lookup"><span data-stu-id="a9d0d-148">This property is inherited from [**CIM\_StatisticalInformation**](cim-statisticalinformation.md).</span></span>

</dd> <dt>

<span data-ttu-id="a9d0d-149">**\_Objeto timestamp**</span><span class="sxs-lookup"><span data-stu-id="a9d0d-149">**Timestamp\_Object**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9d0d-150">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="a9d0d-150">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="a9d0d-151">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a9d0d-151">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a9d0d-152">Carimbo de data/hora definido pelo objeto.</span><span class="sxs-lookup"><span data-stu-id="a9d0d-152">Object-defined timestamp.</span></span> <span data-ttu-id="a9d0d-153">O provedor define sua propriedade.</span><span class="sxs-lookup"><span data-stu-id="a9d0d-153">The provider defines his property.</span></span>

<span data-ttu-id="a9d0d-154">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="a9d0d-154">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="a9d0d-155">**Carimbo de data/hora \_ PerfTime**</span><span class="sxs-lookup"><span data-stu-id="a9d0d-155">**Timestamp\_PerfTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9d0d-156">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="a9d0d-156">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="a9d0d-157">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a9d0d-157">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a9d0d-158">Carimbo de data/hora do contador de alto desempenho.</span><span class="sxs-lookup"><span data-stu-id="a9d0d-158">High Performance counter timestamp.</span></span> <span data-ttu-id="a9d0d-159">Um valor pode ser obtido chamando a função do Windows [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter).</span><span class="sxs-lookup"><span data-stu-id="a9d0d-159">A value can be obtained by calling the Windows function [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter).</span></span>

<span data-ttu-id="a9d0d-160">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="a9d0d-160">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="a9d0d-161">**\_Sys100NS timestamp**</span><span class="sxs-lookup"><span data-stu-id="a9d0d-161">**Timestamp\_Sys100NS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a9d0d-162">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="a9d0d-162">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="a9d0d-163">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a9d0d-163">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a9d0d-164">Valor de carimbo de data/hora em unidades de 100 nanossegundos.</span><span class="sxs-lookup"><span data-stu-id="a9d0d-164">Timestamp value in 100 nanosecond units.</span></span>

<span data-ttu-id="a9d0d-165">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="a9d0d-165">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a9d0d-166">Comentários</span><span class="sxs-lookup"><span data-stu-id="a9d0d-166">Remarks</span></span>

<span data-ttu-id="a9d0d-167">A **classe \_ perf do Win32** deriva de [**\_ StatisticalInformation CIM**](cim-statisticalinformation.md).</span><span class="sxs-lookup"><span data-stu-id="a9d0d-167">The **Win32\_Perf** class derives from [**CIM\_StatisticalInformation**](cim-statisticalinformation.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a9d0d-168">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a9d0d-168">Requirements</span></span>



| <span data-ttu-id="a9d0d-169">Requisito</span><span class="sxs-lookup"><span data-stu-id="a9d0d-169">Requirement</span></span> | <span data-ttu-id="a9d0d-170">Valor</span><span class="sxs-lookup"><span data-stu-id="a9d0d-170">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="a9d0d-171">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a9d0d-171">Minimum supported client</span></span><br/> | <span data-ttu-id="a9d0d-172">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a9d0d-172">Windows Vista</span></span><br/>                                                                   |
| <span data-ttu-id="a9d0d-173">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a9d0d-173">Minimum supported server</span></span><br/> | <span data-ttu-id="a9d0d-174">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a9d0d-174">Windows Server 2008</span></span><br/>                                                             |
| <span data-ttu-id="a9d0d-175">Namespace</span><span class="sxs-lookup"><span data-stu-id="a9d0d-175">Namespace</span></span><br/>                | <span data-ttu-id="a9d0d-176">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="a9d0d-176">Root\\CIMV2</span></span><br/>                                                                     |
| <span data-ttu-id="a9d0d-177">DLL</span><span class="sxs-lookup"><span data-stu-id="a9d0d-177">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a9d0d-178"><dt>WmiPerfInst.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a9d0d-178"><dt>WmiPerfInst.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a9d0d-179">Confira também</span><span class="sxs-lookup"><span data-stu-id="a9d0d-179">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a9d0d-180">**\_STATISTICALINFORMATION CIM**</span><span class="sxs-lookup"><span data-stu-id="a9d0d-180">**CIM\_StatisticalInformation**</span></span>](cim-statisticalinformation.md)
</dt> <dt>

[<span data-ttu-id="a9d0d-181">Classes de contador de desempenho</span><span class="sxs-lookup"><span data-stu-id="a9d0d-181">Performance Counter Classes</span></span>](performance-counter-classes.md)
</dt> <dt>

[<span data-ttu-id="a9d0d-182">Acessando classes de desempenho de WMI pré-instalado</span><span class="sxs-lookup"><span data-stu-id="a9d0d-182">Accessing WMI Preinstalled Performance Classes</span></span>](../wmisdk/accessing-wmi-preinstalled-performance-classes.md)
</dt> <dt>

[<span data-ttu-id="a9d0d-183">Tarefas do WMI: monitoramento de desempenho</span><span class="sxs-lookup"><span data-stu-id="a9d0d-183">WMI Tasks: Performance Monitoring</span></span>](../wmisdk/wmi-tasks--performance-monitoring.md)
</dt> <dt>

[<span data-ttu-id="a9d0d-184">Acessando dados de desempenho no script</span><span class="sxs-lookup"><span data-stu-id="a9d0d-184">Accessing Performance Data in Script</span></span>](../wmisdk/accessing-performance-data-in-script.md)
</dt> </dl>

 

 
