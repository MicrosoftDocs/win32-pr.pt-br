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
# <a name="about-the-object-model-versions"></a>Sobre as versões do modelo de objeto

O Windows Media Player 7,0 introduziu um novo modelo de objeto. Esse modelo de objeto foi estendido com o Windows Media Player 7,1, Windows Media Player para Windows XP, Windows Media Player 9 Series, Windows Media Player 10, Windows Media Player 11 e Windows Media Player 12. Cada tópico na referência de modelo de objeto inclui uma seção de requisitos que detalha o requisito mínimo para a propriedade, o método ou o evento individual. A lista a seguir detalha os novos objetos, métodos, propriedades e eventos que foram adicionados para cada versão desde a versão 7,0. Essas listas também incluem novas interfaces, métodos e eventos do C++.

Onde uma interface nova ou atualizada também é exposta como um objeto, somente o objeto é listado. Para localizar a interface, consulte a [referência de modelo de objeto para C++](object-model-reference-for-c.md). Normalmente, você só precisará adicionar o prefixo IWMP ao nome do objeto. Se uma nova interface estender uma existente, talvez seja necessário procurar o número de versão mais recente. Por exemplo, o Windows Media Player 9 Series introduziu novas propriedades e métodos disponíveis no objeto [**Settings**](settings-object.md) . Em C++, elas estão disponíveis por meio da interface [**IWMPSettings2**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsettings2) , que estende [**IWMPSettings**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsettings).

## <a name="added-for-windows-media-player-71"></a>Adicionado ao Windows Media Player 7,1

-   [**Propriedade Player. stretchToFit**](player-stretchtofit.md)

## <a name="added-for-windows-media-player-for-windows-xp"></a>Adicionado ao Windows Media Player para Windows XP

-   [**Método Controls. Step**](controls-step.md)
-   [**Objeto de DVD**](dvd-object.md)
-   [**Propriedade Media. Error**](media-error.md)
-   [**Evento Player. DomainChange**](player-player-domainchange.md)
-   [**Evento Player. MediaError**](player-player-mediaerror.md)
-   [**Evento Player. OpenPlaylistSwitch**](player-player-openplaylistswitch.md)
-   [**Propriedade Player. windowlessVideo**](player-windowlessvideo.md)

## <a name="added-for-windows-media-player-9-series"></a>Adicionado ao Windows Media Player 9 Series

-   [**Método ClosedCaption. getSAMILangID**](closedcaption-getsamilangid.md)
-   [**Método ClosedCaption. getSAMILangName**](closedcaption-getsamilangname.md)
-   [**Método ClosedCaption. getSAMIStyleName**](closedcaption-getsamistylename.md)
-   [**Propriedade ClosedCaption. SAMILangCount**](closedcaption-samilangcount.md)
-   [**Propriedade ClosedCaption. SAMIStyleCount**](closedcaption-samistylecount.md)
-   [**Propriedade Controls. audioLanguageCount**](controls-audiolanguagecount.md)
-   [**Propriedade Controls. currentAudioLanguage**](controls-currentaudiolanguage.md)
-   [**Propriedade Controls. currentAudioLanguageIndex**](controls-currentaudiolanguageindex.md)
-   [**Propriedade Controls. currentPositionTimecode**](controls-currentpositiontimecode.md)
-   [**Método Controls. getAudioLanguageDescription**](controls-getaudiolanguagedescription.md)
-   [**Método Controls. getAudioLanguageID**](controls-getaudiolanguageid.md)
-   [**Método Controls. getLanguageName**](controls-getlanguagename.md)
-   [**Propriedade ErrorItem. Condition**](erroritem-condition.md)
-   [**Propriedade external. appColorLight**](external-appcolorlight.md)
-   [**Evento external. OnColorChange**](external-oncolorchange-event.md)
-   [**Propriedade externa. Version**](external-version.md)
-   [**IWMPEvents: evento layerDockedStateChange de:P**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents-playerdockedstatechange)
-   [**IWMPEvents: evento layerReconnect de:P**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents-playerreconnect)
-   [**Evento IWMPEvents:: SwitchedToControl**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents-switchedtocontrol)
-   [**Evento IWMPEvents:: SwitchedToPlayerApplication**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents-switchedtoplayerapplication)
-   [**Interface IWMPPlayerServices**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplayerservices)
-   [**Interface IWMPRemoteMediaServices**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpremotemediaservices)
-   [**Interface IWMPSkinManager**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpskinmanager)
-   [**Método Media. getAttributeCountByType**](media-getattributecountbytype.md)
-   [**Método Media. getItemInfoByType**](media-getiteminfobytype.md)
-   [**Objeto MetadataPicture**](metadatapicture-object.md)
-   [**Objeto MetadataText**](metadatatext-object.md)
-   [**Evento Player. AudioLanguageChange**](player-player-audiolanguagechange.md)
-   [**Propriedade Player. IsRemote**](player-isremote.md)
-   [**Evento Player. MediaCollectionAttributeStringChanged**](player-player-mediacollectionattributestringchanged.md)
-   [**Método Player. newMedia**](player-newmedia.md)
-   [**Método Player. newPlaylist**](player-newplaylist.md)
-   [**Método Player. openPlayer**](player-openplayer.md)
-   [**Propriedade Player. playerApplication**](player-playerapplication.md)
-   [**Evento Player. StatusChange**](player-player-statuschange.md)
-   [**Objeto PlayerApplication**](playerapplication-object.md)
-   [**Propriedade Settings. defaultAudioLanguage**](settings-defaultaudiolanguage.md)
-   [**Propriedade Settings. mediaAccessRights**](settings-mediaaccessrights.md)
-   [**Método Settings. requestMediaAccessRights**](settings-requestmediaaccessrights.md)

