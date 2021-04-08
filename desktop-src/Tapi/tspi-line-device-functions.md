---
description: Esta seção contém uma lista alfabética das funções de dispositivo de linha disponíveis no SPI de telefonia.
ms.assetid: 2a27fbb7-93b5-4106-afd3-e63456650fb9
title: Funções de dispositivo de linha TSPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dea2ca54096ac89b76a4658129362e87d4281fcd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103828673"
---
# <a name="tspi-line-device-functions"></a><span data-ttu-id="10fdc-103">Funções de dispositivo de linha TSPI</span><span class="sxs-lookup"><span data-stu-id="10fdc-103">TSPI Line Device Functions</span></span>

<span data-ttu-id="10fdc-104">Esta seção contém uma lista alfabética das funções de dispositivo de linha disponíveis no SPI de telefonia.</span><span class="sxs-lookup"><span data-stu-id="10fdc-104">This section contains an alphabetic list of the available line device functions in the Telephony SPI.</span></span> <span data-ttu-id="10fdc-105">As informações para cada função incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="10fdc-105">The information for each function includes the following:</span></span>

-   <span data-ttu-id="10fdc-106">Uma instrução da finalidade da função.</span><span class="sxs-lookup"><span data-stu-id="10fdc-106">A statement of the function's purpose.</span></span>
-   <span data-ttu-id="10fdc-107">A sintaxe correta para a função.</span><span class="sxs-lookup"><span data-stu-id="10fdc-107">The correct syntax for the function.</span></span>
-   <span data-ttu-id="10fdc-108">Uma descrição dos parâmetros da função, incluindo Estados de chamada válidos.</span><span class="sxs-lookup"><span data-stu-id="10fdc-108">A description of the function's parameters, including valid call states.</span></span>
-   <span data-ttu-id="10fdc-109">Uma descrição do valor de retorno da função.</span><span class="sxs-lookup"><span data-stu-id="10fdc-109">A description of the function's return value.</span></span>
-   <span data-ttu-id="10fdc-110">Uma seção de comentários que pode incluir qualquer ou todas as seguintes opções: uma lista dos Estados de chamada válidos na entrada da função e as transições de estado de chamada típicas quando a solicitação for concluída; uma descrição de quais membros de grandes estruturas de dados devem ser preenchidos pelo provedor de serviços e quais membros devem ter seus valores preservados intactos; e comparação com uma função correspondente dentro da TAPI.</span><span class="sxs-lookup"><span data-stu-id="10fdc-110">A Remarks section that can include any or all of the following: a list of the valid call states on entry of the function and typical call state transitions when the request completes; a description of which members of large data structures must be filled in by the service provider and which members must have their values preserved intact; and comparison with a corresponding function within TAPI.</span></span>
-   <span data-ttu-id="10fdc-111">Referências a outras funções, mensagens ou estruturas de dados.</span><span class="sxs-lookup"><span data-stu-id="10fdc-111">References to other functions, messages, or data structures.</span></span>
    > [!Note]  
    > <span data-ttu-id="10fdc-112">Os Estados reais nos quais uma função pode ser executada podem ser limitados pelos recursos do provedor de serviços.</span><span class="sxs-lookup"><span data-stu-id="10fdc-112">The actual states in which a function can be performed may be limited by the capabilities of the service provider.</span></span> <span data-ttu-id="10fdc-113">Os provedores de serviço devem definir o membro **dwCallFeatures** na estrutura [**LINECALLSTATUS**](/windows/win32/api/tapi/ns-tapi-linecallstatus) , o membro **dwAddressFeatures** na estrutura [**LINEADDRESSSTATUS**](/windows/win32/api/tapi/ns-tapi-lineaddressstatus) e o membro **dwLineFeatures** na estrutura [**LINEDEVSTATUS**](/windows/win32/api/tapi/ns-tapi-linedevstatus) para indicar aos aplicativos se uma função é permitida ou não nesse ponto no tempo.</span><span class="sxs-lookup"><span data-stu-id="10fdc-113">Service providers must set the **dwCallFeatures** member in the [**LINECALLSTATUS**](/windows/win32/api/tapi/ns-tapi-linecallstatus) structure, the **dwAddressFeatures** member in the [**LINEADDRESSSTATUS**](/windows/win32/api/tapi/ns-tapi-lineaddressstatus) structure, and the **dwLineFeatures** member in the [**LINEDEVSTATUS**](/windows/win32/api/tapi/ns-tapi-linedevstatus) structure to indicate to applications whether or not a function is permitted at that point in time.</span></span>

     

