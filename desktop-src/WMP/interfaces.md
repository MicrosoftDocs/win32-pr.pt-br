---
title: Interfaces do SDK do WMP
description: Interfaces do SDK do WMP
ms.assetid: 68a0bdaf-ae1b-4ba1-817b-a31c68b9fddd
keywords:
- Windows Media Player, interfaces
- Windows Media Player Dispositivos móveis, interfaces
- modelo de objeto Windows Media Player, interfaces
- modelo de objeto, interfaces
- controle de ActiveX, interfaces
- Windows Media Player ActiveX controle, interfaces
- Windows Media Player controle de ActiveX móvel, interfaces
- referência para modelo de objeto, interfaces
- referência de modelo de objeto de interface
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7db8e5ebe29e38da9f92370f60a622fad70f36395b271eb7bd86ef49f49a3d49
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120123496"
---
# <a name="wmp-sdk-interfaces"></a>Interfaces do SDK do WMP

esta seção documenta as interfaces COM expostas pelo controle de ActiveX de Windows Media Player e o controle ActiveX móvel do Windows Media Player.

Os métodos de acessador da interface **IWMPCore** ou **IWMPPlayer** são usados para recuperar interfaces específicas. Essas interfaces, por sua vez, podem ter métodos acessadores para recuperar outras interfaces. Chamar **QueryInterface** em uma dessas interfaces só é necessário quando você recupera a versão base de uma interface e deseja chamar um método em uma versão posterior da mesma interface.

> [!Note]  
> todos os métodos e eventos têm suporte total no Windows Media Player 10 Mobile e posteriores, a menos que explicitamente declarado de outra forma.

o controle Windows Media Player expõe as interfaces a seguir.

