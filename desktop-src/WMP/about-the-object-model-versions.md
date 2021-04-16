---
title: Sobre as versões do modelo de objeto
description: Sobre as versões do modelo de objeto
ms.assetid: 20bb1681-9079-4f8c-bb5e-5c98e3bdc76a
keywords:
- Windows Media Player, versões
- Modelo de objeto do Windows Media Player, versões
- modelo de objeto, versões
- Controle ActiveX do Windows Media Player, versões para modelo de objeto
- Controle ActiveX, versões para modelo de objeto
- Controle ActiveX móvel do Windows Media Player, versões para modelo de objeto
- Windows Media Player Mobile, versões para modelo de objeto
- versões do Windows Media Player, modelo de objeto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59886f5750b6fc42112f73d6bb6e05e8d013ffdc
ms.sourcegitcommit: b04e152a7f51618fc174ffa872654623fe088db2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/21/2020
ms.locfileid: "104365740"
---
# <a name="about-the-object-model-versions"></a><span data-ttu-id="d842a-111">Sobre as versões do modelo de objeto</span><span class="sxs-lookup"><span data-stu-id="d842a-111">About the Object Model Versions</span></span>

<span data-ttu-id="d842a-112">O Windows Media Player 7,0 introduziu um novo modelo de objeto.</span><span class="sxs-lookup"><span data-stu-id="d842a-112">Windows Media Player 7.0 introduced a new object model.</span></span> <span data-ttu-id="d842a-113">Esse modelo de objeto foi estendido com o Windows Media Player 7,1, Windows Media Player para Windows XP, Windows Media Player 9 Series, Windows Media Player 10, Windows Media Player 11 e Windows Media Player 12.</span><span class="sxs-lookup"><span data-stu-id="d842a-113">This object model has been extended with Windows Media Player 7.1, Windows Media Player for Windows XP, Windows Media Player 9 Series, Windows Media Player 10, Windows Media Player 11, and Windows Media Player 12.</span></span> <span data-ttu-id="d842a-114">Cada tópico na referência de modelo de objeto inclui uma seção de requisitos que detalha o requisito mínimo para a propriedade, o método ou o evento individual.</span><span class="sxs-lookup"><span data-stu-id="d842a-114">Each topic in the Object Model Reference includes a Requirements section that details the minimum requirement for the individual property, method, or event.</span></span> <span data-ttu-id="d842a-115">A lista a seguir detalha os novos objetos, métodos, propriedades e eventos que foram adicionados para cada versão desde a versão 7,0.</span><span class="sxs-lookup"><span data-stu-id="d842a-115">The following lists detail the new objects, methods, properties, and events that have been added for each version since version 7.0.</span></span> <span data-ttu-id="d842a-116">Essas listas também incluem novas interfaces, métodos e eventos do C++.</span><span class="sxs-lookup"><span data-stu-id="d842a-116">These lists also include new C++ interfaces, methods, and events.</span></span>

<span data-ttu-id="d842a-117">Onde uma interface nova ou atualizada também é exposta como um objeto, somente o objeto é listado.</span><span class="sxs-lookup"><span data-stu-id="d842a-117">Where a new or updated interface is also exposed as an object, only the object is listed.</span></span> <span data-ttu-id="d842a-118">Para localizar a interface, consulte a [referência de modelo de objeto para C++](object-model-reference-for-c.md).</span><span class="sxs-lookup"><span data-stu-id="d842a-118">To locate the interface, refer to the [Object Model Reference for C++](object-model-reference-for-c.md).</span></span> <span data-ttu-id="d842a-119">Normalmente, você só precisará adicionar o prefixo IWMP ao nome do objeto.</span><span class="sxs-lookup"><span data-stu-id="d842a-119">Usually, you will simply need to add the IWMP prefix to the object name.</span></span> <span data-ttu-id="d842a-120">Se uma nova interface estender uma existente, talvez seja necessário procurar o número de versão mais recente.</span><span class="sxs-lookup"><span data-stu-id="d842a-120">If a new interface extends an existing one, you may need to look for the latest version number.</span></span> <span data-ttu-id="d842a-121">Por exemplo, o Windows Media Player 9 Series introduziu novas propriedades e métodos disponíveis no objeto [**Settings**](settings-object.md) .</span><span class="sxs-lookup"><span data-stu-id="d842a-121">For example, Windows Media Player 9 Series introduced new properties and methods available from the [**Settings**](settings-object.md) object.</span></span> <span data-ttu-id="d842a-122">Em C++, elas estão disponíveis por meio da interface [**IWMPSettings2**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsettings2) , que estende [**IWMPSettings**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsettings).</span><span class="sxs-lookup"><span data-stu-id="d842a-122">In C++, these are available through the [**IWMPSettings2**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsettings2) interface, which extends [**IWMPSettings**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsettings).</span></span>

