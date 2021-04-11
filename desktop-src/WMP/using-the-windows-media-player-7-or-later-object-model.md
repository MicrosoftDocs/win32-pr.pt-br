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
# <a name="using-the-windows-media-player-7-or-later-object-model"></a><span data-ttu-id="12b35-112">Usando o modelo de objeto do Windows Media Player 7 ou posterior</span><span class="sxs-lookup"><span data-stu-id="12b35-112">Using the Windows Media Player 7 or Later Object Model</span></span>

<span data-ttu-id="12b35-113">A maioria das tarefas que você pode ter realizado usando o modelo de objeto de controle ActiveX do Windows Media Player 6,4 exigirá uma nova abordagem.</span><span class="sxs-lookup"><span data-stu-id="12b35-113">Most of the tasks you may have been performing using the Windows Media Player 6.4 ActiveX control object model will require a new approach.</span></span> <span data-ttu-id="12b35-114">Em muitos casos, os nomes das propriedades, métodos e eventos foram alterados no modelo de objeto do Windows Media Player 7 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="12b35-114">In many cases, the names of the properties, methods, and events have changed in the Windows Media Player 7 or later object model.</span></span> <span data-ttu-id="12b35-115">Por exemplo, para especificar o caminho do arquivo no modelo de objeto da versão 6,4, defina a propriedade **Player6. FileName** :</span><span class="sxs-lookup"><span data-stu-id="12b35-115">For instance, to specify the file path in the version 6.4 object model, you set the **Player6.FileName** property:</span></span>


```C++
WMP64.FileName = "https://www.microsoft.com/somefile.wmv";

```



<span data-ttu-id="12b35-116">Ao usar o modelo de objeto do Windows Media Player 7 ou posterior, você deve definir a propriedade **Player. URL** :</span><span class="sxs-lookup"><span data-stu-id="12b35-116">When using the Windows Media Player 7 or later object model, you must set the **Player.URL** property:</span></span>


```C++
WMP9.URL = "https://www.microsoft.com/somefile.wmv";

```



<span data-ttu-id="12b35-117">Como alternativa, usando o modelo de 10 objetos, você pode obter um objeto de **mídia** da biblioteca e, em seguida, definir a propriedade **Player. currentMedia** :</span><span class="sxs-lookup"><span data-stu-id="12b35-117">Alternatively, using the 10 object model, you can obtain a **Media** object from the library, and then set the **Player.currentMedia** property:</span></span>


```C++
// Get the first media object in the media collection.
var MyMediaItem = WMP9.mediaCollection.getAll().item(0)

// Make the MyMediaItem object the current media.
WMP9.currentMedia = MyMediaItem;

```



<span data-ttu-id="12b35-118">Grande parte da funcionalidade no modelo de objeto do Windows Media Player 7 ou posterior é acessada por meio da hierarquia de objetos.</span><span class="sxs-lookup"><span data-stu-id="12b35-118">Much of the functionality in the Windows Media Player 7 or later object model is accessed through the object hierarchy.</span></span> <span data-ttu-id="12b35-119">Como mostrado no exemplo anterior, você pode obter um objeto de **playlist** usando o método **getAll** do objeto **mediacollection** , que é acessado por meio do objeto do **Player** raiz.</span><span class="sxs-lookup"><span data-stu-id="12b35-119">As the previous example showed, you can obtain a **Playlist** object by using the **getAll** method of the **mediaCollection** object, which is accessed through the root **Player** object.</span></span> <span data-ttu-id="12b35-120">Em seguida, você pode obter um objeto de **mídia** específico do objeto **playlist** usando o método **Item** do objeto **playlist** .</span><span class="sxs-lookup"><span data-stu-id="12b35-120">You can then obtain a particular **Media** object from the **Playlist** object by using the **item** method of the **Playlist** object.</span></span> <span data-ttu-id="12b35-121">Há cinco métodos adicionais acessíveis por meio do objeto **mediacollection** que retornam um objeto **playlist** ; cada método permite que você recupere o objeto com base em critérios específicos, como gênero ou álbum.</span><span class="sxs-lookup"><span data-stu-id="12b35-121">There are five additional methods accessible through the **mediaCollection** object that return a **Playlist** object; each method allows you to retrieve the object based on specific criteria, like genre or album.</span></span>

<span data-ttu-id="12b35-122">A estrutura hierárquica do modelo de objeto de controle ActiveX do Windows Media Player 7 ou posterior fornece uma abordagem mais lógica para organizar as propriedades, os métodos e os eventos disponíveis para seu uso.</span><span class="sxs-lookup"><span data-stu-id="12b35-122">The hierarchical structure of the Windows Media Player 7 or later ActiveX control object model provides a more logical approach to organizing the properties, methods, and events available for your use.</span></span> <span data-ttu-id="12b35-123">Toda a funcionalidade para os controles do jogador está contida no objeto **Controls** , toda a funcionalidade da conexão de rede do player está contida no objeto **Network** e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="12b35-123">All the functionality for the Player controls is contained in the **Controls** object, all the functionality for the Player network connection is contained in the **Network** object, and so forth.</span></span> <span data-ttu-id="12b35-124">Por exemplo, para iniciar a reprodução de conteúdo usando o modelo de objeto da versão 6,4, use o método **Player6. Play** :</span><span class="sxs-lookup"><span data-stu-id="12b35-124">For example, to start content playing using the version 6.4 object model, you use the **Player6.Play** method:</span></span>


