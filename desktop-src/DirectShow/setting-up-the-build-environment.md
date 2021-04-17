---
description: Criando aplicativos do DirectShow
ms.assetid: 2fbdbe49-0d4d-4dce-afc3-7049c793ace0
title: Criando aplicativos do DirectShow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56c6ab8a0731e93eece734abd4380b092414ff5f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105812766"
---
# <a name="building-directshow-applications"></a><span data-ttu-id="d32ee-103">Criando aplicativos do DirectShow</span><span class="sxs-lookup"><span data-stu-id="d32ee-103">Building DirectShow Applications</span></span>

<span data-ttu-id="d32ee-104">Este tópico descreve os cabeçalhos e as bibliotecas necessárias para criar aplicativos do DirectShow.</span><span class="sxs-lookup"><span data-stu-id="d32ee-104">This topic describes the headers and libraries needed to build DirectShow applications.</span></span>

<span data-ttu-id="d32ee-105">Os cabeçalhos e as bibliotecas do DirectShow mais recentes estão disponíveis na [SDK do Windows](https://msdn.microsoft.com/windows/aa904949.aspx).</span><span class="sxs-lookup"><span data-stu-id="d32ee-105">The latest DirectShow headers and libraries are available in the [Windows SDK](https://msdn.microsoft.com/windows/aa904949.aspx).</span></span>

## <a name="header-files"></a><span data-ttu-id="d32ee-106">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="d32ee-106">Header Files</span></span>

<span data-ttu-id="d32ee-107">Todos os aplicativos do DirectShow usam o arquivo de cabeçalho mostrado na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="d32ee-107">All DirectShow applications use the header file shown in the following table.</span></span>



| <span data-ttu-id="d32ee-108">Arquivos de cabeçalho</span><span class="sxs-lookup"><span data-stu-id="d32ee-108">Header File</span></span> | <span data-ttu-id="d32ee-109">Necessário para</span><span class="sxs-lookup"><span data-stu-id="d32ee-109">Required For</span></span>                 |
|-------------|------------------------------|
| <span data-ttu-id="d32ee-110">DShow. h</span><span class="sxs-lookup"><span data-stu-id="d32ee-110">Dshow.h</span></span>     | <span data-ttu-id="d32ee-111">Todos os aplicativos do DirectShow.</span><span class="sxs-lookup"><span data-stu-id="d32ee-111">All DirectShow applications.</span></span> |



 

<span data-ttu-id="d32ee-112">Algumas interfaces do DirectShow exigem arquivos de cabeçalho adicionais.</span><span class="sxs-lookup"><span data-stu-id="d32ee-112">Some DirectShow interfaces require additional header files.</span></span> <span data-ttu-id="d32ee-113">Esses requisitos são indicados na referência de interface.</span><span class="sxs-lookup"><span data-stu-id="d32ee-113">These requirements are noted in the interface reference.</span></span>

## <a name="library-files"></a><span data-ttu-id="d32ee-114">Arquivos de biblioteca</span><span class="sxs-lookup"><span data-stu-id="d32ee-114">Library Files</span></span>

<span data-ttu-id="d32ee-115">O DirectShow usa os arquivos de biblioteca estática mostrados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="d32ee-115">DirectShow uses the static library files shown in the following table.</span></span>



| <span data-ttu-id="d32ee-116">Arquivo de biblioteca</span><span class="sxs-lookup"><span data-stu-id="d32ee-116">Library File</span></span> | <span data-ttu-id="d32ee-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="d32ee-117">Description</span></span>                                                                                                                    |
|--------------|--------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d32ee-118">Strmiids. lib</span><span class="sxs-lookup"><span data-stu-id="d32ee-118">Strmiids.lib</span></span> | <span data-ttu-id="d32ee-119">Exporta identificadores de classe (CLSIDs) e identificadores de interface (IIDs).</span><span class="sxs-lookup"><span data-stu-id="d32ee-119">Exports class identifiers (CLSIDs) and interface identifiers (IIDs).</span></span>                                                           |
| <span data-ttu-id="d32ee-120">Quartz. lib</span><span class="sxs-lookup"><span data-stu-id="d32ee-120">Quartz.lib</span></span>   | <span data-ttu-id="d32ee-121">Exporta a função [**AMGetErrorText**](/windows/win32/api/errors/nf-errors-amgeterrortexta) .</span><span class="sxs-lookup"><span data-stu-id="d32ee-121">Exports the [**AMGetErrorText**](/windows/win32/api/errors/nf-errors-amgeterrortexta) function.</span></span> <span data-ttu-id="d32ee-122">Se você não chamar essa função, essa biblioteca não será necessária.</span><span class="sxs-lookup"><span data-stu-id="d32ee-122">If you do not call this function, this library is not required.</span></span> |



 

<span data-ttu-id="d32ee-123">Use os mesmos arquivos. lib para compilações de depuração e versão.</span><span class="sxs-lookup"><span data-stu-id="d32ee-123">Use the same .lib files for debug and release builds.</span></span>

## <a name="filter-base-classes"></a><span data-ttu-id="d32ee-124">Filtrar classes base</span><span class="sxs-lookup"><span data-stu-id="d32ee-124">Filter Base Classes</span></span>

<span data-ttu-id="d32ee-125">O SDK do Windows fornece um conjunto de classes C++ que são recomendadas se você estiver escrevendo um filtro DirectShow personalizado.</span><span class="sxs-lookup"><span data-stu-id="d32ee-125">The Windows SDK provides a set of C++ classes that are recommended if you are writing a custom DirectShow filter.</span></span> <span data-ttu-id="d32ee-126">Essas classes são fornecidas como um código de exemplo, que você pode compilar em uma biblioteca estática.</span><span class="sxs-lookup"><span data-stu-id="d32ee-126">These classes are provided as sample code, which you can compile to a static library.</span></span> <span data-ttu-id="d32ee-127">Para obter mais informações, consulte [classes base do DirectShow](directshow-base-classes.md).</span><span class="sxs-lookup"><span data-stu-id="d32ee-127">For more information, see [DirectShow Base Classes](directshow-base-classes.md).</span></span>

## <a name="redistributable-dlls"></a><span data-ttu-id="d32ee-128">DLLs redistribuíveis</span><span class="sxs-lookup"><span data-stu-id="d32ee-128">Redistributable DLLs</span></span>

<span data-ttu-id="d32ee-129">Os aplicativos do DirectShow escritos para o Windows XP com Service Pack 2 (SP2) e posterior não precisam redistribuir as DLLs do DirectShow.</span><span class="sxs-lookup"><span data-stu-id="d32ee-129">DirectShow applications written for Windows XP with Service Pack 2 (SP2) and later do not need to redistribute any DirectShow DLLs.</span></span>

<span data-ttu-id="d32ee-130">Para o Windows XP com Service Pack 1 (SP1) e versões anteriores, as DLLs do DirectShow redistribuíveis estão disponíveis no SDK do Microsoft DirectX.</span><span class="sxs-lookup"><span data-stu-id="d32ee-130">For Windows XP with Service Pack 1 (SP1) and earlier, redistributable DirectShow DLLs are available from the Microsoft DirectX SDK.</span></span> <span data-ttu-id="d32ee-131">A versão mais recente dessas DLLs é a versão 9.0 c.</span><span class="sxs-lookup"><span data-stu-id="d32ee-131">The latest version of these DLLs is version 9.0c.</span></span> <span data-ttu-id="d32ee-132">Não é planejado nenhum desenvolvimento adicional dessas DLLs redistribuíveis.</span><span class="sxs-lookup"><span data-stu-id="d32ee-132">No further development of these redistributable DLLs is planned.</span></span> <span data-ttu-id="d32ee-133">O Windows XP com Service Pack 2 (SP2) contém as DLLs da versão 9.0 c.</span><span class="sxs-lookup"><span data-stu-id="d32ee-133">Windows XP with Service Pack 2 (SP2) contains the version 9.0c DLLs.</span></span>

<span data-ttu-id="d32ee-134">Os pacotes redstributable contêm as seguintes DLLs:</span><span class="sxs-lookup"><span data-stu-id="d32ee-134">The redstributable packages contain the following DLLs:</span></span>

-   <span data-ttu-id="d32ee-135">dxnt.cab</span><span class="sxs-lookup"><span data-stu-id="d32ee-135">dxnt.cab</span></span>
    -   <span data-ttu-id="d32ee-136">amstream.dll</span><span class="sxs-lookup"><span data-stu-id="d32ee-136">amstream.dll</span></span>
    -   <span data-ttu-id="d32ee-137">devenum.dll</span><span class="sxs-lookup"><span data-stu-id="d32ee-137">devenum.dll</span></span>
    -   <span data-ttu-id="d32ee-138">encapi.dll</span><span class="sxs-lookup"><span data-stu-id="d32ee-138">encapi.dll</span></span>
    -   <span data-ttu-id="d32ee-139">ks.sys</span><span class="sxs-lookup"><span data-stu-id="d32ee-139">ks.sys</span></span>
    -   <span data-ttu-id="d32ee-140">ksolay.ax</span><span class="sxs-lookup"><span data-stu-id="d32ee-140">ksolay.ax</span></span>
    -   <span data-ttu-id="d32ee-141">ksproxy.ax</span><span class="sxs-lookup"><span data-stu-id="d32ee-141">ksproxy.ax</span></span>
    -   <span data-ttu-id="d32ee-142">ksuser.dll</span><span class="sxs-lookup"><span data-stu-id="d32ee-142">ksuser.dll</span></span>
    -   <span data-ttu-id="d32ee-143">l3codecx.ax</span><span class="sxs-lookup"><span data-stu-id="d32ee-143">l3codecx.ax</span></span>
    -   <span data-ttu-id="d32ee-144">mciqtz32.dll</span><span class="sxs-lookup"><span data-stu-id="d32ee-144">mciqtz32.dll</span></span>
    -   <span data-ttu-id="d32ee-145">mpg2splt.ax</span><span class="sxs-lookup"><span data-stu-id="d32ee-145">mpg2splt.ax</span></span>
    -   <span data-ttu-id="d32ee-146">msdmo.dll</span><span class="sxs-lookup"><span data-stu-id="d32ee-146">msdmo.dll</span></span>
    -   <span data-ttu-id="d32ee-147">mskssrv.sys</span><span class="sxs-lookup"><span data-stu-id="d32ee-147">mskssrv.sys</span></span>
    -   <span data-ttu-id="d32ee-148">mspclock.sys</span><span class="sxs-lookup"><span data-stu-id="d32ee-148">mspclock.sys</span></span>
    -   <span data-ttu-id="d32ee-149">mspqm.sys</span><span class="sxs-lookup"><span data-stu-id="d32ee-149">mspqm.sys</span></span>
    -   <span data-ttu-id="d32ee-150">mstee.sys</span><span class="sxs-lookup"><span data-stu-id="d32ee-150">mstee.sys</span></span>
    -   <span data-ttu-id="d32ee-151">mswebdvd.dll</span><span class="sxs-lookup"><span data-stu-id="d32ee-151">mswebdvd.dll</span></span>
    -   <span data-ttu-id="d32ee-152">qasf.dll</span><span class="sxs-lookup"><span data-stu-id="d32ee-152">qasf.dll</span></span>
    -   <span data-ttu-id="d32ee-153">qcap.dll</span><span class="sxs-lookup"><span data-stu-id="d32ee-153">qcap.dll</span></span>
    -   <span data-ttu-id="d32ee-154">qdv.dll</span><span class="sxs-lookup"><span data-stu-id="d32ee-154">qdv.dll</span></span>
    -   <span data-ttu-id="d32ee-155">qdvd.dll</span><span class="sxs-lookup"><span data-stu-id="d32ee-155">qdvd.dll</span></span>
    -   <span data-ttu-id="d32ee-156">qedit.dll</span><span class="sxs-lookup"><span data-stu-id="d32ee-156">qedit.dll</span></span>
    -   <span data-ttu-id="d32ee-157">qedwipes.dll</span><span class="sxs-lookup"><span data-stu-id="d32ee-157">qedwipes.dll</span></span>
    -   <span data-ttu-id="d32ee-158">quartz.dll</span><span class="sxs-lookup"><span data-stu-id="d32ee-158">quartz.dll</span></span>
    -   <span data-ttu-id="d32ee-159">stream.sys</span><span class="sxs-lookup"><span data-stu-id="d32ee-159">stream.sys</span></span>
    -   <span data-ttu-id="d32ee-160">swenum.sys</span><span class="sxs-lookup"><span data-stu-id="d32ee-160">swenum.sys</span></span>
-   <span data-ttu-id="d32ee-161">bda.cab</span><span class="sxs-lookup"><span data-stu-id="d32ee-161">bda.cab</span></span>
    -   <span data-ttu-id="d32ee-162">bdaplgin.ax</span><span class="sxs-lookup"><span data-stu-id="d32ee-162">bdaplgin.ax</span></span>
    -   <span data-ttu-id="d32ee-163">bdasup.sys</span><span class="sxs-lookup"><span data-stu-id="d32ee-163">bdasup.sys</span></span>
    -   <span data-ttu-id="d32ee-164">ccdecode.sys</span><span class="sxs-lookup"><span data-stu-id="d32ee-164">ccdecode.sys</span></span>
    -   <span data-ttu-id="d32ee-165">ipsink.ax</span><span class="sxs-lookup"><span data-stu-id="d32ee-165">ipsink.ax</span></span>
    -   <span data-ttu-id="d32ee-166">kstvtune.ax</span><span class="sxs-lookup"><span data-stu-id="d32ee-166">kstvtune.ax</span></span>
    -   <span data-ttu-id="d32ee-167">kswdmcap.ax</span><span class="sxs-lookup"><span data-stu-id="d32ee-167">kswdmcap.ax</span></span>
    -   <span data-ttu-id="d32ee-168">ksxbar.ax</span><span class="sxs-lookup"><span data-stu-id="d32ee-168">ksxbar.ax</span></span>
    -   <span data-ttu-id="d32ee-169">mpe.sys</span><span class="sxs-lookup"><span data-stu-id="d32ee-169">mpe.sys</span></span>
    -   <span data-ttu-id="d32ee-170">mpeg2data.ax</span><span class="sxs-lookup"><span data-stu-id="d32ee-170">mpeg2data.ax</span></span>
    -   <span data-ttu-id="d32ee-171">msdv.sys</span><span class="sxs-lookup"><span data-stu-id="d32ee-171">msdv.sys</span></span>
    -   <span data-ttu-id="d32ee-172">msdvbnp.ax</span><span class="sxs-lookup"><span data-stu-id="d32ee-172">msdvbnp.ax</span></span>
    -   <span data-ttu-id="d32ee-173">msvidctl.dll</span><span class="sxs-lookup"><span data-stu-id="d32ee-173">msvidctl.dll</span></span>
    -   <span data-ttu-id="d32ee-174">msyuv.dll</span><span class="sxs-lookup"><span data-stu-id="d32ee-174">msyuv.dll</span></span>
    -   <span data-ttu-id="d32ee-175">nabtsfec.sys</span><span class="sxs-lookup"><span data-stu-id="d32ee-175">nabtsfec.sys</span></span>
    -   <span data-ttu-id="d32ee-176">ndisip.sys</span><span class="sxs-lookup"><span data-stu-id="d32ee-176">ndisip.sys</span></span>
    -   <span data-ttu-id="d32ee-177">psisdecd.dll</span><span class="sxs-lookup"><span data-stu-id="d32ee-177">psisdecd.dll</span></span>
    -   <span data-ttu-id="d32ee-178">psisrndr.ax</span><span class="sxs-lookup"><span data-stu-id="d32ee-178">psisrndr.ax</span></span>
    -   <span data-ttu-id="d32ee-179">slip.sys</span><span class="sxs-lookup"><span data-stu-id="d32ee-179">slip.sys</span></span>
    -   <span data-ttu-id="d32ee-180">streamip.sys</span><span class="sxs-lookup"><span data-stu-id="d32ee-180">streamip.sys</span></span>
    -   <span data-ttu-id="d32ee-181">vbisurf.ax</span><span class="sxs-lookup"><span data-stu-id="d32ee-181">vbisurf.ax</span></span>
    -   <span data-ttu-id="d32ee-182">wstcodec.sys</span><span class="sxs-lookup"><span data-stu-id="d32ee-182">wstcodec.sys</span></span>
    -   <span data-ttu-id="d32ee-183">wstdecod.dll</span><span class="sxs-lookup"><span data-stu-id="d32ee-183">wstdecod.dll</span></span>

## <a name="related-topics"></a><span data-ttu-id="d32ee-184">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="d32ee-184">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d32ee-185">Criando filtros do DirectShow</span><span class="sxs-lookup"><span data-stu-id="d32ee-185">Building DirectShow Filters</span></span>](building-directshow-filters.md)
</dt> </dl>

 

 
