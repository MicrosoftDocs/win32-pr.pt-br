---
title: TraceLogging macros de wrapper
description: Lista as macros de wrapper para provedores de TraceLogging.
ms.assetid: 806F43F3-D376-4DBD-A4C5-B5F01E5D009D
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9dc28b3a35074089b1f5c613b041534b8b282423
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103637119"
---
# <a name="tracelogging-wrapper-macros"></a><span data-ttu-id="a3ef4-103">TraceLogging macros de wrapper</span><span class="sxs-lookup"><span data-stu-id="a3ef4-103">TraceLogging Wrapper Macros</span></span>

<span data-ttu-id="a3ef4-104">Lista as macros de wrapper para provedores de TraceLogging.</span><span class="sxs-lookup"><span data-stu-id="a3ef4-104">Lists the wrapper macros for TraceLogging providers.</span></span>

<span data-ttu-id="a3ef4-105">Para registrar eventos usando provedores de TraceLogging, você precisa usar as macros TraceLogging Write [**TraceLoggingWrite**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingwrite) ou [**TraceLoggingWriteActivity**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingwriteactivity).</span><span class="sxs-lookup"><span data-stu-id="a3ef4-105">In order to record events using TraceLogging providers, you need to use the TraceLogging write macros [**TraceLoggingWrite**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingwrite) or [**TraceLoggingWriteActivity**](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingwriteactivity).</span></span> <span data-ttu-id="a3ef4-106">Ambas as macros exigem que você empacote todos os dados de evento em uma macro wrapper.</span><span class="sxs-lookup"><span data-stu-id="a3ef4-106">Both of these macros require you to wrap any event data in a wrapper macro.</span></span> <span data-ttu-id="a3ef4-107">Há várias macros de wrapper diferentes para tipos de dados diferentes.</span><span class="sxs-lookup"><span data-stu-id="a3ef4-107">There are several different wrapper macros for different data types.</span></span> <span data-ttu-id="a3ef4-108">Para obter uma lista completa de macros do TraceLogging, consulte [macros do TraceLogging](trace-logging-macros.md).</span><span class="sxs-lookup"><span data-stu-id="a3ef4-108">For a complete list of TraceLogging macros, see [TraceLogging Macros](trace-logging-macros.md).</span></span>

<span data-ttu-id="a3ef4-109">Além das macros do wrapper acima, várias macros estão disponíveis para tipos de dados individuais.</span><span class="sxs-lookup"><span data-stu-id="a3ef4-109">In addition to the wrapper macros above, several macros are available for individual data types.</span></span> <span data-ttu-id="a3ef4-110">Todas essas macros têm o mesmo formato que a macro [TraceLoggingValue](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingvalue) .</span><span class="sxs-lookup"><span data-stu-id="a3ef4-110">All of these macros have the same format as the [TraceLoggingValue](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingvalue) macro.</span></span> <span data-ttu-id="a3ef4-111">Você pode usar a macro TraceLoggingValue para detectar automaticamente a macro wrapper apropriada a ser usada ou usar a macro específica diretamente.</span><span class="sxs-lookup"><span data-stu-id="a3ef4-111">You can use the TraceLoggingValue macro to automatically detect the appropriate wrapper macro to use, or use the specific macro directly.</span></span>