<span data-ttu-id="10fdc-114">Esta seção contém as seguintes funções de dispositivo TSPI line:</span><span class="sxs-lookup"><span data-stu-id="10fdc-114">This section contains the following TSPI line device functions:</span></span>

-   [<span data-ttu-id="10fdc-115">**TSPI \_ lineAccept**</span><span class="sxs-lookup"><span data-stu-id="10fdc-115">**TSPI\_lineAccept**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_lineaccept)
-   [<span data-ttu-id="10fdc-116">**TSPI \_ lineAddToConference**</span><span class="sxs-lookup"><span data-stu-id="10fdc-116">**TSPI\_lineAddToConference**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_lineaddtoconference)
-   [<span data-ttu-id="10fdc-117">**TSPI \_ lineAnswer**</span><span class="sxs-lookup"><span data-stu-id="10fdc-117">**TSPI\_lineAnswer**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_lineanswer)
-   [<span data-ttu-id="10fdc-118">**TSPI \_ lineBlindTransfer**</span><span class="sxs-lookup"><span data-stu-id="10fdc-118">**TSPI\_lineBlindTransfer**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_lineblindtransfer)
-   [<span data-ttu-id="10fdc-119">**TSPI \_ lineClose**</span><span class="sxs-lookup"><span data-stu-id="10fdc-119">**TSPI\_lineClose**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_lineclose)
-   [<span data-ttu-id="10fdc-120">**TSPI \_ lineCloseCall**</span><span class="sxs-lookup"><span data-stu-id="10fdc-120">**TSPI\_lineCloseCall**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_lineclosecall)
-   [<span data-ttu-id="10fdc-121">**TSPI \_ lineCloseMSPInstance**</span><span class="sxs-lookup"><span data-stu-id="10fdc-121">**TSPI\_lineCloseMSPInstance**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_lineclosemspinstance)
-   [<span data-ttu-id="10fdc-122">**TSPI \_ lineCompleteCall**</span><span class="sxs-lookup"><span data-stu-id="10fdc-122">**TSPI\_lineCompleteCall**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linecompletecall)
-   [<span data-ttu-id="10fdc-123">**TSPI \_ lineCompleteTransfer**</span><span class="sxs-lookup"><span data-stu-id="10fdc-123">**TSPI\_lineCompleteTransfer**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linecompletetransfer)
-   [<span data-ttu-id="10fdc-124">**TSPI \_ lineConditionalMediaDetection**</span><span class="sxs-lookup"><span data-stu-id="10fdc-124">**TSPI\_lineConditionalMediaDetection**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_lineconditionalmediadetection)
-   [<span data-ttu-id="10fdc-125">**TSPI \_ lineConfigDialog**</span><span class="sxs-lookup"><span data-stu-id="10fdc-125">**TSPI\_lineConfigDialog**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_lineconfigdialog)
-   [<span data-ttu-id="10fdc-126">**TSPI \_ lineConfigDialogEdit**</span><span class="sxs-lookup"><span data-stu-id="10fdc-126">**TSPI\_lineConfigDialogEdit**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_lineconfigdialogedit)
-   [<span data-ttu-id="10fdc-127">**TSPI \_ lineCreateMSPInstance**</span><span class="sxs-lookup"><span data-stu-id="10fdc-127">**TSPI\_lineCreateMSPInstance**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linecreatemspinstance)
-   [<span data-ttu-id="10fdc-128">**TSPI \_ lineDevSpecific**</span><span class="sxs-lookup"><span data-stu-id="10fdc-128">**TSPI\_lineDevSpecific**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linedevspecific)
-   [<span data-ttu-id="10fdc-129">**TSPI \_ lineDevSpecificFeature**</span><span class="sxs-lookup"><span data-stu-id="10fdc-129">**TSPI\_lineDevSpecificFeature**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linedevspecificfeature)
-   [<span data-ttu-id="10fdc-130">**TSPI \_ lineDial**</span><span class="sxs-lookup"><span data-stu-id="10fdc-130">**TSPI\_lineDial**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linedial)
-   [<span data-ttu-id="10fdc-131">**TSPI \_ lineDrop**</span><span class="sxs-lookup"><span data-stu-id="10fdc-131">**TSPI\_lineDrop**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linedrop)
-   [<span data-ttu-id="10fdc-132">TSPI \_ lineDropNoOwner</span><span class="sxs-lookup"><span data-stu-id="10fdc-132">TSPI\_lineDropNoOwner</span></span>](tspi-linedropnoowner.md)
-   [<span data-ttu-id="10fdc-133">TSPI \_ lineDropOnClose</span><span class="sxs-lookup"><span data-stu-id="10fdc-133">TSPI\_lineDropOnClose</span></span>](tspi-linedroponclose.md)
-   [<span data-ttu-id="10fdc-134">**TSPI \_ lineForward**</span><span class="sxs-lookup"><span data-stu-id="10fdc-134">**TSPI\_lineForward**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_lineforward)
-   [<span data-ttu-id="10fdc-135">**TSPI \_ lineGatherDigits**</span><span class="sxs-lookup"><span data-stu-id="10fdc-135">**TSPI\_lineGatherDigits**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linegatherdigits)
-   [<span data-ttu-id="10fdc-136">**TSPI \_ lineGenerateDigits**</span><span class="sxs-lookup"><span data-stu-id="10fdc-136">**TSPI\_lineGenerateDigits**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linegeneratedigits)
-   [<span data-ttu-id="10fdc-137">**TSPI \_ lineGenerateTone**</span><span class="sxs-lookup"><span data-stu-id="10fdc-137">**TSPI\_lineGenerateTone**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linegeneratetone)
-   [<span data-ttu-id="10fdc-138">**TSPI \_ lineGetAddressCaps**</span><span class="sxs-lookup"><span data-stu-id="10fdc-138">**TSPI\_lineGetAddressCaps**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linegetaddresscaps)
-   [<span data-ttu-id="10fdc-139">**TSPI \_ lineGetAddressID**</span><span class="sxs-lookup"><span data-stu-id="10fdc-139">**TSPI\_lineGetAddressID**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linegetaddressid)
-   [<span data-ttu-id="10fdc-140">**TSPI \_ lineGetAddressStatus**</span><span class="sxs-lookup"><span data-stu-id="10fdc-140">**TSPI\_lineGetAddressStatus**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linegetaddressstatus)
-   [<span data-ttu-id="10fdc-141">**TSPI \_ lineGetCallAddressID**</span><span class="sxs-lookup"><span data-stu-id="10fdc-141">**TSPI\_lineGetCallAddressID**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linegetcalladdressid)
-   [<span data-ttu-id="10fdc-142">**TSPI \_ lineGetCallHubTracking**</span><span class="sxs-lookup"><span data-stu-id="10fdc-142">**TSPI\_lineGetCallHubTracking**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linegetcallhubtracking)
-   [<span data-ttu-id="10fdc-143">**TSPI \_ lineGetCallIDs**</span><span class="sxs-lookup"><span data-stu-id="10fdc-143">**TSPI\_lineGetCallIDs**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linegetcallids)
-   [<span data-ttu-id="10fdc-144">**TSPI \_ lineGetCallInfo**</span><span class="sxs-lookup"><span data-stu-id="10fdc-144">**TSPI\_lineGetCallInfo**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linegetcallinfo)
-   [<span data-ttu-id="10fdc-145">**TSPI \_ lineGetCallStatus**</span><span class="sxs-lookup"><span data-stu-id="10fdc-145">**TSPI\_lineGetCallStatus**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linegetcallstatus)
-   [<span data-ttu-id="10fdc-146">**TSPI \_ lineGetDevCaps**</span><span class="sxs-lookup"><span data-stu-id="10fdc-146">**TSPI\_lineGetDevCaps**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linegetdevcaps)
-   [<span data-ttu-id="10fdc-147">**TSPI \_ lineGetDevConfig**</span><span class="sxs-lookup"><span data-stu-id="10fdc-147">**TSPI\_lineGetDevConfig**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linegetdevconfig)
-   [<span data-ttu-id="10fdc-148">**TSPI \_ lineGetExtensionID**</span><span class="sxs-lookup"><span data-stu-id="10fdc-148">**TSPI\_lineGetExtensionID**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linegetextensionid)
-   [<span data-ttu-id="10fdc-149">**TSPI \_ lineGetIcon**</span><span class="sxs-lookup"><span data-stu-id="10fdc-149">**TSPI\_lineGetIcon**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linegeticon)
-   [<span data-ttu-id="10fdc-150">**TSPI \_ lineGetID**</span><span class="sxs-lookup"><span data-stu-id="10fdc-150">**TSPI\_lineGetID**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linegetid)
-   [<span data-ttu-id="10fdc-151">**TSPI \_ lineGetLineDevStatus**</span><span class="sxs-lookup"><span data-stu-id="10fdc-151">**TSPI\_lineGetLineDevStatus**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linegetlinedevstatus)
-   [<span data-ttu-id="10fdc-152">**TSPI \_ lineGetNumAddressIDs**</span><span class="sxs-lookup"><span data-stu-id="10fdc-152">**TSPI\_lineGetNumAddressIDs**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linegetnumaddressids)
-   [<span data-ttu-id="10fdc-153">**TSPI \_ lineHold**</span><span class="sxs-lookup"><span data-stu-id="10fdc-153">**TSPI\_lineHold**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linehold)
-   [<span data-ttu-id="10fdc-154">**TSPI \_ lineMakeCall**</span><span class="sxs-lookup"><span data-stu-id="10fdc-154">**TSPI\_lineMakeCall**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linemakecall)
-   [<span data-ttu-id="10fdc-155">**TSPI \_ lineMonitorDigits**</span><span class="sxs-lookup"><span data-stu-id="10fdc-155">**TSPI\_lineMonitorDigits**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linemonitordigits)
-   [<span data-ttu-id="10fdc-156">**TSPI \_ lineMonitorMedia**</span><span class="sxs-lookup"><span data-stu-id="10fdc-156">**TSPI\_lineMonitorMedia**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linemonitormedia)
-   [<span data-ttu-id="10fdc-157">**TSPI \_ lineMonitorTones**</span><span class="sxs-lookup"><span data-stu-id="10fdc-157">**TSPI\_lineMonitorTones**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linemonitortones)
-   [<span data-ttu-id="10fdc-158">**TSPI \_ lineMSPIdentify**</span><span class="sxs-lookup"><span data-stu-id="10fdc-158">**TSPI\_lineMSPIdentify**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linemspidentify)
-   [<span data-ttu-id="10fdc-159">**TSPI \_ lineNegotiateExtVersion**</span><span class="sxs-lookup"><span data-stu-id="10fdc-159">**TSPI\_lineNegotiateExtVersion**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linenegotiateextversion)
-   [<span data-ttu-id="10fdc-160">**TSPI \_ lineNegotiateTSPIVersion**</span><span class="sxs-lookup"><span data-stu-id="10fdc-160">**TSPI\_lineNegotiateTSPIVersion**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linenegotiatetspiversion)
-   [<span data-ttu-id="10fdc-161">**TSPI \_ lineOpen**</span><span class="sxs-lookup"><span data-stu-id="10fdc-161">**TSPI\_lineOpen**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_lineopen)
-   [<span data-ttu-id="10fdc-162">**TSPI \_ linePark**</span><span class="sxs-lookup"><span data-stu-id="10fdc-162">**TSPI\_linePark**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linepark)
-   [<span data-ttu-id="10fdc-163">**TSPI \_ linePickup**</span><span class="sxs-lookup"><span data-stu-id="10fdc-163">**TSPI\_linePickup**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linepickup)
-   [<span data-ttu-id="10fdc-164">**TSPI \_ linePrepareAddToConference**</span><span class="sxs-lookup"><span data-stu-id="10fdc-164">**TSPI\_linePrepareAddToConference**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_lineprepareaddtoconference)
-   [<span data-ttu-id="10fdc-165">**TSPI \_ lineReceiveMSPData**</span><span class="sxs-lookup"><span data-stu-id="10fdc-165">**TSPI\_lineReceiveMSPData**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linereceivemspdata)
-   [<span data-ttu-id="10fdc-166">**TSPI \_ lineRedirect**</span><span class="sxs-lookup"><span data-stu-id="10fdc-166">**TSPI\_lineRedirect**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_lineredirect)
-   [<span data-ttu-id="10fdc-167">**TSPI \_ lineReleaseUserUserInfo**</span><span class="sxs-lookup"><span data-stu-id="10fdc-167">**TSPI\_lineReleaseUserUserInfo**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linereleaseuseruserinfo)
-   [<span data-ttu-id="10fdc-168">**TSPI \_ lineRemoveFromConference**</span><span class="sxs-lookup"><span data-stu-id="10fdc-168">**TSPI\_lineRemoveFromConference**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_lineremovefromconference)
-   [<span data-ttu-id="10fdc-169">**TSPI \_ lineSecureCall**</span><span class="sxs-lookup"><span data-stu-id="10fdc-169">**TSPI\_lineSecureCall**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linesecurecall)
-   [<span data-ttu-id="10fdc-170">**TSPI \_ lineSelectExtVersion**</span><span class="sxs-lookup"><span data-stu-id="10fdc-170">**TSPI\_lineSelectExtVersion**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_lineselectextversion)
-   [<span data-ttu-id="10fdc-171">**TSPI \_ lineSendUserUserInfo**</span><span class="sxs-lookup"><span data-stu-id="10fdc-171">**TSPI\_lineSendUserUserInfo**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linesenduseruserinfo)
-   [<span data-ttu-id="10fdc-172">**TSPI \_ lineSetAppSpecific**</span><span class="sxs-lookup"><span data-stu-id="10fdc-172">**TSPI\_lineSetAppSpecific**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linesetappspecific)
-   [<span data-ttu-id="10fdc-173">**TSPI \_ lineSetCallData**</span><span class="sxs-lookup"><span data-stu-id="10fdc-173">**TSPI\_lineSetCallData**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linesetcalldata)
-   [<span data-ttu-id="10fdc-174">**TSPI \_ lineSetCallHubTracking**</span><span class="sxs-lookup"><span data-stu-id="10fdc-174">**TSPI\_lineSetCallHubTracking**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linesetcallhubtracking)
-   [<span data-ttu-id="10fdc-175">**TSPI \_ lineSetCallParams**</span><span class="sxs-lookup"><span data-stu-id="10fdc-175">**TSPI\_lineSetCallParams**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linesetcallparams)
-   [<span data-ttu-id="10fdc-176">**TSPI \_ lineSetCallQualityOfService**</span><span class="sxs-lookup"><span data-stu-id="10fdc-176">**TSPI\_lineSetCallQualityOfService**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linesetcallqualityofservice)
-   [<span data-ttu-id="10fdc-177">**TSPI \_ lineSetCallTreatment**</span><span class="sxs-lookup"><span data-stu-id="10fdc-177">**TSPI\_lineSetCallTreatment**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linesetcalltreatment)
-   [<span data-ttu-id="10fdc-178">TSPI \_ lineSetCurrentLocation</span><span class="sxs-lookup"><span data-stu-id="10fdc-178">TSPI\_lineSetCurrentLocation</span></span>](tspi-linesetcurrentlocation.md)
-   [<span data-ttu-id="10fdc-179">**TSPI \_ lineSetDefaultMediaDetection**</span><span class="sxs-lookup"><span data-stu-id="10fdc-179">**TSPI\_lineSetDefaultMediaDetection**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linesetdefaultmediadetection)
-   [<span data-ttu-id="10fdc-180">**TSPI \_ lineSetDevConfig**</span><span class="sxs-lookup"><span data-stu-id="10fdc-180">**TSPI\_lineSetDevConfig**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linesetdevconfig)
-   [<span data-ttu-id="10fdc-181">**TSPI \_ lineSetLineDevStatus**</span><span class="sxs-lookup"><span data-stu-id="10fdc-181">**TSPI\_lineSetLineDevStatus**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linesetlinedevstatus)
-   [<span data-ttu-id="10fdc-182">**TSPI \_ lineSetMediaControl**</span><span class="sxs-lookup"><span data-stu-id="10fdc-182">**TSPI\_lineSetMediaControl**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linesetmediacontrol)
-   [<span data-ttu-id="10fdc-183">**TSPI \_ lineSetMediaMode**</span><span class="sxs-lookup"><span data-stu-id="10fdc-183">**TSPI\_lineSetMediaMode**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linesetmediamode)
-   [<span data-ttu-id="10fdc-184">**TSPI \_ lineSetStatusMessages**</span><span class="sxs-lookup"><span data-stu-id="10fdc-184">**TSPI\_lineSetStatusMessages**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linesetstatusmessages)
-   [<span data-ttu-id="10fdc-185">**TSPI \_ lineSetTerminal**</span><span class="sxs-lookup"><span data-stu-id="10fdc-185">**TSPI\_lineSetTerminal**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linesetterminal)
-   [<span data-ttu-id="10fdc-186">**TSPI \_ lineSetupConference**</span><span class="sxs-lookup"><span data-stu-id="10fdc-186">**TSPI\_lineSetupConference**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linesetupconference)
-   [<span data-ttu-id="10fdc-187">**TSPI \_ lineSetupTransfer**</span><span class="sxs-lookup"><span data-stu-id="10fdc-187">**TSPI\_lineSetupTransfer**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_linesetuptransfer)
-   [<span data-ttu-id="10fdc-188">**TSPI \_ lineSwapHold**</span><span class="sxs-lookup"><span data-stu-id="10fdc-188">**TSPI\_lineSwapHold**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_lineswaphold)
-   [<span data-ttu-id="10fdc-189">**TSPI \_ lineUncompleteCall**</span><span class="sxs-lookup"><span data-stu-id="10fdc-189">**TSPI\_lineUncompleteCall**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_lineuncompletecall)
-   [<span data-ttu-id="10fdc-190">**TSPI \_ lineUnhold**</span><span class="sxs-lookup"><span data-stu-id="10fdc-190">**TSPI\_lineUnhold**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_lineunhold)
-   [<span data-ttu-id="10fdc-191">**TSPI \_ lineUnpark**</span><span class="sxs-lookup"><span data-stu-id="10fdc-191">**TSPI\_lineUnpark**</span></span>](/windows/win32/api/tspi/nf-tspi-tspi_lineunpark)

 

 
