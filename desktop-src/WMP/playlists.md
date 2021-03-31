---
title: Playlists
description: Playlists
ms.assetid: b1ac9208-33d1-448f-9e2e-920fad9c6add
keywords:
- Windows Media Player, listas de reprodução
- Modelo de objeto do Windows Media Player, listas de reprodução
- modelo de objeto, listas de reprodução
- Controle ActiveX do Windows Media Player, listas de reprodução
- Controle ActiveX, listas de reprodução
- Controle ActiveX móvel do Windows Media Player, listas de reprodução
- Windows Media Player Mobile, listas de reprodução
- listas de reprodução, migração
- Listas de reprodução do metarquivo do Windows Media, migração
- listas de reprodução de metarquivo, migração
- Guia de migração, listas de reprodução
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 124c07a6bd3aec0bebd235678e9fa8a5f069ec73
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005251"
---
# <a name="playlists"></a><span data-ttu-id="ba134-114">Playlists</span><span class="sxs-lookup"><span data-stu-id="ba134-114">Playlists</span></span>

<span data-ttu-id="ba134-115">O modelo de objeto de controle ActiveX do Windows Media Player 6,4 inclui quatro métodos e uma propriedade para trabalhar com as listas de reprodução do metarquivo de mídia do Windows:</span><span class="sxs-lookup"><span data-stu-id="ba134-115">The Windows Media Player 6.4 ActiveX control object model includes four methods and one property for working with Windows Media metafile playlists:</span></span>

-   <span data-ttu-id="ba134-116">*Player6*. **GetCurrentEntry**</span><span class="sxs-lookup"><span data-stu-id="ba134-116">*Player6*.**GetCurrentEntry**</span></span>
-   <span data-ttu-id="ba134-117">*Player6*. **SetCurrentEntry**</span><span class="sxs-lookup"><span data-stu-id="ba134-117">*Player6*.**SetCurrentEntry**</span></span>
-   <span data-ttu-id="ba134-118">*Player6*. **GetMediaParameter**</span><span class="sxs-lookup"><span data-stu-id="ba134-118">*Player6*.**GetMediaParameter**</span></span>
-   <span data-ttu-id="ba134-119">*Player6*. **GetMediaParameterName**</span><span class="sxs-lookup"><span data-stu-id="ba134-119">*Player6*.**GetMediaParameterName**</span></span>
-   <span data-ttu-id="ba134-120">*Player6*. **EntryCount**.</span><span class="sxs-lookup"><span data-stu-id="ba134-120">*Player6*.**EntryCount**.</span></span>

<span data-ttu-id="ba134-121">Juntos, eles fornecem funcionalidade limitada para navegar em um metarquivo de playlist com uma extensão de nome de arquivo. ASX e recuperar informações sobre as entradas contidas na lista de reprodução.</span><span class="sxs-lookup"><span data-stu-id="ba134-121">Together, these provide limited functionality for navigating a playlist metafile with an .asx file name extension and retrieving information about the entries contained in the playlist.</span></span>

<span data-ttu-id="ba134-122">O Windows Media Player 7 apresentou "biblioteca de mídia".</span><span class="sxs-lookup"><span data-stu-id="ba134-122">Windows Media Player 7 introduced "Media Library."</span></span> <span data-ttu-id="ba134-123">A biblioteca permite que os usuários organizem seu conteúdo de mídia digital, bem como criem listas de reprodução personalizadas que podem ser gerenciadas na interface gráfica do usuário do Player.</span><span class="sxs-lookup"><span data-stu-id="ba134-123">The library allows users to organize their digital media content, as well as to create custom playlists that can be managed from the Player graphical user interface.</span></span> <span data-ttu-id="ba134-124">O modelo de objeto de controle ActiveX do Windows Media Player 7 ou posterior fornece suporte para trabalhar com playlists de biblioteca, bem como listas de reprodução contidas em metaarquivos do Windows Media com uma extensão de nome de arquivo. asx.</span><span class="sxs-lookup"><span data-stu-id="ba134-124">The Windows Media Player 7 or later ActiveX control object model provides support for working with library playlists, as well as playlists contained in Windows Media metafiles with an .asx file name extension.</span></span>