-   [<span data-ttu-id="a3ef4-112">**TraceLoggingBinary**</span><span class="sxs-lookup"><span data-stu-id="a3ef4-112">**TraceLoggingBinary**</span></span>](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingbinary)
-   [<span data-ttu-id="a3ef4-113">**TraceLoggingChannel**</span><span class="sxs-lookup"><span data-stu-id="a3ef4-113">**TraceLoggingChannel**</span></span>](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingchannel)
-   [<span data-ttu-id="a3ef4-114">**TraceLoggingCustomAttribute**</span><span class="sxs-lookup"><span data-stu-id="a3ef4-114">**TraceLoggingCustomAttribute**</span></span>](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingcustomattribute)
-   [<span data-ttu-id="a3ef4-115">**TraceLoggingDescription**</span><span class="sxs-lookup"><span data-stu-id="a3ef4-115">**TraceLoggingDescription**</span></span>](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingdescription)
-   [<span data-ttu-id="a3ef4-116">**TraceLoggingEventTag**</span><span class="sxs-lookup"><span data-stu-id="a3ef4-116">**TraceLoggingEventTag**</span></span>](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingeventtag)
-   [<span data-ttu-id="a3ef4-117">**TraceLoggingKeyword**</span><span class="sxs-lookup"><span data-stu-id="a3ef4-117">**TraceLoggingKeyword**</span></span>](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingkeyword)
-   [<span data-ttu-id="a3ef4-118">**TraceLoggingLevel**</span><span class="sxs-lookup"><span data-stu-id="a3ef4-118">**TraceLoggingLevel**</span></span>](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-tracelogginglevel)
-   [<span data-ttu-id="a3ef4-119">**TraceLoggingOpcode**</span><span class="sxs-lookup"><span data-stu-id="a3ef4-119">**TraceLoggingOpcode**</span></span>](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingopcode)
-   [<span data-ttu-id="a3ef4-120">**TraceLoggingSocketAddress**</span><span class="sxs-lookup"><span data-stu-id="a3ef4-120">**TraceLoggingSocketAddress**</span></span>](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingsocketaddress)
-   [<span data-ttu-id="a3ef4-121">**TraceLoggingStruct**</span><span class="sxs-lookup"><span data-stu-id="a3ef4-121">**TraceLoggingStruct**</span></span>](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingstruct)
-   [<span data-ttu-id="a3ef4-122">**TraceLoggingValue**</span><span class="sxs-lookup"><span data-stu-id="a3ef4-122">**TraceLoggingValue**</span></span>](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingvalue)

> [!Note]
>
> <span data-ttu-id="a3ef4-123">**TraceLoggingOptionGroup** é especificamente para uso dentro do provedor de definição de TRACELOGGING \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="a3ef4-123">**TraceLoggingOptionGroup** is specifically for use inside of TRACELOGGING\_DEFINE\_PROVIDER.</span></span>
>
> -   [<span data-ttu-id="a3ef4-124">**TraceLoggingOptionGroup**</span><span class="sxs-lookup"><span data-stu-id="a3ef4-124">**TraceLoggingOptionGroup**</span></span>](/windows/desktop/api/traceloggingprovider/nf-traceloggingprovider-traceloggingoptiongroup)

 

<span data-ttu-id="a3ef4-125">Aqui estão as macros individuais do wrapper.</span><span class="sxs-lookup"><span data-stu-id="a3ef4-125">Here are the individual wrapper macros.</span></span>

-   <span data-ttu-id="a3ef4-126">TraceLoggingInt8</span><span class="sxs-lookup"><span data-stu-id="a3ef4-126">TraceLoggingInt8</span></span>

-   <span data-ttu-id="a3ef4-127">TraceLoggingUInt8</span><span class="sxs-lookup"><span data-stu-id="a3ef4-127">TraceLoggingUInt8</span></span>

-   <span data-ttu-id="a3ef4-128">TraceLoggingInt16</span><span class="sxs-lookup"><span data-stu-id="a3ef4-128">TraceLoggingInt16</span></span>

-   <span data-ttu-id="a3ef4-129">TraceLoggingUInt16</span><span class="sxs-lookup"><span data-stu-id="a3ef4-129">TraceLoggingUInt16</span></span>

-   <span data-ttu-id="a3ef4-130">TraceLoggingInt32</span><span class="sxs-lookup"><span data-stu-id="a3ef4-130">TraceLoggingInt32</span></span>

-   <span data-ttu-id="a3ef4-131">TraceLoggingUInt32</span><span class="sxs-lookup"><span data-stu-id="a3ef4-131">TraceLoggingUInt32</span></span>

-   <span data-ttu-id="a3ef4-132">TraceLoggingInt64</span><span class="sxs-lookup"><span data-stu-id="a3ef4-132">TraceLoggingInt64</span></span>

-   <span data-ttu-id="a3ef4-133">TraceLoggingUInt64</span><span class="sxs-lookup"><span data-stu-id="a3ef4-133">TraceLoggingUInt64</span></span>

-   <span data-ttu-id="a3ef4-134">TraceLoggingFloat32</span><span class="sxs-lookup"><span data-stu-id="a3ef4-134">TraceLoggingFloat32</span></span>

-   <span data-ttu-id="a3ef4-135">TraceLoggingFloat64</span><span class="sxs-lookup"><span data-stu-id="a3ef4-135">TraceLoggingFloat64</span></span>