```C++
WMP64.Play();

```



<span data-ttu-id="12b35-125">Ao usar o modelo de objeto do Windows Media Player 7 ou posterior, você deve acessar o método **Play** usando o objeto **Controls** :</span><span class="sxs-lookup"><span data-stu-id="12b35-125">When using the Windows Media Player 7 or later object model, you must access the **Play** method by using the **Controls** object:</span></span>


```C++
WMP9.controls.play();

```



<span data-ttu-id="12b35-126">No entanto, a profundidade do modelo de objeto pode levar a instruções de script muito longas:</span><span class="sxs-lookup"><span data-stu-id="12b35-126">The depth of the object model, however, can lead to very long script statements:</span></span>


```C++
WMP9.currentPlaylist.appendItem(WMP9.mediaCollection.getByName("MySong").item(0));

```



<span data-ttu-id="12b35-127">Instruções como a anterior podem se tornar muito mais simples e legíveis ao trabalhar com objetos nomeados individuais.</span><span class="sxs-lookup"><span data-stu-id="12b35-127">Statements like the preceding one can be made much simpler and more readable by working with individual named objects.</span></span> <span data-ttu-id="12b35-128">O exemplo a seguir substitui a instrução de código anterior pela sintaxe usando variáveis de objeto separadas:</span><span class="sxs-lookup"><span data-stu-id="12b35-128">The following example replaces the preceding code statement with syntax using separate object variables:</span></span>


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



<span data-ttu-id="12b35-129">Esse estilo de codificação requer mais linhas de script, mas é muito mais fácil de seguir, especialmente com os comentários adicionados.</span><span class="sxs-lookup"><span data-stu-id="12b35-129">This coding style requires more lines of script, but is much easier to follow, especially with the added comments.</span></span> <span data-ttu-id="12b35-130">Há outra vantagem: o objeto **currentPlaylist** é fácil de ser reutilizado porque é armazenado na variável pl.</span><span class="sxs-lookup"><span data-stu-id="12b35-130">There is another advantage: the **currentPlaylist** object is easy to reuse because it is stored in the variable pl.</span></span>

<span data-ttu-id="12b35-131">Muitas das propriedades, métodos e eventos no modelo de objeto do Windows Media Player 7 ou posterior definem ou recuperam valores diferentes ou retornam valores de um tipo ou número diferente, em comparação com a funcionalidade correspondente no modelo de objeto da versão 6,4.</span><span class="sxs-lookup"><span data-stu-id="12b35-131">Many of the properties, methods, and events in the Windows Media Player 7 or later object model set or retrieve different values, or return values of a different type or number, compared to corresponding functionality in the version 6.4 object model.</span></span> <span data-ttu-id="12b35-132">Por exemplo, quando **Player6. OpenState** recupera 2, esse valor corresponde à constante de Visual Basic **nsLoadingNSC**, o que significa que o player está carregando um arquivo de estação com uma extensão de nome de arquivo. NSC.</span><span class="sxs-lookup"><span data-stu-id="12b35-132">For instance, when **Player6.openState** retrieves 2, that value corresponds to the Visual Basic constant **nsLoadingNSC**, meaning the Player is loading a station file with a .nsc file name extension.</span></span> <span data-ttu-id="12b35-133">Mas quando a propriedade de modelo de objeto do Windows Media Player 7 ou posterior **. OpenState** recupera 2, esse valor corresponde ao estado PlaylistLocating, o que significa que o Windows Media Player está tentando localizar uma lista de reprodução.</span><span class="sxs-lookup"><span data-stu-id="12b35-133">But when the Windows Media Player 7 or later object model property **Player.openState** retrieves 2, that value corresponds to the state PlaylistLocating, meaning Windows Media Player is attempting to locate a playlist.</span></span> <span data-ttu-id="12b35-134">Além disso, a propriedade **Player6. OpenState** pode recuperar sete valores diferentes, enquanto a propriedade **Player. OpenState** do Windows Media Player 7 ou posterior pode recuperar 22 valores diferentes.</span><span class="sxs-lookup"><span data-stu-id="12b35-134">Additionally, the **Player6.openState** property can retrieve seven different values, while the Windows Media Player 7 or later **Player.openState** property can retrieve 22 different values.</span></span> <span data-ttu-id="12b35-135">Certifique-se de consultar a seção referência de modelo de objeto para script do SDK do Windows Media Player ao revisar o código para usar uma versão de modelo de objeto diferente.</span><span class="sxs-lookup"><span data-stu-id="12b35-135">Be sure to refer to the Object Model Reference for Scripting section of the Windows Media Player SDK when revising code to use a different object model version.</span></span>

## <a name="related-topics"></a><span data-ttu-id="12b35-136">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="12b35-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="12b35-137">**Sobre o modelo de objeto do Player**</span><span class="sxs-lookup"><span data-stu-id="12b35-137">**About the Player Object Model**</span></span>](about-the-player-object-model.md)
</dt> <dt>

[<span data-ttu-id="12b35-138">**Referência de modelo de objeto para scripts**</span><span class="sxs-lookup"><span data-stu-id="12b35-138">**Object Model Reference for Scripting**</span></span>](object-model-reference-for-scripting.md)
</dt> <dt>

[<span data-ttu-id="12b35-139">**Guia de migração do modelo de objeto**</span><span class="sxs-lookup"><span data-stu-id="12b35-139">**Object Model Migration Guide**</span></span>](object-model-migration-guide.md)
</dt> </dl>

 

 




