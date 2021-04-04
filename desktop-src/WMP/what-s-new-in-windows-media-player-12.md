---
title: Novidades no Windows Media Player 12
description: Este tópico lista os recursos que são novos no Windows Media Player 12.
ms.assetid: 17f76963-c96d-46c9-82c0-3ed2d8a4e892
keywords:
- Windows Media Player, o que há de novo
- Windows Media Player, novos recursos
- Software Development Kit (SDK), Windows Media Player 12
- SDK (Software Development Kit), Windows Media Player 12
- documentação, SDK do Windows Media Player 12
- o que há de novo, Windows Media Player 12
- novos recursos, Windows Media Player 12
- interfaces, novos recursos no Windows Media Player 12
- atributos, novos recursos no Windows Media Player 12
- metadados, novos recursos no Windows Media Player 12
- enumerações, novos recursos no Windows Media Player 12
- sinalizadores, novos recursos no Windows Media Player 12
- interfaces, preteridas no Windows Media Player 12
- métodos, preteridos no Windows Media Player 11 e não 12
- versões do Windows Media Player, novos recursos na versão 12
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d16b21077df1f4a9c11edbfa20032ed473f872a0
ms.sourcegitcommit: c2a1c4314550ea9bd202d28adfcc7bfe6180932f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2020
ms.locfileid: "104084409"
---
# <a name="whats-new-in-windows-media-player-12"></a><span data-ttu-id="1b575-118">Novidades no Windows Media Player 12</span><span class="sxs-lookup"><span data-stu-id="1b575-118">What's New in Windows Media Player 12</span></span>

<span data-ttu-id="1b575-119">Este tópico lista os recursos que são novos no Windows Media Player 12.</span><span class="sxs-lookup"><span data-stu-id="1b575-119">This topic lists features that are new in Windows Media Player 12.</span></span>

## <a name="new-interfaces"></a><span data-ttu-id="1b575-120">Novas interfaces</span><span class="sxs-lookup"><span data-stu-id="1b575-120">New Interfaces</span></span>

-   [<span data-ttu-id="1b575-121">**IWMPAudioRenderConfig**</span><span class="sxs-lookup"><span data-stu-id="1b575-121">**IWMPAudioRenderConfig**</span></span>](/previous-versions/windows/desktop/api/wmprealestate/nn-wmprealestate-iwmpaudiorenderconfig)
-   [<span data-ttu-id="1b575-122">**IWMPEvents4**</span><span class="sxs-lookup"><span data-stu-id="1b575-122">**IWMPEvents4**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpevents4)
-   [<span data-ttu-id="1b575-123">**IWMPLibrary2**</span><span class="sxs-lookup"><span data-stu-id="1b575-123">**IWMPLibrary2**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmplibrary2)
-   [<span data-ttu-id="1b575-124">**IWMPSyncDevice3**</span><span class="sxs-lookup"><span data-stu-id="1b575-124">**IWMPSyncDevice3**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsyncdevice3)

## <a name="new-attributes"></a><span data-ttu-id="1b575-125">Novos atributos</span><span class="sxs-lookup"><span data-stu-id="1b575-125">New Attributes</span></span>

<span data-ttu-id="1b575-126">Os novos atributos a seguir para itens de mídia estão disponíveis por meio das interfaces [**IWMPMedia**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpmedia) e [**IWMPMedia3**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpmedia3) .</span><span class="sxs-lookup"><span data-stu-id="1b575-126">The following new attributes for media items are available through the [**IWMPMedia**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpmedia) and [**IWMPMedia3**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpmedia3) interfaces.</span></span>

