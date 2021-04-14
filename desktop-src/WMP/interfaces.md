---
title: Interfaces do SDK do WMP
description: Interfaces do SDK do WMP
ms.assetid: 68a0bdaf-ae1b-4ba1-817b-a31c68b9fddd
keywords:
- Windows Media Player, interfaces
- Windows Media Player Mobile, interfaces
- Modelo de objeto do Windows Media Player, interfaces
- modelo de objeto, interfaces
- Controle ActiveX, interfaces
- Controle ActiveX do Windows Media Player, interfaces
- Controle ActiveX móvel do Windows Media Player, interfaces
- referência para modelo de objeto, interfaces
- referência de modelo de objeto de interface
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ffff5a4c609d13d84972989ac32dae1600f5f02d
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104369066"
---
# <a name="wmp-sdk-interfaces"></a>Interfaces do SDK do WMP

Esta seção documenta as interfaces COM expostas pelo controle ActiveX do Windows Media Player e o controle ActiveX do Windows Media Player Mobile.

Os métodos de acessador da interface **IWMPCore** ou **IWMPPlayer** são usados para recuperar interfaces específicas. Essas interfaces, por sua vez, podem ter métodos acessadores para recuperar outras interfaces. Chamar **QueryInterface** em uma dessas interfaces só é necessário quando você recupera a versão base de uma interface e deseja chamar um método em uma versão posterior da mesma interface.

> [!Note]  
> Todos os métodos e eventos têm suporte total no Windows Media Player 10 Mobile e posterior, a menos que explicitamente declarado de outra forma.

O controle do Windows Media Player expõe as seguintes interfaces.