-   <span data-ttu-id="a3ef4-136">TraceLoggingBool</span><span class="sxs-lookup"><span data-stu-id="a3ef4-136">TraceLoggingBool</span></span>

-   <span data-ttu-id="a3ef4-137">TraceLoggingFileTime</span><span class="sxs-lookup"><span data-stu-id="a3ef4-137">TraceLoggingFileTime</span></span>

-   <span data-ttu-id="a3ef4-138">TraceLoggingGuid</span><span class="sxs-lookup"><span data-stu-id="a3ef4-138">TraceLoggingGuid</span></span>

-   <span data-ttu-id="a3ef4-139">TraceLoggingPointer</span><span class="sxs-lookup"><span data-stu-id="a3ef4-139">TraceLoggingPointer</span></span>

-   <span data-ttu-id="a3ef4-140">TraceLoggingSystemTime</span><span class="sxs-lookup"><span data-stu-id="a3ef4-140">TraceLoggingSystemTime</span></span>

-   <span data-ttu-id="a3ef4-141">TraceLoggingHexInt8</span><span class="sxs-lookup"><span data-stu-id="a3ef4-141">TraceLoggingHexInt8</span></span>

-   <span data-ttu-id="a3ef4-142">TraceLoggingHexUInt8</span><span class="sxs-lookup"><span data-stu-id="a3ef4-142">TraceLoggingHexUInt8</span></span>

-   <span data-ttu-id="a3ef4-143">TraceLoggingHexInt32</span><span class="sxs-lookup"><span data-stu-id="a3ef4-143">TraceLoggingHexInt32</span></span>

-   <span data-ttu-id="a3ef4-144">TraceLoggingHexUInt32</span><span class="sxs-lookup"><span data-stu-id="a3ef4-144">TraceLoggingHexUInt32</span></span>

-   <span data-ttu-id="a3ef4-145">TraceLoggingHexInt64</span><span class="sxs-lookup"><span data-stu-id="a3ef4-145">TraceLoggingHexInt64</span></span>

-   <span data-ttu-id="a3ef4-146">TraceLoggingHexUInt64</span><span class="sxs-lookup"><span data-stu-id="a3ef4-146">TraceLoggingHexUInt64</span></span>

-   <span data-ttu-id="a3ef4-147">TraceLoggingWchar</span><span class="sxs-lookup"><span data-stu-id="a3ef4-147">TraceLoggingWchar</span></span>

-   <span data-ttu-id="a3ef4-148">TraceLoggingChar</span><span class="sxs-lookup"><span data-stu-id="a3ef4-148">TraceLoggingChar</span></span>

-   <span data-ttu-id="a3ef4-149">TraceLoggingIntPtr</span><span class="sxs-lookup"><span data-stu-id="a3ef4-149">TraceLoggingIntPtr</span></span>

-   <span data-ttu-id="a3ef4-150">TraceLoggingUIntPtr</span><span class="sxs-lookup"><span data-stu-id="a3ef4-150">TraceLoggingUIntPtr</span></span>

-   <span data-ttu-id="a3ef4-151">TraceLoggingBoolean</span><span class="sxs-lookup"><span data-stu-id="a3ef4-151">TraceLoggingBoolean</span></span>

-   <span data-ttu-id="a3ef4-152">TraceLoggingHexInt16</span><span class="sxs-lookup"><span data-stu-id="a3ef4-152">TraceLoggingHexInt16</span></span>

-   <span data-ttu-id="a3ef4-153">TraceLoggingHexUInt16</span><span class="sxs-lookup"><span data-stu-id="a3ef4-153">TraceLoggingHexUInt16</span></span>

-   <span data-ttu-id="a3ef4-154">TraceLoggingPid</span><span class="sxs-lookup"><span data-stu-id="a3ef4-154">TraceLoggingPid</span></span>

-   <span data-ttu-id="a3ef4-155">TraceLoggingTid</span><span class="sxs-lookup"><span data-stu-id="a3ef4-155">TraceLoggingTid</span></span>

-   <span data-ttu-id="a3ef4-156">TraceLoggingPort</span><span class="sxs-lookup"><span data-stu-id="a3ef4-156">TraceLoggingPort</span></span>

-   <span data-ttu-id="a3ef4-157">TraceLoggingWinError</span><span class="sxs-lookup"><span data-stu-id="a3ef4-157">TraceLoggingWinError</span></span>