> [!Note]  
> <span data-ttu-id="ba134-125">Por motivos de segurança, o usuário deve conceder direitos de acesso à biblioteca antes que seu programa possa manipular seu conteúdo.</span><span class="sxs-lookup"><span data-stu-id="ba134-125">For security reasons, the user must grant access rights to the library before your program can manipulate its content.</span></span> <span data-ttu-id="ba134-126">Direitos de acesso só podem ser solicitados e concedidos por meio do modelo de objeto do Windows Media Player 9 Series ou posterior.</span><span class="sxs-lookup"><span data-stu-id="ba134-126">Access rights can only be requested and granted through the Windows Media Player 9 Series or later object model.</span></span> <span data-ttu-id="ba134-127">Para obter detalhes sobre direitos de acesso, consulte [acesso à biblioteca](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="ba134-127">For details about access rights, see [Library Access](library-access.md).</span></span>

 

<span data-ttu-id="ba134-128">O modelo de objeto do Windows Media Player 7 ou posterior inclui três objetos para lidar com listas de reprodução.</span><span class="sxs-lookup"><span data-stu-id="ba134-128">The Windows Media Player 7 or later object model includes three objects for handling playlists.</span></span> <span data-ttu-id="ba134-129">O objeto **playlistcollection** fornece funcionalidade para organizar as listas de reprodução; Ele representa a coleção inteira de listas de reprodução na biblioteca do usuário.</span><span class="sxs-lookup"><span data-stu-id="ba134-129">The **PlaylistCollection** object provides functionality for organizing playlists; it represents the entire collection of playlists in the user's library.</span></span> <span data-ttu-id="ba134-130">O objeto **PlaylistArray** fornece uma maneira de recuperar uma lista de reprodução específica do objeto **playlistcollection** usando um número de índice; dois dos métodos de objeto **playlistcollection** recuperam um objeto **PlaylistArray** .</span><span class="sxs-lookup"><span data-stu-id="ba134-130">The **PlaylistArray** object provides a way to retrieve a specific playlist from the **PlaylistCollection** object by using an index number; two of the **PlaylistCollection** object methods retrieve a **PlaylistArray** object.</span></span> <span data-ttu-id="ba134-131">O objeto **playlist** fornece as propriedades e os métodos necessários para manipular itens de mídia contidos em uma única lista de reprodução.</span><span class="sxs-lookup"><span data-stu-id="ba134-131">The **Playlist** object provides the properties and methods necessary to manipulate media items contained in a single playlist.</span></span>

<span data-ttu-id="ba134-132">Por exemplo, como cada playlist na biblioteca tem um nome exclusivo, você pode recuperar uma lista de reprodução da biblioteca usando a *playlistcollection*. método **getByName** :</span><span class="sxs-lookup"><span data-stu-id="ba134-132">As an example, since each playlist in the library has a unique name, you can retrieve a playlist from the library using the *PlaylistCollection*.**getByName** method:</span></span>


```C++
// Retrieve a PlaylistArray object that contains 
// exactly one Playlist object.
var plarray = WMP9.playlistCollection.getByName("MyPlaylist");

// Get the Playlist object from the PlaylistArray object.
// The Playlist object has index number zero.
var pl = plarray.item(0);

// Make the retrieved playlist the current playlist.
WMP9.currentPlaylist = pl;

```



<span data-ttu-id="ba134-133">Com mais frequência, você desejará trabalhar com a playlist atual.</span><span class="sxs-lookup"><span data-stu-id="ba134-133">You will most frequently want to work with the current playlist.</span></span> <span data-ttu-id="ba134-134">Embora seja possível usar vários objetos de lista de reprodução, apenas um pode ser recuperado pelo *jogador*. Propriedade **currentPlaylist** em um determinado momento: aquela que o Windows Media Player está processando naquele momento.</span><span class="sxs-lookup"><span data-stu-id="ba134-134">While it is possible to use several playlist objects, only one can be retrieved by the *Player*.**currentPlaylist** property at any given time: the one that Windows Media Player is processing at that moment.</span></span>

<span data-ttu-id="ba134-135">Quando o Windows Media Player 7 ou posterior reproduz um metarquivo do Windows Media com uma extensão de nome de arquivo. ASX, ele primeiro cria um objeto de **lista de reprodução** .</span><span class="sxs-lookup"><span data-stu-id="ba134-135">When Windows Media Player 7 or later plays a Windows Media metafile with an .asx file name extension, it first creates a **Playlist** object.</span></span> <span data-ttu-id="ba134-136">Em seguida, ele preenche o objeto com as informações da lista de reprodução. ASX e, em seguida, torna esse objeto de **playlist** a playlist atual.</span><span class="sxs-lookup"><span data-stu-id="ba134-136">Next, it fills the object with the information from the .asx playlist, and then makes that **Playlist** object the current playlist.</span></span> <span data-ttu-id="ba134-137">Isso significa que você pode usar as propriedades e os métodos associados ao objeto **playlist** para manipular as listas de reprodução. asx exatamente como trataria as listas de reprodução na biblioteca.</span><span class="sxs-lookup"><span data-stu-id="ba134-137">This means that you can use the properties and methods associated with the **Playlist** object to manipulate .asx playlists exactly as you would handle playlists in the library.</span></span> <span data-ttu-id="ba134-138">Por exemplo, para recuperar o número de entradas em uma lista de reprodução. asx usando o modelo de objeto da versão 6,4, use o *Player6*. Propriedade **EntryCount** :</span><span class="sxs-lookup"><span data-stu-id="ba134-138">For instance, to retrieve the number of entries in an .asx playlist using the version 6.4 object model, you use the *Player6*.**EntryCount** property:</span></span>


```C++
var entrycount = WMP64.EntryCount;

```



<span data-ttu-id="ba134-139">Ao usar o modelo de objeto do Windows Media Player 7 ou posterior, use a *lista de reprodução*. Propriedade de **contagem** :</span><span class="sxs-lookup"><span data-stu-id="ba134-139">When using the Windows Media Player 7 or later object model, you use the *Playlist*.**count** property:</span></span>


```C++
var entrycount = WMP9.currentPlaylist.count;

```



<span data-ttu-id="ba134-140">Ao usar o controle da versão 6,4, você pode usar o *Player6*. Método **GetCurrentEntry** para recuperar o índice da entrada atual em uma lista de reprodução. ASX:</span><span class="sxs-lookup"><span data-stu-id="ba134-140">When using the version 6.4 control, you can use the *Player6*.**GetCurrentEntry** method to retrieve the index of the current entry in an .asx playlist:</span></span>


```C++
var entrynum = WMP64.GetCurrentEntry();

```



<span data-ttu-id="ba134-141">Você pode obter o mesmo resultado usando o modelo de objeto do Windows Media Player 7 ou posterior no script.</span><span class="sxs-lookup"><span data-stu-id="ba134-141">You can achieve the same result by using the Windows Media Player 7 or later object model in script.</span></span> <span data-ttu-id="ba134-142">O exemplo de JScript a seguir compara o objeto de mídia atual com cada item na lista de reprodução.</span><span class="sxs-lookup"><span data-stu-id="ba134-142">The following JScript example compares the current media object to each item in the playlist.</span></span> <span data-ttu-id="ba134-143">Quando *mídia*. **isidêntico** retorna true, uma caixa de mensagem exibe o índice do item de mídia atual.</span><span class="sxs-lookup"><span data-stu-id="ba134-143">When *Media*.**isIdentical** returns true, a message box displays the index of the current media item.</span></span>


```C++
function matchit(){
// Store the current playlist object in a variable.
var pl = WMP9.currentPlaylist;

// Loop through the playlist one entry at a time.
  for (var i = 0; i < pl.count; i++){

   // Test whether the current media item matches 
   // the item in the playlist at the current loop index.
   if (WMP9.currentmedia.isIdentical(pl.item(i))){

       // They match, display the index.
       var message = "Current media at index: " + i;
       alert(message);

       // Exit the function, don't continue looping!
       return;
      }
  }
}

```



<span data-ttu-id="ba134-144">Para especificar o índice da entrada atual em uma lista de reprodução. ASX, use *Player6*. **SetCurrentEntry**.</span><span class="sxs-lookup"><span data-stu-id="ba134-144">To specify the index of the current entry in an .asx playlist, you use *Player6*.**SetCurrentEntry**.</span></span> <span data-ttu-id="ba134-145">Os índices de entrada de playlist na versão 6,4 começam com 1, portanto, para tornar a segunda entrada em uma lista de reprodução de metarquivo a atual, use a seguinte sintaxe:</span><span class="sxs-lookup"><span data-stu-id="ba134-145">Playlist entry indexes in version 6.4 start with 1, so to make the second entry in a metafile playlist the current one, use the following syntax:</span></span>


```C++
WMP6.SetCurrentEntry(2);

```



<span data-ttu-id="ba134-146">Os índices de entrada de playlist são baseados em zero no Windows Media Player 7 ou posterior; para tornar a segunda entrada em uma lista de reprodução de metarquivo a atual, ao usar o modelo de objeto do Windows Media Player 7 ou posterior, use a seguinte sintaxe:</span><span class="sxs-lookup"><span data-stu-id="ba134-146">Playlist entry indexes are zero-based in Windows Media Player 7 or later; to make the second entry in a metafile playlist the current one, when using the Windows Media Player 7 or later object model, use the following syntax:</span></span>


```C++
WMP9.controls.currentItem = WMP9.currentPlaylist.item(1);

```



<span data-ttu-id="ba134-147">O exemplo de JScript a seguir demonstra uma função que aceita um número de índice como um parâmetro e, em seguida, torna a entrada da playlist que corresponde ao índice do item de mídia atual:</span><span class="sxs-lookup"><span data-stu-id="ba134-147">The following JScript example demonstrates a function that accepts an index number as a parameter, and then makes the playlist entry that corresponds to the index the current media item:</span></span>


```C++
function setindex(idx){
// Store the current playlist in a variable.
var pl = WMP9.currentPlaylist;

// Get the first playlist entry.
var firstmedia = pl.item(0);

// Start the Player to allow navigation within the playlist.
WMP9.controls.playItem(firstmedia);

// Test whether idx is within a valid range.
   if (idx < pl.count && idx >= 0){

     // Set the currentItem to the desired playlist item.
     WMP9.controls.currentItem = pl.item(idx);

     // Display the name of the media item.
     alert(WMP9.currentMedia.name);
     return true;
 }

// The index is out of range, stop the Player, alert the user.
WMP9.controls.stop();
alert("Index out of range");
return false;
}

```



<span data-ttu-id="ba134-148">Os metaarquivos de mídia do Windows podem conter elementos de parâmetro personalizados, que você especifica usando a **<PARAM>** marca.</span><span class="sxs-lookup"><span data-stu-id="ba134-148">Windows Media metafiles can contain custom parameter elements, which you specify by using the **<PARAM>** tag.</span></span> <span data-ttu-id="ba134-149">Ao usar o modelo de objeto da versão 6,4, você pode recuperar o nome de um parâmetro específico com o *Player6*. Método **GetMediaParameterName** .</span><span class="sxs-lookup"><span data-stu-id="ba134-149">When using the version 6.4 object model, you can retrieve the name of a particular parameter with the *Player6*.**GetMediaParameterName** method.</span></span> <span data-ttu-id="ba134-150">O exemplo de JScript a seguir recupera o nome do primeiro parâmetro na primeira entrada de uma lista de reprodução. ASX:</span><span class="sxs-lookup"><span data-stu-id="ba134-150">The following JScript example retrieves the name of the first parameter in the first entry of an .asx playlist:</span></span>


```C++
var paramname = WMP6.GetMediaParameterName(1,1);

```



<span data-ttu-id="ba134-151">Da mesma forma, você pode recuperar o valor associado ao parâmetro usando *Player6*. **GetMediaParameter**:</span><span class="sxs-lookup"><span data-stu-id="ba134-151">Similarly, you can retrieve the value associated with the parameter using *Player6*.**GetMediaParameter**:</span></span>


```C++
var paramvalue = WMP6.GetMediaParameter(1, paramname);

```



<span data-ttu-id="ba134-152">O exemplo de JScript a seguir usa o modelo de objeto do Windows Media Player 7 ou posterior para recuperar o nome e o valor do parâmetro da primeira entrada em uma lista de reprodução. ASX:</span><span class="sxs-lookup"><span data-stu-id="ba134-152">The following JScript example uses the Windows Media Player 7 or later object model to retrieve the parameter name and value from the first entry in an .asx playlist:</span></span>


```C++
function getattribute(){
// Store the first playlist entry as a Media object.
var firstmedia = WMP9.currentplaylist.item(0);

// Get the name of the first parameter in the object named firstmedia.
var attname = firstmedia.getAttributeName(0);

// Get the value of the first parameter in the object named firstmedia.
var attval = firstmedia.getItemInfo(attname);

// Display the information.
alert(attname + ": " + attval);
}

```



<span data-ttu-id="ba134-153">Você pode usar a *playlistcollection*. método **importPlaylist** para adicionar uma lista de reprodução. asx à biblioteca.</span><span class="sxs-lookup"><span data-stu-id="ba134-153">You can use the *PlaylistCollection*.**importPlaylist** method to add an .asx playlist to the library.</span></span> <span data-ttu-id="ba134-154">Depois de importado, a lista de reprodução de metarquivo se torna uma lista de reprodução de biblioteca, para que você possa manipulá-la usando todas as propriedades e métodos à sua disposição.</span><span class="sxs-lookup"><span data-stu-id="ba134-154">Once imported, the metafile playlist becomes a library playlist, so you can manipulate it using all the properties and methods at your disposal.</span></span> <span data-ttu-id="ba134-155">O usuário deve conceder direitos de acesso completo à biblioteca para que seu aplicativo possa usar o método **importPlaylist** .</span><span class="sxs-lookup"><span data-stu-id="ba134-155">The user must grant full access rights to the library for your application to be able to use the **importPlaylist** method.</span></span>

<span data-ttu-id="ba134-156">Você pode usar *playlistcollection*. **getByName** para testar se existe uma lista de reprodução.</span><span class="sxs-lookup"><span data-stu-id="ba134-156">You can use *PlaylistCollection*.**getByName** to test whether a playlist exists.</span></span> <span data-ttu-id="ba134-157">Esse método sempre retorna um objeto **PlaylistArray** válido.</span><span class="sxs-lookup"><span data-stu-id="ba134-157">This method always returns a valid **PlaylistArray** object.</span></span> <span data-ttu-id="ba134-158">Se a matriz de playlist recuperada contiver exatamente uma lista de reprodução, existirá uma playlist com esse nome na biblioteca.</span><span class="sxs-lookup"><span data-stu-id="ba134-158">If the playlist array retrieved contains exactly one playlist, then there exists a playlist with that name in the library.</span></span> <span data-ttu-id="ba134-159">Caso contrário, a matriz de playlist não conterá nenhum objeto de playlist; Isso significa que não há nenhuma lista de reprodução na biblioteca com o nome passado como um argumento para o método **getByName** .</span><span class="sxs-lookup"><span data-stu-id="ba134-159">Otherwise, the playlist array will contain no playlist object; this means there is no playlist in the library with the name passed as an argument to the **getByName** method.</span></span> <span data-ttu-id="ba134-160">O exemplo de JScript a seguir demonstra isso:</span><span class="sxs-lookup"><span data-stu-id="ba134-160">The following JScript example demonstrates this:</span></span>


```C++
// Specify an .asx playlist file.
WMP9.URL = "https://www.microsoft.com/someplaylist.asx";

// Open the playlist and start playing the content.
WMP9.controls.play();

// Store the current playlist object.
var pl = WMP9.currentPlaylist;

// Attempt to retrieve from the library 
// a playlist having the same name as the current playlist.
var plarray = WMP9.playlistCollection.getByName(pl.name);

// Test whether the PlaylistArray object, plarray, contains
// a Playlist object.
if (!plarray.count)
   
   // If plarray contains no playlist, then import 
   // the current one.
   WMP9.playlistCollection.importPlaylist(pl);
}

```



## <a name="related-topics"></a><span data-ttu-id="ba134-161">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="ba134-161">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ba134-162">**Gerenciando listas de reprodução**</span><span class="sxs-lookup"><span data-stu-id="ba134-162">**Managing Playlists**</span></span>](managing-playlists.md)
</dt> <dt>

[<span data-ttu-id="ba134-163">**Guia de migração do modelo de objeto**</span><span class="sxs-lookup"><span data-stu-id="ba134-163">**Object Model Migration Guide**</span></span>](object-model-migration-guide.md)
</dt> <dt>

[<span data-ttu-id="ba134-164">**Objeto playlist**</span><span class="sxs-lookup"><span data-stu-id="ba134-164">**Playlist Object**</span></span>](playlist-object.md)
</dt> </dl>

 

 




