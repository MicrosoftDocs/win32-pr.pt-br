---
title: Listas de reprodução estáticas e automáticas
description: Listas de reprodução estáticas e automáticas
ms.assetid: 708c236e-8f3c-4188-aefb-eda7da598944
keywords:
- Windows Media Player, listas de reprodução
- Modelo de objeto do Windows Media Player, listas de reprodução
- modelo de objeto, listas de reprodução
- Windows Media Player Mobile, listas de reprodução
- Controle ActiveX do Windows Media Player, listas de reprodução
- Controle ActiveX móvel do Windows Media Player, listas de reprodução
- Controle ActiveX, listas de reprodução
- listas de reprodução, estáticas
- listas de reprodução de metarquivo, estáticos
- Playlists do metarquivo do Windows Media, estáticos
- listas de reprodução estáticas
- playlists automáticas
- listas de reprodução, automática
- listas de reprodução de metarquivo, automática
- Playlists do metarquivo do Windows Media, automática
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 083ee2029eec2cfee7510766790f4ca7eb6468e5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104363745"
---
# <a name="static-and-auto-playlists"></a>Listas de reprodução estáticas e automáticas

Há dois tipos de listas de reprodução:

-   Listas de reprodução estáticas, que incluem itens de mídia específicos
-   Listas de reprodução automáticas, que pesquisam a biblioteca toda vez que são abertas e podem conter itens de mídia diferentes em momentos diferentes. Uma lista de reprodução automática é o resultado de uma consulta de banco de dados.

Para importar uma lista de reprodução estática de um metarquivo, primeiro chame *Player*. **newPlaylist** para criar um objeto de **lista de reprodução** com base nos dados no metarquivo e, em seguida, passar esse objeto para *playlistcollection*. **importPlaylist** para adicionar a lista de reprodução à biblioteca.

Para importar uma lista de reprodução automática de um metarquivo, use *mediacollection*. **Adicionar**. Para obter mais informações, consulte [playlists e o objeto mediacollection](playlists-and-the-mediacollection-object.md).

Para importar uma lista de reprodução estática de um metarquivo de playlist automática, use o *Player*. **newPlaylist** e *playlistcollection*. **importPlaylist** conforme descrito anteriormente. A lista de reprodução automática será executada uma vez e uma lista de reprodução estática será criada com base no resultado dessa execução.

O uso de uma lista de reprodução automática para consultar a biblioteca do usuário não tem suporte para páginas da Web que os usuários acessam pela Internet.

O código de exemplo C# a seguir demonstra a importação de um metarquivo de playlist automática como uma lista de reprodução estática. Para executar este exemplo, crie uma lista de reprodução automática usando a interface do usuário da biblioteca e, em seguida, inclua o caminho correto para o metarquivo de playlist automática neste código.


```C++
private void addStaticPlaylist()
{
    IWMPPlaylist pList;

    pList = Player.newPlaylist("NewImportedList", "\\\\myServer\\myPath\\artistcollection.wpl");
    if (pList.count == 0)
        MessageBox.Show("The specified playlist is empty.");
    else
        Player.playlistCollection.importPlaylist(pList);
}

```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Gerenciando listas de reprodução**](managing-playlists.md)
</dt> </dl>

 

 




