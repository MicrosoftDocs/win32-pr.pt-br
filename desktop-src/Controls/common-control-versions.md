---
title: Versões de controle comum
description: Este tópico lista as versões disponíveis da biblioteca de Controle Comum (ComCtl32.dll), descreve como identificar a versão que seu aplicativo está usando e explica como direcionar seu aplicativo para uma versão específica.
ms.assetid: 1B524A91-B433-4968-9546-8A6AFB67E89C
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1131466bd4d3afcaae3a241a6f7854fd5a49450
ms.sourcegitcommit: 0f7a8198bacd5493ab1e78a9583c7a3578794765
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/25/2021
ms.locfileid: "110423956"
---
# <a name="common-control-versions"></a><span data-ttu-id="3687b-103">Versões de controle comum</span><span class="sxs-lookup"><span data-stu-id="3687b-103">Common Control Versions</span></span>

<span data-ttu-id="3687b-104">Este tópico lista as versões disponíveis da biblioteca de Controle Comum (ComCtl32.dll), descreve como identificar a versão que seu aplicativo está usando e explica como direcionar seu aplicativo para uma versão específica.</span><span class="sxs-lookup"><span data-stu-id="3687b-104">This topic lists the available versions of the Common Control library (ComCtl32.dll), describes how to identify the version that your application is using, and explains how to target your application for a specific version.</span></span>