## <a name="added-for-windows-media-player-71"></a><span data-ttu-id="d842a-123">Adicionado ao Windows Media Player 7,1</span><span class="sxs-lookup"><span data-stu-id="d842a-123">Added for Windows Media Player 7.1</span></span>

-   [<span data-ttu-id="d842a-124">**Propriedade Player. stretchToFit**</span><span class="sxs-lookup"><span data-stu-id="d842a-124">**Player.stretchToFit Property**</span></span>](player-stretchtofit.md)

## <a name="added-for-windows-media-player-for-windows-xp"></a><span data-ttu-id="d842a-125">Adicionado ao Windows Media Player para Windows XP</span><span class="sxs-lookup"><span data-stu-id="d842a-125">Added for Windows Media Player for Windows XP</span></span>

-   [<span data-ttu-id="d842a-126">**Método Controls. Step**</span><span class="sxs-lookup"><span data-stu-id="d842a-126">**Controls.step Method**</span></span>](controls-step.md)
-   [<span data-ttu-id="d842a-127">**Objeto de DVD**</span><span class="sxs-lookup"><span data-stu-id="d842a-127">**DVD Object**</span></span>](dvd-object.md)
-   [<span data-ttu-id="d842a-128">**Propriedade Media. Error**</span><span class="sxs-lookup"><span data-stu-id="d842a-128">**Media.error Property**</span></span>](media-error.md)
-   [<span data-ttu-id="d842a-129">**Evento Player. DomainChange**</span><span class="sxs-lookup"><span data-stu-id="d842a-129">**Player.DomainChange Event**</span></span>](player-player-domainchange.md)
-   [<span data-ttu-id="d842a-130">**Evento Player. MediaError**</span><span class="sxs-lookup"><span data-stu-id="d842a-130">**Player.MediaError Event**</span></span>](player-player-mediaerror.md)
-   [<span data-ttu-id="d842a-131">**Evento Player. OpenPlaylistSwitch**</span><span class="sxs-lookup"><span data-stu-id="d842a-131">**Player.OpenPlaylistSwitch Event**</span></span>](player-player-openplaylistswitch.md)
-   [<span data-ttu-id="d842a-132">**Propriedade Player. windowlessVideo**</span><span class="sxs-lookup"><span data-stu-id="d842a-132">**Player.windowlessVideo Property**</span></span>](player-windowlessvideo.md)

## <a name="added-for-windows-media-player-9-series"></a><span data-ttu-id="d842a-133">Adicionado ao Windows Media Player 9 Series</span><span class="sxs-lookup"><span data-stu-id="d842a-133">Added for Windows Media Player 9 Series</span></span>