## <a name="added-for-windows-media-player-10"></a>Adicionado ao Windows Media Player 10

-   [**Interface IWMPGraphCreation**](/previous-versions/windows/desktop/api/wmpservices/nn-wmpservices-iwmpgraphcreation)
-   [**Interface IWMPPlayerServices2**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplayerservices2)
-   [**Interface IWMPSyncDevice**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsyncdevice)
-   [**Interface IWMPSyncServices**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsyncservices)
-   [**Enumeração WMPDeviceStatus**](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpdevicestatus)
-   [**Enumeração WMPSyncState**](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpsyncstate)

## <a name="added-for-windows-media-player-11"></a>Adicionado ao Windows Media Player 11

-   [**Interface IWMPCdromBurn**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromburn)
-   [**Interface IWMPCdromBurn (VB e C#)**](iwmpcdromburn--vb-and-c.md)
-   [**Interface IWMPCdromRip**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromrip)
-   [**Interface IWMPCdromRip (VB e C#)**](iwmpcdromrip--vb-and-c.md)
-   [**Interface IWMPEvents3**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpevents3)
-   [**Interface IWMPFolderMonitorServices**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpfoldermonitorservices)
-   [**Interface IWMPLibrary**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmplibrary)
-   [**Interface IWMPLibrary (VB e C#)**](iwmplibrary--vb-and-c.md)
-   [**Interface IWMPLibraryServices**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmplibraryservices)
-   [**Interface IWMPLibraryServices (VB e C#)**](iwmplibraryservices--vb-and-c.md)
-   [**Interface IWMPLibrarySharingServices**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmplibrarysharingservices)
-   [**Interface IWMPMediaCollection2**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpmediacollection2)
-   [**Interface IWMPMediaCollection2 (VB e C#)**](iwmpmediacollection2--vb-and-c.md)
-   [**Interface IWMPQuery**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpquery)
-   [**Interface IWMPQuery (VB e C#)**](iwmpquery--vb-and-c.md)
-   [**Interface IWMPRenderConfig**](/previous-versions/windows/desktop/api/wmprealestate/nn-wmprealestate-iwmprenderconfig)
-   [**Interface IWMPStringCollection2**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpstringcollection2)
-   [**Interface IWMPStringCollection2 (VB e C#)**](iwmpstringcollection2--vb-and-c.md)
-   [**Interface IWMPSyncDevice2**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsyncdevice2)
-   [**Interface IWMPVideoRenderConfig**](/previous-versions/windows/desktop/api/wmprealestate/nn-wmprealestate-iwmpvideorenderconfig)
-   [**Objeto de consulta**](query-object.md)
-   [**Enumeração WMPBurnFormat**](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpburnformat)
-   [**Enumeração WMPBurnState**](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpburnstate)
-   [**Enumeração WMPLibraryType**](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmplibrarytype)
-   [**Enumeração WMPRipState**](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpripstate)

## <a name="added-for-windows-media-player-12"></a>Adicionado ao Windows Media Player 12

-   [**Interface IWMPAudioRenderConfig**](/previous-versions/windows/desktop/api/wmprealestate/nn-wmprealestate-iwmpaudiorenderconfig)
-   [**Interface IWMPEvents4**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpevents4)
-   [**Interface IWMPLibrary2**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmplibrary2)
-   [**Interface IWMPSyncDevice3**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsyncdevice3)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Sobre o modelo de objeto do Player**](about-the-player-object-model.md)
</dt> <dt>

[**Referência de modelo de objeto para scripts**](object-model-reference-for-scripting.md)
</dt> </dl>

 

 