-   [<span data-ttu-id="1b575-127">**AlbumCoverURL**</span><span class="sxs-lookup"><span data-stu-id="1b575-127">**AlbumCoverURL**</span></span>](wm-albumcoverurl-attribute.md)
-   [<span data-ttu-id="1b575-128">**AlternateSourceURL**</span><span class="sxs-lookup"><span data-stu-id="1b575-128">**AlternateSourceURL**</span></span>](alternatesourceurl-attribute.md)
-   [<span data-ttu-id="1b575-129">**DLNASourceURI**</span><span class="sxs-lookup"><span data-stu-id="1b575-129">**DLNASourceURI**</span></span>](dlnasourceuri-attribute.md)
-   [<span data-ttu-id="1b575-130">**DLNAServerUDN**</span><span class="sxs-lookup"><span data-stu-id="1b575-130">**DLNAServerUDN**</span></span>](dlnaserverudn-attribute.md)
-   [<span data-ttu-id="1b575-131">**DTCPIPHost**</span><span class="sxs-lookup"><span data-stu-id="1b575-131">**DTCPIPHost**</span></span>](dtcpiphost-attribute.md)
-   [<span data-ttu-id="1b575-132">**DTCPIPPort**</span><span class="sxs-lookup"><span data-stu-id="1b575-132">**DTCPIPPort**</span></span>](dtcpipport-attribute.md)
-   [<span data-ttu-id="1b575-133">**LibraryID**</span><span class="sxs-lookup"><span data-stu-id="1b575-133">**LibraryID**</span></span>](libraryid-attribute.md)
-   [<span data-ttu-id="1b575-134">**LibraryName**</span><span class="sxs-lookup"><span data-stu-id="1b575-134">**LibraryName**</span></span>](libraryname-attribute.md)

## <a name="new-device-metadata"></a><span data-ttu-id="1b575-135">Novos metadados de dispositivo</span><span class="sxs-lookup"><span data-stu-id="1b575-135">New Device Metadata</span></span>

<span data-ttu-id="1b575-136">Os novos itens de metadados de dispositivo a seguir podem ser recuperados chamando [**IWMPSyncDevice:: getItemInfo**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-getiteminfo).</span><span class="sxs-lookup"><span data-stu-id="1b575-136">The following new device metadata items can be retrieved by calling [**IWMPSyncDevice::getItemInfo**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-getiteminfo).</span></span>

-   <span data-ttu-id="1b575-137">**BackgroundSyncState**</span><span class="sxs-lookup"><span data-stu-id="1b575-137">**BackgroundSyncState**</span></span>
-   <span data-ttu-id="1b575-138">**SkippedFiles**</span><span class="sxs-lookup"><span data-stu-id="1b575-138">**SkippedFiles**</span></span>
-   <span data-ttu-id="1b575-139">**SyncFilter**</span><span class="sxs-lookup"><span data-stu-id="1b575-139">**SyncFilter**</span></span>

<span data-ttu-id="1b575-140">Os novos itens de metadados de dispositivo a seguir podem ser definidos chamando [**IWMPSyncDevice2:: setItemInfo**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice2-setiteminfo).</span><span class="sxs-lookup"><span data-stu-id="1b575-140">The following new device metadata items can be set by calling [**IWMPSyncDevice2::setItemInfo**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice2-setiteminfo).</span></span>

-   <span data-ttu-id="1b575-141">**AutoSyncDefaultRules**</span><span class="sxs-lookup"><span data-stu-id="1b575-141">**AutoSyncDefaultRules**</span></span>
-   <span data-ttu-id="1b575-142">**BackgroundSyncState**</span><span class="sxs-lookup"><span data-stu-id="1b575-142">**BackgroundSyncState**</span></span>
-   <span data-ttu-id="1b575-143">**IncludeSkippedFiles**</span><span class="sxs-lookup"><span data-stu-id="1b575-143">**IncludeSkippedFiles**</span></span>
-   <span data-ttu-id="1b575-144">**SyncFilter**</span><span class="sxs-lookup"><span data-stu-id="1b575-144">**SyncFilter**</span></span>
-   <span data-ttu-id="1b575-145">**SyncOnConnect**</span><span class="sxs-lookup"><span data-stu-id="1b575-145">**SyncOnConnect**</span></span>

