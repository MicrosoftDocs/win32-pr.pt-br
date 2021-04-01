---
title: Alterando valores de atributo
description: Alterando valores de atributo
ms.assetid: c7dd7355-453c-44a5-9932-c41bb3ae2e40
keywords:
- Windows Media Player, atributos para itens de mídia
- Modelo de objeto do Windows Media Player, atributos para itens de mídia
- modelo de objeto, atributos para itens de mídia
- Windows Media Player Mobile, atributos para itens de mídia
- Controle ActiveX do Windows Media Player, atributos para itens de mídia
- Controle ActiveX móvel do Windows Media Player, atributos para itens de mídia
- Controle ActiveX, atributos para itens de mídia
- Biblioteca do Windows Media Player, atributos para itens de mídia
- biblioteca, atributos para itens de mídia
- atributos, alterando valores
- alterando valores de atributo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 133e004e1140bdaac19b22be8bc1c77fe9327601
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104005669"
---
# <a name="changing-attribute-values"></a><span data-ttu-id="8b988-114">Alterando valores de atributo</span><span class="sxs-lookup"><span data-stu-id="8b988-114">Changing Attribute Values</span></span>

<span data-ttu-id="8b988-115">Você pode alterar o valor de um atributo se sua página da Web ou aplicativo tiver acesso de leitura/gravação à biblioteca e o atributo puder ser lido e gravado.</span><span class="sxs-lookup"><span data-stu-id="8b988-115">You can change the value of an attribute if your webpage or application has read/write access to the library and the attribute can be both read and written.</span></span>

<span data-ttu-id="8b988-116">Você pode alterar um atributo do item de mídia atual.</span><span class="sxs-lookup"><span data-stu-id="8b988-116">You can change an attribute of the current media item.</span></span> <span data-ttu-id="8b988-117">Para alterar os atributos de vários itens de mídia, você pode atribuir cada um deles por vez ao *Player*. Propriedade **currentMedia** .</span><span class="sxs-lookup"><span data-stu-id="8b988-117">To change attributes of multiple media items, you can assign each one in turn to the *Player*.**currentMedia** property.</span></span>

<span data-ttu-id="8b988-118">Ao longo deste tópico, o objeto **Player** foi definido da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="8b988-118">Throughout this topic, the **Player** object was defined in the following manner:</span></span>


```C++
AxWMPLib.AxWindowsMediaPlayer Player;
using WMPLib;

```



<span data-ttu-id="8b988-119">Para alterar um atributo, chame o *Player*. *currentMedia*. método **setItemInfo** , conforme mostrado no exemplo de C# a seguir.</span><span class="sxs-lookup"><span data-stu-id="8b988-119">To change an attribute, call the *Player*.*currentMedia*.**setItemInfo** method as shown in the following C# example.</span></span>


```C++
IWMPMedia3 media;
// Initialize the Media object
media = Player.currentMedia;
// Set the new genre value
media.setItemInfo("WM/Genre", "My New Genre");

```



<span data-ttu-id="8b988-120">Recomendamos que você chame a *mídia*. método **isReadOnlyItem** para determinar se você pode alterar um atributo específico.</span><span class="sxs-lookup"><span data-stu-id="8b988-120">We recommend that you call the *Media*.**isReadOnlyItem** method to determine whether you can change a particular attribute.</span></span>

> [!Note]  
> <span data-ttu-id="8b988-121">Se você inserir o controle em seu aplicativo, os atributos de arquivo alterados não serão gravados no arquivo de mídia digital até que o usuário execute o Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="8b988-121">If you embed the control in your application, file attributes that you change will not be written to the digital media file until the user runs Windows Media Player.</span></span> <span data-ttu-id="8b988-122">Se você usar o controle em um aplicativo remoto escrito em C++, os atributos de arquivo alterados serão gravados no arquivo de mídia digital logo depois que você fizer as alterações.</span><span class="sxs-lookup"><span data-stu-id="8b988-122">If you use the control in a remoted application written in C++, file attributes that you change will be written to the digital media file shortly after you make the changes.</span></span> <span data-ttu-id="8b988-123">Em ambos os casos, as alterações ficam imediatamente disponíveis por meio da biblioteca.</span><span class="sxs-lookup"><span data-stu-id="8b988-123">In either case, the changes are immediately available to you through the library.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="8b988-124">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="8b988-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8b988-125">**Atributos de item de mídia**</span><span class="sxs-lookup"><span data-stu-id="8b988-125">**Media Item Attributes**</span></span>](media-item-attributes.md)
</dt> <dt>

[<span data-ttu-id="8b988-126">**Acesso à biblioteca**</span><span class="sxs-lookup"><span data-stu-id="8b988-126">**Library Access**</span></span>](library-access.md)
</dt> <dt>

[<span data-ttu-id="8b988-127">**Objeto de mídia**</span><span class="sxs-lookup"><span data-stu-id="8b988-127">**Media Object**</span></span>](media-object.md)
</dt> <dt>

[<span data-ttu-id="8b988-128">**Lendo valores de atributo**</span><span class="sxs-lookup"><span data-stu-id="8b988-128">**Reading Attribute Values**</span></span>](reading-attribute-values.md)
</dt> </dl>

 

 




