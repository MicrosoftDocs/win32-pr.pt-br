---
title: Gerenciando itens de mídia
description: Gerenciando itens de mídia
ms.assetid: fba1df60-d603-4e37-a021-8fa618144149
keywords:
- Windows Media Player, biblioteca
- Modelo de objeto do Windows Media Player, biblioteca
- modelo de objeto, biblioteca
- Windows Media Player Mobile, biblioteca para modelo de objeto
- Controle ActiveX do Windows Media Player, biblioteca para modelo de objeto
- Controle ActiveX móvel do Windows Media Player, biblioteca para modelo de objeto
- Controle ActiveX, biblioteca para modelo de objeto
- Biblioteca do Windows Media Player, gerenciando itens de mídia
- biblioteca, gerenciando itens de mídia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03b8003de49de9b7e4e51aabeffa222fb649ddef
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104084127"
---
# <a name="managing-media-items"></a><span data-ttu-id="e1426-112">Gerenciando itens de mídia</span><span class="sxs-lookup"><span data-stu-id="e1426-112">Managing Media Items</span></span>

<span data-ttu-id="e1426-113">Um objeto de **mídia** representa um item de mídia.</span><span class="sxs-lookup"><span data-stu-id="e1426-113">A **Media** object represents one media item.</span></span> <span data-ttu-id="e1426-114">Ele tem propriedades e métodos que você pode usar para recuperar informações e exibi-las para o usuário, ou para executar ações diferentes com base no valor recuperado.</span><span class="sxs-lookup"><span data-stu-id="e1426-114">It has properties and methods you can use to retrieve information and display it to the user, or to take different actions based on the value you retrieve.</span></span>

<span data-ttu-id="e1426-115">Grande parte do seu trabalho com objetos de **mídia** envolve metadados sobre o conteúdo do item de mídia, chamado de atributos.</span><span class="sxs-lookup"><span data-stu-id="e1426-115">Much of your work with **Media** objects involves metadata about the content of the media item, called the attributes.</span></span> <span data-ttu-id="e1426-116">O tópico [atributos de item de mídia](media-item-attributes.md) descreve como ler e alterar valores de atributo.</span><span class="sxs-lookup"><span data-stu-id="e1426-116">The topic [Media Item Attributes](media-item-attributes.md) describes how to read and change attribute values.</span></span> <span data-ttu-id="e1426-117">Além deste tópico, consulte as diretrizes de [uso de metadados do Windows Media](/previous-versions/ms867702(v=msdn.10)) no site da Microsoft para obter mais informações sobre os atributos e seu uso.</span><span class="sxs-lookup"><span data-stu-id="e1426-117">In addition to this topic, see the [Windows Media Metadata Usage Guidelines](/previous-versions/ms867702(v=msdn.10)) on the Microsoft website for more information about the attributes and their use.</span></span>

<span data-ttu-id="e1426-118">O objeto de **mídia** tem propriedades e métodos que recuperam alguns atributos diretamente, como o nome ou a duração do item.</span><span class="sxs-lookup"><span data-stu-id="e1426-118">The **Media** object has properties and methods that retrieve some attributes directly, such as the name or duration of the item.</span></span> <span data-ttu-id="e1426-119">Para itens de vídeo, você pode recuperar a altura e a largura da imagem e pode recuperar informações de marcador com base no nome ou no índice de um marcador.</span><span class="sxs-lookup"><span data-stu-id="e1426-119">For video items, you can retrieve the height and width of the image, and you can retrieve marker information based on the name or index of a marker.</span></span> <span data-ttu-id="e1426-120">Você também pode determinar se um item de mídia específico está incluído em uma determinada lista de reprodução.</span><span class="sxs-lookup"><span data-stu-id="e1426-120">You can also determine whether a particular media item is included in a particular playlist.</span></span>

## <a name="retrieving-a-media-object"></a><span data-ttu-id="e1426-121">Recuperando um objeto de mídia</span><span class="sxs-lookup"><span data-stu-id="e1426-121">Retrieving a Media Object</span></span>

<span data-ttu-id="e1426-122">Você pode acessar rapidamente o item de mídia atual usando o *Player*. Propriedade **currentMedia** .</span><span class="sxs-lookup"><span data-stu-id="e1426-122">You can quickly access the current media item by using the *Player*.**currentMedia** property.</span></span>

<span data-ttu-id="e1426-123">Ao longo deste tópico, o objeto **Player** foi definido da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="e1426-123">Throughout this topic, the **Player** object was defined in the following manner:</span></span>


```C++
AxWMPLib.AxWindowsMediaPlayer Player;
using WMPLib;

```



<span data-ttu-id="e1426-124">O exemplo de C# a seguir recupera um objeto de **mídia** que representa o item atual.</span><span class="sxs-lookup"><span data-stu-id="e1426-124">The following C# example retrieves a **Media** object representing the current item.</span></span>


```C++
IWMPMedia media;
media = Player.currentMedia;

```



<span data-ttu-id="e1426-125">Você pode criar um novo item de mídia de um arquivo de mídia digital usando o *Player*. método **newMedia** .</span><span class="sxs-lookup"><span data-stu-id="e1426-125">You can create a new media item from a digital media file by using the *Player*.**newMedia** method.</span></span> <span data-ttu-id="e1426-126">Você passa o método do caminho da URL para um arquivo de mídia digital e retorna uma referência ao novo objeto de **mídia** .</span><span class="sxs-lookup"><span data-stu-id="e1426-126">You pass the method the URL path to a digital media file, and it returns a reference to the new **Media** object.</span></span> <span data-ttu-id="e1426-127">O método não adiciona o novo objeto à biblioteca diretamente.</span><span class="sxs-lookup"><span data-stu-id="e1426-127">The method does not add the new object to the library directly.</span></span> <span data-ttu-id="e1426-128">No entanto, você pode passar o objeto para a *lista de reprodução*. método **appendItem** ou a *playlist*. método **insertItem** .</span><span class="sxs-lookup"><span data-stu-id="e1426-128">However, you can pass the object to the *Playlist*.**appendItem** method or the *Playlist*.**insertItem** method.</span></span>