## <a name="new-enumeration-member"></a><span data-ttu-id="1b575-146">Novo membro de enumeração</span><span class="sxs-lookup"><span data-stu-id="1b575-146">New Enumeration Member</span></span>

<span data-ttu-id="1b575-147">A enumeração [**WMPSyncState**](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpsyncstate) tem o novo membro a seguir.</span><span class="sxs-lookup"><span data-stu-id="1b575-147">The [**WMPSyncState**](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpsyncstate) enumeration has the following new member.</span></span>

-   <span data-ttu-id="1b575-148">**wmpssEstimating**</span><span class="sxs-lookup"><span data-stu-id="1b575-148">**wmpssEstimating**</span></span>

## <a name="new-flag"></a><span data-ttu-id="1b575-149">Novo sinalizador</span><span class="sxs-lookup"><span data-stu-id="1b575-149">New Flag</span></span>

<span data-ttu-id="1b575-150">O método [**IWMPGraphCreation:: GetGraphCreationFlags**](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmpgraphcreation-getgraphcreationflags) dá suporte ao novo sinalizador a seguir.</span><span class="sxs-lookup"><span data-stu-id="1b575-150">The [**IWMPGraphCreation::GetGraphCreationFlags**](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmpgraphcreation-getgraphcreationflags) method supports the following new flag.</span></span>

-   <span data-ttu-id="1b575-151">**\_sinalizadores WMPGC \_ usam \_ \_ grafo personalizado**</span><span class="sxs-lookup"><span data-stu-id="1b575-151">**WMPGC\_FLAGS\_USE\_CUSTOM\_GRAPH**</span></span>

## <a name="deprecated-interface"></a><span data-ttu-id="1b575-152">Interface preterida</span><span class="sxs-lookup"><span data-stu-id="1b575-152">Deprecated Interface</span></span>

<span data-ttu-id="1b575-153">A interface a seguir foi preterida.</span><span class="sxs-lookup"><span data-stu-id="1b575-153">The following interface is deprecated.</span></span>

-   [<span data-ttu-id="1b575-154">**IWMPFolderMonitorServices**</span><span class="sxs-lookup"><span data-stu-id="1b575-154">**IWMPFolderMonitorServices**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpfoldermonitorservices)

## <a name="methods-that-are-no-longer-deprecated"></a><span data-ttu-id="1b575-155">Métodos que não são mais preteridos</span><span class="sxs-lookup"><span data-stu-id="1b575-155">Methods That Are No Longer Deprecated</span></span>

<span data-ttu-id="1b575-156">Os métodos a seguir foram preteridos no SDK do Windows Media Player 11, mas não são mais preteridos.</span><span class="sxs-lookup"><span data-stu-id="1b575-156">The following methods were deprecated in Windows Media Player 11 SDK, but are no longer deprecated.</span></span>

-   [<span data-ttu-id="1b575-157">**IWMPGraphCreation::GraphCreationPreRender**</span><span class="sxs-lookup"><span data-stu-id="1b575-157">**IWMPGraphCreation::GraphCreationPreRender**</span></span>](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmpgraphcreation-graphcreationprerender)
-   [<span data-ttu-id="1b575-158">**IWMPGraphCreation::GraphCreationPostRender**</span><span class="sxs-lookup"><span data-stu-id="1b575-158">**IWMPGraphCreation::GraphCreationPostRender**</span></span>](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmpgraphcreation-graphcreationpostrender)

## <a name="related-topics"></a><span data-ttu-id="1b575-159">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="1b575-159">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1b575-160">Sobre o SDK do Windows Media Player</span><span class="sxs-lookup"><span data-stu-id="1b575-160">About the Windows Media Player SDK</span></span>](about-the-windows-media-player-sdk.md)
</dt> </dl>

 

 