-   [<span data-ttu-id="d842a-134">**Método ClosedCaption. getSAMILangID**</span><span class="sxs-lookup"><span data-stu-id="d842a-134">**ClosedCaption.getSAMILangID Method**</span></span>](closedcaption-getsamilangid.md)
-   [<span data-ttu-id="d842a-135">**Método ClosedCaption. getSAMILangName**</span><span class="sxs-lookup"><span data-stu-id="d842a-135">**ClosedCaption.getSAMILangName Method**</span></span>](closedcaption-getsamilangname.md)
-   [<span data-ttu-id="d842a-136">**Método ClosedCaption. getSAMIStyleName**</span><span class="sxs-lookup"><span data-stu-id="d842a-136">**ClosedCaption.getSAMIStyleName Method**</span></span>](closedcaption-getsamistylename.md)
-   [<span data-ttu-id="d842a-137">**Propriedade ClosedCaption. SAMILangCount**</span><span class="sxs-lookup"><span data-stu-id="d842a-137">**ClosedCaption.SAMILangCount Property**</span></span>](closedcaption-samilangcount.md)
-   [<span data-ttu-id="d842a-138">**Propriedade ClosedCaption. SAMIStyleCount**</span><span class="sxs-lookup"><span data-stu-id="d842a-138">**ClosedCaption.SAMIStyleCount Property**</span></span>](closedcaption-samistylecount.md)
-   [<span data-ttu-id="d842a-139">**Propriedade Controls. audioLanguageCount**</span><span class="sxs-lookup"><span data-stu-id="d842a-139">**Controls.audioLanguageCount Property**</span></span>](controls-audiolanguagecount.md)
-   [<span data-ttu-id="d842a-140">**Propriedade Controls. currentAudioLanguage**</span><span class="sxs-lookup"><span data-stu-id="d842a-140">**Controls.currentAudioLanguage Property**</span></span>](controls-currentaudiolanguage.md)
-   [<span data-ttu-id="d842a-141">**Propriedade Controls. currentAudioLanguageIndex**</span><span class="sxs-lookup"><span data-stu-id="d842a-141">**Controls.currentAudioLanguageIndex Property**</span></span>](controls-currentaudiolanguageindex.md)
-   [<span data-ttu-id="d842a-142">**Propriedade Controls. currentPositionTimecode**</span><span class="sxs-lookup"><span data-stu-id="d842a-142">**Controls.currentPositionTimecode Property**</span></span>](controls-currentpositiontimecode.md)
-   [<span data-ttu-id="d842a-143">**Método Controls. getAudioLanguageDescription**</span><span class="sxs-lookup"><span data-stu-id="d842a-143">**Controls.getAudioLanguageDescription Method**</span></span>](controls-getaudiolanguagedescription.md)
-   [<span data-ttu-id="d842a-144">**Método Controls. getAudioLanguageID**</span><span class="sxs-lookup"><span data-stu-id="d842a-144">**Controls.getAudioLanguageID Method**</span></span>](controls-getaudiolanguageid.md)
-   [<span data-ttu-id="d842a-145">**Método Controls. getLanguageName**</span><span class="sxs-lookup"><span data-stu-id="d842a-145">**Controls.getLanguageName Method**</span></span>](controls-getlanguagename.md)
-   [<span data-ttu-id="d842a-146">**Propriedade ErrorItem. Condition**</span><span class="sxs-lookup"><span data-stu-id="d842a-146">**ErrorItem.condition Property**</span></span>](erroritem-condition.md)
-   [<span data-ttu-id="d842a-147">**Propriedade external. appColorLight**</span><span class="sxs-lookup"><span data-stu-id="d842a-147">**External.appColorLight Property**</span></span>](external-appcolorlight.md)
-   [<span data-ttu-id="d842a-148">**Evento external. OnColorChange**</span><span class="sxs-lookup"><span data-stu-id="d842a-148">**External.OnColorChange Event**</span></span>](external-oncolorchange-event.md)
-   [<span data-ttu-id="d842a-149">**Propriedade externa. Version**</span><span class="sxs-lookup"><span data-stu-id="d842a-149">**External.version Property**</span></span>](external-version.md)
-   [<span data-ttu-id="d842a-150">**IWMPEvents: evento layerDockedStateChange de:P**</span><span class="sxs-lookup"><span data-stu-id="d842a-150">**IWMPEvents::PlayerDockedStateChange Event**</span></span>](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents-playerdockedstatechange)
-   [<span data-ttu-id="d842a-151">**IWMPEvents: evento layerReconnect de:P**</span><span class="sxs-lookup"><span data-stu-id="d842a-151">**IWMPEvents::PlayerReconnect Event**</span></span>](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents-playerreconnect)
-   [<span data-ttu-id="d842a-152">**Evento IWMPEvents:: SwitchedToControl**</span><span class="sxs-lookup"><span data-stu-id="d842a-152">**IWMPEvents::SwitchedToControl Event**</span></span>](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents-switchedtocontrol)
-   [<span data-ttu-id="d842a-153">**Evento IWMPEvents:: SwitchedToPlayerApplication**</span><span class="sxs-lookup"><span data-stu-id="d842a-153">**IWMPEvents::SwitchedToPlayerApplication Event**</span></span>](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents-switchedtoplayerapplication)
-   [<span data-ttu-id="d842a-154">**Interface IWMPPlayerServices**</span><span class="sxs-lookup"><span data-stu-id="d842a-154">**IWMPPlayerServices Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplayerservices)
-   [<span data-ttu-id="d842a-155">**Interface IWMPRemoteMediaServices**</span><span class="sxs-lookup"><span data-stu-id="d842a-155">**IWMPRemoteMediaServices Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpremotemediaservices)
-   [<span data-ttu-id="d842a-156">**Interface IWMPSkinManager**</span><span class="sxs-lookup"><span data-stu-id="d842a-156">**IWMPSkinManager Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpskinmanager)
-   [<span data-ttu-id="d842a-157">**Método Media. getAttributeCountByType**</span><span class="sxs-lookup"><span data-stu-id="d842a-157">**Media.getAttributeCountByType Method**</span></span>](media-getattributecountbytype.md)
-   [<span data-ttu-id="d842a-158">**Método Media. getItemInfoByType**</span><span class="sxs-lookup"><span data-stu-id="d842a-158">**Media.getItemInfoByType Method**</span></span>](media-getiteminfobytype.md)
-   [<span data-ttu-id="d842a-159">**Objeto MetadataPicture**</span><span class="sxs-lookup"><span data-stu-id="d842a-159">**MetadataPicture Object**</span></span>](metadatapicture-object.md)
-   [<span data-ttu-id="d842a-160">**Objeto MetadataText**</span><span class="sxs-lookup"><span data-stu-id="d842a-160">**MetadataText Object**</span></span>](metadatatext-object.md)
-   [<span data-ttu-id="d842a-161">**Evento Player. AudioLanguageChange**</span><span class="sxs-lookup"><span data-stu-id="d842a-161">**Player.AudioLanguageChange Event**</span></span>](player-player-audiolanguagechange.md)
-   [<span data-ttu-id="d842a-162">**Propriedade Player. IsRemote**</span><span class="sxs-lookup"><span data-stu-id="d842a-162">**Player.isRemote Property**</span></span>](player-isremote.md)
-   [<span data-ttu-id="d842a-163">**Evento Player. MediaCollectionAttributeStringChanged**</span><span class="sxs-lookup"><span data-stu-id="d842a-163">**Player.MediaCollectionAttributeStringChanged Event**</span></span>](player-player-mediacollectionattributestringchanged.md)
-   [<span data-ttu-id="d842a-164">**Método Player. newMedia**</span><span class="sxs-lookup"><span data-stu-id="d842a-164">**Player.newMedia Method**</span></span>](player-newmedia.md)
-   [<span data-ttu-id="d842a-165">**Método Player. newPlaylist**</span><span class="sxs-lookup"><span data-stu-id="d842a-165">**Player.newPlaylist Method**</span></span>](player-newplaylist.md)
-   [<span data-ttu-id="d842a-166">**Método Player. openPlayer**</span><span class="sxs-lookup"><span data-stu-id="d842a-166">**Player.openPlayer Method**</span></span>](player-openplayer.md)
-   [<span data-ttu-id="d842a-167">**Propriedade Player. playerApplication**</span><span class="sxs-lookup"><span data-stu-id="d842a-167">**Player.playerApplication Property**</span></span>](player-playerapplication.md)
-   [<span data-ttu-id="d842a-168">**Evento Player. StatusChange**</span><span class="sxs-lookup"><span data-stu-id="d842a-168">**Player.StatusChange Event**</span></span>](player-player-statuschange.md)
-   [<span data-ttu-id="d842a-169">**Objeto PlayerApplication**</span><span class="sxs-lookup"><span data-stu-id="d842a-169">**PlayerApplication Object**</span></span>](playerapplication-object.md)
-   [<span data-ttu-id="d842a-170">**Propriedade Settings. defaultAudioLanguage**</span><span class="sxs-lookup"><span data-stu-id="d842a-170">**Settings.defaultAudioLanguage Property**</span></span>](settings-defaultaudiolanguage.md)
-   [<span data-ttu-id="d842a-171">**Propriedade Settings. mediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="d842a-171">**Settings.mediaAccessRights Property**</span></span>](settings-mediaaccessrights.md)
-   [<span data-ttu-id="d842a-172">**Método Settings. requestMediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="d842a-172">**Settings.requestMediaAccessRights Method**</span></span>](settings-requestmediaaccessrights.md)

