---
title: Adicionando uma lista de reprodução
description: Adicionando uma lista de reprodução
ms.assetid: be0c2cac-245d-4435-87d9-4f17076e005a
keywords:
- Criando capas, listas de reprodução
- Capas do Windows Media Player, listas de reprodução
- capas, listas de reprodução
- listas de reprodução, capas
- listas de reprodução de metarquivo, capas
- Listas de reprodução do metarquivo do Windows Media, capas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c42a4bc253d4b1a3ba9b8fe0f31ca16b0d522956
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105796449"
---
# <a name="adding-a-playlist"></a><span data-ttu-id="2e533-109">Adicionando uma lista de reprodução</span><span class="sxs-lookup"><span data-stu-id="2e533-109">Adding a Playlist</span></span>

<span data-ttu-id="2e533-110">Você pode usar as listas de reprodução para escolher entre coleções de áudio e vídeo.</span><span class="sxs-lookup"><span data-stu-id="2e533-110">You can use playlists to choose from collections of your audio and video.</span></span>

<span data-ttu-id="2e533-111">Usando a arte de sua primeira capa, você pode fazer algumas alterações no arquivo de definição de capa.</span><span class="sxs-lookup"><span data-stu-id="2e533-111">Using the artwork from your first skin, you can make a few changes to the skin definition file.</span></span>

<span data-ttu-id="2e533-112">A primeira etapa é usar o shell que será usado para a maioria das capas:</span><span class="sxs-lookup"><span data-stu-id="2e533-112">The first step is to use the shell you will use for most skins:</span></span>


```C++
<THEME>
    <VIEW
        clippingColor = "#CCCC00"
        backgroundImage = "background.bmp"
        titleBar = "false">

        <BUTTONGROUP
            mappingImage = "map.bmp"
            hoverImage = "hover.bmp"> 
                
    </VIEW>


</THEME>

```



<span data-ttu-id="2e533-113">Agora, adicione uma segunda **exibição**, que contém uma lista de reprodução.</span><span class="sxs-lookup"><span data-stu-id="2e533-113">Now add a second **VIEW**, which contains a playlist.</span></span> <span data-ttu-id="2e533-114">Coloque o código a seguir após o </VIEW> do código do Shell.</span><span class="sxs-lookup"><span data-stu-id="2e533-114">Place the following code after the </VIEW> of the shell code.</span></span>


```C++
     <VIEW 
          id = "playview">
          <PLAYLIST/>
     </VIEW>

```



<span data-ttu-id="2e533-115">Você precisará dar a essa segunda exibição uma ID para que possa consultá-la mais tarde.</span><span class="sxs-lookup"><span data-stu-id="2e533-115">You will need to give this second view an ID so you can refer to it later.</span></span> <span data-ttu-id="2e533-116">Adicione um PLAYelement e um STOPelement.</span><span class="sxs-lookup"><span data-stu-id="2e533-116">Add a PLAYELEMENT and a STOPELEMENT.</span></span> <span data-ttu-id="2e533-117">Esses botões predefinidos facilitam a vida.</span><span class="sxs-lookup"><span data-stu-id="2e533-117">These predefined buttons make life easier.</span></span>


```C++
        <PLAYELEMENT
            mappingColor = "#00FF00" />
                          
        <STOPELEMENT
            mappingColor = "#FF0000" />

```



<span data-ttu-id="2e533-118">Por fim, adicione um evento OnClick ao PLAYelement para exibir uma lista de reprodução no segundo modo de exibição:</span><span class="sxs-lookup"><span data-stu-id="2e533-118">Finally, add an onClick event to the PLAYELEMENT to display a playlist in the second view:</span></span>


```C++
            onClick = "JScript: theme.openView('playview');" />

```



<span data-ttu-id="2e533-119">Você pode ver uma capa de playlist de trabalho semelhante na seção de exemplo do SDK.</span><span class="sxs-lookup"><span data-stu-id="2e533-119">You can see a similar working playlist skin in the sample section of the SDK.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2e533-120">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="2e533-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2e533-121">**Guia de criação de capa**</span><span class="sxs-lookup"><span data-stu-id="2e533-121">**Skin Creation Guide**</span></span>](skin-creation-guide.md)
</dt> </dl>

 

 




