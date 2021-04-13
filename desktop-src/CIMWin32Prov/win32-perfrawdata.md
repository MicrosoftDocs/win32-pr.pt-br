---
description: A classe base abstrata para todas as classes de contador de desempenho brutos concretos.
ms.assetid: 3c457996-54d9-4425-8a57-15176d027e3a
ms.tgt_platform: multiple
title: Classe Win32_PerfRawData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_PerfRawData
- Win32_PerfRawData.Caption
- Win32_PerfRawData.Description
- Win32_PerfRawData.Name
- Win32_PerfRawData.Frequency_Object
- Win32_PerfRawData.Frequency_PerfTime
- Win32_PerfRawData.Frequency_Sys100NS
- Win32_PerfRawData.Timestamp_Object
- Win32_PerfRawData.Timestamp_PerfTime
- Win32_PerfRawData.Timestamp_Sys100NS
api_type:
- DllExport
api_location:
- WmiPerfInst.dll
ms.openlocfilehash: db5b74ae7508d15a48d2f71c3a586ad7e40362f7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501105"
---
# <a name="win32_perfrawdata-class"></a><span data-ttu-id="776f3-103">\_Classe Win32 PerfRawData</span><span class="sxs-lookup"><span data-stu-id="776f3-103">Win32\_PerfRawData class</span></span>

<span data-ttu-id="776f3-104">A classe base abstrata para todas as classes de contador de desempenho brutos concretos.</span><span class="sxs-lookup"><span data-stu-id="776f3-104">The abstract base class for all concrete raw performance counter classes.</span></span>

<span data-ttu-id="776f3-105">Para aparecer no monitor do sistema, as classes do contador de desempenho devem ser adicionadas ao \\ namespace raiz cimv2 e derivadas do **Win32 \_ PerfRawData**.</span><span class="sxs-lookup"><span data-stu-id="776f3-105">To appear in System Monitor, performance counter classes must be added to the root\\cimv2 namespace and derived from **Win32\_PerfRawData**.</span></span> <span data-ttu-id="776f3-106">Os dados nessas classes são fornecidos pelo [provedor de contador de desempenho](../wmisdk/performance-counter-provider.md)de alto desempenho.</span><span class="sxs-lookup"><span data-stu-id="776f3-106">Data in these classes are provided by the high-performance [Performance Counter Provider](../wmisdk/performance-counter-provider.md).</span></span>

<span data-ttu-id="776f3-107">As propriedades a seguir são herdadas quando uma classe é derivada do **Win32 \_ PerfRawData**:</span><span class="sxs-lookup"><span data-stu-id="776f3-107">The following properties are inherited when a class is derived from **Win32\_PerfRawData**:</span></span>

-   <span data-ttu-id="776f3-108">**Carimbo de data/hora \_ PerfTime**</span><span class="sxs-lookup"><span data-stu-id="776f3-108">**Timestamp\_PerfTime**</span></span>
-   <span data-ttu-id="776f3-109">**\_Sys100NS timestamp**</span><span class="sxs-lookup"><span data-stu-id="776f3-109">**Timestamp\_Sys100NS**</span></span>
-   <span data-ttu-id="776f3-110">**\_Objeto timestamp**</span><span class="sxs-lookup"><span data-stu-id="776f3-110">**Timestamp\_Object**</span></span>
-   <span data-ttu-id="776f3-111">**Frequência \_ PerfTime**</span><span class="sxs-lookup"><span data-stu-id="776f3-111">**Frequency\_PerfTime**</span></span>
-   <span data-ttu-id="776f3-112">**Frequência \_ Sys100NS**</span><span class="sxs-lookup"><span data-stu-id="776f3-112">**Frequency\_Sys100NS**</span></span>
-   <span data-ttu-id="776f3-113">**\_Objeto Frequency**</span><span class="sxs-lookup"><span data-stu-id="776f3-113">**Frequency\_Object**</span></span>