## <a name="added-for-windows-media-player-10"></a><span data-ttu-id="d842a-173">Adicionado ao Windows Media Player 10</span><span class="sxs-lookup"><span data-stu-id="d842a-173">Added for Windows Media Player 10</span></span>

-   [<span data-ttu-id="d842a-174">**Interface IWMPGraphCreation**</span><span class="sxs-lookup"><span data-stu-id="d842a-174">**IWMPGraphCreation Interface**</span></span>](/previous-versions/windows/desktop/api/wmpservices/nn-wmpservices-iwmpgraphcreation)
-   [<span data-ttu-id="d842a-175">**Interface IWMPPlayerServices2**</span><span class="sxs-lookup"><span data-stu-id="d842a-175">**IWMPPlayerServices2 Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplayerservices2)
-   [<span data-ttu-id="d842a-176">**Interface IWMPSyncDevice**</span><span class="sxs-lookup"><span data-stu-id="d842a-176">**IWMPSyncDevice Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsyncdevice)
-   [<span data-ttu-id="d842a-177">**Interface IWMPSyncServices**</span><span class="sxs-lookup"><span data-stu-id="d842a-177">**IWMPSyncServices Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsyncservices)
-   [<span data-ttu-id="d842a-178">**Enumeração WMPDeviceStatus**</span><span class="sxs-lookup"><span data-stu-id="d842a-178">**WMPDeviceStatus Enumeration**</span></span>](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpdevicestatus)
-   [<span data-ttu-id="d842a-179">**Enumeração WMPSyncState**</span><span class="sxs-lookup"><span data-stu-id="d842a-179">**WMPSyncState Enumeration**</span></span>](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpsyncstate)