-   <span data-ttu-id="a3ef4-158">TraceLoggingNTStatus</span><span class="sxs-lookup"><span data-stu-id="a3ef4-158">TraceLoggingNTStatus</span></span>

-   <span data-ttu-id="a3ef4-159">TraceLoggingHResult</span><span class="sxs-lookup"><span data-stu-id="a3ef4-159">TraceLoggingHResult</span></span>

-   <span data-ttu-id="a3ef4-160">TraceLoggingSocketAddress</span><span class="sxs-lookup"><span data-stu-id="a3ef4-160">TraceLoggingSocketAddress</span></span>

-   <span data-ttu-id="a3ef4-161">TraceLoggingSid</span><span class="sxs-lookup"><span data-stu-id="a3ef4-161">TraceLoggingSid</span></span>

-   <span data-ttu-id="a3ef4-162">TraceLoggingString</span><span class="sxs-lookup"><span data-stu-id="a3ef4-162">TraceLoggingString</span></span>

-   <span data-ttu-id="a3ef4-163">TraceLoggingWideString</span><span class="sxs-lookup"><span data-stu-id="a3ef4-163">TraceLoggingWideString</span></span>

-   <span data-ttu-id="a3ef4-164">TraceLoggingCountedString</span><span class="sxs-lookup"><span data-stu-id="a3ef4-164">TraceLoggingCountedString</span></span>

-   <span data-ttu-id="a3ef4-165">TraceLoggingCountedWideString</span><span class="sxs-lookup"><span data-stu-id="a3ef4-165">TraceLoggingCountedWideString</span></span>

-   <span data-ttu-id="a3ef4-166">TraceLoggingAnsiString</span><span class="sxs-lookup"><span data-stu-id="a3ef4-166">TraceLoggingAnsiString</span></span>

-   <span data-ttu-id="a3ef4-167">TraceLoggingUnicodeString</span><span class="sxs-lookup"><span data-stu-id="a3ef4-167">TraceLoggingUnicodeString</span></span>

-   <span data-ttu-id="a3ef4-168">TraceLoggingBinary (dados nulos \* , tamanho dos dados em bytes, \[ \] nome opcional) os parâmetros para essa macro diferem daqueles acima.</span><span class="sxs-lookup"><span data-stu-id="a3ef4-168">TraceLoggingBinary(void \*data, size of the data in bytes, \[optional\] name ) The parameters to this macro differ from those above.</span></span> <span data-ttu-id="a3ef4-169">Se o parâmetro *Name* for especificado, ele deverá ser um literal de cadeia de caracteres (não uma variável) e não poderá conter nenhum caractere nulo inserido.</span><span class="sxs-lookup"><span data-stu-id="a3ef4-169">If the *name* parameter is specified, it must be a string literal (not a variable) and may not contain any embedded null characters.</span></span> <span data-ttu-id="a3ef4-170">Se o parâmetro *Name* não for fornecido, um nome será gerado automaticamente.</span><span class="sxs-lookup"><span data-stu-id="a3ef4-170">If the *name* parameter is not provided, a name is generated automatically.</span></span>

<span data-ttu-id="a3ef4-171">A API TraceLogging também disponibiliza várias macros para matrizes.</span><span class="sxs-lookup"><span data-stu-id="a3ef4-171">The TraceLogging API also makes several macros available for arrays.</span></span> <span data-ttu-id="a3ef4-172">Essas matrizes podem ter um comprimento fixo ou ter um comprimento variável, dependendo da macro do wrapper que você escolher usar.</span><span class="sxs-lookup"><span data-stu-id="a3ef4-172">These arrays can either have a fixed length or be of a variable length, depending on the wrapper macro you choose to use.</span></span> <span data-ttu-id="a3ef4-173">Todas essas macros de wrapper seguem esse formato.</span><span class="sxs-lookup"><span data-stu-id="a3ef4-173">All of these wrapper macros follow this format.</span></span>

`TraceLoggingBooleanArray(pVals, cVals, name, desc, tags)`

