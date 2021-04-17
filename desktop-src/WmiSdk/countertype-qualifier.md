---
description: O qualificador de tipo contém o valor inteiro para o tipo de contador de propriedade para propriedades em \_ classes PerfRawData do Win32. O Culináriatype contém as constantes para tipos de fórmulas de propriedade em \_ classes PerfFormattedData do Win32.
ms.assetid: aa79fcdb-503f-4928-b2b7-f07baeaf9fb5
ms.tgt_platform: multiple
title: Qualificador de tipo
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CounterType
api_type:
- NA
api_location: ''
ms.openlocfilehash: 883ee7aa2f230756d62294d46e6402fe7f962d4e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105768617"
---
# <a name="countertype-qualifier"></a><span data-ttu-id="29d20-104">Qualificador de tipo</span><span class="sxs-lookup"><span data-stu-id="29d20-104">CounterType Qualifier</span></span>

<span data-ttu-id="29d20-105">O qualificador de **tipo** contém o valor inteiro para o tipo de contador de propriedade para propriedades em classes [**\_ PerfRawData do Win32**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) .</span><span class="sxs-lookup"><span data-stu-id="29d20-105">The **CounterType** qualifier contains the integer value for the property counter type for properties in [**Win32\_PerfRawData**](/windows/desktop/CIMWin32Prov/win32-perfrawdata) classes.</span></span> <span data-ttu-id="29d20-106">O **culináriatype** contém as constantes para tipos de fórmulas de propriedade em classes [**\_ PerfFormattedData do Win32**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) .</span><span class="sxs-lookup"><span data-stu-id="29d20-106">The **CookingType** contains the constants for property formula types in [**Win32\_PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata) classes.</span></span>

<span data-ttu-id="29d20-107">Para obter mais informações e uma divisão dos tipos de contadores por função, consulte [tipos de contadores](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10)).</span><span class="sxs-lookup"><span data-stu-id="29d20-107">For more information and a breakdown of counter types by function, see [Counter Types](/previous-versions/windows/it-pro/windows-server-2003/cc785636(v=ws.10)).</span></span>



