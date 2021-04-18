---
title: Lendo valores de atributo
description: Lendo valores de atributo
ms.assetid: 5f791f47-472e-409f-b716-2ace11f34742
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
- atributos, lendo valores
- lendo valores de atributo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d527429b71cff5594c127b3ad2bfb82b3f3b2ef
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105789230"
---
# <a name="reading-attribute-values"></a><span data-ttu-id="bc3fb-114">Lendo valores de atributo</span><span class="sxs-lookup"><span data-stu-id="bc3fb-114">Reading Attribute Values</span></span>

<span data-ttu-id="bc3fb-115">Os atributos que você pode encontrar na biblioteca e nos arquivos de mídia do Windows têm nomes predefinidos.</span><span class="sxs-lookup"><span data-stu-id="bc3fb-115">The attributes you can find in the library and in Windows Media files have predefined names.</span></span> <span data-ttu-id="bc3fb-116">Você pode escrever um código que recupere o valor de um atributo, passando o nome desse atributo para a *mídia*. **getItemInfo** ou *mídia*. **getItemInfoByType**.</span><span class="sxs-lookup"><span data-stu-id="bc3fb-116">You can write code that retrieves the value of one attribute by passing the name of that attribute to *Media*.**getItemInfo** or *Media*.**getItemInfoByType**.</span></span> <span data-ttu-id="bc3fb-117">Você também pode escrever um código que recupere os valores de todos os atributos em um arquivo ou item.</span><span class="sxs-lookup"><span data-stu-id="bc3fb-117">You can also write code that retrieves the values of all of the attributes in a file or item.</span></span>

<span data-ttu-id="bc3fb-118">O exemplo de C# a seguir recupera o valor do atributo **title** e o exibe em uma caixa de mensagem.</span><span class="sxs-lookup"><span data-stu-id="bc3fb-118">The following C# example retrieves the value of the **Title** attribute and displays it in a message box.</span></span> <span data-ttu-id="bc3fb-119">Neste exemplo, o objeto **Player** foi definido como AxWMPLib. AxWindowsMediaPlayer Player.</span><span class="sxs-lookup"><span data-stu-id="bc3fb-119">In this example, the **Player** object was defined as axWMPLib.AxWindowsMediaPlayer Player.</span></span>


```C++
IWMPMedia media;
string strAttribValue = "";

// Initialize the media object
media = Player.currentMedia;

// Retrieve the object's Title attribute
strAttribValue = media.getItemInfo("Title");

// Display the title
if (strAttribValue != "")
{
    MessageBox.Show("Current title: " + strAttribValue);
}

```



<span data-ttu-id="bc3fb-120">Na chamada para **getItemInfoByType**, o segundo parâmetro é uma cadeia de caracteres que especifica o idioma.</span><span class="sxs-lookup"><span data-stu-id="bc3fb-120">In the call to **getItemInfoByType**, the second parameter is a string that specifies the language.</span></span> <span data-ttu-id="bc3fb-121">Se você passar uma cadeia de caracteres vazia, conforme mostrado neste exemplo, o método recuperará o valor no idioma padrão.</span><span class="sxs-lookup"><span data-stu-id="bc3fb-121">If you pass an empty string as shown in this example, the method retrieves the value in the default language.</span></span> <span data-ttu-id="bc3fb-122">Para obter informações sobre o terceiro parâmetro, consulte [atributos com vários valores](attributes-with-multiple-values.md).</span><span class="sxs-lookup"><span data-stu-id="bc3fb-122">For information about the third parameter, see [Attributes with Multiple Values](attributes-with-multiple-values.md).</span></span>

<span data-ttu-id="bc3fb-123">O exemplo C# a seguir recupera os valores para um determinado atributo no item de mídia atual.</span><span class="sxs-lookup"><span data-stu-id="bc3fb-123">The following C# example retrieves the values for a given attribute in the current media item.</span></span> <span data-ttu-id="bc3fb-124">Ele retorna esses valores como uma cadeia de caracteres delimitada por ponto e vírgula.</span><span class="sxs-lookup"><span data-stu-id="bc3fb-124">It returns these values as a semicolon-delimited string.</span></span> <span data-ttu-id="bc3fb-125">Observe que, para os atributos representados como objetos, como o **WM/música \_ sincronizado**, o **WM/Picture** e o **WM/UserWebURL**, a função retorna uma cadeia de caracteres vazia.</span><span class="sxs-lookup"><span data-stu-id="bc3fb-125">Note that for attributes represented as objects, such as **WM/Lyrics\_Synchronised**, **WM/Picture**, and **WM/UserWebURL**, the function returns an empty string.</span></span>


```C++
private string getAttributeValues(string strAttrName, IWMPMedia3 media)
{
    string strAttrValue = "";
    int iAttrCount = 0;

    if (media != null)
    {
        // Retrieve the count of values for this attribute
        iAttrCount = media.getAttributeCountByType(strAttrName, "");

        // Retrieve the values
        for (int i = 0; i < iAttrCount; i++)
        {
            strAttrValue += media.getItemInfoByType(strAttrName, "", i);
            strAttrValue += ";";
        }
    }

    // Return the resulting string
    return strAttrValue;
}

```



<span data-ttu-id="bc3fb-126">O terceiro argumento passado para o método **getItemInfoByType** é o índice de um atributo específico em um conjunto de atributos com o mesmo nome.</span><span class="sxs-lookup"><span data-stu-id="bc3fb-126">The third argument passed to the **getItemInfoByType** method is the index of a particular attribute in a set of attributes with the same name.</span></span>

<span data-ttu-id="bc3fb-127">Você pode usar um código semelhante para recuperar atributos que têm nomes exclusivos.</span><span class="sxs-lookup"><span data-stu-id="bc3fb-127">You can use similar code to retrieve attributes that have unique names.</span></span> <span data-ttu-id="bc3fb-128">Nesses casos, **getAttributeCountByType** retorna 1.</span><span class="sxs-lookup"><span data-stu-id="bc3fb-128">In those cases, **getAttributeCountByType** returns 1.</span></span> <span data-ttu-id="bc3fb-129">No exemplo mostrado anteriormente, a chamada para **getItemInfoByType** seria executada apenas uma vez.</span><span class="sxs-lookup"><span data-stu-id="bc3fb-129">In the example shown earlier, the call to **getItemInfoByType** would execute only once.</span></span>

## <a name="related-topics"></a><span data-ttu-id="bc3fb-130">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="bc3fb-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bc3fb-131">**Alterando valores de atributo**</span><span class="sxs-lookup"><span data-stu-id="bc3fb-131">**Changing Attribute Values**</span></span>](changing-attribute-values.md)
</dt> <dt>

[<span data-ttu-id="bc3fb-132">**Atributos de item de mídia**</span><span class="sxs-lookup"><span data-stu-id="bc3fb-132">**Media Item Attributes**</span></span>](media-item-attributes.md)
</dt> <dt>

[<span data-ttu-id="bc3fb-133">**Objeto de mídia**</span><span class="sxs-lookup"><span data-stu-id="bc3fb-133">**Media Object**</span></span>](media-object.md)
</dt> <dt>

[<span data-ttu-id="bc3fb-134">**Lendo valores de atributo de um CD ou DVD**</span><span class="sxs-lookup"><span data-stu-id="bc3fb-134">**Reading Attribute Values from a CD or DVD**</span></span>](reading-attribute-values-from-a-cd-or-dvd.md)
</dt> </dl>

 

 