<span data-ttu-id="e1426-129">O exemplo de C# a seguir cria um objeto de **mídia** baseado em um dos exemplos de mídia digital instalados com o SDK do Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="e1426-129">The following C# example creates a **Media** object based on one of the digital media samples installed with the Windows Media Player SDK.</span></span>


```C++
IWMPMedia media;
media = Player.newMedia("C:\\WMSDK\\WMPSDK10\\samples\\media\\laure.wma");

```



> [!Note]  
> <span data-ttu-id="e1426-130">Você deve incluir duas barras invertidas ( \) caracteres (ou usar o caractere @ em C#) em uma cadeia de caracteres para representar um caractere de barra invertida real.</span><span class="sxs-lookup"><span data-stu-id="e1426-130">You must include two backslash (\) characters (or use the @ character in C#) in a string to represent one actual backslash character.</span></span> <span data-ttu-id="e1426-131">Isso ocorre porque o C# usa um caractere de barra invertida única para definir uma sequência de escape.</span><span class="sxs-lookup"><span data-stu-id="e1426-131">This is because C# uses a single backslash character to define an escape sequence.</span></span>

 

<span data-ttu-id="e1426-132">Você pode criar um novo item de mídia de um arquivo de mídia digital e adicioná-lo à biblioteca em uma só etapa usando o *mediacollection*. **Adicionar** método.</span><span class="sxs-lookup"><span data-stu-id="e1426-132">You can create a new media item from a digital media file and add it to the library in one step by using the *MediaCollection*.**add** method.</span></span> <span data-ttu-id="e1426-133">Como o *jogador*. o método **newMedia** , o método **Add** , usa um caminho para um arquivo de mídia digital.</span><span class="sxs-lookup"><span data-stu-id="e1426-133">Like the *Player*.**newMedia** method, the **add** method takes a path to a digital media file.</span></span>

<span data-ttu-id="e1426-134">O exemplo de C# a seguir cria um objeto de **mídia** baseado em um dos arquivos de exemplo do SDK e adiciona esse objeto à biblioteca.</span><span class="sxs-lookup"><span data-stu-id="e1426-134">The following C# example creates a **Media** object based on one of the SDK sample files and adds that object to the library.</span></span>


```C++
IWMPMedia media;
media = Player.mediaCollection.add("C:\\WMSDK\\WMPSDK10\\samples\\media\\laure.wma");

```



<span data-ttu-id="e1426-135">Você pode recuperar um objeto de **mídia** que representa um item de mídia em uma lista de reprodução usando a *lista de reprodução*. método de **Item** .</span><span class="sxs-lookup"><span data-stu-id="e1426-135">You can retrieve a **Media** object representing a media item in a playlist by using the *Playlist*.**item** method.</span></span> <span data-ttu-id="e1426-136">O exemplo de C# a seguir recupera o sexto item de mídia da playlist atual.</span><span class="sxs-lookup"><span data-stu-id="e1426-136">The following C# example retrieves the sixth media item from the current playlist.</span></span>


```C++
IWMPMedia media;
media = Player.currentPlaylist.get_Item(5);

```



## <a name="related-topics"></a><span data-ttu-id="e1426-137">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="e1426-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e1426-138">**Controls. currentItem**</span><span class="sxs-lookup"><span data-stu-id="e1426-138">**Controls.currentItem**</span></span>](controls-currentitem.md)
</dt> <dt>

[<span data-ttu-id="e1426-139">**Gerenciando listas de reprodução**</span><span class="sxs-lookup"><span data-stu-id="e1426-139">**Managing Playlists**</span></span>](managing-playlists.md)
</dt> <dt>

[<span data-ttu-id="e1426-140">**Objeto de mídia**</span><span class="sxs-lookup"><span data-stu-id="e1426-140">**Media Object**</span></span>](media-object.md)
</dt> <dt>

[<span data-ttu-id="e1426-141">**Mediacollection. adicionar**</span><span class="sxs-lookup"><span data-stu-id="e1426-141">**MediaCollection.add**</span></span>](mediacollection-add.md)
</dt> <dt>

[<span data-ttu-id="e1426-142">**Player. currentMedia**</span><span class="sxs-lookup"><span data-stu-id="e1426-142">**Player.currentMedia**</span></span>](player-currentmedia.md)
</dt> <dt>

[<span data-ttu-id="e1426-143">**Player. newMedia**</span><span class="sxs-lookup"><span data-stu-id="e1426-143">**Player.newMedia**</span></span>](player-newmedia.md)
</dt> <dt>

[<span data-ttu-id="e1426-144">**Lista de reprodução. Item**</span><span class="sxs-lookup"><span data-stu-id="e1426-144">**Playlist.item**</span></span>](playlist-item.md)
</dt> <dt>

[<span data-ttu-id="e1426-145">**Trabalhando com a biblioteca**</span><span class="sxs-lookup"><span data-stu-id="e1426-145">**Working with the Library**</span></span>](working-with-the-library.md)
</dt> </dl>

 

 




