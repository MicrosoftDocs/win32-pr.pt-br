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
# <a name="whats-new-in-windows-media-player-12"></a>Novidades no Windows Media Player 12

Este tópico lista os recursos que são novos no Windows Media Player 12.

## <a name="new-interfaces"></a>Novas interfaces

-   [**IWMPAudioRenderConfig**](/previous-versions/windows/desktop/api/wmprealestate/nn-wmprealestate-iwmpaudiorenderconfig)
-   [**IWMPEvents4**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpevents4)
-   [**IWMPLibrary2**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmplibrary2)
-   [**IWMPSyncDevice3**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsyncdevice3)

## <a name="new-attributes"></a>Novos atributos

Os novos atributos a seguir para itens de mídia estão disponíveis por meio das interfaces [**IWMPMedia**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpmedia) e [**IWMPMedia3**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpmedia3) .

-   [**AlbumCoverURL**](wm-albumcoverurl-attribute.md)
-   [**AlternateSourceURL**](alternatesourceurl-attribute.md)
-   [**DLNASourceURI**](dlnasourceuri-attribute.md)
-   [**DLNAServerUDN**](dlnaserverudn-attribute.md)
-   [**DTCPIPHost**](dtcpiphost-attribute.md)
-   [**DTCPIPPort**](dtcpipport-attribute.md)
-   [**LibraryID**](libraryid-attribute.md)
-   [**LibraryName**](libraryname-attribute.md)

## <a name="new-device-metadata"></a>Novos metadados de dispositivo

Os novos itens de metadados de dispositivo a seguir podem ser recuperados chamando [**IWMPSyncDevice:: getItemInfo**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-getiteminfo).

-   **BackgroundSyncState**
-   **SkippedFiles**
-   **SyncFilter**

Os novos itens de metadados de dispositivo a seguir podem ser definidos chamando [**IWMPSyncDevice2:: setItemInfo**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice2-setiteminfo).

-   **AutoSyncDefaultRules**
-   **BackgroundSyncState**
-   **IncludeSkippedFiles**
-   **SyncFilter**
-   **SyncOnConnect**

## <a name="new-enumeration-member"></a>Novo membro de enumeração

A enumeração [**WMPSyncState**](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpsyncstate) tem o novo membro a seguir.

-   **wmpssEstimating**

## <a name="new-flag"></a>Novo sinalizador

O método [**IWMPGraphCreation:: GetGraphCreationFlags**](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmpgraphcreation-getgraphcreationflags) dá suporte ao novo sinalizador a seguir.

-   **\_sinalizadores WMPGC \_ usam \_ \_ grafo personalizado**

## <a name="deprecated-interface"></a>Interface preterida

A interface a seguir foi preterida.

-   [**IWMPFolderMonitorServices**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpfoldermonitorservices)

## <a name="methods-that-are-no-longer-deprecated"></a>Métodos que não são mais preteridos

Os métodos a seguir foram preteridos no SDK do Windows Media Player 11, mas não são mais preteridos.

-   [**IWMPGraphCreation::GraphCreationPreRender**](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmpgraphcreation-graphcreationprerender)
-   [**IWMPGraphCreation::GraphCreationPostRender**](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmpgraphcreation-graphcreationpostrender)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sobre o SDK do Windows Media Player](about-the-windows-media-player-sdk.md)
</dt> </dl>

 

 