## <a name="added-for-windows-media-player-11"></a><span data-ttu-id="d842a-180">Adicionado ao Windows Media Player 11</span><span class="sxs-lookup"><span data-stu-id="d842a-180">Added for Windows Media Player 11</span></span>

-   [<span data-ttu-id="d842a-181">**Interface IWMPCdromBurn**</span><span class="sxs-lookup"><span data-stu-id="d842a-181">**IWMPCdromBurn Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromburn)
-   [<span data-ttu-id="d842a-182">**Interface IWMPCdromBurn (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="d842a-182">**IWMPCdromBurn Interface (VB and C#)**</span></span>](iwmpcdromburn--vb-and-c.md)
-   [<span data-ttu-id="d842a-183">**Interface IWMPCdromRip**</span><span class="sxs-lookup"><span data-stu-id="d842a-183">**IWMPCdromRip Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromrip)
-   [<span data-ttu-id="d842a-184">**Interface IWMPCdromRip (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="d842a-184">**IWMPCdromRip Interface (VB and C#)**</span></span>](iwmpcdromrip--vb-and-c.md)
-   [<span data-ttu-id="d842a-185">**Interface IWMPEvents3**</span><span class="sxs-lookup"><span data-stu-id="d842a-185">**IWMPEvents3 Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpevents3)
-   [<span data-ttu-id="d842a-186">**Interface IWMPFolderMonitorServices**</span><span class="sxs-lookup"><span data-stu-id="d842a-186">**IWMPFolderMonitorServices Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpfoldermonitorservices)
-   [<span data-ttu-id="d842a-187">**Interface IWMPLibrary**</span><span class="sxs-lookup"><span data-stu-id="d842a-187">**IWMPLibrary Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmplibrary)
-   [<span data-ttu-id="d842a-188">**Interface IWMPLibrary (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="d842a-188">**IWMPLibrary Interface (VB and C#)**</span></span>](iwmplibrary--vb-and-c.md)
-   [<span data-ttu-id="d842a-189">**Interface IWMPLibraryServices**</span><span class="sxs-lookup"><span data-stu-id="d842a-189">**IWMPLibraryServices Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmplibraryservices)
-   [<span data-ttu-id="d842a-190">**Interface IWMPLibraryServices (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="d842a-190">**IWMPLibraryServices Interface (VB and C#)**</span></span>](iwmplibraryservices--vb-and-c.md)
-   [<span data-ttu-id="d842a-191">**Interface IWMPLibrarySharingServices**</span><span class="sxs-lookup"><span data-stu-id="d842a-191">**IWMPLibrarySharingServices Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmplibrarysharingservices)
-   [<span data-ttu-id="d842a-192">**Interface IWMPMediaCollection2**</span><span class="sxs-lookup"><span data-stu-id="d842a-192">**IWMPMediaCollection2 Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpmediacollection2)
-   [<span data-ttu-id="d842a-193">**Interface IWMPMediaCollection2 (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="d842a-193">**IWMPMediaCollection2 Interface (VB and C#)**</span></span>](iwmpmediacollection2--vb-and-c.md)
-   [<span data-ttu-id="d842a-194">**Interface IWMPQuery**</span><span class="sxs-lookup"><span data-stu-id="d842a-194">**IWMPQuery Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpquery)
-   [<span data-ttu-id="d842a-195">**Interface IWMPQuery (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="d842a-195">**IWMPQuery Interface (VB and C#)**</span></span>](iwmpquery--vb-and-c.md)
-   [<span data-ttu-id="d842a-196">**Interface IWMPRenderConfig**</span><span class="sxs-lookup"><span data-stu-id="d842a-196">**IWMPRenderConfig Interface**</span></span>](/previous-versions/windows/desktop/api/wmprealestate/nn-wmprealestate-iwmprenderconfig)
-   [<span data-ttu-id="d842a-197">**Interface IWMPStringCollection2**</span><span class="sxs-lookup"><span data-stu-id="d842a-197">**IWMPStringCollection2 Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpstringcollection2)
-   [<span data-ttu-id="d842a-198">**Interface IWMPStringCollection2 (VB e C#)**</span><span class="sxs-lookup"><span data-stu-id="d842a-198">**IWMPStringCollection2 Interface (VB and C#)**</span></span>](iwmpstringcollection2--vb-and-c.md)
-   [<span data-ttu-id="d842a-199">**Interface IWMPSyncDevice2**</span><span class="sxs-lookup"><span data-stu-id="d842a-199">**IWMPSyncDevice2 Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsyncdevice2)
-   [<span data-ttu-id="d842a-200">**Interface IWMPVideoRenderConfig**</span><span class="sxs-lookup"><span data-stu-id="d842a-200">**IWMPVideoRenderConfig Interface**</span></span>](/previous-versions/windows/desktop/api/wmprealestate/nn-wmprealestate-iwmpvideorenderconfig)
-   [<span data-ttu-id="d842a-201">**Objeto de consulta**</span><span class="sxs-lookup"><span data-stu-id="d842a-201">**Query Object**</span></span>](query-object.md)
-   [<span data-ttu-id="d842a-202">**Enumeração WMPBurnFormat**</span><span class="sxs-lookup"><span data-stu-id="d842a-202">**WMPBurnFormat Enumeration**</span></span>](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpburnformat)
-   [<span data-ttu-id="d842a-203">**Enumeração WMPBurnState**</span><span class="sxs-lookup"><span data-stu-id="d842a-203">**WMPBurnState Enumeration**</span></span>](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpburnstate)
-   [<span data-ttu-id="d842a-204">**Enumeração WMPLibraryType**</span><span class="sxs-lookup"><span data-stu-id="d842a-204">**WMPLibraryType Enumeration**</span></span>](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmplibrarytype)
-   [<span data-ttu-id="d842a-205">**Enumeração WMPRipState**</span><span class="sxs-lookup"><span data-stu-id="d842a-205">**WMPRipState Enumeration**</span></span>](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpripstate)

## <a name="added-for-windows-media-player-12"></a><span data-ttu-id="d842a-206">Adicionado ao Windows Media Player 12</span><span class="sxs-lookup"><span data-stu-id="d842a-206">Added for Windows Media Player 12</span></span>

-   [<span data-ttu-id="d842a-207">**Interface IWMPAudioRenderConfig**</span><span class="sxs-lookup"><span data-stu-id="d842a-207">**IWMPAudioRenderConfig Interface**</span></span>](/previous-versions/windows/desktop/api/wmprealestate/nn-wmprealestate-iwmpaudiorenderconfig)
-   [<span data-ttu-id="d842a-208">**Interface IWMPEvents4**</span><span class="sxs-lookup"><span data-stu-id="d842a-208">**IWMPEvents4 Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpevents4)
-   [<span data-ttu-id="d842a-209">**Interface IWMPLibrary2**</span><span class="sxs-lookup"><span data-stu-id="d842a-209">**IWMPLibrary2 Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmplibrary2)
-   [<span data-ttu-id="d842a-210">**Interface IWMPSyncDevice3**</span><span class="sxs-lookup"><span data-stu-id="d842a-210">**IWMPSyncDevice3 Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsyncdevice3)

## <a name="related-topics"></a><span data-ttu-id="d842a-211">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="d842a-211">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d842a-212">**Sobre o modelo de objeto do Player**</span><span class="sxs-lookup"><span data-stu-id="d842a-212">**About the Player Object Model**</span></span>](about-the-player-object-model.md)
</dt> <dt>

[<span data-ttu-id="d842a-213">**Referência de modelo de objeto para scripts**</span><span class="sxs-lookup"><span data-stu-id="d842a-213">**Object Model Reference for Scripting**</span></span>](object-model-reference-for-scripting.md)
</dt> </dl>

 

 




