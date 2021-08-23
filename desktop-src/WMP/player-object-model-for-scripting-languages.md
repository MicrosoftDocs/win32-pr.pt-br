---
title: Modelo de objeto do player para linguagens de script
description: Modelo de objeto do player para linguagens de script
ms.assetid: 785c1a3a-902a-4f30-8419-bbfb11b584a3
keywords:
- Windows Media Player,modelo de objeto
- Windows Media Player modelo de objeto,sobre
- modelo de objeto, sobre
- Windows Media Player ActiveX controle,modelo de objeto
- ActiveX controle,modelo de objeto
- Windows Media Player Controle ActiveX dispositivo móvel, modelo de objeto
- Windows Media Player Móvel, modelo de objeto
- software development kit (SDK), Windows Media Player ActiveX de objeto de controle
- SDK (software development kit), Windows Media Player ActiveX de objeto de controle
- documentation,Windows Media Player ActiveX de objeto de controle
- Windows Media Player, linguagens de script
- Windows Media Player de objeto, linguagens de script
- modelo de objeto, linguagens de script
- Windows Media Player ActiveX controle, linguagens de script
- ActiveX controle, linguagens de script
- Windows Media Player Controle ActiveX dispositivos móveis, linguagens de script
- Windows Media Player Mobile, linguagens de script
- linguagens de script
- Windows Media Player, objeto Player
- Windows Media Player de objeto, objeto Player
- modelo de objeto, objeto Player
- Windows Media Player ActiveX controle, objeto Player
- ActiveX controle, objeto Player
- Windows Media Player Controle de ActiveX móvel, objeto Player
- Windows Media Player Móvel, objeto Player
- Objeto player
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bffe34bfc227dfe250a9c9d7ebb60977a9ab079c4a062067c65e83e62f0e5976
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118996017"
---
# <a name="player-object-model-for-scripting-languages"></a>Modelo de objeto do player para linguagens de script

ActiveX usa o conceito de objetos para conter a funcionalidade de programação. Windows Media Player usa vários objetos para dividir a funcionalidade que o controle fornece. O objeto raiz é o **objeto Player** e os outros objetos são anexados ao **objeto Player** por meio de propriedades específicas.

O diagrama a seguir mostra como o Windows Media Player 11 ActiveX de objeto de controle funciona para linguagens de script.

![diagrama do modelo de objeto do Windows Media Player 11](images/playeromdiag.png)

No C++, e às vezes em linguagens .NET, os objetos são representados por interfaces COM. No modelo Windows Media Player objeto, os nomes de interface COM são os mesmos que o nome do objeto, mas são prefixados com "IWMP". Por exemplo, o **objeto Network** é exposto por meio da interface **IWMPNetwork.**

As seções a seguir fornecem visão geral conceitual para cada objeto:

-   [Sobre os objetos Cdrom e CdromCollection](about-the-cdrom-and-cdromcollection-objects.md)
-   [Sobre o objeto ClosedCaption](about-the-closedcaption-object.md)
-   [Sobre o objeto Controls](about-the-controls-object.md)
-   [Sobre o objeto DVD](about-the-dvd-object.md)
-   [Sobre os objetos Error e ErrorItem](about-the-error-and-erroritem-objects.md)
-   [Sobre os objetos MediaCollection e Media](about-the-mediacollection-and-media-objects.md)
-   [Sobre o objeto MetadataPicture](about-the-metadatapicture-object.md)
-   [Sobre o objeto MetadataText](about-the-metadatatext-object.md)
-   [Sobre o objeto de rede](about-the-network-object.md)
-   [Sobre o objeto player](about-the-player-object.md)
-   [Sobre o objeto PlayerApplication](about-the-playerapplication-object.md)
-   [Sobre os objetos Playlist, PlaylistCollection e PlaylistArray](about-the-playlist--playlistcollection--and-playlistarray-objects.md)
-   [Sobre o objeto de consulta](about-the-query-object.md)
-   [Sobre o Configurações objeto](about-the-settings-object.md)
-   [Sobre o objeto StringCollection](about-the-stringcollection-object.md)

A funcionalidade adicional está disponível por meio de determinadas interfaces COM. Se você pode acessar essas interfaces pode depender da linguagem usada para programação e outros fatores, como o modo usado para criar a instância do Windows Media Player controle. Para ver uma lista completa das interfaces COM expostas pelo controle Windows Media Player, consulte a Referência [de modelo de objeto para C++.](object-model-reference-for-c.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Sobre o modelo de objeto do player**](about-the-player-object-model.md)
</dt> <dt>

[**Usando o Windows Media Player controle em uma solução .NET Framework aplicativo**](using-the-windows-media-player-control-in-a--net-framework-solution.md)
</dt> </dl>

 

 