| Interface                                                    | Descrição                                                                                                                                                                               |
|--------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [\_WMPOCXEvents](-wmpocxevents-interface.md)                | Fornece eventos provenientes do controle do Windows Media Player para o qual um programa de inserção pode responder.                                                                              |
| [IWMPCdrom](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdrom)                                   | Acessa um CD ou DVD em uma unidade.                                                                                                                                                          |
| [IWMPCdromBurn](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromburn)                           | Fornece métodos para gerenciar a criação de CDs de áudio.                                                                                                                                            |
| [IWMPCdromCollection](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromcollection)               | Acessa uma coleção de unidades de CD ou DVD.                                                                                                                                                |
| [IWMPCdromRip](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromrip)                             | Fornece métodos para gerenciar a cópia de faixas de um CD de áudio.                                                                                                                               |
| [IWMPClosedCaption](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpclosedcaption)                   | Inclui legendas com um clipe de mídia.                                                                                                                                                      |
| [IWMPClosedCaption2](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpclosedcaption2)                 | Fornece métodos de legendagem de fechamento adicionais.                                                                                                                                            |
| [IWMPControls](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcontrols)                             | Representa os controles de transporte do Windows Media Player, como reproduzir, parar e pausar.                                                                                                 |
| [IWMPControls2](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcontrols2)                           | Fornece métodos de controle adicionais.                                                                                                                                                      |
| [IWMPControls3](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcontrols3)                           | Fornece métodos de controle adicionais.                                                                                                                                                      |
| [IWMPCore](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcore)                                     | Recupera ponteiros para outras interfaces e acessa recursos básicos do controle. Essa é a interface raiz do modelo de objeto do Windows Media Player.                                  |
| [IWMPCore2](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcore2)                                   | Fornece métodos principais adicionais.                                                                                                                                                         |
| [IWMPCore3](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcore3)                                   | Fornece métodos principais adicionais.                                                                                                                                                         |
| [IWMPDVD](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpdvd)                                       | Acessa o menu de conteúdo de um DVD.                                                                                                                                                       |
| [IWMPError](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmperror)                                   | Acessa uma coleção de ponteiros [IWMPErrorItem](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmperroritem) .                                                                                                                     |
| [IWMPErrorItem](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmperroritem)                           | Fornece informações sobre erros.                                                                                                                                                        |
| [IWMPErrorItem2](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmperroritem2)                         | Fornece métodos de item de erro adicionais.                                                                                                                                                   |
| [IWMPEvents](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpevents)                       | Expõe eventos originados no controle do Windows Media Player para o qual um programa de inserção pode responder.                                                                            |
| [IWMPEvents2](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpevents2)                     | Expõe eventos originados do controle do Windows Media Player 10 ao qual um programa de inserção pode responder. Esses eventos são usados especificamente para programas de sincronização de dispositivos. |
| [IWMPEvents3](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpevents3)                               | Fornece eventos relacionados à cópia de CD, gravação de CD, monitoramento de pasta e serviços de biblioteca remota.                                                                                        |
| [IWMPFolderMonitorServices](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpfoldermonitorservices)   | Fornece métodos para enumerar, verificar e modificar pastas de arquivos que o Windows Media Player monitora para conteúdo de mídia digital.                                                                |
| [IWMPGraphCreation](/previous-versions/windows/desktop/api/wmpservices/nn-wmpservices-iwmpgraphcreation)                   | Gerencia o grafo do DirectShow.                                                                                                                                                             |
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
| [IWMPPlayer](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplayer)                                 | Controla o comportamento da interface do usuário de controle do Windows Media Player.                                                                                                                 |
| [IWMPPlayer2](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplayer2)                               | Fornece métodos adicionais para controlar o Windows Media Player.                                                                                                                         |
| [IWMPPlayer3](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplayer3)                               | Fornece métodos adicionais para controlar o Windows Media Player.                                                                                                                         |
| [IWMPPlayer4](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplayer4)                               | Fornece métodos adicionais para controlar o Windows Media Player.                                                                                                                         |
| [IWMPPlayerApplication](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplayerapplication)           | Alterna entre um controle do Windows Media Player remoto e o modo completo do Player. Projetado para ser usado por programas C++ que incorporam o controle no modo remoto.                          |
| [IWMPPlayerServices](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplayerservices)                 | Usado pelo host de um controle remoto para manipular o modo completo do Windows Media Player. Projetado para uso com C++.                                                                     |
| [IWMPPlayerServices2](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplayerservices2)               | Define a prioridade de processamento em segundo plano.                                                                                                                                                  |
| [IWMPPlaylist](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplaylist)                             | Cria e gerencia listas de reprodução.                                                                                                                                                            |
| [IWMPPlaylistArray](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplaylistarray)                   | Acessa uma coleção de ponteiros [IWMPPlaylist](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplaylist) por número de índice.                                                                                                       |
| [IWMPPlaylistCollection](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplaylistcollection)         | Manipula ponteiros [IWMPPlaylist](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplaylist) e [IWMPPlaylistArray](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplaylistarray) .                                                                                     |
| [IWMPQuery](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpquery)                                   | Representa uma consulta composta.                                                                                                                                                              |
| [IWMPRemoteMediaServices](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpremotemediaservices)       | Fornece serviços para o Windows Media Player a partir de um programa que hospeda o controle do jogador. Projetado para uso com C++.                                                                        |
| [IWMPRenderConfig](/previous-versions/windows/desktop/api/wmprealestate/nn-wmprealestate-iwmprenderconfig)                     | Fornece métodos para especificar ou recuperar um valor que indica se a reprodução ocorre apenas no processo atual.                                                                          |
| [IWMPSettings](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsettings)                             | Define ou recupera as configurações do Windows Media Player.                                                                                                                                          |
| [IWMPSettings2](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsettings2)                           | Define ou recupera as configurações do Windows Media Player.                                                                                                                                          |
| [IWMPSkinManager](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpskinmanager)                       | Especifica a capa usada com o Windows Media Player.                                                                                                                                        |
| [IWMPStringCollection](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpstringcollection)             | Acessa uma coleção de cadeias de caracteres.                                                                                                                                                         |
| [IWMPStringCollection2](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpstringcollection2)           | Fornece métodos que complementam a interface **IWMPStringCollection** .                                                                                                                  |
| [IWMPSyncDevice](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsyncdevice)                         | Representa um dispositivo que pode sincronizar arquivos de mídia digital com o Windows Media Player 10.                                                                                                |
| [IWMPSyncDevice2](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsyncdevice2)                       | Fornece um método que complementa a interface **IWMPSyncDevice** .                                                                                                                      |
| [IWMPSyncServices](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsyncservices)                     | Enumera os dispositivos disponíveis que podem sincronizar arquivos de mídia digital com o Windows Media Player 10.                                                                                       |
| [IWMPTranscodePolicy](/previous-versions/windows/desktop/api/wmpservices/nn-wmpservices-iwmptranscodepolicy)               | Fornece um método implementado por filtros de origem do DirectShow para gerenciar a alteração do formato dos arquivos de mídia digital.                                                                          |
| [IWMPVideoRenderConfig](/previous-versions/windows/desktop/api/wmprealestate/nn-wmprealestate-iwmpvideorenderconfig)           | Fornece um método que configura o processador de vídeo avançado usado pelo Windows Media Player.                                                                                               |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Referência de modelo de objeto para C++**](object-model-reference-for-c.md)
</dt> </dl>

 

 




