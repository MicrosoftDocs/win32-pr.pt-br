---
title: Interfaces para Visual Basic .NET e C
description: Interfaces para Visual Basic .NET e C\
ms.assetid: c66f1e03-20eb-45b1-8710-be9eae63e7ad
keywords:
- Windows Media Player,interfaces
- Windows Media Player Mobile,interfaces
- Windows Media Player modelo de objeto, interfaces
- modelo de objeto, interfaces
- ActiveX controle,interfaces
- Windows Media Player ActiveX controle,interfaces
- Windows Media Player Controle ActiveX dispositivo móvel, interfaces
- referência para o modelo de objeto, interfaces
- referência de modelo de objeto de interface
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a7024c60235b0a545463826fc8948adf3716c9c2d5b491414212d788087404b2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119862576"
---
# <a name="interfaces-for-visual-basic-net-and-c"></a>Interfaces para Visual Basic .NET e C #

Esta seção documenta as interfaces expostas pelo Windows Media Player ActiveX controle.

Várias propriedades e métodos do [objeto AxWindowsMediaPlayer](axwindowsmediaplayer-object--vb-and-c.md) são usados para recuperar interfaces específicas. Essas interfaces, por sua vez, podem ter propriedades e métodos de acessador para recuperar outras interfaces.

O Windows Media Player controle expõe as interfaces a seguir.