<span data-ttu-id="a3ef4-174">O parâmetro *pVals* aponta para a matriz de dados e *cVals* indica o número de elementos na matriz.</span><span class="sxs-lookup"><span data-stu-id="a3ef4-174">The parameter *pVals* points to the array of data and *cVals* indicates the number of elements in the array.</span></span> <span data-ttu-id="a3ef4-175">*cVals* deve ser uma constante e não pode ser uma variável.</span><span class="sxs-lookup"><span data-stu-id="a3ef4-175">*cVals* must be a constant and cannot be a variable.</span></span> <span data-ttu-id="a3ef4-176">Assim como as macros do único valor wrapper, *Name*, **desc** e *Tags* são parâmetros opcionais e devem seguir as mesmas restrições, conforme explicado com a macro **TraceLoggingValue** .</span><span class="sxs-lookup"><span data-stu-id="a3ef4-176">As with the single value wrapper macros, *name*, **desc**, and *tags* are optional parameters and must follow the same restrictions as explained with the **TraceLoggingValue** macro.</span></span>

-   <span data-ttu-id="a3ef4-177">TraceLoggingInt8FixedArray</span><span class="sxs-lookup"><span data-stu-id="a3ef4-177">TraceLoggingInt8FixedArray</span></span>

-   <span data-ttu-id="a3ef4-178">TraceLoggingUInt8FixedArray</span><span class="sxs-lookup"><span data-stu-id="a3ef4-178">TraceLoggingUInt8FixedArray</span></span>

-   <span data-ttu-id="a3ef4-179">TraceLoggingInt16FixedArray</span><span class="sxs-lookup"><span data-stu-id="a3ef4-179">TraceLoggingInt16FixedArray</span></span>

-   <span data-ttu-id="a3ef4-180">TraceLoggingUInt16FixedArray</span><span class="sxs-lookup"><span data-stu-id="a3ef4-180">TraceLoggingUInt16FixedArray</span></span>

-   <span data-ttu-id="a3ef4-181">TraceLoggingInt32FixedArray</span><span class="sxs-lookup"><span data-stu-id="a3ef4-181">TraceLoggingInt32FixedArray</span></span>

-   <span data-ttu-id="a3ef4-182">TraceLoggingUInt32FixedArray</span><span class="sxs-lookup"><span data-stu-id="a3ef4-182">TraceLoggingUInt32FixedArray</span></span>

-   <span data-ttu-id="a3ef4-183">TraceLoggingInt64FixedArray</span><span class="sxs-lookup"><span data-stu-id="a3ef4-183">TraceLoggingInt64FixedArray</span></span>

-   <span data-ttu-id="a3ef4-184">TraceLoggingUInt64FixedArray</span><span class="sxs-lookup"><span data-stu-id="a3ef4-184">TraceLoggingUInt64FixedArray</span></span>

-   <span data-ttu-id="a3ef4-185">TraceLoggingFloat32FixedArray</span><span class="sxs-lookup"><span data-stu-id="a3ef4-185">TraceLoggingFloat32FixedArray</span></span>

-   <span data-ttu-id="a3ef4-186">TraceLoggingFloat64FixedArray</span><span class="sxs-lookup"><span data-stu-id="a3ef4-186">TraceLoggingFloat64FixedArray</span></span>

-   <span data-ttu-id="a3ef4-187">TraceLoggingBoolFixedArray</span><span class="sxs-lookup"><span data-stu-id="a3ef4-187">TraceLoggingBoolFixedArray</span></span>

-   <span data-ttu-id="a3ef4-188">TraceLoggingGuidFixedArray</span><span class="sxs-lookup"><span data-stu-id="a3ef4-188">TraceLoggingGuidFixedArray</span></span>

-   <span data-ttu-id="a3ef4-189">TraceLoggingPointerFixedArray</span><span class="sxs-lookup"><span data-stu-id="a3ef4-189">TraceLoggingPointerFixedArray</span></span>

-   <span data-ttu-id="a3ef4-190">TraceLoggingFileTimeFixedArray</span><span class="sxs-lookup"><span data-stu-id="a3ef4-190">TraceLoggingFileTimeFixedArray</span></span>

-   <span data-ttu-id="a3ef4-191">TraceLoggingSystemTimeFixedArray</span><span class="sxs-lookup"><span data-stu-id="a3ef4-191">TraceLoggingSystemTimeFixedArray</span></span>

-   <span data-ttu-id="a3ef4-192">TraceLoggingHexInt8FixedArray</span><span class="sxs-lookup"><span data-stu-id="a3ef4-192">TraceLoggingHexInt8FixedArray</span></span>

