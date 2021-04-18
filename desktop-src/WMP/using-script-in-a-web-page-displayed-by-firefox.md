---
title: Usando o script em uma página da Web exibida pelo Firefox
description: Usando o script em uma página da Web exibida pelo Firefox
ms.assetid: 0f1d21b1-1824-4ba9-9c0e-bd23ba847d9d
keywords:
- Windows Media Player, incorporando controle ActiveX
- Modelo de objeto do Windows Media Player, inserindo controle ActiveX
- modelo de objeto, inserindo controle ActiveX
- Windows Media Player Mobile, inserindo controle ActiveX
- Controle ActiveX do Windows Media Player, incorporando
- Controle ActiveX móvel do Windows Media Player, incorporando
- Controle ActiveX, incorporando
- Controle ActiveX do Windows Media Player, páginas da Web
- Controle ActiveX móvel do Windows Media Player, páginas da Web
- Controle ActiveX, páginas da Web
- Controle ActiveX do Windows Media Player, exemplo de script
- Controle ActiveX móvel do Windows Media Player, exemplo de script
- Controle ActiveX, exemplo de script
- inserindo, páginas da Web
- Inserção de página da Web, exemplo de script
- Windows Media Player, Firefox
- Modelo de objeto do Windows Media Player, Firefox
- modelo de objeto, Firefox
- Windows Media Player Mobile, Firefox
- Controle ActiveX do Windows Media Player, Firefox
- Controle ActiveX móvel do Windows Media Player, Firefox
- Controle ActiveX, Firefox
- Firefox, exemplo de script
- Incorporação de página da Web, Firefox
- exemplo de script para inserção de página da Web
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8629f87f954d12602999f76483fdd36ab279290
ms.sourcegitcommit: e22adfb0dd3bb989e59455baedb4d905a877a240
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/21/2019
ms.locfileid: "105771522"
---
# <a name="using-script-in-a-web-page-displayed-by-firefox"></a>Usando o script em uma página da Web exibida pelo Firefox

O script em uma página da Web pode usar o modelo de objeto do Player para controlar o Player à medida que o usuário interage com a página. Por exemplo, o elemento INPUT a seguir tem um script que define o volume do Player.


```HTML
<INPUT type="button" value="Vol" OnClick="ChangeVolume()"/>
 
<SCRIPT>
  function ChangeVolume()
  {
    Player.settings.volume = 90;
  }
</SCRIPT>

```



Muitos dos objetos no modelo de objeto do Windows Media Player têm suporte do Internet Explorer e do plug-in do Firefox. No entanto, há alguns objetos que não têm suporte do plug-in do Firefox. A tabela a seguir lista todos os objetos no modelo de objeto do Player e mostra quais objetos têm suporte no plug-in do Firefox.



| Objeto                                              | Suporte do Firefox |
|-----------------------------------------------------|-----------------|
| [ROMs](cdrom-object.md)                           | não              |
| [CdromCollection](cdromcollection-object.md)       | não              |
| [ClosedCaption](closedcaption-object.md)           | sim             |
| [Controles](controls-object.md)                     | não              |
| [DVD](dvd-object.md)                               | não              |
| [Erro](error-object.md)                           | sim             |
| [ErrorItem](erroritem-object.md)                   | sim             |
| [Mídia](media-object.md)                           | sim             |
| [Mediacollection](mediacollection-object.md)       | não              |
| [MetadataPicture](metadatapicture-object.md)       | não              |
| [MetadataText](metadatatext-object.md)             | não              |
| [Rede](network-object.md)                       | sim             |
| [Jogador](player-object.md)                         | sim             |
| [PlayerApplication](playerapplication-object.md)   | não              |
| [7.1](playlist-object.md)                     | sim             |
| [PlaylistArray](playlistarray-object.md)           | não              |
| [Playlistcollection](playlistcollection-object.md) | não              |
| [Consulta](query-object.md)                           | não              |
| [Configurações](settings-object.md)                     | sim             |
| [StringCollection](stringcollection-object.md)     | não              |



 

O plug-in do Firefox dá suporte ao objeto **Player** , mas determinadas propriedades do objeto **Player** retornam **NULL** em um navegador Firefox. Por exemplo, a propriedade [cdromCollection](player-cdromcollection.md) do objeto **Player** retorna **NULL** porque o plug-in do Firefox não oferece suporte ao objeto **cdrom** . Da mesma forma, as propriedades [DVD](player-dvd.md), [mediacollection](player-mediacollection.md), [playerApplication](player-playerapplication.md)e [playlistcollection](player-playlistcollection.md) do objeto **Player** retornam **NULL** em um navegador Firefox.

A propriedade **Player. pluginVersionInfo** é suportada pelo plug-in do Firefox, mas não pelo Internet Explorer. Essa propriedade retorna a versão do plug-in do Firefox.

O plug-in do Firefox dá suporte ao objeto de **mídia** , incluindo a propriedade [getItemInfoByType](media-getiteminfobytype.md) . No entanto, em um navegador Firefox, a propriedade **getItemInfoByType** não dá suporte aos tipos de retorno **MetadataText** e **MetadataPicture** .

O plug-in do Firefox dá suporte ao objeto de [configurações](settings-object.md) , exceto para o método [setmode](settings-setmode.md) e a propriedade [requestMediaAccessRights](settings-requestmediaaccessrights.md) . Em um navegador Firefox, a propriedade **requestMediaAccessRight** sempre retorna false.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Usando o controle do Windows Media Player com o Firefox**](using-the-windows-media-player-control-with-firefox.md)
</dt> </dl>

 

 