<span data-ttu-id="3687b-105">Este tópico inclui as seções a seguir.</span><span class="sxs-lookup"><span data-stu-id="3687b-105">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="3687b-106">Números de versões de DLL de controle comum</span><span class="sxs-lookup"><span data-stu-id="3687b-106">Common Control DLL Versions Numbers</span></span>](#common-control-dll-versions-numbers)
-   [<span data-ttu-id="3687b-107">Tamanhos de estrutura para versões de controle comuns diferentes</span><span class="sxs-lookup"><span data-stu-id="3687b-107">Structure Sizes for Different Common Control Versions</span></span>](#structure-sizes-for-different-common-control-versions)
-   [<span data-ttu-id="3687b-108">Usando DllGetVersion para determinar o número de versão</span><span class="sxs-lookup"><span data-stu-id="3687b-108">Using DllGetVersion to Determine the Version Number</span></span>](#using-dllgetversion-to-determine-the-version-number)
-   [<span data-ttu-id="3687b-109">Versões do projeto</span><span class="sxs-lookup"><span data-stu-id="3687b-109">Project Versions</span></span>](#project-versions)
-   [<span data-ttu-id="3687b-110">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="3687b-110">Related topics</span></span>](#related-topics)

## <a name="common-control-dll-versions-numbers"></a><span data-ttu-id="3687b-111">Números de versões de DLL de controle comum</span><span class="sxs-lookup"><span data-stu-id="3687b-111">Common Control DLL Versions Numbers</span></span>

<span data-ttu-id="3687b-112">O suporte para controles comuns é fornecido pelo ComCtl32.dll, que inclui todas as versões de 32 bits e 64 bits do Windows.</span><span class="sxs-lookup"><span data-stu-id="3687b-112">Support for common controls is provided by ComCtl32.dll, which all 32-bit and 64-bit versions of Windows include.</span></span> <span data-ttu-id="3687b-113">Cada versão sucessiva da DLL dá suporte aos recursos e à API de versões anteriores e adiciona novos recursos.</span><span class="sxs-lookup"><span data-stu-id="3687b-113">Each successive version of the DLL supports the features and API of earlier versions and adds new features.</span></span>

<span data-ttu-id="3687b-114">Como várias versões do ComCtl32.dll foram distribuídas com Internet Explorer, a versão que está ativa às vezes é diferente da versão que foi enviada com o sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="3687b-114">Because various versions of ComCtl32.dll were distributed with Internet Explorer, the version that is active is sometimes different from the version that was shipped with the operating system.</span></span> <span data-ttu-id="3687b-115">Portanto, seu aplicativo deve determinar diretamente qual versão do ComCtl32.dll está presente.</span><span class="sxs-lookup"><span data-stu-id="3687b-115">Therefore, your application must directly determine which version of ComCtl32.dll is present.</span></span>

<span data-ttu-id="3687b-116">Na documentação de referência de controles comuns, muitos elementos de programação especificam um número mínimo de versão de DLL com suporte.</span><span class="sxs-lookup"><span data-stu-id="3687b-116">In the common controls reference documentation, many programming elements specify a minimum supported DLL version number.</span></span> <span data-ttu-id="3687b-117">Esse número de versão indica que o elemento de programação é implementado nessa versão e nas versões subsequentes da DLL, a menos que especificado de outra forma.</span><span class="sxs-lookup"><span data-stu-id="3687b-117">This version number indicates that the programming element is implemented in that version and subsequent versions of the DLL unless otherwise specified.</span></span> <span data-ttu-id="3687b-118">Se nenhum número de versão for especificado, o elemento de programação será implementado em todas as versões existentes da DLL.</span><span class="sxs-lookup"><span data-stu-id="3687b-118">If no version number is specified, the programming element is implemented in all existing versions of the DLL.</span></span>

<span data-ttu-id="3687b-119">A tabela a seguir descreve as diferentes versões de DLL e como elas foram distribuídas em SOs com suporte.</span><span class="sxs-lookup"><span data-stu-id="3687b-119">The following table outlines the different DLL versions and how they were distributed on supported OSes.</span></span>



<span data-ttu-id="3687b-120">ComCtl32.dll</span><span class="sxs-lookup"><span data-stu-id="3687b-120">ComCtl32.dll</span></span>

<span data-ttu-id="3687b-121">Versão</span><span class="sxs-lookup"><span data-stu-id="3687b-121">Version</span></span>

<span data-ttu-id="3687b-122">Plataforma de distribuição</span><span class="sxs-lookup"><span data-stu-id="3687b-122">Distribution Platform</span></span>

<span data-ttu-id="3687b-123">5.81</span><span class="sxs-lookup"><span data-stu-id="3687b-123">5.81</span></span>

<span data-ttu-id="3687b-124">Microsoft Internet Explorer 5, 1, Microsoft Internet Explorer 5,5 e Microsoft Internet Explorer 6</span><span class="sxs-lookup"><span data-stu-id="3687b-124">Microsoft Internet Explorer 5.01, Microsoft Internet Explorer 5.5, and Microsoft Internet Explorer 6</span></span>

<span data-ttu-id="3687b-125">5,82</span><span class="sxs-lookup"><span data-stu-id="3687b-125">5.82</span></span>

<span data-ttu-id="3687b-126">Windows Server 2003, Windows Vista, Windows Server 2008 e Windows 7</span><span class="sxs-lookup"><span data-stu-id="3687b-126">Windows Server 2003, Windows Vista, Windows Server 2008, and Windows 7</span></span>

<span data-ttu-id="3687b-127">6,0</span><span class="sxs-lookup"><span data-stu-id="3687b-127">6.0</span></span>

<span data-ttu-id="3687b-128">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="3687b-128">Windows Server 2003</span></span>

<span data-ttu-id="3687b-129">6.10</span><span class="sxs-lookup"><span data-stu-id="3687b-129">6.10</span></span>

<span data-ttu-id="3687b-130">Windows Vista, Windows Server 2008 e Windows 7</span><span class="sxs-lookup"><span data-stu-id="3687b-130">Windows Vista, Windows Server 2008, and Windows 7</span></span>



 

## <a name="structure-sizes-for-different-common-control-versions"></a><span data-ttu-id="3687b-131">Tamanhos de estrutura para diferentes versões de controle comuns</span><span class="sxs-lookup"><span data-stu-id="3687b-131">Structure Sizes for Different Common Control Versions</span></span>

<span data-ttu-id="3687b-132">Os aprimoramentos contínuos para controles comuns resultaram na necessidade de estender muitas das estruturas.</span><span class="sxs-lookup"><span data-stu-id="3687b-132">Ongoing enhancements to common controls have resulted in the need to extend many of the structures.</span></span> <span data-ttu-id="3687b-133">Por esse motivo, o tamanho das estruturas foi alterado entre diferentes versões de commctrl. h.</span><span class="sxs-lookup"><span data-stu-id="3687b-133">For this reason, the size of the structures has changed between different versions of Commctrl.h.</span></span> <span data-ttu-id="3687b-134">Como a maioria das estruturas de controle comuns assume um tamanho de estrutura como um dos parâmetros, uma mensagem ou função pode falhar se o tamanho não for reconhecido.</span><span class="sxs-lookup"><span data-stu-id="3687b-134">Because most of the common control structures take a structure size as one of the parameters, a message or function can fail if the size is not recognized.</span></span> <span data-ttu-id="3687b-135">Para corrigir isso, as constantes de tamanho da estrutura foram definidas para auxiliar na destinação à versão diferente do ComCtl32.dll.</span><span class="sxs-lookup"><span data-stu-id="3687b-135">To remedy this, structure size constants have been defined to aid in targeting different version of ComCtl32.dll.</span></span> <span data-ttu-id="3687b-136">A lista a seguir define as constantes de tamanho da estrutura.</span><span class="sxs-lookup"><span data-stu-id="3687b-136">The following list defines the structure size constants.</span></span>



|    <span data-ttu-id="3687b-137">Constante de tamanho da estrutura</span><span class="sxs-lookup"><span data-stu-id="3687b-137">Structure Size Constant</span></span>                           |     <span data-ttu-id="3687b-138">Definição</span><span class="sxs-lookup"><span data-stu-id="3687b-138">Definition</span></span>                                                                                         |
|-------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="3687b-139">Tamanho de HDITEM \_ v1 \_</span><span class="sxs-lookup"><span data-stu-id="3687b-139">HDITEM\_V1\_SIZE</span></span>              | <span data-ttu-id="3687b-140">O tamanho da estrutura [**HDITEM**](/windows/win32/api/commctrl/ns-commctrl-hditema) na versão 4,0.</span><span class="sxs-lookup"><span data-stu-id="3687b-140">The size of the [**HDITEM**](/windows/win32/api/commctrl/ns-commctrl-hditema) structure in version 4.0.</span></span>                           |
| <span data-ttu-id="3687b-141">Tamanho da IMAGELISTDRAWPARAMS \_ v3 \_</span><span class="sxs-lookup"><span data-stu-id="3687b-141">IMAGELISTDRAWPARAMS\_V3\_SIZE</span></span> | <span data-ttu-id="3687b-142">O tamanho da estrutura [**IMAGELISTDRAWPARAMS**](/windows/win32/api/commctrl/ns-commctrl-imagelistdrawparams) na versão 5,9.</span><span class="sxs-lookup"><span data-stu-id="3687b-142">The size of the [**IMAGELISTDRAWPARAMS**](/windows/win32/api/commctrl/ns-commctrl-imagelistdrawparams) structure in version 5.9.</span></span> |
| <span data-ttu-id="3687b-143">Tamanho de LVCOLUMN \_ v1 \_</span><span class="sxs-lookup"><span data-stu-id="3687b-143">LVCOLUMN\_V1\_SIZE</span></span>            | <span data-ttu-id="3687b-144">O tamanho da estrutura [**LVCOLUMN**](/windows/win32/api/commctrl/ns-commctrl-lvcolumna) na versão 4,0.</span><span class="sxs-lookup"><span data-stu-id="3687b-144">The size of the [**LVCOLUMN**](/windows/win32/api/commctrl/ns-commctrl-lvcolumna) structure in version 4.0.</span></span>                       |
| <span data-ttu-id="3687b-145">\_Tamanho LVGROUP V5 \_</span><span class="sxs-lookup"><span data-stu-id="3687b-145">LVGROUP\_V5\_SIZE</span></span>             | <span data-ttu-id="3687b-146">O tamanho da estrutura [**LVGROUP**](/windows/win32/api/commctrl/ns-commctrl-lvgroup) na versão 6,0.</span><span class="sxs-lookup"><span data-stu-id="3687b-146">The size of the [**LVGROUP**](/windows/win32/api/commctrl/ns-commctrl-lvgroup) structure in version 6.0.</span></span>                         |
| <span data-ttu-id="3687b-147">Tamanho de LVHITTESTINFO \_ v1 \_</span><span class="sxs-lookup"><span data-stu-id="3687b-147">LVHITTESTINFO\_V1\_SIZE</span></span>       | <span data-ttu-id="3687b-148">O tamanho da estrutura [**LVHITTESTINFO**](/windows/win32/api/commctrl/ns-commctrl-lvhittestinfo) na versão 4.0.</span><span class="sxs-lookup"><span data-stu-id="3687b-148">The size of the [**LVHITTESTINFO**](/windows/win32/api/commctrl/ns-commctrl-lvhittestinfo) structure in version 4.0.</span></span>             |
| <span data-ttu-id="3687b-149">LVITEM \_ V1 \_ SIZE</span><span class="sxs-lookup"><span data-stu-id="3687b-149">LVITEM\_V1\_SIZE</span></span>              | <span data-ttu-id="3687b-150">O tamanho da estrutura [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) na versão 4.0.</span><span class="sxs-lookup"><span data-stu-id="3687b-150">The size of the [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) structure in version 4.0.</span></span>                           |
| <span data-ttu-id="3687b-151">LVITEM \_ V5 \_ SIZE</span><span class="sxs-lookup"><span data-stu-id="3687b-151">LVITEM\_V5\_SIZE</span></span>              | <span data-ttu-id="3687b-152">O tamanho da estrutura [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) na versão 6.0.</span><span class="sxs-lookup"><span data-stu-id="3687b-152">The size of the [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) structure in version 6.0.</span></span>                           |
| <span data-ttu-id="3687b-153">TAMANHO LVTILEINFO \_ V5 \_</span><span class="sxs-lookup"><span data-stu-id="3687b-153">LVTILEINFO\_V5\_SIZE</span></span>          | <span data-ttu-id="3687b-154">O tamanho da estrutura [**LVTILEINFO**](/windows/win32/api/commctrl/ns-commctrl-lvtileinfo) na versão 6.0.</span><span class="sxs-lookup"><span data-stu-id="3687b-154">The size of the [**LVTILEINFO**](/windows/win32/api/commctrl/ns-commctrl-lvtileinfo) structure in version 6.0.</span></span>                   |
| <span data-ttu-id="3687b-155">TAMANHO DO MCHITTESTINFO \_ V1 \_</span><span class="sxs-lookup"><span data-stu-id="3687b-155">MCHITTESTINFO\_V1\_SIZE</span></span>       | <span data-ttu-id="3687b-156">O tamanho da [**estrutura MCHITTESTINFO**](/windows/desktop/api/Commctrl/ns-commctrl-mchittestinfo) na versão 4.0.</span><span class="sxs-lookup"><span data-stu-id="3687b-156">The size of the [**MCHITTESTINFO**](/windows/desktop/api/Commctrl/ns-commctrl-mchittestinfo) structure in version 4.0.</span></span>             |
| <span data-ttu-id="3687b-157">NMLVCUSTOMDRAW \_ TAMANHO V3 \_</span><span class="sxs-lookup"><span data-stu-id="3687b-157">NMLVCUSTOMDRAW\_V3\_SIZE</span></span>      | <span data-ttu-id="3687b-158">O tamanho da estrutura [**NMLVCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmlvcustomdraw) na versão 4.7.</span><span class="sxs-lookup"><span data-stu-id="3687b-158">The size of the [**NMLVCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmlvcustomdraw) structure in version 4.7.</span></span>           |
| <span data-ttu-id="3687b-159">TAMANHO DE NMTTDISPINFO \_ V1 \_</span><span class="sxs-lookup"><span data-stu-id="3687b-159">NMTTDISPINFO\_V1\_SIZE</span></span>        | <span data-ttu-id="3687b-160">O tamanho da [**estrutura NMTTDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmttdispinfoa) na versão 4.0.</span><span class="sxs-lookup"><span data-stu-id="3687b-160">The size of the [**NMTTDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmttdispinfoa) structure in version 4.0.</span></span>               |
| <span data-ttu-id="3687b-161">NMTVCUSTOMDRAW \_ TAMANHO V3 \_</span><span class="sxs-lookup"><span data-stu-id="3687b-161">NMTVCUSTOMDRAW\_V3\_SIZE</span></span>      | <span data-ttu-id="3687b-162">O tamanho da estrutura [**NMTVCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmtvcustomdraw) na versão 4.7.</span><span class="sxs-lookup"><span data-stu-id="3687b-162">The size of the [**NMTVCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmtvcustomdraw) structure in version 4.7.</span></span>           |
| <span data-ttu-id="3687b-163">TAMANHO DE PROPSHEETHEADER \_ V1 \_</span><span class="sxs-lookup"><span data-stu-id="3687b-163">PROPSHEETHEADER\_V1\_SIZE</span></span>     | <span data-ttu-id="3687b-164">O tamanho da estrutura [**PROPSHEETHEADER**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2) na versão 4.0.</span><span class="sxs-lookup"><span data-stu-id="3687b-164">The size of the [**PROPSHEETHEADER**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2) structure in version 4.0.</span></span>         |
| <span data-ttu-id="3687b-165">TAMANHO DE PROPSHEETPAGE \_ V1 \_</span><span class="sxs-lookup"><span data-stu-id="3687b-165">PROPSHEETPAGE\_V1\_SIZE</span></span>       | <span data-ttu-id="3687b-166">O tamanho da estrutura [**PROPSHEETPAGE**](/windows/desktop/api/Prsht/ns-prsht-propsheetpagea_v2) na versão 4.0.</span><span class="sxs-lookup"><span data-stu-id="3687b-166">The size of the [**PROPSHEETPAGE**](/windows/desktop/api/Prsht/ns-prsht-propsheetpagea_v2) structure in version 4.0.</span></span>             |
| <span data-ttu-id="3687b-167">TAMANHO REBARBANDINFO \_ V3 \_</span><span class="sxs-lookup"><span data-stu-id="3687b-167">REBARBANDINFO\_V3\_SIZE</span></span>       | <span data-ttu-id="3687b-168">O tamanho da estrutura [**REBARBANDINFO**](/windows/win32/api/commctrl/ns-commctrl-rebarbandinfoa) na versão 4,7.</span><span class="sxs-lookup"><span data-stu-id="3687b-168">The size of the [**REBARBANDINFO**](/windows/win32/api/commctrl/ns-commctrl-rebarbandinfoa) structure in version 4.7.</span></span>             |
| <span data-ttu-id="3687b-169">\_Tamanho do V6 REBARBANDINFO \_</span><span class="sxs-lookup"><span data-stu-id="3687b-169">REBARBANDINFO\_V6\_SIZE</span></span>       | <span data-ttu-id="3687b-170">O tamanho da estrutura [**REBARBANDINFO**](/windows/win32/api/commctrl/ns-commctrl-rebarbandinfoa) na versão 6,0.</span><span class="sxs-lookup"><span data-stu-id="3687b-170">The size of the [**REBARBANDINFO**](/windows/win32/api/commctrl/ns-commctrl-rebarbandinfoa) structure in version 6.0.</span></span>             |
| <span data-ttu-id="3687b-171">Tamanho de TTTOOLINFO \_ v1 \_</span><span class="sxs-lookup"><span data-stu-id="3687b-171">TTTOOLINFO\_V1\_SIZE</span></span>          | <span data-ttu-id="3687b-172">O tamanho da estrutura [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) na versão 4,0.</span><span class="sxs-lookup"><span data-stu-id="3687b-172">The size of the [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) structure in version 4.0.</span></span>                       |
| <span data-ttu-id="3687b-173">Tamanho de TTTOOLINFO \_ v2 \_</span><span class="sxs-lookup"><span data-stu-id="3687b-173">TTTOOLINFO\_V2\_SIZE</span></span>          | <span data-ttu-id="3687b-174">O tamanho da estrutura [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) na versão 4,7.</span><span class="sxs-lookup"><span data-stu-id="3687b-174">The size of the [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) structure in version 4.7.</span></span>                       |
| <span data-ttu-id="3687b-175">Tamanho da TTTOOLINFO \_ v3 \_</span><span class="sxs-lookup"><span data-stu-id="3687b-175">TTTOOLINFO\_V3\_SIZE</span></span>          | <span data-ttu-id="3687b-176">O tamanho da estrutura [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) na versão 6,0.</span><span class="sxs-lookup"><span data-stu-id="3687b-176">The size of the [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) structure in version 6.0.</span></span>                       |
| <span data-ttu-id="3687b-177">Tamanho de TVINSERTSTRUCT \_ v1 \_</span><span class="sxs-lookup"><span data-stu-id="3687b-177">TVINSERTSTRUCT\_V1\_SIZE</span></span>      | <span data-ttu-id="3687b-178">O tamanho da estrutura [**TVINSERTSTRUCT**](/windows/win32/api/commctrl/ns-commctrl-tvinsertstructa) na versão 4,0.</span><span class="sxs-lookup"><span data-stu-id="3687b-178">The size of the [**TVINSERTSTRUCT**](/windows/win32/api/commctrl/ns-commctrl-tvinsertstructa) structure in version 4.0.</span></span>           |



 

## <a name="using-dllgetversion-to-determine-the-version-number"></a><span data-ttu-id="3687b-179">Usando DllGetVersion para determinar o número de versão</span><span class="sxs-lookup"><span data-stu-id="3687b-179">Using DllGetVersion to Determine the Version Number</span></span>

<span data-ttu-id="3687b-180">A função [**DllGetVersion**](/windows/desktop/api/shlwapi/nc-shlwapi-dllgetversionproc) pode ser chamada por um aplicativo para determinar qual versão de dll está presente no sistema.</span><span class="sxs-lookup"><span data-stu-id="3687b-180">The [**DllGetVersion**](/windows/desktop/api/shlwapi/nc-shlwapi-dllgetversionproc) function can be called by an application to determine which DLL version is present on the system.</span></span>

<span data-ttu-id="3687b-181">[**DllGetVersion**](/windows/desktop/api/shlwapi/nc-shlwapi-dllgetversionproc) retorna uma estrutura [**DLLVERSIONINFO2**](/windows/desktop/api/shlwapi/ns-shlwapi-dllversioninfo2) .</span><span class="sxs-lookup"><span data-stu-id="3687b-181">[**DllGetVersion**](/windows/desktop/api/shlwapi/nc-shlwapi-dllgetversionproc) returns a [**DLLVERSIONINFO2**](/windows/desktop/api/shlwapi/ns-shlwapi-dllversioninfo2) structure.</span></span> <span data-ttu-id="3687b-182">Além das informações fornecidas por meio do [**DLLVERSIONINFO**](/windows/desktop/api/shlwapi/ns-shlwapi-dllversioninfo), o **DLLVERSIONINFO2** também fornece o número do hotfix que identifica o Service Pack mais recente instalado, que fornece uma maneira mais robusta de comparar os números de versão.</span><span class="sxs-lookup"><span data-stu-id="3687b-182">In addition to the information provided through [**DLLVERSIONINFO**](/windows/desktop/api/shlwapi/ns-shlwapi-dllversioninfo), **DLLVERSIONINFO2** also provides the hotfix number that identifies the latest installed service pack, which provides a more robust way to compare version numbers.</span></span> <span data-ttu-id="3687b-183">Como o primeiro membro de **DLLVERSIONINFO2** é uma estrutura **DLLVERSIONINFO** , a estrutura posterior é compatível com versões anteriores.</span><span class="sxs-lookup"><span data-stu-id="3687b-183">Because the first member of **DLLVERSIONINFO2** is a **DLLVERSIONINFO** structure, the later structure is backward-compatible.</span></span>


<span data-ttu-id="3687b-184">A função de exemplo a seguir `GetVersion` carrega uma DLL especificada e tenta chamar sua função [**DllGetVersion**](/windows/desktop/api/shlwapi/nc-shlwapi-dllgetversionproc) .</span><span class="sxs-lookup"><span data-stu-id="3687b-184">The following sample function `GetVersion` loads a specified DLL and attempts to call its [**DllGetVersion**](/windows/desktop/api/shlwapi/nc-shlwapi-dllgetversionproc) function.</span></span> <span data-ttu-id="3687b-185">Se for bem-sucedido, ele usará uma macro para empacotar os números de versão principal e secundária da estrutura [**DLLVERSIONINFO**](/windows/desktop/api/shlwapi/ns-shlwapi-dllversioninfo) em um **DWORD** que é retornado para o aplicativo de chamada.</span><span class="sxs-lookup"><span data-stu-id="3687b-185">If successful, it uses a macro to pack the major and minor version numbers from the [**DLLVERSIONINFO**](/windows/desktop/api/shlwapi/ns-shlwapi-dllversioninfo) structure into a **DWORD** that is returned to the calling application.</span></span> <span data-ttu-id="3687b-186">Se a DLL não exportar **DllGetVersion**, a função retornará zero.</span><span class="sxs-lookup"><span data-stu-id="3687b-186">If the DLL does not export **DllGetVersion**, the function returns zero.</span></span> <span data-ttu-id="3687b-187">Você pode modificar a função para lidar com a possibilidade de que **DllGetVersion** retorne uma estrutura [**DLLVERSIONINFO2**](/windows/desktop/api/shlwapi/ns-shlwapi-dllversioninfo2) .</span><span class="sxs-lookup"><span data-stu-id="3687b-187">You can modify the function to handle the possibility that **DllGetVersion** returns a [**DLLVERSIONINFO2**](/windows/desktop/api/shlwapi/ns-shlwapi-dllversioninfo2) structure.</span></span> <span data-ttu-id="3687b-188">Nesse caso, use as informações no membro **ullVersion** dessa estrutura **DLLVERSIONINFO2** para comparar versões, números de build e service pack versões.</span><span class="sxs-lookup"><span data-stu-id="3687b-188">If so, use the information in that **DLLVERSIONINFO2** structure's **ullVersion** member to compare versions, build numbers, and service pack releases.</span></span> <span data-ttu-id="3687b-189">A [**macro MAKEDLLVERULL**](/windows/desktop/api/shlwapi/nf-shlwapi-makedllverull) simplifica a tarefa de comparar esses valores com aqueles em **ullVersion.**</span><span class="sxs-lookup"><span data-stu-id="3687b-189">The [**MAKEDLLVERULL**](/windows/desktop/api/shlwapi/nf-shlwapi-makedllverull) macro simplifies the task of comparing these values to those in **ullVersion**.</span></span>

> [!Note]  
> <span data-ttu-id="3687b-190">Usar [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) incorretamente pode representar riscos de segurança.</span><span class="sxs-lookup"><span data-stu-id="3687b-190">Using [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) incorrectly can pose security risks.</span></span> <span data-ttu-id="3687b-191">Consulte a **documentação do LoadLibrary** para obter informações sobre como carregar DLLs corretamente com versões diferentes do Windows.</span><span class="sxs-lookup"><span data-stu-id="3687b-191">Refer to the **LoadLibrary** documentation for information on how to correctly load DLLs with different versions of Windows.</span></span>

 


```C++
#include "stdafx.h"
#include "windows.h"
#include "windef.h"
#include "winbase.h"
#include "shlwapi.h"

#define PACKVERSION(major,minor) MAKELONG(minor,major)

DWORD GetVersion(LPCTSTR lpszDllName)
{
    HINSTANCE hinstDll;
    DWORD dwVersion = 0;

    // For security purposes, LoadLibrary should be provided with a fully qualified 
    // path to the DLL. The lpszDllName variable should be tested to ensure that it 
    // is a fully qualified path before it is used. 
    hinstDll = LoadLibrary(lpszDllName);
    
    if(hinstDll)
    {
        DLLGETVERSIONPROC pDllGetVersion;
        pDllGetVersion = (DLLGETVERSIONPROC)GetProcAddress(hinstDll, "DllGetVersion");

        // Because some DLLs might not implement this function, you must test for 
        // it explicitly. Depending on the particular DLL, the lack of a DllGetVersion 
        // function can be a useful indicator of the version. 

        if(pDllGetVersion)
        {
            DLLVERSIONINFO dvi;
            HRESULT hr;

            ZeroMemory(&dvi, sizeof(dvi));
            dvi.info1.cbSize = sizeof(dvi);

            hr = (*pDllGetVersion)(&dvi);

            if(SUCCEEDED(hr))
            {
               dwVersion = PACKVERSION(dvi.info1.dwMajorVersion, dvi.info1.dwMinorVersion);
            }
        }
        FreeLibrary(hinstDll);
    }
    return dwVersion;
}
```



<span data-ttu-id="3687b-192">O exemplo de código a seguir mostra como você pode `GetVersion` usar para testar se ComCtl32.dll é a versão 6.0 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="3687b-192">The following code example shows how you can use `GetVersion` to test whether ComCtl32.dll is version 6.0 or later.</span></span>


```C++
LPCTSTR lpszDllName = L"C:\\Windows\\System32\\ComCtl32.dll";
DWORD dwVer = GetVersion(lpszDllName);
DWORD dwTarget = PACKVERSION(6,0);

if(dwVer >= dwTarget)
{
    // This version of ComCtl32.dll is version 6.0 or later.
}
else
{
    // Proceed knowing that version 6.0 or later additions are not available.
    // Use an alternate approach for older the DLL version.
}
```



## <a name="project-versions"></a><span data-ttu-id="3687b-193">Versões do projeto</span><span class="sxs-lookup"><span data-stu-id="3687b-193">Project Versions</span></span>

<span data-ttu-id="3687b-194">Para garantir que seu aplicativo seja compatível com diferentes versões direcionadas de um arquivo .dll, as macros de versão estão presentes nos arquivos de header.</span><span class="sxs-lookup"><span data-stu-id="3687b-194">To ensure that your application is compatible with different targeted versions of a .dll file, version macros are present in the header files.</span></span> <span data-ttu-id="3687b-195">Essas macros são usadas para definir, excluir ou redefinir determinadas definições para versões diferentes da DLL.</span><span class="sxs-lookup"><span data-stu-id="3687b-195">These macros are used to define, exclude, or redefine certain definitions for different versions of the DLL.</span></span> <span data-ttu-id="3687b-196">Consulte [Usando os Headers do Windows](/windows/desktop/WinProg/using-the-windows-headers) para ver uma descrição detalhada dessas macros.</span><span class="sxs-lookup"><span data-stu-id="3687b-196">See [Using the Windows Headers](/windows/desktop/WinProg/using-the-windows-headers) for an in-depth description of these macros.</span></span>

<span data-ttu-id="3687b-197">Por exemplo, o nome da macro **\_ WIN32 \_ IE** normalmente é encontrado em títulos mais antigos.</span><span class="sxs-lookup"><span data-stu-id="3687b-197">For example, the macro name **\_WIN32\_IE** is commonly found in older headers.</span></span> <span data-ttu-id="3687b-198">Você é responsável por definir a macro como um número hexadecimal.</span><span class="sxs-lookup"><span data-stu-id="3687b-198">You are responsible for defining the macro as a hexadecimal number.</span></span> <span data-ttu-id="3687b-199">Esse número de versão define a versão de destino do aplicativo que está usando a DLL.</span><span class="sxs-lookup"><span data-stu-id="3687b-199">This version number defines the target version of the application that is using the DLL.</span></span> <span data-ttu-id="3687b-200">A tabela a seguir mostra os números de versão disponíveis e o efeito que cada um tem em seu aplicativo.</span><span class="sxs-lookup"><span data-stu-id="3687b-200">The following table shows the available version numbers and the effect each has on your application.</span></span>



| <span data-ttu-id="3687b-201">Versão</span><span class="sxs-lookup"><span data-stu-id="3687b-201">Version</span></span> | <span data-ttu-id="3687b-202">Descrição</span><span class="sxs-lookup"><span data-stu-id="3687b-202">Description</span></span>                                                                                                                                           |
|---------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3687b-203">0x0300</span><span class="sxs-lookup"><span data-stu-id="3687b-203">0x0300</span></span>  | <span data-ttu-id="3687b-204">O aplicativo é compatível com ComCtl32.dll versão 4.70 e posterior.</span><span class="sxs-lookup"><span data-stu-id="3687b-204">The application is compatible with ComCtl32.dll version 4.70 and later.</span></span> <span data-ttu-id="3687b-205">O aplicativo não pode implementar recursos que foram adicionados após a versão 4.70.</span><span class="sxs-lookup"><span data-stu-id="3687b-205">The application cannot implement features that were added after version 4.70.</span></span> |
| <span data-ttu-id="3687b-206">0x0400</span><span class="sxs-lookup"><span data-stu-id="3687b-206">0x0400</span></span>  | <span data-ttu-id="3687b-207">O aplicativo é compatível com ComCtl32.dll versão 4.71 e posterior.</span><span class="sxs-lookup"><span data-stu-id="3687b-207">The application is compatible with ComCtl32.dll version 4.71 and later.</span></span> <span data-ttu-id="3687b-208">O aplicativo não pode implementar recursos que foram adicionados após a versão 4.71.</span><span class="sxs-lookup"><span data-stu-id="3687b-208">The application cannot implement features that were added after version 4.71.</span></span> |
| <span data-ttu-id="3687b-209">0x0401</span><span class="sxs-lookup"><span data-stu-id="3687b-209">0x0401</span></span>  | <span data-ttu-id="3687b-210">O aplicativo é compatível com ComCtl32.dll versão 4.72 e posterior.</span><span class="sxs-lookup"><span data-stu-id="3687b-210">The application is compatible with ComCtl32.dll version 4.72 and later.</span></span> <span data-ttu-id="3687b-211">O aplicativo não pode implementar recursos que foram adicionados após a versão 4.72.</span><span class="sxs-lookup"><span data-stu-id="3687b-211">The application cannot implement features that were added after version 4.72.</span></span> |
| <span data-ttu-id="3687b-212">0x0500</span><span class="sxs-lookup"><span data-stu-id="3687b-212">0x0500</span></span>  | <span data-ttu-id="3687b-213">O aplicativo é compatível com ComCtl32.dll versão 5,80 e posterior.</span><span class="sxs-lookup"><span data-stu-id="3687b-213">The application is compatible with ComCtl32.dll version 5.80 and later.</span></span> <span data-ttu-id="3687b-214">O aplicativo não pode implementar recursos que foram adicionados após a versão 5,80.</span><span class="sxs-lookup"><span data-stu-id="3687b-214">The application cannot implement features that were added after version 5.80.</span></span> |
| <span data-ttu-id="3687b-215">0x0501</span><span class="sxs-lookup"><span data-stu-id="3687b-215">0x0501</span></span>  | <span data-ttu-id="3687b-216">O aplicativo é compatível com ComCtl32.dll versão 5,81 e posterior.</span><span class="sxs-lookup"><span data-stu-id="3687b-216">The application is compatible with ComCtl32.dll version 5.81 and later.</span></span> <span data-ttu-id="3687b-217">O aplicativo não pode implementar recursos que foram adicionados após a versão 5,81.</span><span class="sxs-lookup"><span data-stu-id="3687b-217">The application cannot implement features that were added after version 5.81.</span></span> |
| <span data-ttu-id="3687b-218">0x0600</span><span class="sxs-lookup"><span data-stu-id="3687b-218">0x0600</span></span>  | <span data-ttu-id="3687b-219">O aplicativo é compatível com ComCtl32.dll versão 6,0 e posterior.</span><span class="sxs-lookup"><span data-stu-id="3687b-219">The application is compatible with ComCtl32.dll version 6.0 and later.</span></span> <span data-ttu-id="3687b-220">O aplicativo não pode implementar recursos que foram adicionados após a versão 6,0.</span><span class="sxs-lookup"><span data-stu-id="3687b-220">The application cannot implement features that were added after version 6.0.</span></span>   |



 

<span data-ttu-id="3687b-221">Se você não definir a macro **\_ \_ IE do Win32** em seu projeto, ela será definida automaticamente como 0x0500.</span><span class="sxs-lookup"><span data-stu-id="3687b-221">If you do not define the **\_WIN32\_IE** macro in your project, it is automatically defined as 0x0500.</span></span> <span data-ttu-id="3687b-222">Para definir um valor diferente, você pode adicionar o seguinte às diretivas do compilador em seu arquivo Make; Substitua o número de versão desejado por 0x0400.</span><span class="sxs-lookup"><span data-stu-id="3687b-222">To define a different value, you can add the following to the compiler directives in your make file; substitute the desired version number for 0x0400.</span></span>


```C++
/D _WIN32_IE=0x0400
```



<span data-ttu-id="3687b-223">Outro método é adicionar uma linha semelhante à seguinte em seu código-fonte antes de incluir os arquivos de cabeçalho do Shell.</span><span class="sxs-lookup"><span data-stu-id="3687b-223">Another method is to add a line similar to the following in your source code before you include the Shell header files.</span></span> <span data-ttu-id="3687b-224">Substitua o número de versão desejado por 0x0400.</span><span class="sxs-lookup"><span data-stu-id="3687b-224">Substitute the desired version number for 0x0400.</span></span>


```C++
#define _WIN32_IE 0x0400
#include <commctrl.h>
```



## <a name="related-topics"></a><span data-ttu-id="3687b-225">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="3687b-225">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3687b-226">Sobre controles comuns</span><span class="sxs-lookup"><span data-stu-id="3687b-226">About Common Controls</span></span>](common-controls-intro.md)
</dt> </dl>

 

 