| <span data-ttu-id="29d20-108">CounterType</span><span class="sxs-lookup"><span data-stu-id="29d20-108">CounterType</span></span> | <span data-ttu-id="29d20-109">Culináriatype</span><span class="sxs-lookup"><span data-stu-id="29d20-109">CookingType</span></span>                              |
|-------------|------------------------------------------|
| <span data-ttu-id="29d20-110">0</span><span class="sxs-lookup"><span data-stu-id="29d20-110">0</span></span>           | <span data-ttu-id="29d20-111">contador de desempenho \_ \_ RAWCOUNT \_ hex</span><span class="sxs-lookup"><span data-stu-id="29d20-111">PERF\_COUNTER\_RAWCOUNT\_HEX</span></span>             |
| <span data-ttu-id="29d20-112">256</span><span class="sxs-lookup"><span data-stu-id="29d20-112">256</span></span>         | <span data-ttu-id="29d20-113">contador de desempenho \_ \_ grande \_ RAWCOUNT \_ hex</span><span class="sxs-lookup"><span data-stu-id="29d20-113">PERF\_COUNTER\_LARGE\_RAWCOUNT\_HEX</span></span>      |
| <span data-ttu-id="29d20-114">2816</span><span class="sxs-lookup"><span data-stu-id="29d20-114">2816</span></span>        | <span data-ttu-id="29d20-115">\_texto do contador de desempenho \_</span><span class="sxs-lookup"><span data-stu-id="29d20-115">PERF\_COUNTER\_TEXT</span></span>                      |
| <span data-ttu-id="29d20-116">65536</span><span class="sxs-lookup"><span data-stu-id="29d20-116">65536</span></span>       | <span data-ttu-id="29d20-117">contador de desempenho \_ \_ RAWCOUNT</span><span class="sxs-lookup"><span data-stu-id="29d20-117">PERF\_COUNTER\_RAWCOUNT</span></span>                  |
| <span data-ttu-id="29d20-118">65792</span><span class="sxs-lookup"><span data-stu-id="29d20-118">65792</span></span>       | <span data-ttu-id="29d20-119">contador de desempenho \_ \_ grande \_ RAWCOUNT</span><span class="sxs-lookup"><span data-stu-id="29d20-119">PERF\_COUNTER\_LARGE\_RAWCOUNT</span></span>           |
| <span data-ttu-id="29d20-120">73728</span><span class="sxs-lookup"><span data-stu-id="29d20-120">73728</span></span>       | <span data-ttu-id="29d20-121">PERF \_ duplo \_ bruto</span><span class="sxs-lookup"><span data-stu-id="29d20-121">PERF\_DOUBLE\_RAW</span></span>                        |
| <span data-ttu-id="29d20-122">4195328</span><span class="sxs-lookup"><span data-stu-id="29d20-122">4195328</span></span>     | <span data-ttu-id="29d20-123">\_Delta do contador de desempenho \_</span><span class="sxs-lookup"><span data-stu-id="29d20-123">PERF\_COUNTER\_DELTA</span></span>                     |
| <span data-ttu-id="29d20-124">4195584</span><span class="sxs-lookup"><span data-stu-id="29d20-124">4195584</span></span>     | <span data-ttu-id="29d20-125">\_ \_ Delta grande do contador de desempenho \_</span><span class="sxs-lookup"><span data-stu-id="29d20-125">PERF\_COUNTER\_LARGE\_DELTA</span></span>              |
| <span data-ttu-id="29d20-126">4260864</span><span class="sxs-lookup"><span data-stu-id="29d20-126">4260864</span></span>     | <span data-ttu-id="29d20-127">\_contador de exemplo de desempenho \_</span><span class="sxs-lookup"><span data-stu-id="29d20-127">PERF\_SAMPLE\_COUNTER</span></span>                    |
| <span data-ttu-id="29d20-128">4523008</span><span class="sxs-lookup"><span data-stu-id="29d20-128">4523008</span></span>     | <span data-ttu-id="29d20-129">\_tipo de \_ QUEUELEN do contador de desempenho \_</span><span class="sxs-lookup"><span data-stu-id="29d20-129">PERF\_COUNTER\_QUEUELEN\_TYPE</span></span>            |
| <span data-ttu-id="29d20-130">4523264</span><span class="sxs-lookup"><span data-stu-id="29d20-130">4523264</span></span>     | <span data-ttu-id="29d20-131">\_tipo de \_ \_ QUEUELEN grande do contador \_ de desempenho</span><span class="sxs-lookup"><span data-stu-id="29d20-131">PERF\_COUNTER\_LARGE\_QUEUELEN\_TYPE</span></span>     |
| <span data-ttu-id="29d20-132">5571840</span><span class="sxs-lookup"><span data-stu-id="29d20-132">5571840</span></span>     | <span data-ttu-id="29d20-133">Tipo de QUEUELEN do contador de desempenho de \_ \_ 100 NS \_ \_</span><span class="sxs-lookup"><span data-stu-id="29d20-133">PERF\_COUNTER\_100NS\_QUEUELEN\_TYPE</span></span>     |
| <span data-ttu-id="29d20-134">6620416</span><span class="sxs-lookup"><span data-stu-id="29d20-134">6620416</span></span>     | <span data-ttu-id="29d20-135">\_tipo de \_ QUEUELEN de tempo de obj do contador de \_ \_ desempenho \_</span><span class="sxs-lookup"><span data-stu-id="29d20-135">PERF\_COUNTER\_OBJ\_TIME\_QUEUELEN\_TYPE</span></span> |
| <span data-ttu-id="29d20-136">272696320</span><span class="sxs-lookup"><span data-stu-id="29d20-136">272696320</span></span>   | <span data-ttu-id="29d20-137">\_contador de contador de desempenho \_</span><span class="sxs-lookup"><span data-stu-id="29d20-137">PERF\_COUNTER\_COUNTER</span></span>                   |
| <span data-ttu-id="29d20-138">272696576</span><span class="sxs-lookup"><span data-stu-id="29d20-138">272696576</span></span>   | <span data-ttu-id="29d20-139">\_ \_ contagem em massa do contador de desempenho \_</span><span class="sxs-lookup"><span data-stu-id="29d20-139">PERF\_COUNTER\_BULK\_COUNT</span></span>               |
| <span data-ttu-id="29d20-140">537003008</span><span class="sxs-lookup"><span data-stu-id="29d20-140">537003008</span></span>   | <span data-ttu-id="29d20-141">\_fração bruta de desempenho \_</span><span class="sxs-lookup"><span data-stu-id="29d20-141">PERF\_RAW\_FRACTION</span></span>                      |
| <span data-ttu-id="29d20-142">541132032</span><span class="sxs-lookup"><span data-stu-id="29d20-142">541132032</span></span>   | <span data-ttu-id="29d20-143">\_Timer do contador de desempenho \_</span><span class="sxs-lookup"><span data-stu-id="29d20-143">PERF\_COUNTER\_TIMER</span></span>                     |
| <span data-ttu-id="29d20-144">541525248</span><span class="sxs-lookup"><span data-stu-id="29d20-144">541525248</span></span>   | <span data-ttu-id="29d20-145">\_ \_ temporizador do sistema de precisão de desempenho \_</span><span class="sxs-lookup"><span data-stu-id="29d20-145">PERF\_PRECISION\_SYSTEM\_TIMER</span></span>           |
| <span data-ttu-id="29d20-146">542180608</span><span class="sxs-lookup"><span data-stu-id="29d20-146">542180608</span></span>   | <span data-ttu-id="29d20-147">\_ \_ Temporizador 100NSEC perf</span><span class="sxs-lookup"><span data-stu-id="29d20-147">PERF\_100NSEC\_TIMER</span></span>                     |
| <span data-ttu-id="29d20-148">542573824</span><span class="sxs-lookup"><span data-stu-id="29d20-148">542573824</span></span>   | <span data-ttu-id="29d20-149">\_ \_ Temporizador de 100ns de precisão de desempenho \_</span><span class="sxs-lookup"><span data-stu-id="29d20-149">PERF\_PRECISION\_100NS\_TIMER</span></span>            |
| <span data-ttu-id="29d20-150">543229184</span><span class="sxs-lookup"><span data-stu-id="29d20-150">543229184</span></span>   | <span data-ttu-id="29d20-151">\_ \_ temporizador de tempo de obj perf \_</span><span class="sxs-lookup"><span data-stu-id="29d20-151">PERF\_OBJ\_TIME\_TIMER</span></span>                   |
| <span data-ttu-id="29d20-152">543622400</span><span class="sxs-lookup"><span data-stu-id="29d20-152">543622400</span></span>   | <span data-ttu-id="29d20-153">\_ \_ temporizador de objeto de precisão de desempenho \_</span><span class="sxs-lookup"><span data-stu-id="29d20-153">PERF\_PRECISION\_OBJECT\_TIMER</span></span>           |
| <span data-ttu-id="29d20-154">549585920</span><span class="sxs-lookup"><span data-stu-id="29d20-154">549585920</span></span>   | <span data-ttu-id="29d20-155">\_fração de exemplo de perf \_</span><span class="sxs-lookup"><span data-stu-id="29d20-155">PERF\_SAMPLE\_FRACTION</span></span>                   |
| <span data-ttu-id="29d20-156">557909248</span><span class="sxs-lookup"><span data-stu-id="29d20-156">557909248</span></span>   | <span data-ttu-id="29d20-157">Timer do contador de desempenho \_ \_ \_ inv</span><span class="sxs-lookup"><span data-stu-id="29d20-157">PERF\_COUNTER\_TIMER\_INV</span></span>                |
| <span data-ttu-id="29d20-158">558957824</span><span class="sxs-lookup"><span data-stu-id="29d20-158">558957824</span></span>   | <span data-ttu-id="29d20-159">\_Contador de \_ temporizador 100NSEC de desempenho \_ inv</span><span class="sxs-lookup"><span data-stu-id="29d20-159">PERF\_100NSEC\_TIMER\_INV</span></span>                |
| <span data-ttu-id="29d20-160">574686464</span><span class="sxs-lookup"><span data-stu-id="29d20-160">574686464</span></span>   | <span data-ttu-id="29d20-161">\_ \_ múltiplo Timer do contador de desempenho \_</span><span class="sxs-lookup"><span data-stu-id="29d20-161">PERF\_COUNTER\_MULTI\_TIMER</span></span>              |
| <span data-ttu-id="29d20-162">575735040</span><span class="sxs-lookup"><span data-stu-id="29d20-162">575735040</span></span>   | <span data-ttu-id="29d20-163">\_Timer de \_ vários \_ 100NSEC perf</span><span class="sxs-lookup"><span data-stu-id="29d20-163">PERF\_100NSEC\_MULTI\_TIMER</span></span>              |
| <span data-ttu-id="29d20-164">591463680</span><span class="sxs-lookup"><span data-stu-id="29d20-164">591463680</span></span>   | <span data-ttu-id="29d20-165">\_ \_ multi timer de \_ contador de desempenho \_</span><span class="sxs-lookup"><span data-stu-id="29d20-165">PERF\_COUNTER\_MULTI\_TIMER\_INV</span></span>         |
| <span data-ttu-id="29d20-166">592512256</span><span class="sxs-lookup"><span data-stu-id="29d20-166">592512256</span></span>   | <span data-ttu-id="29d20-167">PERF \_ 100NSEC \_ multi \_ timer \_ inv</span><span class="sxs-lookup"><span data-stu-id="29d20-167">PERF\_100NSEC\_MULTI\_TIMER\_INV</span></span>         |
| <span data-ttu-id="29d20-168">805438464</span><span class="sxs-lookup"><span data-stu-id="29d20-168">805438464</span></span>   | <span data-ttu-id="29d20-169">\_temporizador de média de desempenho \_</span><span class="sxs-lookup"><span data-stu-id="29d20-169">PERF\_AVERAGE\_TIMER</span></span>                     |
| <span data-ttu-id="29d20-170">807666944</span><span class="sxs-lookup"><span data-stu-id="29d20-170">807666944</span></span>   | <span data-ttu-id="29d20-171">\_tempo decorrido de desempenho \_</span><span class="sxs-lookup"><span data-stu-id="29d20-171">PERF\_ELAPSED\_TIME</span></span>                      |
| <span data-ttu-id="29d20-172">1073742336</span><span class="sxs-lookup"><span data-stu-id="29d20-172">1073742336</span></span>  | <span data-ttu-id="29d20-173">contador de desempenho \_ \_ NODATA</span><span class="sxs-lookup"><span data-stu-id="29d20-173">PERF\_COUNTER\_NODATA</span></span>                    |
| <span data-ttu-id="29d20-174">1073874176</span><span class="sxs-lookup"><span data-stu-id="29d20-174">1073874176</span></span>  | <span data-ttu-id="29d20-175">\_massa média de desempenho \_</span><span class="sxs-lookup"><span data-stu-id="29d20-175">PERF\_AVERAGE\_BULK</span></span>                      |
| <span data-ttu-id="29d20-176">1073939457</span><span class="sxs-lookup"><span data-stu-id="29d20-176">1073939457</span></span>  | <span data-ttu-id="29d20-177">\_base de exemplo de perf \_</span><span class="sxs-lookup"><span data-stu-id="29d20-177">PERF\_SAMPLE\_BASE</span></span>                       |
| <span data-ttu-id="29d20-178">1073939458</span><span class="sxs-lookup"><span data-stu-id="29d20-178">1073939458</span></span>  | <span data-ttu-id="29d20-179">\_base média de desempenho \_</span><span class="sxs-lookup"><span data-stu-id="29d20-179">PERF\_AVERAGE\_BASE</span></span>                      |
| <span data-ttu-id="29d20-180">1073939459</span><span class="sxs-lookup"><span data-stu-id="29d20-180">1073939459</span></span>  | <span data-ttu-id="29d20-181">\_base bruta de desempenho \_</span><span class="sxs-lookup"><span data-stu-id="29d20-181">PERF\_RAW\_BASE</span></span>                          |
| <span data-ttu-id="29d20-182">1073939712</span><span class="sxs-lookup"><span data-stu-id="29d20-182">1073939712</span></span>  | <span data-ttu-id="29d20-183">\_timestamp de precisão de desempenho \_</span><span class="sxs-lookup"><span data-stu-id="29d20-183">PERF\_PRECISION\_TIMESTAMP</span></span>               |
| <span data-ttu-id="29d20-184">1073939715</span><span class="sxs-lookup"><span data-stu-id="29d20-184">1073939715</span></span>  | <span data-ttu-id="29d20-185">\_ \_ base bruta de perf grande \_</span><span class="sxs-lookup"><span data-stu-id="29d20-185">PERF\_LARGE\_RAW\_BASE</span></span>                   |
| <span data-ttu-id="29d20-186">1107494144</span><span class="sxs-lookup"><span data-stu-id="29d20-186">1107494144</span></span>  | <span data-ttu-id="29d20-187">\_ \_ vários base do contador de desempenho \_</span><span class="sxs-lookup"><span data-stu-id="29d20-187">PERF\_COUNTER\_MULTI\_BASE</span></span>               |
| <span data-ttu-id="29d20-188">2147483648</span><span class="sxs-lookup"><span data-stu-id="29d20-188">2147483648</span></span>  | <span data-ttu-id="29d20-189">\_tipo de \_ histograma do contador de desempenho \_</span><span class="sxs-lookup"><span data-stu-id="29d20-189">PERF\_COUNTER\_HISTOGRAM\_TYPE</span></span>           |



 

## <a name="requirements"></a><span data-ttu-id="29d20-190">Requisitos</span><span class="sxs-lookup"><span data-stu-id="29d20-190">Requirements</span></span>



| <span data-ttu-id="29d20-191">Requisito</span><span class="sxs-lookup"><span data-stu-id="29d20-191">Requirement</span></span> | <span data-ttu-id="29d20-192">Valor</span><span class="sxs-lookup"><span data-stu-id="29d20-192">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="29d20-193">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="29d20-193">Minimum supported client</span></span><br/> | <span data-ttu-id="29d20-194">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="29d20-194">Windows Vista</span></span><br/>       |
| <span data-ttu-id="29d20-195">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="29d20-195">Minimum supported server</span></span><br/> | <span data-ttu-id="29d20-196">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="29d20-196">Windows Server 2008</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="29d20-197">Confira também</span><span class="sxs-lookup"><span data-stu-id="29d20-197">See also</span></span>

<dl> <dt>

[<span data-ttu-id="29d20-198">Qualificadores específicos para classes de desempenho WMI</span><span class="sxs-lookup"><span data-stu-id="29d20-198">Qualifiers Specific to WMI Performance Classes</span></span>](qualifiers-specific-to-wmi-performance-classes.md)
</dt> </dl>

 