<span data-ttu-id="776f3-114">Em cada caso, as propriedades devem ser preenchidas pelo provedor ou a classe não pode ser exibida no monitor do sistema.</span><span class="sxs-lookup"><span data-stu-id="776f3-114">In each case, the properties must be filled out by the provider or the class cannot be displayed in System Monitor.</span></span> <span data-ttu-id="776f3-115">Essas propriedades são usadas para computar fórmulas de tipo de contador por consumidores de dados de desempenho.</span><span class="sxs-lookup"><span data-stu-id="776f3-115">These properties are used to compute counter type formulas by consumers of performance data.</span></span>

<span data-ttu-id="776f3-116">A sintaxe a seguir é simplificada do código MOF e mostra todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="776f3-116">The following syntax is simplified from MOF code and shows all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="776f3-117">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="776f3-117">Syntax</span></span>

``` syntax
[abstract, AMENDMENT]
class Win32_PerfRawData : Win32_Perf
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

## <a name="members"></a><span data-ttu-id="776f3-118">Membros</span><span class="sxs-lookup"><span data-stu-id="776f3-118">Members</span></span>

<span data-ttu-id="776f3-119">A classe **Win32 \_ PerfRawData** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="776f3-119">The **Win32\_PerfRawData** class has these types of members:</span></span>

-   [<span data-ttu-id="776f3-120">Propriedades</span><span class="sxs-lookup"><span data-stu-id="776f3-120">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="776f3-121">Propriedades</span><span class="sxs-lookup"><span data-stu-id="776f3-121">Properties</span></span>

<span data-ttu-id="776f3-122">A classe **Win32 \_ PerfRawData** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="776f3-122">The **Win32\_PerfRawData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="776f3-123">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="776f3-123">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="776f3-124">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="776f3-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="776f3-125">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="776f3-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="776f3-126">Qualificadores: [**maxlen**](../wmisdk/standard-qualifiers.md) (64)</span><span class="sxs-lookup"><span data-stu-id="776f3-126">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)</span></span>
</dt> </dl>

<span data-ttu-id="776f3-127">Breve descrição textual para a estatística ou métrica.</span><span class="sxs-lookup"><span data-stu-id="776f3-127">Short textual description for the statistic or metric.</span></span>

<span data-ttu-id="776f3-128">Essa propriedade é herdada do [**CIM \_ StatisticalInformation**](cim-statisticalinformation.md).</span><span class="sxs-lookup"><span data-stu-id="776f3-128">This property is inherited from [**CIM\_StatisticalInformation**](cim-statisticalinformation.md).</span></span>

</dd> <dt>

<span data-ttu-id="776f3-129">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="776f3-129">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="776f3-130">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="776f3-130">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="776f3-131">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="776f3-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="776f3-132">Descrição textual da estatística ou métrica.</span><span class="sxs-lookup"><span data-stu-id="776f3-132">Textual description of the statistic or metric.</span></span>

<span data-ttu-id="776f3-133">Essa propriedade é herdada do [**CIM \_ StatisticalInformation**](cim-statisticalinformation.md).</span><span class="sxs-lookup"><span data-stu-id="776f3-133">This property is inherited from [**CIM\_StatisticalInformation**](cim-statisticalinformation.md).</span></span>

</dd> <dt>

<span data-ttu-id="776f3-134">**\_Objeto Frequency**</span><span class="sxs-lookup"><span data-stu-id="776f3-134">**Frequency\_Object**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="776f3-135">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="776f3-135">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="776f3-136">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="776f3-136">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="776f3-137">Frequência em tiques por segundo da propriedade **do \_ objeto timestamp** .</span><span class="sxs-lookup"><span data-stu-id="776f3-137">Frequency in ticks per second of the **Timestamp\_Object** property.</span></span> <span data-ttu-id="776f3-138">Quando em subclasse, o provedor define essa propriedade.</span><span class="sxs-lookup"><span data-stu-id="776f3-138">When sub-classed, the provider defines this property.</span></span>

<span data-ttu-id="776f3-139">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="776f3-139">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

<span data-ttu-id="776f3-140">Essa propriedade é herdada [**do \_ desempenho do Win32**](win32-perf.md).</span><span class="sxs-lookup"><span data-stu-id="776f3-140">This property is inherited from [**Win32\_Perf**](win32-perf.md).</span></span>

</dd> <dt>

<span data-ttu-id="776f3-141">**Frequência \_ PerfTime**</span><span class="sxs-lookup"><span data-stu-id="776f3-141">**Frequency\_PerfTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="776f3-142">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="776f3-142">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="776f3-143">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="776f3-143">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="776f3-144">Frequência em tiques por segundo da propriedade **de \_ PerfTime de frequência** .</span><span class="sxs-lookup"><span data-stu-id="776f3-144">Frequency in ticks per second of the **Frequency\_PerfTime** property.</span></span> <span data-ttu-id="776f3-145">Um valor pode ser obtido chamando a função do Windows [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter).</span><span class="sxs-lookup"><span data-stu-id="776f3-145">A value can be obtained by calling the Windows function [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter).</span></span>

<span data-ttu-id="776f3-146">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="776f3-146">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

<span data-ttu-id="776f3-147">Essa propriedade é herdada [**do \_ desempenho do Win32**](win32-perf.md).</span><span class="sxs-lookup"><span data-stu-id="776f3-147">This property is inherited from [**Win32\_Perf**](win32-perf.md).</span></span>

</dd> <dt>

<span data-ttu-id="776f3-148">**Frequência \_ Sys100NS**</span><span class="sxs-lookup"><span data-stu-id="776f3-148">**Frequency\_Sys100NS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="776f3-149">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="776f3-149">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="776f3-150">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="776f3-150">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="776f3-151">Frequência em tiques por segundo da propriedade **timestamp \_ Sys100NS** (10 milhões).</span><span class="sxs-lookup"><span data-stu-id="776f3-151">Frequency in ticks per second of the **Timestamp\_Sys100NS** property (10000000).</span></span>

<span data-ttu-id="776f3-152">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="776f3-152">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

<span data-ttu-id="776f3-153">Essa propriedade é herdada [**do \_ desempenho do Win32**](win32-perf.md).</span><span class="sxs-lookup"><span data-stu-id="776f3-153">This property is inherited from [**Win32\_Perf**](win32-perf.md).</span></span>

</dd> <dt>

<span data-ttu-id="776f3-154">**Nome**</span><span class="sxs-lookup"><span data-stu-id="776f3-154">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="776f3-155">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="776f3-155">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="776f3-156">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="776f3-156">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="776f3-157">Qualificadores: [**maxlen**](../wmisdk/standard-qualifiers.md) (256)</span><span class="sxs-lookup"><span data-stu-id="776f3-157">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)</span></span>
</dt> </dl>

<span data-ttu-id="776f3-158">Rótulo pelo qual a estatística ou métrica é conhecida.</span><span class="sxs-lookup"><span data-stu-id="776f3-158">Label by which the statistic or metric is known.</span></span> <span data-ttu-id="776f3-159">Quando em uma subclasse, essa propriedade pode ser substituída como uma propriedade de chave.</span><span class="sxs-lookup"><span data-stu-id="776f3-159">When subclassed, this property can be overridden to be a key property.</span></span>

<span data-ttu-id="776f3-160">Essa propriedade é herdada do [**CIM \_ StatisticalInformation**](cim-statisticalinformation.md).</span><span class="sxs-lookup"><span data-stu-id="776f3-160">This property is inherited from [**CIM\_StatisticalInformation**](cim-statisticalinformation.md).</span></span>

</dd> <dt>

<span data-ttu-id="776f3-161">**\_Objeto timestamp**</span><span class="sxs-lookup"><span data-stu-id="776f3-161">**Timestamp\_Object**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="776f3-162">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="776f3-162">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="776f3-163">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="776f3-163">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="776f3-164">Carimbo de data/hora definido pelo objeto.</span><span class="sxs-lookup"><span data-stu-id="776f3-164">Object-defined timestamp.</span></span> <span data-ttu-id="776f3-165">O provedor define sua propriedade.</span><span class="sxs-lookup"><span data-stu-id="776f3-165">The provider defines his property.</span></span>

<span data-ttu-id="776f3-166">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="776f3-166">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

<span data-ttu-id="776f3-167">Essa propriedade é herdada [**do \_ desempenho do Win32**](win32-perf.md).</span><span class="sxs-lookup"><span data-stu-id="776f3-167">This property is inherited from [**Win32\_Perf**](win32-perf.md).</span></span>

</dd> <dt>

<span data-ttu-id="776f3-168">**Carimbo de data/hora \_ PerfTime**</span><span class="sxs-lookup"><span data-stu-id="776f3-168">**Timestamp\_PerfTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="776f3-169">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="776f3-169">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="776f3-170">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="776f3-170">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="776f3-171">Carimbo de data/hora do contador de alto desempenho.</span><span class="sxs-lookup"><span data-stu-id="776f3-171">High Performance counter timestamp.</span></span> <span data-ttu-id="776f3-172">Um valor pode ser obtido chamando a função do Windows [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter).</span><span class="sxs-lookup"><span data-stu-id="776f3-172">A value can be obtained by calling the Windows function [**QueryPerformanceCounter**](/windows/win32/api/profileapi/nf-profileapi-queryperformancecounter).</span></span>

<span data-ttu-id="776f3-173">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="776f3-173">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

<span data-ttu-id="776f3-174">Essa propriedade é herdada [**do \_ desempenho do Win32**](win32-perf.md).</span><span class="sxs-lookup"><span data-stu-id="776f3-174">This property is inherited from [**Win32\_Perf**](win32-perf.md).</span></span>

</dd> <dt>

<span data-ttu-id="776f3-175">**\_Sys100NS timestamp**</span><span class="sxs-lookup"><span data-stu-id="776f3-175">**Timestamp\_Sys100NS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="776f3-176">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="776f3-176">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="776f3-177">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="776f3-177">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="776f3-178">Valor de carimbo de data/hora em unidades de 100 nanossegundos.</span><span class="sxs-lookup"><span data-stu-id="776f3-178">Timestamp value in 100 nanosecond units.</span></span>

<span data-ttu-id="776f3-179">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="776f3-179">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

<span data-ttu-id="776f3-180">Essa propriedade é herdada [**do \_ desempenho do Win32**](win32-perf.md).</span><span class="sxs-lookup"><span data-stu-id="776f3-180">This property is inherited from [**Win32\_Perf**](win32-perf.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="776f3-181">Comentários</span><span class="sxs-lookup"><span data-stu-id="776f3-181">Remarks</span></span>

<span data-ttu-id="776f3-182">A classe **Win32 \_ PerfRawData** é derivada do [**\_ desempenho do Win32**](win32-perf.md), que é derivado de [**CIM \_ StatisticalInformation**](cim-statisticalinformation.md).</span><span class="sxs-lookup"><span data-stu-id="776f3-182">The **Win32\_PerfRawData** class is derived from [**Win32\_Perf**](win32-perf.md), which is derived from [**CIM\_StatisticalInformation**](cim-statisticalinformation.md).</span></span>

<span data-ttu-id="776f3-183">Todas as classes derivadas do [**Win32 \_ perf**](win32-perf.md) são projetadas para serem usadas com um objeto de [*atualização*](../wmisdk/gloss-r.md) .</span><span class="sxs-lookup"><span data-stu-id="776f3-183">All classes derived from [**Win32\_Perf**](win32-perf.md) are designed to be used with a [*refresher*](../wmisdk/gloss-r.md) object.</span></span> <span data-ttu-id="776f3-184">Para obter mais informações sobre como criar e usar um objeto atualizador na linguagem de programação C++, consulte [acessando dados de desempenho em C++](../wmisdk/accessing-performance-data-in-c--.md).</span><span class="sxs-lookup"><span data-stu-id="776f3-184">For more information about how to create and use a refresher object in the C++ programming language, see [Accessing Performance Data in C++](../wmisdk/accessing-performance-data-in-c--.md).</span></span> <span data-ttu-id="776f3-185">Para obter mais informações sobre como criar e usar um objeto de atualização em uma linguagem de programação de script, consulte [atualizando dados do WMI em scripts](../wmisdk/refreshing-wmi-data-in-scripts.md).</span><span class="sxs-lookup"><span data-stu-id="776f3-185">For more information about how to create and use a refresher object in a script programming language, see [Refreshing WMI Data in Scripts](../wmisdk/refreshing-wmi-data-in-scripts.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="776f3-186">Requisitos</span><span class="sxs-lookup"><span data-stu-id="776f3-186">Requirements</span></span>



| <span data-ttu-id="776f3-187">Requisito</span><span class="sxs-lookup"><span data-stu-id="776f3-187">Requirement</span></span> | <span data-ttu-id="776f3-188">Valor</span><span class="sxs-lookup"><span data-stu-id="776f3-188">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="776f3-189">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="776f3-189">Minimum supported client</span></span><br/> | <span data-ttu-id="776f3-190">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="776f3-190">Windows Vista</span></span><br/>                                                                   |
| <span data-ttu-id="776f3-191">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="776f3-191">Minimum supported server</span></span><br/> | <span data-ttu-id="776f3-192">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="776f3-192">Windows Server 2008</span></span><br/>                                                             |
| <span data-ttu-id="776f3-193">Namespace</span><span class="sxs-lookup"><span data-stu-id="776f3-193">Namespace</span></span><br/>                | <span data-ttu-id="776f3-194">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="776f3-194">Root\\CIMV2</span></span><br/>                                                                     |
| <span data-ttu-id="776f3-195">MOF</span><span class="sxs-lookup"><span data-stu-id="776f3-195">MOF</span></span><br/>                      | <dl> <span data-ttu-id="776f3-196"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="776f3-196"><dt>CIMWin32.mof</dt></span></span> </dl>    |
| <span data-ttu-id="776f3-197">DLL</span><span class="sxs-lookup"><span data-stu-id="776f3-197">DLL</span></span><br/>                      | <dl> <span data-ttu-id="776f3-198"><dt>WmiPerfInst.dll</dt></span><span class="sxs-lookup"><span data-stu-id="776f3-198"><dt>WmiPerfInst.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="776f3-199">Confira também</span><span class="sxs-lookup"><span data-stu-id="776f3-199">See also</span></span>

<dl> <dt>

[<span data-ttu-id="776f3-200">**Desempenho do Win32 \_**</span><span class="sxs-lookup"><span data-stu-id="776f3-200">**Win32\_Perf**</span></span>](win32-perf.md)
</dt> <dt>

[<span data-ttu-id="776f3-201">Classes de contador de desempenho</span><span class="sxs-lookup"><span data-stu-id="776f3-201">Performance Counter Classes</span></span>](performance-counter-classes.md)
</dt> <dt>

[<span data-ttu-id="776f3-202">Acessando classes de desempenho de WMI pré-instalado</span><span class="sxs-lookup"><span data-stu-id="776f3-202">Accessing WMI Preinstalled Performance Classes</span></span>](../wmisdk/accessing-wmi-preinstalled-performance-classes.md)
</dt> <dt>

[<span data-ttu-id="776f3-203">Tarefas do WMI: monitoramento de desempenho</span><span class="sxs-lookup"><span data-stu-id="776f3-203">WMI Tasks: Performance Monitoring</span></span>](../wmisdk/wmi-tasks--performance-monitoring.md)
</dt> <dt>

[<span data-ttu-id="776f3-204">Acessando dados de desempenho no script</span><span class="sxs-lookup"><span data-stu-id="776f3-204">Accessing Performance Data in Script</span></span>](../wmisdk/accessing-performance-data-in-script.md)
</dt> </dl>

 

 