-   <span data-ttu-id="a3ef4-193">TraceLoggingHexUInt8FixedArray</span><span class="sxs-lookup"><span data-stu-id="a3ef4-193">TraceLoggingHexUInt8FixedArray</span></span>

-   <span data-ttu-id="a3ef4-194">TraceLoggingHexInt32FixedArray</span><span class="sxs-lookup"><span data-stu-id="a3ef4-194">TraceLoggingHexInt32FixedArray</span></span>

-   <span data-ttu-id="a3ef4-195">TraceLoggingHexUInt32FixedArray</span><span class="sxs-lookup"><span data-stu-id="a3ef4-195">TraceLoggingHexUInt32FixedArray</span></span>

-   <span data-ttu-id="a3ef4-196">TraceLoggingHexInt64FixedArray</span><span class="sxs-lookup"><span data-stu-id="a3ef4-196">TraceLoggingHexInt64FixedArray</span></span>

-   <span data-ttu-id="a3ef4-197">TraceLoggingHexUInt64FixedArray</span><span class="sxs-lookup"><span data-stu-id="a3ef4-197">TraceLoggingHexUInt64FixedArray</span></span>

-   <span data-ttu-id="a3ef4-198">TraceLoggingWcharFixedArray</span><span class="sxs-lookup"><span data-stu-id="a3ef4-198">TraceLoggingWcharFixedArray</span></span>

-   <span data-ttu-id="a3ef4-199">TraceLoggingCharFixedArray</span><span class="sxs-lookup"><span data-stu-id="a3ef4-199">TraceLoggingCharFixedArray</span></span>

-   <span data-ttu-id="a3ef4-200">TraceLoggingIntPtrFixedArray</span><span class="sxs-lookup"><span data-stu-id="a3ef4-200">TraceLoggingIntPtrFixedArray</span></span>

-   <span data-ttu-id="a3ef4-201">TraceLoggingUIntPtrFixedArray</span><span class="sxs-lookup"><span data-stu-id="a3ef4-201">TraceLoggingUIntPtrFixedArray</span></span>

-   <span data-ttu-id="a3ef4-202">TraceLoggingBooleanFixedArray</span><span class="sxs-lookup"><span data-stu-id="a3ef4-202">TraceLoggingBooleanFixedArray</span></span>

-   <span data-ttu-id="a3ef4-203">TraceLoggingHexInt16FixedArray</span><span class="sxs-lookup"><span data-stu-id="a3ef4-203">TraceLoggingHexInt16FixedArray</span></span>

-   <span data-ttu-id="a3ef4-204">TraceLoggingHexUInt16FixedArray</span><span class="sxs-lookup"><span data-stu-id="a3ef4-204">TraceLoggingHexUInt16FixedArray</span></span>

-   <span data-ttu-id="a3ef4-205">TraceLoggingInt8Array</span><span class="sxs-lookup"><span data-stu-id="a3ef4-205">TraceLoggingInt8Array</span></span>

-   <span data-ttu-id="a3ef4-206">TraceLoggingUInt8Array</span><span class="sxs-lookup"><span data-stu-id="a3ef4-206">TraceLoggingUInt8Array</span></span>

-   <span data-ttu-id="a3ef4-207">TraceLoggingInt16Array</span><span class="sxs-lookup"><span data-stu-id="a3ef4-207">TraceLoggingInt16Array</span></span>

-   <span data-ttu-id="a3ef4-208">TraceLoggingUInt16Array</span><span class="sxs-lookup"><span data-stu-id="a3ef4-208">TraceLoggingUInt16Array</span></span>

-   <span data-ttu-id="a3ef4-209">TraceLoggingInt32Array</span><span class="sxs-lookup"><span data-stu-id="a3ef4-209">TraceLoggingInt32Array</span></span>

-   <span data-ttu-id="a3ef4-210">TraceLoggingUInt32Array</span><span class="sxs-lookup"><span data-stu-id="a3ef4-210">TraceLoggingUInt32Array</span></span>

-   <span data-ttu-id="a3ef4-211">TraceLoggingInt64Array</span><span class="sxs-lookup"><span data-stu-id="a3ef4-211">TraceLoggingInt64Array</span></span>

-   <span data-ttu-id="a3ef4-212">TraceLoggingUInt64Array</span><span class="sxs-lookup"><span data-stu-id="a3ef4-212">TraceLoggingUInt64Array</span></span>

