---
title: Sobre as versões do modelo de objeto
description: Sobre as versões do modelo de objeto
ms.assetid: 20bb1681-9079-4f8c-bb5e-5c98e3bdc76a
keywords:
- Windows Media Player,versões
- Windows Media Player modelo de objeto,versões
- modelo de objeto, versões
- Windows Media Player ActiveX controle,versões para o modelo de objeto
- ActiveX controle,versões para o modelo de objeto
- Windows Media Player Controle de ActiveX móvel, versões para o modelo de objeto
- Windows Media Player Mobile,versions for object model
- versões do Windows Media Player,modelo de objeto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce90455d93d71f6fde62b97d3b4d38e34963307e60b831c8110a914cc535cffd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119510056"
---
# <a name="about-the-object-model-versions"></a>Sobre as versões do modelo de objeto

Windows Media Player 7.0 introduziu um novo modelo de objeto. Esse modelo de objeto foi estendido com Windows Media Player 7.1, Windows Media Player para Windows XP, série Windows Media Player 9, Windows Media Player 10, Windows Media Player 11 e Windows Media Player 12. Cada tópico na referência de modelo de objeto inclui uma seção Requisitos que detalha o requisito mínimo para a propriedade individual, o método ou o evento. As listas a seguir detalham os novos objetos, métodos, propriedades e eventos que foram adicionados para cada versão desde a versão 7.0. Essas listas também incluem novas interfaces, métodos e eventos do C++.

Quando uma interface nova ou atualizada também é exposta como um objeto, somente o objeto é listado. Para localizar a interface, consulte a Referência [de Modelo de Objeto para C++.](object-model-reference-for-c.md) Normalmente, você simplesmente precisará adicionar o prefixo IWMP ao nome do objeto. Se uma nova interface estender uma existente, talvez seja necessário procurar o número de versão mais recente. Por exemplo, Windows Media Player Série 9 introduziu novas propriedades e métodos disponíveis no [**Configurações**](settings-object.md) objeto . No C++, eles estão disponíveis por meio da interface [**IWMPSettings2,**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsettings2) que estende [**IWMPSettings**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsettings).

## <a name="added-for-windows-media-player-71"></a>Adicionado para Windows Media Player 7.1

-   [**Propriedade Player.stretchToFit**](player-stretchtofit.md)

## <a name="added-for-windows-media-player-for-windows-xp"></a>Adicionado para Windows Media Player para Windows XP

-   [**Método Controls.step**](controls-step.md)
-   [**Objeto DVD**](dvd-object.md)
-   [**Propriedade Media.error**](media-error.md)
-   [**Evento Player.DomainChange**](player-player-domainchange.md)
-   [**Evento Player.MediaError**](player-player-mediaerror.md)
-   [**Evento Player.OpenPlaylistSwitch**](player-player-openplaylistswitch.md)
-   [**Propriedade Player.windowlessVideo**](player-windowlessvideo.md)

## <a name="added-for-windows-media-player-9-series"></a>Adicionado para Windows Media Player Série 9

-   [**Método ClosedCaption.getSAMILangID**](closedcaption-getsamilangid.md)
-   [**Método ClosedCaption.getSAMILangName**](closedcaption-getsamilangname.md)
-   [**Método ClosedCaption.getSAMIStyleName**](closedcaption-getsamistylename.md)
-   [**Propriedade ClosedCaption.SAMILangCount**](closedcaption-samilangcount.md)
-   [**Propriedade ClosedCaption.SAMIStyleCount**](closedcaption-samistylecount.md)
-   [**Propriedade Controls.audioLanguageCount**](controls-audiolanguagecount.md)
-   [**Propriedade Controls.currentAudioLanguage**](controls-currentaudiolanguage.md)
-   [**Propriedade Controls.currentAudioLanguageIndex**](controls-currentaudiolanguageindex.md)
-   [**Propriedade Controls.currentPositionTimecode**](controls-currentpositiontimecode.md)
-   [**Método Controls.getAudioLanguageDescription**](controls-getaudiolanguagedescription.md)
-   [**Método Controls.getAudioLanguageID**](controls-getaudiolanguageid.md)
-   [**Método Controls.getLanguageName**](controls-getlanguagename.md)
-   [**Propriedade ErrorItem.condition**](erroritem-condition.md)
-   [**Propriedade External.appColorLight**](external-appcolorlight.md)
-   [**Evento External.OnColorChange**](external-oncolorchange-event.md)
-   [**Propriedade External.version**](external-version.md)
-   [**Evento IWMPEvents::P layerDockedStateChange**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents-playerdockedstatechange)
-   [**Evento IWMPEvents::P layerReconnect**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents-playerreconnect)
-   [**Evento IWMPEvents::SwitchedToControl**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents-switchedtocontrol)
-   [**Evento IWMPEvents::SwitchedToPlayerApplication**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents-switchedtoplayerapplication)
-   [**IWMPPlayerServices Interface**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplayerservices)
-   [**IWMPRemoteMediaServices Interface**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpremotemediaservices)
-   [**IWMPSkinManager Interface**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpskinmanager)
-   [**Método Media.getAttributeCountByType**](media-getattributecountbytype.md)
-   [**Método Media.getItemInfoByType**](media-getiteminfobytype.md)
-   [**Objeto MetadataPicture**](metadatapicture-object.md)
-   [**Objeto MetadataText**](metadatatext-object.md)
-   [**Evento Player.AudioLanguageChange**](player-player-audiolanguagechange.md)
-   [**Propriedade Player.isRemote**](player-isremote.md)
-   [**Evento Player.MediaCollectionAttributeStringChanged**](player-player-mediacollectionattributestringchanged.md)
-   [**Método Player.newMedia**](player-newmedia.md)
-   [**Método Player.newPlaylist**](player-newplaylist.md)
-   [**Método Player.openPlayer**](player-openplayer.md)
-   [**Propriedade Player.playerApplication**](player-playerapplication.md)
-   [**Evento Player.StatusChange**](player-player-statuschange.md)
-   [**Objeto PlayerApplication**](playerapplication-object.md)
-   [**propriedade Configurações.defaultAudioLanguage**](settings-defaultaudiolanguage.md)
-   [**propriedade Configurações.mediaAccessRights**](settings-mediaaccessrights.md)
-   [**Método Configurações.requestMediaAccessRights**](settings-requestmediaaccessrights.md)

