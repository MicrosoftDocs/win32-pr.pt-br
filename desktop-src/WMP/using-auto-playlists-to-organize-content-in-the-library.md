---
title: Usando listas de reprodução automáticas para organizar o conteúdo na biblioteca
description: Usando listas de reprodução automáticas para organizar o conteúdo na biblioteca
ms.assetid: 118d4357-044f-4986-af51-0c344470e891
keywords:
- Windows Media Player lojas online, listas de reprodução automáticas
- lojas online, listas de reprodução automáticas
- Digite 1 lojas online, listas de reprodução automáticas
- tipo 2 lojas online, listas de reprodução automáticas
- Windows Media Player lojas online, organizando o conteúdo da biblioteca
- lojas online, organizando o conteúdo da biblioteca
- Digite 1 lojas online, organizando o conteúdo da biblioteca
- Digite 2 lojas online, organizando o conteúdo da biblioteca
- Windows Media Player lojas online, organização de conteúdo de biblioteca
- lojas online, organização de conteúdo de biblioteca
- Digite 1 lojas online, organização de conteúdo de biblioteca
- Digite 2 lojas online, organização de conteúdo de biblioteca
- biblioteca, organizando conteúdo
- organizando o conteúdo da biblioteca
- playlists automáticas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c0e32d0f95093d9550c71643330267d59a57f56db7e0d666274a492ac29b2c58
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119507166"
---
# <a name="using-auto-playlists-to-organize-content-in-the-library"></a>Usando listas de reprodução automáticas para organizar o conteúdo na biblioteca

Você pode usar listas de reprodução automáticas para organizar o conteúdo premium fornecido por você. por exemplo, você pode usar Windows Media Player para criar uma lista de reprodução automática que contém apenas o conteúdo que você forneceu tendo uma classificação de usuário de pelo menos quatro estrelas. em seguida, você pode adicionar a lista de reprodução automática à biblioteca no Windows Media Player para que ela seja exibida no nó músicas adquiridas no nó distribuidor de conteúdo.

Para fazer isso, execute estas etapas:

1.  Crie a lista de reprodução automática.
2.  usando o Windows Explorer, navegue até a lista de reprodução automática e recupere o arquivo. wpl.
3.  usando o modelo de objeto Windows Media Player, adicione a lista de reprodução automática à biblioteca.
4.  Defina o atributo **WM/ContentDistributor** da lista de reprodução para o nome da chave do distribuidor de conteúdo.
5.  Defina o atributo **SyncOnly** para a lista de reprodução como true.

o código de exemplo a seguir JScript mostra uma função que adiciona uma lista de reprodução automática chamada "visitas favoritas" ao nó da proseware na biblioteca:


```C++
function AddWPL()
{
    var pl = Player.mediaCollection.add("c:\\media\\Favorite Hits.wpl");
    pl.setItemInfo("WM/ContentDistributor", "Proseware");
    pl.setItemInfo("SyncOnly", true);
}
```



## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Sobre a integração de biblioteca](download-manager-overview.md)
</dt> <dt>

[**Informações comuns às lojas online tipo 1 e tipo 2**](information-common-to-type-1-and-type-2-online-stores.md)
</dt> <dt>

[**Mediacollection. adicionar**](mediacollection-add.md)
</dt> <dt>

[**Playlist. setItemInfo**](playlist-setiteminfo.md)
</dt> <dt>

[**Listas de reprodução estáticas e automáticas**](static-and-auto-playlists.md)
</dt> <dt>

[**Atributo SyncOnly**](synconly-attribute.md)
</dt> <dt>

[**Atributo WM/ContentDistributor**](wm-contentdistributor-attribute.md)
</dt> <dt>

[**Trabalhando com a biblioteca**](working-with-the-library.md)
</dt> </dl>

 

 