-   <span data-ttu-id="a3ef4-213">TraceLoggingFloat32Array</span><span class="sxs-lookup"><span data-stu-id="a3ef4-213">TraceLoggingFloat32Array</span></span>

-   <span data-ttu-id="a3ef4-214">TraceLoggingFloat64Array</span><span class="sxs-lookup"><span data-stu-id="a3ef4-214">TraceLoggingFloat64Array</span></span>

-   <span data-ttu-id="a3ef4-215">TraceLoggingBoolArray</span><span class="sxs-lookup"><span data-stu-id="a3ef4-215">TraceLoggingBoolArray</span></span>

-   <span data-ttu-id="a3ef4-216">TraceLoggingGuidArray</span><span class="sxs-lookup"><span data-stu-id="a3ef4-216">TraceLoggingGuidArray</span></span>

-   <span data-ttu-id="a3ef4-217">TraceLoggingPointerArray</span><span class="sxs-lookup"><span data-stu-id="a3ef4-217">TraceLoggingPointerArray</span></span>

-   <span data-ttu-id="a3ef4-218">TraceLoggingFileTimeArray</span><span class="sxs-lookup"><span data-stu-id="a3ef4-218">TraceLoggingFileTimeArray</span></span>

-   <span data-ttu-id="a3ef4-219">TraceLoggingSystemTimeArray</span><span class="sxs-lookup"><span data-stu-id="a3ef4-219">TraceLoggingSystemTimeArray</span></span>

-   <span data-ttu-id="a3ef4-220">TraceLoggingHexInt8Array</span><span class="sxs-lookup"><span data-stu-id="a3ef4-220">TraceLoggingHexInt8Array</span></span>

-   <span data-ttu-id="a3ef4-221">TraceLoggingHexUInt8Array</span><span class="sxs-lookup"><span data-stu-id="a3ef4-221">TraceLoggingHexUInt8Array</span></span>

-   <span data-ttu-id="a3ef4-222">TraceLoggingHexInt32Array</span><span class="sxs-lookup"><span data-stu-id="a3ef4-222">TraceLoggingHexInt32Array</span></span>

-   <span data-ttu-id="a3ef4-223">TraceLoggingHexUInt32Array</span><span class="sxs-lookup"><span data-stu-id="a3ef4-223">TraceLoggingHexUInt32Array</span></span>

-   <span data-ttu-id="a3ef4-224">TraceLoggingHexInt64Array</span><span class="sxs-lookup"><span data-stu-id="a3ef4-224">TraceLoggingHexInt64Array</span></span>

-   <span data-ttu-id="a3ef4-225">TraceLoggingHexUInt64Array</span><span class="sxs-lookup"><span data-stu-id="a3ef4-225">TraceLoggingHexUInt64Array</span></span>

-   <span data-ttu-id="a3ef4-226">TraceLoggingWcharArray</span><span class="sxs-lookup"><span data-stu-id="a3ef4-226">TraceLoggingWcharArray</span></span>

-   <span data-ttu-id="a3ef4-227">TraceLoggingCharArray</span><span class="sxs-lookup"><span data-stu-id="a3ef4-227">TraceLoggingCharArray</span></span>

-   <span data-ttu-id="a3ef4-228">TraceLoggingIntPtrArray</span><span class="sxs-lookup"><span data-stu-id="a3ef4-228">TraceLoggingIntPtrArray</span></span>

-   <span data-ttu-id="a3ef4-229">TraceLoggingUIntPtrArray</span><span class="sxs-lookup"><span data-stu-id="a3ef4-229">TraceLoggingUIntPtrArray</span></span>

-   <span data-ttu-id="a3ef4-230">TraceLoggingBooleanArray</span><span class="sxs-lookup"><span data-stu-id="a3ef4-230">TraceLoggingBooleanArray</span></span>

-   <span data-ttu-id="a3ef4-231">TraceLoggingHexInt16Array</span><span class="sxs-lookup"><span data-stu-id="a3ef4-231">TraceLoggingHexInt16Array</span></span>

-   <span data-ttu-id="a3ef4-232">TraceLoggingHexUInt16Array</span><span class="sxs-lookup"><span data-stu-id="a3ef4-232">TraceLoggingHexUInt16Array</span></span>

 

 




