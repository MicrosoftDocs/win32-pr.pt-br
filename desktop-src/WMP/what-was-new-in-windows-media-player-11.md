---
title: O que era novidade no Windows Media Player 11
description: Este tópico lista os recursos que foram novos no Windows Media Player 11 e no SDK do Windows Media Player 11.
ms.assetid: d2a6b6ce-a924-4b55-9dc7-68cc57e5651f
keywords:
- Windows Media Player, o que há de novo
- Windows Media Player, novos recursos
- Software Development Kit (SDK), Windows Media Player 11
- SDK (Software Development Kit), Windows Media Player 11
- documentação, SDK do Windows Media Player 11
- o que há de novo, Windows Media Player 11
- novos recursos, Windows Media Player 11
- interfaces, novos recursos no Windows Media Player 11
- atributos, novos recursos no Windows Media Player 11
- Controle ActiveX do Windows Media Player, novos recursos na versão 11
- Controle ActiveX, novos recursos na versão 11
- capas, novos recursos no Windows Media Player 11
- Capas do Windows Media Player, novos recursos na versão 11
- plug-ins, novos recursos no Windows Media Player 11
- Plug-ins do Windows Media Player, novos recursos na versão 11
- lojas online, novos recursos no Windows Media Player 11
- Lojas online do Windows Media Player, novos recursos na versão 11
- exemplos, novos recursos no Windows Media Player 11
- versões do Windows Media Player, novos recursos na versão 11
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12aa728aa1552ac0e65f5825cad62d8e9e0c7300
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 05/25/2020
ms.locfileid: "104007241"
---
# <a name="what-was-new-in-windows-media-player-11"></a>O que era novidade no Windows Media Player 11

Este tópico lista os recursos que foram novos no Windows Media Player 11 e no SDK do Windows Media Player 11.

## <a name="windows-media-player-control"></a>Controle do Windows Media Player

As seguintes interfaces foram novas no controle ActiveX do Windows Media Player 11.

-   [**Interface IWMPLibrary**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmplibrary)
-   [**Interface IWMPLibraryServices**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmplibraryservices)
-   [**Interface IWMPLibrarySharingServices**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmplibrarysharingservices)
-   [**Interface IWMPMediaCollection2**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpmediacollection2)
-   [**Interface IWMPQuery**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpquery)
-   [**Interface IWMPStringCollection2**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpstringcollection2)
-   [**Objeto mediacollection**](mediacollection-object.md)
-   [**Objeto de consulta**](query-object.md)
-   [**Objeto StringCollection**](stringcollection-object.md)
-   [**Interface IWMPCdromRip**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromrip)
-   [**Interface IWMPCdromBurn**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromburn)
-   [**Interface IWMPFolderMonitorServices**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpfoldermonitorservices)
-   [**Interface IWMPSyncDevice2**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsyncdevice2)
-   [**Interface IWMPVideoRenderConfig**](/previous-versions/windows/desktop/api/wmprealestate/nn-wmprealestate-iwmpvideorenderconfig)
-   [**IWMPUserEventSink**](/previous-versions/windows/desktop/api/wmpservices/nn-wmpservices-iwmpusereventsink)
-   [**Interface IWMPEvents3**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpevents3)

## <a name="windows-media-player-skins"></a>Capas do Windows Media Player

Os seguintes recursos de capa eram novos no Windows Media Player 11.

-   Novos atributos para posicionamento de controles. Consulte [**ambienteattributes. direita**](ambientattributes-right.md) e [**ambienteattributes. inferior**](ambientattributes-bottom.md).
-   Novos atributos para movimentação e dimensionamento de controles. Consulte [**ambienteattributes. moveSizeTo**](ambientattributes-movesizeto.md) e [**ambienteattributes. slide**](ambientattributes-slideto.md).
-   Um novo atributo para especificar o comportamento de redimensionamento de imagem. Consulte [**ambienteattributes. resizeImages**](ambientattributes-resizeimages.md).
-   Um novo atributo para especificar o dimensionamento não uniforme de um elemento de capa. Consulte [**ambienteattributes. nineGridMargins**](ambientattributes-ninegridmargins.md).

## <a name="windows-media-player-plug-ins"></a>Plug-ins do Windows Media Player

O SDK do Windows Media Player 11 introduziu um novo tipo de plug-in para converter formatos de arquivo de mídia digital. Consulte [plug-ins de conversão do Windows Media Player](windows-media-player-conversion-plug-ins.md).

Plug-ins DSP criados antes do lançamento do SDK do Windows Media Player 11 devem ser atualizados para funcionar com o Windows Media Player 11. Consulte [atualizando plug-ins de DSP existentes](updating-existing-dsp-plug-ins.md).

O assistente de plug-in do Windows Media Player foi atualizado para criar plug-ins DSP que funcionam no Windows Media Player 11. Para obter detalhes, consulte [atualizações para o assistente de plug-in do DSP para Windows Media Player 11](updates-to-the-dsp-plug-in-wizard-for-windows-media-player-11.md).

## <a name="windows-media-player-online-stores"></a>Lojas online do Windows Media Player

O Windows Media Player 11 introduziu um novo modelo para a integração de catálogos de loja online no recurso de biblioteca do Windows Media Player. Consulte o [tipo 1 lojas online](type-1-online-stores.md).

## <a name="windows-media-player"></a>Windows Media Player

Os recursos a seguir foram novos no Windows Media Player 11.

-   [Extensões de dispositivo para relatórios de conteúdo adquirido](device-extensions-for-reporting-acquired-content.md)
-   [Extensões de dispositivo para preferências de objeto de playlist](device-extensions-for-playlist-object-preferences.md)

## <a name="windows-media-player-sdk-samples"></a>Exemplos do SDK do Windows Media Player

O exemplo de C# chamado SchemaReader era novo no SDK do Windows Media Player 11. O exemplo cria uma ferramenta que usa o modelo de objeto do Windows Media Player para recuperar e exibir informações sobre metadados na biblioteca do Windows Media Player ou em um arquivo de mídia digital. A ferramenta pode salvar os resultados em um arquivo de texto. A ferramenta enumera os nomes de atributos de metadados armazenados na biblioteca para cada esquema com suporte (áudio, vídeo, playlist, foto e outros). A ferramenta também pode fornecer informações sobre os atributos disponíveis para listas de reprodução na coleção de playlist, faixas de CD, Sumário de CD, títulos de DVD, capítulos de DVD, Sumário de DVD e arquivos de mídia individuais.

O exemplo de C++ chamado WMPML foi atualizado no SDK do Windows Media Player 11 para demonstrar os seguintes recursos:

-   Usando a nova interface [**IWMPStringCollection2**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpstringcollection2) para criar uma interface do usuário semelhante ao recurso de biblioteca do Windows Media Player.
-   Usando as interfaces [**IWMPQuery**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpquery) e [**IWMPMediaCollection2**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpmediacollection2) para criar consultas compostas e exibir os resultados.

 

 




