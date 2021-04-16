---
title: Modelo de objeto do Player para linguagens de script
description: Modelo de objeto do Player para linguagens de script
ms.assetid: 785c1a3a-902a-4f30-8419-bbfb11b584a3
keywords:
- Windows Media Player, modelo de objeto
- Modelo de objeto do Windows Media Player, sobre
- modelo de objeto, sobre
- Controle ActiveX do Windows Media Player, modelo de objeto
- Controle ActiveX, modelo de objeto
- Controle ActiveX móvel do Windows Media Player, modelo de objeto
- Windows Media Player Mobile, modelo de objeto
- Software Development Kit (SDK), modelo de objeto de controle ActiveX do Windows Media Player
- SDK (Software Development Kit), modelo de objeto de controle ActiveX do Windows Media Player
- documentação, modelo de objeto de controle ActiveX do Windows Media Player
- Windows Media Player, linguagens de script
- Modelo de objeto do Windows Media Player, linguagens de script
- modelo de objeto, linguagens de script
- Controle ActiveX do Windows Media Player, linguagens de script
- Controle ActiveX, linguagens de script
- Controle ActiveX móvel do Windows Media Player, linguagens de script
- Windows Media Player Mobile, linguagens de script
- linguagens de script
- Windows Media Player, objeto Player
- Modelo de objeto do Windows Media Player, objeto Player
- modelo de objeto, objeto Player
- Controle ActiveX do Windows Media Player, objeto Player
- Controle ActiveX, objeto Player
- Controle ActiveX móvel do Windows Media Player, objeto Player
- Windows Media Player Mobile, objeto Player
- Objeto de jogador
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 670bff03075fd98812dbee269115e297a137e92d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104559831"
---
# <a name="player-object-model-for-scripting-languages"></a>Modelo de objeto do Player para linguagens de script

O ActiveX usa o conceito de objetos para conter funcionalidade de programação. O Windows Media Player usa vários objetos para dividir a funcionalidade que o controle fornece. O objeto raiz é o objeto de **jogador** e os outros objetos são anexados ao objeto **Player** por meio de propriedades específicas.

O diagrama a seguir mostra como o modelo de objeto de controle ActiveX do Windows Media Player 11 funciona para linguagens de script.

![diagrama do modelo de objeto do Windows Media Player 11](images/playeromdiag.png)

Em C++ e, às vezes, em linguagens .NET, os objetos são representados por interfaces COM. No modelo de objeto do Windows Media Player, os nomes de interface COM são iguais ao nome do objeto, mas são prefixados com "IWMP". Por exemplo, o objeto de **rede** é exposto por meio da interface **IWMPNetwork** .

As seções a seguir fornecem visões gerais conceituais para cada objeto:

-   [Sobre os objetos cdrom e cdromCollection](about-the-cdrom-and-cdromcollection-objects.md)
-   [Sobre o objeto ClosedCaption](about-the-closedcaption-object.md)
-   [Sobre o objeto Controls](about-the-controls-object.md)
-   [Sobre o objeto DVD](about-the-dvd-object.md)
-   [Sobre os objetos Error e ErrorItem](about-the-error-and-erroritem-objects.md)
-   [Sobre o Mediacollection e os objetos de mídia](about-the-mediacollection-and-media-objects.md)
-   [Sobre o objeto MetadataPicture](about-the-metadatapicture-object.md)
-   [Sobre o objeto MetadataText](about-the-metadatatext-object.md)
-   [Sobre o objeto de rede](about-the-network-object.md)
-   [Sobre o objeto do Player](about-the-player-object.md)
-   [Sobre o objeto PlayerApplication](about-the-playerapplication-object.md)
-   [Sobre os objetos playlist, Playlistcollection e PlaylistArray](about-the-playlist--playlistcollection--and-playlistarray-objects.md)
-   [Sobre o objeto de consulta](about-the-query-object.md)
-   [Sobre o objeto de configurações](about-the-settings-object.md)
-   [Sobre o objeto StringCollection](about-the-stringcollection-object.md)

A funcionalidade adicional está disponível por meio de determinadas interfaces COM. Se você pode acessar essas interfaces pode depender do idioma usado para a programação e outros fatores, como o modo usado para criar a instância do controle do Windows Media Player. Para obter uma lista completa de interfaces COM expostas pelo controle do Windows Media Player, consulte a [referência de modelo de objeto para C++](object-model-reference-for-c.md).

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Sobre o modelo de objeto do Player**](about-the-player-object-model.md)
</dt> <dt>

[**Usando o controle do Windows Media Player em uma solução de .NET Framework**](using-the-windows-media-player-control-in-a--net-framework-solution.md)
</dt> </dl>

 

 




