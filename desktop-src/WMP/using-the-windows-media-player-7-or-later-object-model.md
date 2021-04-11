---
title: Usando o modelo de objeto do Windows Media Player 7 ou posterior
description: Usando o modelo de objeto do Windows Media Player 7 ou posterior
ms.assetid: e2dbe2c1-23be-499b-b754-b7e87486ecd6
keywords:
- Windows Media Player, modelo de objeto
- Modelo de objeto do Windows Media Player, versão 7 ou posterior
- modelo de objeto, versão 7 ou posterior
- Controle ActiveX do Windows Media Player, versão 7 ou posterior
- Controle ActiveX, versão 7 ou posterior
- Controle ActiveX móvel do Windows Media Player, versão 7 ou posterior
- Windows Media Player Mobile, modelo de objeto
- Guia de migração, versão 7 ou posterior
- versões do Windows Media Player, modelo de objeto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8eb4d3d09b38e381d0cddeb25ee7cb5d7de3cb2b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292366"
---
# <a name="using-the-windows-media-player-7-or-later-object-model"></a>Usando o modelo de objeto do Windows Media Player 7 ou posterior

A maioria das tarefas que você pode ter realizado usando o modelo de objeto de controle ActiveX do Windows Media Player 6,4 exigirá uma nova abordagem. Em muitos casos, os nomes das propriedades, métodos e eventos foram alterados no modelo de objeto do Windows Media Player 7 ou posterior. Por exemplo, para especificar o caminho do arquivo no modelo de objeto da versão 6,4, defina a propriedade **Player6. FileName** :


```C++
WMP64.FileName = "https://www.microsoft.com/somefile.wmv";

```



Ao usar o modelo de objeto do Windows Media Player 7 ou posterior, você deve definir a propriedade **Player. URL** :


```C++
WMP9.URL = "https://www.microsoft.com/somefile.wmv";

```



Como alternativa, usando o modelo de 10 objetos, você pode obter um objeto de **mídia** da biblioteca e, em seguida, definir a propriedade **Player. currentMedia** :


```C++
// Get the first media object in the media collection.
var MyMediaItem = WMP9.mediaCollection.getAll().item(0)

// Make the MyMediaItem object the current media.
WMP9.currentMedia = MyMediaItem;

```



Grande parte da funcionalidade no modelo de objeto do Windows Media Player 7 ou posterior é acessada por meio da hierarquia de objetos. Como mostrado no exemplo anterior, você pode obter um objeto de **playlist** usando o método **getAll** do objeto **mediacollection** , que é acessado por meio do objeto do **Player** raiz. Em seguida, você pode obter um objeto de **mídia** específico do objeto **playlist** usando o método **Item** do objeto **playlist** . Há cinco métodos adicionais acessíveis por meio do objeto **mediacollection** que retornam um objeto **playlist** ; cada método permite que você recupere o objeto com base em critérios específicos, como gênero ou álbum.

A estrutura hierárquica do modelo de objeto de controle ActiveX do Windows Media Player 7 ou posterior fornece uma abordagem mais lógica para organizar as propriedades, os métodos e os eventos disponíveis para seu uso. Toda a funcionalidade para os controles do jogador está contida no objeto **Controls** , toda a funcionalidade da conexão de rede do player está contida no objeto **Network** e assim por diante. Por exemplo, para iniciar a reprodução de conteúdo usando o modelo de objeto da versão 6,4, use o método **Player6. Play** :


```C++
WMP64.Play();

```



Ao usar o modelo de objeto do Windows Media Player 7 ou posterior, você deve acessar o método **Play** usando o objeto **Controls** :


```C++
WMP9.controls.play();

```



No entanto, a profundidade do modelo de objeto pode levar a instruções de script muito longas:


```C++
WMP9.currentPlaylist.appendItem(WMP9.mediaCollection.getByName("MySong").item(0));

```



Instruções como a anterior podem se tornar muito mais simples e legíveis ao trabalhar com objetos nomeados individuais. O exemplo a seguir substitui a instrução de código anterior pela sintaxe usando variáveis de objeto separadas:


```C++
// Store the current playlist object.
var pl = WMP9.currentPlaylist;

// Get a playlist from the media collection that contains
// one media item named "MySong".
var temp = WMP9.mediaCollection.getByName("MySong");

// Get the individual media item from the temp playlist.
var song = temp.item(0);

// Append the media item to the current playlist.
pl.appendItem(song);

```



Esse estilo de codificação requer mais linhas de script, mas é muito mais fácil de seguir, especialmente com os comentários adicionados. Há outra vantagem: o objeto **currentPlaylist** é fácil de ser reutilizado porque é armazenado na variável pl.

Muitas das propriedades, métodos e eventos no modelo de objeto do Windows Media Player 7 ou posterior definem ou recuperam valores diferentes ou retornam valores de um tipo ou número diferente, em comparação com a funcionalidade correspondente no modelo de objeto da versão 6,4. Por exemplo, quando **Player6. OpenState** recupera 2, esse valor corresponde à constante de Visual Basic **nsLoadingNSC**, o que significa que o player está carregando um arquivo de estação com uma extensão de nome de arquivo. NSC. Mas quando a propriedade de modelo de objeto do Windows Media Player 7 ou posterior **. OpenState** recupera 2, esse valor corresponde ao estado PlaylistLocating, o que significa que o Windows Media Player está tentando localizar uma lista de reprodução. Além disso, a propriedade **Player6. OpenState** pode recuperar sete valores diferentes, enquanto a propriedade **Player. OpenState** do Windows Media Player 7 ou posterior pode recuperar 22 valores diferentes. Certifique-se de consultar a seção referência de modelo de objeto para script do SDK do Windows Media Player ao revisar o código para usar uma versão de modelo de objeto diferente.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Sobre o modelo de objeto do Player**](about-the-player-object-model.md)
</dt> <dt>

[**Referência de modelo de objeto para scripts**](object-model-reference-for-scripting.md)
</dt> <dt>

[**Guia de migração do modelo de objeto**](object-model-migration-guide.md)
</dt> </dl>

 

 




