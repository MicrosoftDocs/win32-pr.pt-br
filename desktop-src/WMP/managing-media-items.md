---
title: Gerenciando itens de mídia
description: Gerenciando itens de mídia
ms.assetid: fba1df60-d603-4e37-a021-8fa618144149
keywords:
- Windows Media Player, biblioteca
- Windows Media Player modelo de objeto, biblioteca
- modelo de objeto, biblioteca
- Windows Media Player Mobile, biblioteca para o modelo de objeto
- Windows Media Player controle ActiveX, biblioteca para modelo de objeto
- Windows Media Player controle ActiveX Móvel, biblioteca para modelo de objeto
- Controle ActiveX, biblioteca para modelo de objeto
- Windows Media Player, gerenciando itens de mídia
- biblioteca, gerenciando itens de mídia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf984c2f884ae828bd6426dd2a3f6da19a78ddea
ms.sourcegitcommit: cb87082135319cbdc5df541e3071eebb83a58972
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/04/2021
ms.locfileid: "111386885"
---
# <a name="managing-media-items"></a><span data-ttu-id="1798f-112">Gerenciando itens de mídia</span><span class="sxs-lookup"><span data-stu-id="1798f-112">Managing Media Items</span></span>

<span data-ttu-id="1798f-113">Um **objeto Media** representa um item de mídia.</span><span class="sxs-lookup"><span data-stu-id="1798f-113">A **Media** object represents one media item.</span></span> <span data-ttu-id="1798f-114">Ele tem propriedades e métodos que você pode usar para recuperar informações e exibi-las para o usuário ou para tomar ações diferentes com base no valor recuperado.</span><span class="sxs-lookup"><span data-stu-id="1798f-114">It has properties and methods you can use to retrieve information and display it to the user, or to take different actions based on the value you retrieve.</span></span>

<span data-ttu-id="1798f-115">Grande parte do seu trabalho com **objetos de** Mídia envolve metadados sobre o conteúdo do item de mídia, chamados de atributos.</span><span class="sxs-lookup"><span data-stu-id="1798f-115">Much of your work with **Media** objects involves metadata about the content of the media item, called the attributes.</span></span> <span data-ttu-id="1798f-116">O tópico [Atributos de Item de](media-item-attributes.md) Mídia descreve como ler e alterar valores de atributo.</span><span class="sxs-lookup"><span data-stu-id="1798f-116">The topic [Media Item Attributes](media-item-attributes.md) describes how to read and change attribute values.</span></span> <span data-ttu-id="1798f-117">Além deste tópico, consulte as Diretrizes de uso de metadados de mídia do [Windows](/previous-versions/ms867702(v=msdn.10)) no site da Microsoft para obter mais informações sobre os atributos e seu uso.</span><span class="sxs-lookup"><span data-stu-id="1798f-117">In addition to this topic, see the [Windows Media Metadata Usage Guidelines](/previous-versions/ms867702(v=msdn.10)) on the Microsoft website for more information about the attributes and their use.</span></span>

<span data-ttu-id="1798f-118">O **objeto Media** tem propriedades e métodos que recuperam alguns atributos diretamente, como o nome ou a duração do item.</span><span class="sxs-lookup"><span data-stu-id="1798f-118">The **Media** object has properties and methods that retrieve some attributes directly, such as the name or duration of the item.</span></span> <span data-ttu-id="1798f-119">Para itens de vídeo, você pode recuperar a altura e a largura da imagem e recuperar informações de marcador com base no nome ou índice de um marcador.</span><span class="sxs-lookup"><span data-stu-id="1798f-119">For video items, you can retrieve the height and width of the image, and you can retrieve marker information based on the name or index of a marker.</span></span> <span data-ttu-id="1798f-120">Você também pode determinar se um item de mídia específico está incluído em uma playlist específica.</span><span class="sxs-lookup"><span data-stu-id="1798f-120">You can also determine whether a particular media item is included in a particular playlist.</span></span>

## <a name="retrieving-a-media-object"></a><span data-ttu-id="1798f-121">Recuperando um objeto de mídia</span><span class="sxs-lookup"><span data-stu-id="1798f-121">Retrieving a Media Object</span></span>

<span data-ttu-id="1798f-122">Você pode acessar rapidamente o item de mídia atual usando o *Player*. **propriedade currentMedia.**</span><span class="sxs-lookup"><span data-stu-id="1798f-122">You can quickly access the current media item by using the *Player*.**currentMedia** property.</span></span>

<span data-ttu-id="1798f-123">Ao longo deste tópico, o **objeto Player** foi definido da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="1798f-123">Throughout this topic, the **Player** object was defined in the following manner:</span></span>


```C++
AxWMPLib.AxWindowsMediaPlayer Player;
using WMPLib;

```



<span data-ttu-id="1798f-124">O exemplo de C# a seguir recupera um **objeto Media** que representa o item atual.</span><span class="sxs-lookup"><span data-stu-id="1798f-124">The following C# example retrieves a **Media** object representing the current item.</span></span>


```C++
IWMPMedia media;
media = Player.currentMedia;

```