| Interface                                                      | Descrição                                                                                                                                                       |
|----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [IWMPCdrom](iwmpcdrom--vb-and-c.md)                           | Acessa um CD ou DVD em uma unidade.                                                                                                                                  |
| [IWMPCdrom Ltda](iwmpcdromburn--vb-and-c.md)                   | Fornece propriedades e métodos para gerenciar a criação de CDs de áudio.                                                                                                     |
| [IWMPCdromCollection](iwmpcdromcollection--vb-and-c.md)       | Acessa uma coleção de unidades de CD ou DVD.                                                                                                                        |
| [IWMPCdromRip](iwmpcdromrip--vb-and-c.md)                     | Fornece propriedades e métodos para gerenciar a cópia ou *controlar* faixas de um CD de áudio.                                                                         |
| [IWMPClosedCaption](iwmpclosedcaption--vb-and-c.md)           | Fornece uma maneira de incluir legendas com um arquivo de mídia digital.                                                                                                     |
| [IWMPClosedCaption2](iwmpclosedcaption2--vb-and-c.md)         | Fornece métodos e propriedades de legendas fechadas adicionais.                                                                                                     |
| [Iwmpcontrols](iwmpcontrols--vb-and-c.md)                     | Representa os controles de transporte Windows Media Player, como Reproduzir, Parar e Pausar.                                                                         |
| [IWMPControls2](iwmpcontrols2--vb-and-c.md)                   | Fornece um método de controle adicional para congelar a reprodução no quadro seguinte ou anterior.                                                                           |
| [IWMPControls3](iwmpcontrols3--vb-and-c.md)                   | Fornece propriedades de controle e métodos adicionais para seleção e suporte de idioma de áudio.                                                                      |
| [IWMPDVD](iwmpdvd--vb-and-c.md)                               | Fornece propriedades e métodos para trabalhar com DVDs.                                                                                                            |
| [IWMPError](iwmperror--vb-and-c.md)                           | Acessa uma coleção de interfaces [IWMPErrorItem](iwmperroritem--vb-and-c.md) para recuperar informações de erro.                                                |
| [IWMPErrorItem](iwmperroritem--vb-and-c.md)                   | Fornece acesso a informações de erro.                                                                                                                             |
| [IWMPErrorItem2](iwmperroritem2--vb-and-c.md)                 | Fornece uma propriedade de item de erro adicional para obter um código de condição de erro.                                                                                   |
| **IWMPFolderMonitorServices**                                  | Não há suporte para programação .NET.                                                                                                                               |
| [IWMPLibrary](iwmplibrary--vb-and-c.md)                       | Representa uma biblioteca.                                                                                                                                             |
| [IWMPLibraryServices](iwmplibraryservices--vb-and-c.md)       | Fornece métodos para enumerar bibliotecas.                                                                                                                          |
| **IWMPLibrarySharingServices**                                 | Não há suporte para programação .NET.                                                                                                                               |
| [Iwmpmedia](iwmpmedia--vb-and-c.md)                           | Fornece uma maneira de definir e recuperar as propriedades de um item de mídia.                                                                                                |
| [IWMPMedia2](iwmpmedia2--vb-and-c.md)                         | Fornece acesso a uma propriedade de item de mídia adicional.                                                                                                             |
| [IWMPMedia3](iwmpmedia3--vb-and-c.md)                         | Fornece métodos adicionais para acessar as propriedades de um item de mídia.                                                                                             |
| [IWMPMediaCollection](iwmpmediacollection--vb-and-c.md)       | Fornece métodos que podem ser usados para organizar uma grande coleção de itens de mídia.                                                                                  |
| [IWMPMediaCollection2](iwmpmediacollection2--vb-and-c.md)     | Fornece métodos que complementam a interface **IWMPMediaCollection.**                                                                                           |
| [IWMPMetadataPicture](iwmpmetadatapicture--vb-and-c.md)       | Fornece propriedades para obter informações sobre a imagem contida em um arquivo de mídia digital representado por um atributo de metadados **WM/Picture.**         |
| [IWMPMetadataText](iwmpmetadatatext--vb-and-c.md)             | Fornece propriedades para obter informações sobre atributos de metadados textuais complexos.                                                                            |
| [IWMPNetwork](iwmpnetwork--vb-and-c.md)                       | Fornece propriedades e métodos para acessar estatísticas relacionadas à qualidade de uma conexão de rede e para especificar e recuperar as configurações de proxy de rede.     |
| **IWMPPlayerApplication**                                      | Não há suporte para programação .NET.                                                                                                                               |
| **IWMPPlayerServices**                                         | Não há suporte para programação .NET.                                                                                                                               |
| **IWMPPlayerServices2**                                        | Não há suporte para programação .NET.                                                                                                                               |
| [IWMPPlaylist](iwmpplaylist--vb-and-c.md)                     | Fornece propriedades e métodos para organizar, gerenciar e manipular itens de mídia em uma playlist.                                                                    |
| [IWMPPlaylistArray](iwmpplaylistarray--vb-and-c.md)           | Acessa uma coleção de interfaces [IWMPPlaylist](iwmpplaylist--vb-and-c.md) por número de índice.                                                                   |
| [IWMPPlaylistCollection](iwmpplaylistcollection--vb-and-c.md) | Fornece métodos para manipular interfaces [IWMPPlaylist](iwmpplaylist--vb-and-c.md) e [IWMPPlaylistArray](iwmpplaylistarray--vb-and-c.md) em uma coleção. |
| [IWMPQuery](iwmpquery--vb-and-c.md)                           | Representa uma consulta composta.                                                                                                                                      |
| [IWMPSettings](iwmpsettings--vb-and-c.md)                     | Fornece propriedades e métodos que obterão ou definirão os valores de Windows Media Player configurações.                                                                      |
| [IWMPSettings2](iwmpsettings2--vb-and-c.md)                   | Fornece propriedades e um método que complementam a interface **IWMPSettings.**                                                                                  |
| [IWMPStringCollection](iwmpstringcollection--vb-and-c.md)     | Fornece uma propriedade e um método para acessar uma coleção de cadeias de caracteres por número de índice.                                                                           |
| [IWMPStringCollection2](iwmpstringcollection2--vb-and-c.md)   | Fornece métodos que complementam a interface **IWMPStringCollection.**                                                                                          |
| **IWMPSyncDevice**                                             | Não há suporte para programação .NET.                                                                                                                               |
| **IWMPSyncDevice2**                                            | Não há suporte para programação .NET.                                                                                                                               |
| **IWMPSyncServices**                                           | Não há suporte para programação .NET.                                                                                                                               |



 

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Referência de modelo de objeto para Visual Basic .NET e C #**](object-model-reference-for-visual-basic--net-and-c.md)
</dt> </dl>

 

 