| Interface                                                    | Descrição                                                                                                                                                                               |
|--------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [\_WMPOCXEvents](-wmpocxevents-interface.md)                | fornece eventos provenientes do controle de Windows Media Player ao qual um programa de inserção pode responder.                                                                              |
| [IWMPCdrom](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdrom)                                   | Acessa um CD ou DVD em uma unidade.                                                                                                                                                          |
| [IWMPCdromBurn](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromburn)                           | Fornece métodos para gerenciar a criação de CDs de áudio.                                                                                                                                            |
| [IWMPCdromCollection](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromcollection)               | Acessa uma coleção de unidades de CD ou DVD.                                                                                                                                                |
| [IWMPCdromRip](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromrip)                             | Fornece métodos para gerenciar a cópia de faixas de um CD de áudio.                                                                                                                               |
| [IWMPClosedCaption](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpclosedcaption)                   | Inclui legendas com um clipe de mídia.                                                                                                                                                      |
| [IWMPClosedCaption2](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpclosedcaption2)                 | Fornece métodos de legendagem de fechamento adicionais.                                                                                                                                            |
| [IWMPControls](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcontrols)                             | representa os controles de transporte de Windows Media Player, como reproduzir, parar e pausar.                                                                                                 |
| [IWMPControls2](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcontrols2)                           | Fornece métodos de controle adicionais.                                                                                                                                                      |
| [IWMPControls3](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcontrols3)                           | Fornece métodos de controle adicionais.                                                                                                                                                      |
| [IWMPCore](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcore)                                     | Recupera ponteiros para outras interfaces e acessa recursos básicos do controle. essa é a interface raiz para o modelo de objeto de Windows Media Player.                                  |
| [IWMPCore2](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcore2)                                   | Fornece métodos principais adicionais.                                                                                                                                                         |
| [IWMPCore3](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcore3)                                   | Fornece métodos principais adicionais.                                                                                                                                                         |
| [IWMPDVD](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpdvd)                                       | Acessa o menu de conteúdo de um DVD.                                                                                                                                                       |
| [IWMPError](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmperror)                                   | Acessa uma coleção de ponteiros [IWMPErrorItem](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmperroritem) .                                                                                                                     |
| [IWMPErrorItem](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmperroritem)                           | Fornece informações sobre erros.                                                                                                                                                        |
| [IWMPErrorItem2](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmperroritem2)                         | Fornece métodos de item de erro adicionais.                                                                                                                                                   |
| [IWMPEvents](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpevents)                       | expõe eventos originados no controle de Windows Media Player ao qual um programa de inserção pode responder.                                                                            |
| [IWMPEvents2](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpevents2)                     | expõe eventos originados do controle Windows Media Player 10 ao qual um programa de inserção pode responder. Esses eventos são usados especificamente para programas de sincronização de dispositivos. |
| [IWMPEvents3](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpevents3)                               | Fornece eventos relacionados à cópia de CD, gravação de CD, monitoramento de pasta e serviços de biblioteca remota.                                                                                        |
| [IWMPFolderMonitorServices](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpfoldermonitorservices)   | fornece métodos para enumerar, verificar e modificar pastas de arquivos que Windows Media Player monitores para conteúdo de mídia digital.                                                                |
| [IWMPGraphCreation](/previous-versions/windows/desktop/api/wmpservices/nn-wmpservices-iwmpgraphcreation)                   | gerencia o grafo de DirectShow.                                                                                                                                                             |
| [IWMPLibrary](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmplibrary)                               | Representa uma biblioteca.                                                                                                                                                                     |
| [IWMPLibraryServices](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmplibraryservices)               | Fornece métodos para enumerar bibliotecas.                                                                                                                                                  |
| [IWMPLibrarySharingServices](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmplibrarysharingservices) | Fornece métodos para gerenciar o compartilhamento de biblioteca.                                                                                                                                               |
| [IWMPMedia](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpmedia)                                   | Define e recupera as propriedades de um item de mídia.                                                                                                                                        |
| [IWMPMedia2](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpmedia2)                                 | Fornece métodos adicionais para definir e recuperar as propriedades de um item de mídia.                                                                                                           |
| [IWMPMedia3](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpmedia3)                                 | Fornece métodos adicionais para definir e recuperar as propriedades de um item de mídia.                                                                                                           |
| [IWMPMediaCollection](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpmediacollection)               | Acessa uma coleção de ponteiros [IWMPMedia](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpmedia) .                                                                                                                             |
| [IWMPMediaCollection2](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpmediacollection2)             | Fornece métodos que complementam a interface **IWMPMediaCollection** .                                                                                                                   |
| [IWMPMetadataPicture](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpmetadatapicture)               | Recupera informações sobre o atributo de metadados do **WM/Picture** .                                                                                                                        |
| [IWMPMetadataText](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpmetadatatext)                     | Recupera informações sobre atributos de metadados textuais complexos.                                                                                                                          |
| [IWMPNetwork](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpnetwork)                               | Define e recupera as propriedades da conexão de rede usada pelo Windows Media Player.                                                                                                 |
| [IWMPPlayer](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplayer)                                 | controla o comportamento da interface do usuário do controle de Windows Media Player.                                                                                                                 |
| [IWMPPlayer2](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplayer2)                               | Fornece métodos adicionais para controlar Windows Media Player.                                                                                                                         |
| [IWMPPlayer3](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplayer3)                               | Fornece métodos adicionais para controlar Windows Media Player.                                                                                                                         |
| [IWMPPlayer4](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplayer4)                               | Fornece métodos adicionais para controlar Windows Media Player.                                                                                                                         |
| [IWMPPlayerApplication](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplayerapplication)           | alterna entre um controle de Windows Media Player remoto e o modo completo do Player. Projetado para ser usado por programas C++ que incorporam o controle no modo remoto.                          |
| [IWMPPlayerServices](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplayerservices)                 | Usado pelo host de um controle remoto para manipular o modo completo de Windows Media Player. Projetado para uso com C++.                                                                     |
| [IWMPPlayerServices2](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplayerservices2)               | Define a prioridade de processamento em segundo plano.                                                                                                                                                  |
| [IWMPPlaylist](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplaylist)                             | Cria e gerencia playlists.                                                                                                                                                            |
| [IWMPPlaylistArray](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplaylistarray)                   | Acessa uma coleção de ponteiros [IWMPPlaylist](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplaylist) por número de índice.                                                                                                       |
| [IWMPPlaylistCollection](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplaylistcollection)         | Manipula ponteiros [IWMPPlaylist](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplaylist) [e IWMPPlaylistArray.](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplaylistarray)                                                                                     |
| [IWMPQuery](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpquery)                                   | Representa uma consulta composta.                                                                                                                                                              |
| [IWMPRemoteMediaServices](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpremotemediaservices)       | Fornece serviços para Windows Media Player de um programa que hospeda o controle Player. Projetado para uso com C++.                                                                        |
| [IWMPRenderConfig](/previous-versions/windows/desktop/api/wmprealestate/nn-wmprealestate-iwmprenderconfig)                     | Fornece métodos para especificar ou recuperar um valor que indica se a reprodução ocorre somente no processo atual.                                                                          |
| [IWMPSettings](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsettings)                             | Define ou recupera Windows Media Player configurações.                                                                                                                                          |
| [IWMPSettings2](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsettings2)                           | Define ou recupera Windows Media Player configurações.                                                                                                                                          |
| [IWMPSkinManager](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpskinmanager)                       | Especifica a capa usada com Windows Media Player.                                                                                                                                        |
| [IWMPStringCollection](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpstringcollection)             | Acessa uma coleção de cadeias de caracteres.                                                                                                                                                         |
| [IWMPStringCollection2](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpstringcollection2)           | Fornece métodos que complementam a interface **IWMPStringCollection.**                                                                                                                  |
| [IWMPSyncDevice](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsyncdevice)                         | Representa um dispositivo que pode sincronizar arquivos de mídia digital com Windows Media Player 10.                                                                                                |
| [IWMPSyncDevice2](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsyncdevice2)                       | Fornece um método que complementa a interface **IWMPSyncDevice.**                                                                                                                      |
| [IWMPSyncServices](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsyncservices)                     | Enumera dispositivos disponíveis que podem sincronizar arquivos de mídia digital com Windows Media Player 10.                                                                                       |
| [IWMPTranscodePolicy](/previous-versions/windows/desktop/api/wmpservices/nn-wmpservices-iwmptranscodepolicy)               | Fornece um método implementado pelo DirectShow de origem para gerenciar a alteração do formato de arquivos de mídia digital.                                                                          |
| [IWMPVideoRenderConfig](/previous-versions/windows/desktop/api/wmprealestate/nn-wmprealestate-iwmpvideorenderconfig)           | Fornece um método que configura o renderador de vídeo aprimorado usado pelo Windows Media Player.                                                                                               |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Referência de modelo de objeto para C++**](object-model-reference-for-c.md)
</dt> </dl>

 

 