## <a name="added-for-windows-media-player-10"></a>Adicionado para Windows Media Player 10

-   [**IWMPGraphCreation Interface**](/previous-versions/windows/desktop/api/wmpservices/nn-wmpservices-iwmpgraphcreation)
-   [**IWMPPlayerServices2 Interface**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplayerservices2)
-   [**IWMPSyncDevice Interface**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsyncdevice)
-   [**IWMPSyncServices Interface**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsyncservices)
-   [**Enumeração WMPDeviceStatus**](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpdevicestatus)
-   [**Enumeração WMPSyncState**](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpsyncstate)

## <a name="added-for-windows-media-player-11"></a>Adicionado para Windows Media Player 11

-   [**Interface IWMPCdrom Ltda**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromburn)
-   [**Interface IWMPCdrom Ltda (VB e C#)**](iwmpcdromburn--vb-and-c.md)
-   [**IWMPCdromRip Interface**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromrip)
-   [**Interface IWMPCdromRip (VB e C#)**](iwmpcdromrip--vb-and-c.md)
-   [**IWMPEvents3 Interface**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpevents3)
-   [**IWMPFolderMonitorServices Interface**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpfoldermonitorservices)
-   [**IWMPLibrary Interface**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmplibrary)
-   [**Interface IWMPLibrary (VB e C#)**](iwmplibrary--vb-and-c.md)
-   [**IWMPLibraryServices Interface**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmplibraryservices)
-   [**Interface IWMPLibraryServices (VB e C#)**](iwmplibraryservices--vb-and-c.md)
-   [**IWMPLibrarySharingServices Interface**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmplibrarysharingservices)
-   [**IWMPMediaCollection2 Interface**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpmediacollection2)
-   [**Interface IWMPMediaCollection2 (VB e C#)**](iwmpmediacollection2--vb-and-c.md)
-   [**IWMPQuery Interface**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpquery)
-   [**Interface IWMPQuery (VB e C#)**](iwmpquery--vb-and-c.md)
-   [**IWMPRenderConfig Interface**](/previous-versions/windows/desktop/api/wmprealestate/nn-wmprealestate-iwmprenderconfig)
-   [**IWMPStringCollection2 Interface**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpstringcollection2)
-   [**Interface IWMPStringCollection2 (VB e C#)**](iwmpstringcollection2--vb-and-c.md)
-   [**IWMPSyncDevice2 Interface**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsyncdevice2)
-   [**IWMPVideoRenderConfig Interface**](/previous-versions/windows/desktop/api/wmprealestate/nn-wmprealestate-iwmpvideorenderconfig)
-   [**Objeto Query**](query-object.md)
-   [**Enumeração WMP Ltdaformat**](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpburnformat)
-   [**Enumeração WMPState**](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpburnstate)
-   [**Enumeração WMPLibraryType**](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmplibrarytype)
-   [**Enumeração WMPRipState**](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpripstate)

## <a name="added-for-windows-media-player-12"></a>Adicionado para Windows Media Player 12

-   [**IWMPAudioRenderConfig Interface**](/previous-versions/windows/desktop/api/wmprealestate/nn-wmprealestate-iwmpaudiorenderconfig)
-   [**IWMPEvents4 Interface**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpevents4)
-   [**IWMPLibrary2 Interface**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmplibrary2)
-   [**IWMPSyncDevice3 Interface**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsyncdevice3)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Sobre o modelo de objeto do player**](about-the-player-object-model.md)
</dt> <dt>

[**Referência de modelo de objeto para scripts**](object-model-reference-for-scripting.md)
</dt> </dl>

 

 