<span data-ttu-id="1798f-125">Você pode criar um novo item de mídia de um arquivo de mídia digital usando o *Player*. **Método newMedia.**</span><span class="sxs-lookup"><span data-stu-id="1798f-125">You can create a new media item from a digital media file by using the *Player*.**newMedia** method.</span></span> <span data-ttu-id="1798f-126">Você passa o caminho da URL para um arquivo de mídia digital e ele retorna uma referência ao novo **objeto Media.**</span><span class="sxs-lookup"><span data-stu-id="1798f-126">You pass the method the URL path to a digital media file, and it returns a reference to the new **Media** object.</span></span> <span data-ttu-id="1798f-127">O método não adiciona o novo objeto à biblioteca diretamente.</span><span class="sxs-lookup"><span data-stu-id="1798f-127">The method does not add the new object to the library directly.</span></span> <span data-ttu-id="1798f-128">No entanto, você pode passar o objeto para a *Playlist*. **Método appendItem** ou *Playlist*. **Método insertItem.**</span><span class="sxs-lookup"><span data-stu-id="1798f-128">However, you can pass the object to the *Playlist*.**appendItem** method or the *Playlist*.**insertItem** method.</span></span>

<span data-ttu-id="1798f-129">O exemplo de C# a seguir cria um objeto **Media** com base em um dos exemplos de mídia digital instalados com o SDK Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="1798f-129">The following C# example creates a **Media** object based on one of the digital media samples installed with the Windows Media Player SDK.</span></span>


```C++
IWMPMedia media;
media = Player.newMedia("C:\\WMSDK\\WMPSDK10\\samples\\media\\laure.wma");

```



> [!Note]  
> <span data-ttu-id="1798f-130">Você deve incluir dois caracteres de invertida ( ) (ou usar o caractere @ em C#) em uma cadeia de caracteres para representar um caractere de faixa \\ invertida real.</span><span class="sxs-lookup"><span data-stu-id="1798f-130">You must include two backslash (\\) characters (or use the @ character in C#) in a string to represent one actual backslash character.</span></span> <span data-ttu-id="1798f-131">Isso porque o C# usa um único caractere de faixa invertida para definir uma sequência de escape.</span><span class="sxs-lookup"><span data-stu-id="1798f-131">This is because C# uses a single backslash character to define an escape sequence.</span></span>

 

<span data-ttu-id="1798f-132">Você pode criar um novo item de mídia de um arquivo de mídia digital e adicioná-lo à biblioteca em uma etapa usando *MediaCollection*. **método add.**</span><span class="sxs-lookup"><span data-stu-id="1798f-132">You can create a new media item from a digital media file and add it to the library in one step by using the *MediaCollection*.**add** method.</span></span> <span data-ttu-id="1798f-133">Como o *Player*. **método newMedia,** o **método add** leva um caminho para um arquivo de mídia digital.</span><span class="sxs-lookup"><span data-stu-id="1798f-133">Like the *Player*.**newMedia** method, the **add** method takes a path to a digital media file.</span></span>

<span data-ttu-id="1798f-134">O exemplo C# a seguir cria um **objeto Media** com base em um dos arquivos de exemplo do SDK e adiciona esse objeto à biblioteca.</span><span class="sxs-lookup"><span data-stu-id="1798f-134">The following C# example creates a **Media** object based on one of the SDK sample files and adds that object to the library.</span></span>


```C++
IWMPMedia media;
media = Player.mediaCollection.add("C:\\WMSDK\\WMPSDK10\\samples\\media\\laure.wma");

```



<span data-ttu-id="1798f-135">Você pode recuperar um objeto **Media** que representa um item de mídia em uma playlist usando a *Playlist*. **método item.**</span><span class="sxs-lookup"><span data-stu-id="1798f-135">You can retrieve a **Media** object representing a media item in a playlist by using the *Playlist*.**item** method.</span></span> <span data-ttu-id="1798f-136">O exemplo de C# a seguir recupera o sexto item de mídia da playlist atual.</span><span class="sxs-lookup"><span data-stu-id="1798f-136">The following C# example retrieves the sixth media item from the current playlist.</span></span>


```C++
IWMPMedia media;
media = Player.currentPlaylist.get_Item(5);

```



## <a name="related-topics"></a><span data-ttu-id="1798f-137">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="1798f-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1798f-138">**Controls.currentItem**</span><span class="sxs-lookup"><span data-stu-id="1798f-138">**Controls.currentItem**</span></span>](controls-currentitem.md)
</dt> <dt>

[<span data-ttu-id="1798f-139">**Gerenciando playlists**</span><span class="sxs-lookup"><span data-stu-id="1798f-139">**Managing Playlists**</span></span>](managing-playlists.md)
</dt> <dt>

[<span data-ttu-id="1798f-140">**Objeto de mídia**</span><span class="sxs-lookup"><span data-stu-id="1798f-140">**Media Object**</span></span>](media-object.md)
</dt> <dt>

[<span data-ttu-id="1798f-141">**MediaCollection.add**</span><span class="sxs-lookup"><span data-stu-id="1798f-141">**MediaCollection.add**</span></span>](mediacollection-add.md)
</dt> <dt>

[<span data-ttu-id="1798f-142">**Player.currentMedia**</span><span class="sxs-lookup"><span data-stu-id="1798f-142">**Player.currentMedia**</span></span>](player-currentmedia.md)
</dt> <dt>

[<span data-ttu-id="1798f-143">**Player.newMedia**</span><span class="sxs-lookup"><span data-stu-id="1798f-143">**Player.newMedia**</span></span>](player-newmedia.md)
</dt> <dt>

[<span data-ttu-id="1798f-144">**Playlist.item**</span><span class="sxs-lookup"><span data-stu-id="1798f-144">**Playlist.item**</span></span>](playlist-item.md)
</dt> <dt>

[<span data-ttu-id="1798f-145">**Trabalhando com a biblioteca**</span><span class="sxs-lookup"><span data-stu-id="1798f-145">**Working with the Library**</span></span>](working-with-the-library.md)
</dt> </dl>

 

 




