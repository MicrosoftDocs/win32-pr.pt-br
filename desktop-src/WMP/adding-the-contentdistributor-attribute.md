---
title: Adicionando o atributo ContentDistributor
description: Adicionando o atributo ContentDistributor
ms.assetid: b4ba5c9b-f28f-4275-bd39-c0ad1080d122
keywords:
- Lojas online do Windows Media Player, adicionando atributo ContentDistributor
- lojas online, adicionando o atributo ContentDistributor
- Digite 1 lojas online, adicionando o atributo ContentDistributor
- tipo 2 lojas online, adicionando atributo ContentDistributor
- Armazenamentos online do Windows Media Player, atributo ContentDistributor
- lojas online, atributo ContentDistributor
- Digite 1 lojas online, atributo ContentDistributor
- tipo 2 lojas online, atributo ContentDistributor
- adicionando atributo ContentDistributor
- ContentDistributor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1636c002affbcf1235283a22f7eb060c75f24a81
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292214"
---
# <a name="adding-the-contentdistributor-attribute"></a><span data-ttu-id="d3587-113">Adicionando o atributo ContentDistributor</span><span class="sxs-lookup"><span data-stu-id="d3587-113">Adding the ContentDistributor Attribute</span></span>

<span data-ttu-id="d3587-114">Quando o usuário tenta reproduzir o conteúdo da loja online ou copiar o conteúdo para um CD ou dispositivo, o Windows Media Player chama determinados métodos em seu objeto COM.</span><span class="sxs-lookup"><span data-stu-id="d3587-114">When the user attempts to play online store content or to copy the content to a CD or device, Windows Media Player calls certain methods in your COM object.</span></span> <span data-ttu-id="d3587-115">Para fazer isso, o player precisa de uma maneira de diferenciar o conteúdo dos outros provedores de loja online.</span><span class="sxs-lookup"><span data-stu-id="d3587-115">To do this, the Player needs a way to differentiate your content from that of other online store providers.</span></span> <span data-ttu-id="d3587-116">Ao adicionar o nome da sua chave de loja online como o valor para o **ContentDistributor** (que é um alias para o atributo do SDK do Windows Media Format chamado **WM/ContentDistributor**) ao conteúdo baseado no Windows Media, você garante que o Player possa identificar o conteúdo associado ao seu serviço.</span><span class="sxs-lookup"><span data-stu-id="d3587-116">By adding your online store key name as the value for the **ContentDistributor** (which is an alias for the Windows Media Format SDK attribute named **WM/ContentDistributor**) attribute to your Windows Media-based content, you ensure that the Player can identify the content associated with your service.</span></span>

<span data-ttu-id="d3587-117">A adição de um valor a **ContentDistributor** também garante que o Windows Media Player criará um nó na biblioteca para o conteúdo que você fornecer.</span><span class="sxs-lookup"><span data-stu-id="d3587-117">Adding a value for **ContentDistributor** also ensures that Windows Media Player will create a node in the library for content you provide.</span></span> <span data-ttu-id="d3587-118">Consulte [integração de biblioteca](library-integration.md).</span><span class="sxs-lookup"><span data-stu-id="d3587-118">See [Library Integration](library-integration.md).</span></span>

<span data-ttu-id="d3587-119">Você pode especificar esse valor de duas maneiras:</span><span class="sxs-lookup"><span data-stu-id="d3587-119">You can specify this value two ways:</span></span>

-   <span data-ttu-id="d3587-120">Use o modelo de objeto do Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="d3587-120">Use the Windows Media Player object model.</span></span> <span data-ttu-id="d3587-121">Quando você faz isso, o Windows Media Player adiciona o valor que você especifica ao banco de dados de biblioteca.</span><span class="sxs-lookup"><span data-stu-id="d3587-121">When you do this, Windows Media Player adds the value you specify to the library database.</span></span> <span data-ttu-id="d3587-122">Eventualmente, o Player também gravará o valor do atributo no arquivo de mídia digital.</span><span class="sxs-lookup"><span data-stu-id="d3587-122">Eventually, the Player will also write the attribute value to the digital media file.</span></span>
-   <span data-ttu-id="d3587-123">Use o Windows Media Format SDK para adicionar programaticamente o atributo **WM/ContentDistributor** .</span><span class="sxs-lookup"><span data-stu-id="d3587-123">Use the Windows Media Format SDK to programmatically add the **WM/ContentDistributor** attribute.</span></span> <span data-ttu-id="d3587-124">Quando você faz isso, o Windows Media Player lê o valor do atributo e o adiciona ao banco de dados quando o arquivo de mídia digital é adicionado à biblioteca.</span><span class="sxs-lookup"><span data-stu-id="d3587-124">When you do this, Windows Media Player reads the attribute value and adds it to the database when the digital media file is added to the library.</span></span>

