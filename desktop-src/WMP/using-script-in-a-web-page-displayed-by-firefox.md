---
title: Usando script em uma página da Web exibida pelo Firefox
description: Usando script em uma página da Web exibida pelo Firefox
ms.assetid: 0f1d21b1-1824-4ba9-9c0e-bd23ba847d9d
keywords:
- Windows Media Player, incorporando ActiveX controle
- Windows Media Player modelo de objeto, incorporando ActiveX controle
- modelo de objeto, incorporando ActiveX controle
- Windows Media Player Mobile, incorporando ActiveX controle
- Windows Media Player ActiveX controle,incorporação
- Windows Media Player Controle ActiveX dispositivo móvel, incorporação
- ActiveX controle,incorporação
- Windows Media Player ActiveX, páginas da Web
- Windows Media Player Controle de ActiveX móvel, páginas da Web
- ActiveX, páginas da Web
- Windows Media Player ActiveX controle, exemplo de script
- Windows Media Player Controle de ActiveX móvel, exemplo de script
- ActiveX controle, exemplo de script
- incorporação, páginas da Web
- Incorporação de página da Web, exemplo de script
- Windows Media Player, Firefox
- Windows Media Player modelo de objeto, Firefox
- modelo de objeto, Firefox
- Windows Media Player Mobile, Firefox
- Windows Media Player ActiveX controle, Firefox
- Windows Media Player Controle de ActiveX móvel, Firefox
- ActiveX controle,Firefox
- Firefox, exemplo de script
- Incorporação de página da Web, Firefox
- exemplo de script para a incorporação de página da Web
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 450b03f7adefca1a887fb31207f0a3280e1925c9d3e1f1066df370d87f0a7779
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119762056"
---
# <a name="using-script-in-a-web-page-displayed-by-firefox"></a>Usando script em uma página da Web exibida pelo Firefox

O script em uma página da Web pode usar o modelo de objeto Player para controlar o Player conforme o usuário interage com a página. Por exemplo, o elemento INPUT a seguir tem um script que define o volume do Player.


```HTML
<INPUT type="button" value="Vol" OnClick="ChangeVolume()"/>
 
<SCRIPT>
  function ChangeVolume()
  {
    Player.settings.volume = 90;
  }
</SCRIPT>

```



Muitos dos objetos no modelo Windows Media Player objeto são suportados pelo Internet Explorer e pelo plug-in firefox. No entanto, há alguns objetos que não são suportados pelo plug-in firefox. A tabela a seguir lista todos os objetos no modelo de objeto Player e mostra quais objetos têm suporte pelo plug-in firefox.



| Objeto                                              | Suporte do Firefox |
|-----------------------------------------------------|-----------------|
| [Cdrom](cdrom-object.md)                           | não              |
| [CdromCollection](cdromcollection-object.md)       | não              |
| [ClosedCaption](closedcaption-object.md)           | sim             |
| [Controles](controls-object.md)                     | não              |
| [Dvd](dvd-object.md)                               | não              |
| [Erro](error-object.md)                           | sim             |
| [Erroritem](erroritem-object.md)                   | sim             |
| [Mídia](media-object.md)                           | sim             |
| [MediaCollection](mediacollection-object.md)       | não              |
| [MetadataPicture](metadatapicture-object.md)       | não              |
| [MetadataText](metadatatext-object.md)             | não              |
| [Rede](network-object.md)                       | sim             |
| [Jogador](player-object.md)                         | sim             |
| [PlayerApplication](playerapplication-object.md)   | não              |
| [Playlist](playlist-object.md)                     | sim             |
| [PlaylistArray](playlistarray-object.md)           | não              |
| [PlaylistCollection](playlistcollection-object.md) | não              |
| [Consulta](query-object.md)                           | não              |
| [Configurações](settings-object.md)                     | sim             |
| [StringCollection](stringcollection-object.md)     | não              |



 

O plug-in firefox dá suporte ao **objeto Player,** mas determinadas propriedades do **objeto Player** **retornam NULL** em um navegador Firefox. Por exemplo, a [propriedade cdromCollection](player-cdromcollection.md) do objeto **Player** retorna **NULL** porque o plug-in firefox não dá suporte ao **objeto Cdrom.** Da mesma forma, as propriedades [dvd](player-dvd.md), [mediaCollection](player-mediacollection.md), [playerApplication](player-playerapplication.md)e [playlistCollection](player-playlistcollection.md) do objeto **Player** **retornam NULL** em um navegador Firefox.

A **propriedade Player.pluginVersionInfo** é suportada pelo plug-in firefox, mas não por Internet Explorer. Essa propriedade retorna a versão do plug-in firefox.

O plug-in firefox dá suporte **ao objeto Media,** incluindo a [propriedade getItemInfoByType.](media-getiteminfobytype.md) No entanto, em um navegador Firefox, a **propriedade getItemInfoByType** não dá suporte aos tipos de retorno **MetadataText** e **MetadataPicture.**

O plug-in firefox dá suporte [ao objeto Configurações,](settings-object.md) exceto pelo método [setMode](settings-setmode.md) e pela [propriedade requestMediaAccessRights.](settings-requestmediaaccessrights.md) Em um navegador Firefox, a **propriedade requestMediaAccessRight** sempre retorna false.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Usando o controle Windows Media Player com Firefox**](using-the-windows-media-player-control-with-firefox.md)
</dt> </dl>

 

 