<span data-ttu-id="d3587-125">Ao criar seu objeto COM da loja online, o valor do atributo de arquivo definido para **ContentDistributor** e o valor atribuído à constante KszContentDistributorID em seuprojeto. h devem corresponder exatamente.</span><span class="sxs-lookup"><span data-stu-id="d3587-125">When creating your online store COM object, the file attribute value you set for **ContentDistributor** and the value assigned to the constant kszContentDistributorID in YourProject.h must match exactly.</span></span> <span data-ttu-id="d3587-126">Lembre-se de que você especificou esse valor constante para o objeto COM quando criou o projeto usando o assistente de projeto.</span><span class="sxs-lookup"><span data-stu-id="d3587-126">Recall that you specified this constant value for your COM object when you created the project by using the project wizard.</span></span> <span data-ttu-id="d3587-127">Você pode alterar esse valor manualmente.</span><span class="sxs-lookup"><span data-stu-id="d3587-127">You can change this value manually.</span></span> <span data-ttu-id="d3587-128">Certifique-se de usar uma cadeia de caracteres que identifique exclusivamente seu serviço.</span><span class="sxs-lookup"><span data-stu-id="d3587-128">Just be sure to use a string that uniquely identifies your service.</span></span>

## <a name="using-the-windows-media-player-object-model"></a><span data-ttu-id="d3587-129">Usando o modelo de objeto do Windows Media Player</span><span class="sxs-lookup"><span data-stu-id="d3587-129">Using the Windows Media Player Object Model</span></span>

<span data-ttu-id="d3587-130">Para especificar um valor para **ContentDistributor** usando o modelo de objeto do Windows Media Player, use o método [Media. setItemInfo](media-setiteminfo.md) .</span><span class="sxs-lookup"><span data-stu-id="d3587-130">To specify a value for **ContentDistributor** using the Windows Media Player object model, use the [Media.setItemInfo](media-setiteminfo.md) method.</span></span> <span data-ttu-id="d3587-131">O código de exemplo a seguir especifica o valor "Proseware" para **ContentDistributor** para o item de mídia em execução no momento:</span><span class="sxs-lookup"><span data-stu-id="d3587-131">The following example code specifies the value "Proseware" for **ContentDistributor** for the currently playing media item:</span></span>


```C++
// Retrieve the current media item.
var theMedia = Player.currentMedia;

//Test whether the media item was retrieved.
if(theMedia)
{
    // Set the ContentDistributor value.
    theMedia.setItemInfo("ContentDistributor", "Proseware");
}
```



## <a name="using-the-windows-media-format-sdk"></a><span data-ttu-id="d3587-132">Usando o Windows Media Format SDK</span><span class="sxs-lookup"><span data-stu-id="d3587-132">Using the Windows Media Format SDK</span></span>

<span data-ttu-id="d3587-133">O SDK do Windows Media Player inclui um arquivo C++ de exemplo, chamado SetContentDistributor. cpp, que demonstra como usar o SDK do Windows Media Format 9 Series para adicionar o atributo **WM/ContentDistributor** .</span><span class="sxs-lookup"><span data-stu-id="d3587-133">The Windows Media Player SDK includes a sample C++ file, named SetContentDistributor.cpp, which demonstrates how to use the Windows Media Format 9 Series SDK to add the **WM/ContentDistributor** attribute.</span></span> <span data-ttu-id="d3587-134">Você pode localizar esse arquivo de exemplo na pasta denominada metadados onde você instalou o SDK.</span><span class="sxs-lookup"><span data-stu-id="d3587-134">You can locate this sample file in the folder named Metadata where you installed the SDK.</span></span> <span data-ttu-id="d3587-135">Para usar esse código, você deve seguir estas etapas:</span><span class="sxs-lookup"><span data-stu-id="d3587-135">To use this code you must follow these steps:</span></span>

1.  <span data-ttu-id="d3587-136">Instale o SDK da série 9 do Windows Media Format e configure o tempo de execução conforme descrito na documentação.</span><span class="sxs-lookup"><span data-stu-id="d3587-136">Install the Windows Media Format 9 Series SDK and configure the runtime as described in the documentation.</span></span>
2.  <span data-ttu-id="d3587-137">Crie um novo projeto C++ vazio no Visual Studio e adicione o arquivo de exemplo chamado SetContentDistributor. cpp ao projeto.</span><span class="sxs-lookup"><span data-stu-id="d3587-137">Create a new empty C++ project in Visual Studio and add the sample file named SetContentDistributor.cpp to the project.</span></span>
3.  <span data-ttu-id="d3587-138">Adicione o caminho para as pastas de biblioteca do SDK do Windows Media Format 9 Series à lista de caminhos de arquivo.</span><span class="sxs-lookup"><span data-stu-id="d3587-138">Add the path to the Windows Media Format 9 Series SDK Lib folders to your list of file paths.</span></span> <span data-ttu-id="d3587-139">No menu **Ferramentas**, escolha **Opções**.</span><span class="sxs-lookup"><span data-stu-id="d3587-139">From the **Tools** menu, choose **Options**.</span></span>
4.  <span data-ttu-id="d3587-140">Na caixa de diálogo **Opções** , clique em **projetos** e, em seguida, clique em **diretórios do vc + +**.</span><span class="sxs-lookup"><span data-stu-id="d3587-140">In the **Options** dialog box, click **Projects**, and then click **VC++ Directories**.</span></span>
5.  <span data-ttu-id="d3587-141">Na caixa de listagem suspensa **Mostrar diretórios para** , clique em **arquivos de biblioteca**.</span><span class="sxs-lookup"><span data-stu-id="d3587-141">In the **Show Directories for** drop-down list box, click **Library files**.</span></span>
6.  <span data-ttu-id="d3587-142">Use os botões para adicionar os caminhos às caixas de listagem.</span><span class="sxs-lookup"><span data-stu-id="d3587-142">Use the buttons to add the paths to the list boxes.</span></span>
7.  <span data-ttu-id="d3587-143">Abra a caixa de diálogo páginas de propriedades do seu projeto.</span><span class="sxs-lookup"><span data-stu-id="d3587-143">Open the property pages dialog box for your project.</span></span> <span data-ttu-id="d3587-144">Escolha **Propriedades de configuração**, **vinculador** e, em seguida, **entrada**.</span><span class="sxs-lookup"><span data-stu-id="d3587-144">Choose **Configuration Properties**, then **Linker**, and then **Input**.</span></span> <span data-ttu-id="d3587-145">Digite "WMVCORE. lib" na caixa de texto **dependências adicionais** .</span><span class="sxs-lookup"><span data-stu-id="d3587-145">Type "wmvcore.lib" in the **Additional Dependencies** text box.</span></span>

<span data-ttu-id="d3587-146">O código de exemplo cria um programa de linha de comando.</span><span class="sxs-lookup"><span data-stu-id="d3587-146">The sample code creates a command-line program.</span></span> <span data-ttu-id="d3587-147">Os argumentos que você fornece ao executar o programa especificam o caminho para o arquivo de mídia digital a ser modificado e uma cadeia de caracteres para o valor do atributo **ContentDistributor** .</span><span class="sxs-lookup"><span data-stu-id="d3587-147">The arguments you provide when running the program specify the path to the digital media file to modify and a string for the **ContentDistributor** attribute value.</span></span> <span data-ttu-id="d3587-148">O código usa **IWMHeaderInfo:: setAttribute** para adicionar o atributo ao arquivo especificado.</span><span class="sxs-lookup"><span data-stu-id="d3587-148">The code uses **IWMHeaderInfo::SetAttribute** to add the attribute to the file you specified.</span></span> <span data-ttu-id="d3587-149">Você pode usar este exemplo como está ou usá-lo como um ponto de partida para seu próprio programa.</span><span class="sxs-lookup"><span data-stu-id="d3587-149">You can use this sample as is or use it as a starting point for your own program.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d3587-150">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="d3587-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d3587-151">**Informações comuns às lojas online tipo 1 e tipo 2**</span><span class="sxs-lookup"><span data-stu-id="d3587-151">**Information Common to Type 1 and Type 2 Online Stores**</span></span>](information-common-to-type-1-and-type-2-online-stores.md)
</dt> </dl>

 

 




