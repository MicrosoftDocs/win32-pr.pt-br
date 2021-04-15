---
title: Arquivo de definição de capa
description: Arquivo de definição de capa
ms.assetid: ed5f7c61-c830-4075-a79f-d5539454bd3b
keywords:
- Capas do Windows Media Player, arquivos de definição de capa
- capas, arquivos de definição de capa
- arquivos para capas, definição de capa
- arquivos de definição de capa, sobre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2bd06708a99a15dc9a8266278850c0507007f058
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105761280"
---
# <a name="skin-definition-file"></a><span data-ttu-id="1b8e3-107">Arquivo de definição de capa</span><span class="sxs-lookup"><span data-stu-id="1b8e3-107">Skin Definition File</span></span>

<span data-ttu-id="1b8e3-108">Os arquivos de definição de capa contêm as instruções básicas para o que a capa faz e onde outros arquivos usados pela capa podem ser encontrados.</span><span class="sxs-lookup"><span data-stu-id="1b8e3-108">Skin definition files contain the basic instructions for what the skin does and where other files used by the skin can be found.</span></span> <span data-ttu-id="1b8e3-109">Só pode haver um arquivo de definição de capa para uma capa e ele tem uma extensão de nome de arquivo. WMS.</span><span class="sxs-lookup"><span data-stu-id="1b8e3-109">There can only be one skin definition file for a skin, and it has a .wms file name extension.</span></span>

<span data-ttu-id="1b8e3-110">As instruções no arquivo de definição de capa são escritas em linguagem XML (XML), que é semelhante ao HTML.</span><span class="sxs-lookup"><span data-stu-id="1b8e3-110">The instructions in the skin definition file are written in Extensible Markup Language (XML), which is similar to HTML.</span></span> <span data-ttu-id="1b8e3-111">Se você tiver usado HTML para criar páginas da Web, verá que o XML parece familiar.</span><span class="sxs-lookup"><span data-stu-id="1b8e3-111">If you have used HTML to create webpages, you will find that XML looks familiar.</span></span>

<span data-ttu-id="1b8e3-112">O XML no arquivo de definição de capa usa um conjunto de marcas de elemento especiais para definir partes da interface do usuário de capa.</span><span class="sxs-lookup"><span data-stu-id="1b8e3-112">The XML in the skin definition file uses a set of special element tags to define parts of the skin user interface.</span></span> <span data-ttu-id="1b8e3-113">Por exemplo, o elemento [Button](button-element.md) define como um botão se comportará, onde ele vai e como será a aparência.</span><span class="sxs-lookup"><span data-stu-id="1b8e3-113">For example, the [BUTTON](button-element.md) element defines how a button will behave, where it will go, and what it will look like.</span></span>

<span data-ttu-id="1b8e3-114">Cada marca de elemento tem atributos específicos.</span><span class="sxs-lookup"><span data-stu-id="1b8e3-114">Each element tag has specific attributes.</span></span> <span data-ttu-id="1b8e3-115">Por exemplo, o elemento [Button](button-element.md) tem um atributo **Image** que define onde a imagem do botão pode ser encontrada.</span><span class="sxs-lookup"><span data-stu-id="1b8e3-115">For example, the [BUTTON](button-element.md) element has an **image** attribute that defines where the picture for the button can be found.</span></span> <span data-ttu-id="1b8e3-116">Isso é semelhante ao HTML, onde o elemento BODY terá um atributo **bgcolor** que define a cor do plano de fundo da página HTML.</span><span class="sxs-lookup"><span data-stu-id="1b8e3-116">This is similar to HTML, where the BODY element will have a **bgcolor** attribute that defines the background color of the HTML page.</span></span> <span data-ttu-id="1b8e3-117">Informações detalhadas sobre todos os elementos de capa e seus atributos estão incluídas na seção de [referência de programação de capa](skin-programming-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="1b8e3-117">Detailed information about all skin elements and their attributes is included in the [Skin Programming Reference](skin-programming-reference.md) section.</span></span>

<span data-ttu-id="1b8e3-118">O XML tem algumas regras simples que você precisa saber para criar capas.</span><span class="sxs-lookup"><span data-stu-id="1b8e3-118">XML has a few simple rules that you need to know to create skins.</span></span> <span data-ttu-id="1b8e3-119">Ao contrário do HTML, o XML exige que você siga as regras exatamente.</span><span class="sxs-lookup"><span data-stu-id="1b8e3-119">Unlike HTML, XML requires you to follow the rules exactly.</span></span>

## <a name="enclose-elements-with-angle-brackets"></a><span data-ttu-id="1b8e3-120">Incluir elementos com colchetes angulares</span><span class="sxs-lookup"><span data-stu-id="1b8e3-120">Enclose Elements with Angle Brackets</span></span>

<span data-ttu-id="1b8e3-121">Todos os elementos são colocados entre colchetes angulares; por exemplo, o elemento **Button** é digitado da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="1b8e3-121">All elements are enclosed by angle brackets; for example, the **BUTTON** element is typed like this:</span></span>


```C++
<BUTTON>

```



<span data-ttu-id="1b8e3-122">Você não precisa digitar a palavra "BUTTON" em letras maiúsculas, mas a Convenção de digitação de nomes de elementos em letras maiúsculas é usada no código de exemplo desse SDK.</span><span class="sxs-lookup"><span data-stu-id="1b8e3-122">You do not need to type the word "BUTTON" in all uppercase letters, but the convention of typing element names in all uppercase is used in the example code of this SDK.</span></span>

## <a name="put-attributes-before-the-closing-bracket"></a><span data-ttu-id="1b8e3-123">Colocar atributos antes do colchete de fechamento</span><span class="sxs-lookup"><span data-stu-id="1b8e3-123">Put Attributes Before the Closing Bracket</span></span>

<span data-ttu-id="1b8e3-124">Todos os atributos de um determinado elemento devem ser incluídos antes do colchete angular de fechamento.</span><span class="sxs-lookup"><span data-stu-id="1b8e3-124">All attributes for a particular element must be included before the closing angle bracket.</span></span> <span data-ttu-id="1b8e3-125">Um atributo consiste no nome do atributo seguido por um sinal de igual (=) e o valor do atributo entre aspas.</span><span class="sxs-lookup"><span data-stu-id="1b8e3-125">An attribute consists of the attribute name followed by an equal sign (=) and the value of the attribute in quotes.</span></span>


```C++
<BUTTON image="mypic.jpg">

```



<span data-ttu-id="1b8e3-126">Não é necessário digitar a palavra "Image" em minúsculas, mas a Convenção de digitação de nomes de atributo em minúsculas é usada no código de exemplo desse SDK.</span><span class="sxs-lookup"><span data-stu-id="1b8e3-126">You do not need to type the word "image" in lowercase, but the convention of typing attribute names in lowercase is used in the example code of this SDK.</span></span> <span data-ttu-id="1b8e3-127">Observe também que o valor do atributo é colocado entre aspas.</span><span class="sxs-lookup"><span data-stu-id="1b8e3-127">Also note that the value of the attribute is enclosed in quotation marks.</span></span>

## <a name="opening-and-closing-elements"></a><span data-ttu-id="1b8e3-128">Elementos de abertura e fechamento</span><span class="sxs-lookup"><span data-stu-id="1b8e3-128">Opening and Closing Elements</span></span>

<span data-ttu-id="1b8e3-129">Alguns elementos são agrupados dentro de outro elemento.</span><span class="sxs-lookup"><span data-stu-id="1b8e3-129">Some elements are grouped together inside another element.</span></span> <span data-ttu-id="1b8e3-130">Por exemplo, o elemento de **botão** não faz muito sentido, a menos que você use um ou mais elementos **buttonelement** com ele.</span><span class="sxs-lookup"><span data-stu-id="1b8e3-130">For example, the **BUTTONGROUP** element does not make a lot of sense unless you use one or more **BUTTONELEMENT** elements with it.</span></span> <span data-ttu-id="1b8e3-131">Para tornar o agrupamento claro, você precisa ter uma marca de abertura e de fechamento para cada elemento.</span><span class="sxs-lookup"><span data-stu-id="1b8e3-131">To make the grouping clear, you need to have an opening and closing tag for each element.</span></span> <span data-ttu-id="1b8e3-132">A marca de abertura é apenas o nome do elemento e quaisquer atributos relacionados, entre colchetes angulares.</span><span class="sxs-lookup"><span data-stu-id="1b8e3-132">The opening tag is just the element name and any related attributes, surrounded by angle brackets.</span></span> <span data-ttu-id="1b8e3-133">A marca de fechamento é o nome do elemento, precedido por uma barra (/) e, em seguida, entre colchetes angulares.</span><span class="sxs-lookup"><span data-stu-id="1b8e3-133">The closing tag is the element name, preceded by a forward slash (/), and then enclosed by angle brackets.</span></span> <span data-ttu-id="1b8e3-134">Por exemplo, a marca de abertura do elemento do tipo de **botão** tem esta aparência:</span><span class="sxs-lookup"><span data-stu-id="1b8e3-134">For example, the **BUTTONGROUP** element opening tag looks like this:</span></span>


```C++
<BUTTONGROUP>

```



<span data-ttu-id="1b8e3-135">A marca do bloco de **botões** de fechamento tem esta aparência:</span><span class="sxs-lookup"><span data-stu-id="1b8e3-135">The closing **BUTTONGROUP** tag looks like this:</span></span>


```C++
</BUTTONGROUP>

```



<span data-ttu-id="1b8e3-136">Você colocaria as marcas **buttonelement** entre as marcas de elemento do **botão** de abertura e de fechamento.</span><span class="sxs-lookup"><span data-stu-id="1b8e3-136">You would put the **BUTTONELEMENT** tags between the opening and closing **BUTTONGROUP** element tags.</span></span> <span data-ttu-id="1b8e3-137">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="1b8e3-137">For example:</span></span>


```C++
<BUTTONGROUP>
    <BUTTONELEMENT/>
    <BUTTONELEMENT/>
    <BUTTONELEMENT/>
</BUTTONGROUP>

```



## <a name="closing-off-elements"></a><span data-ttu-id="1b8e3-138">Fechando elementos</span><span class="sxs-lookup"><span data-stu-id="1b8e3-138">Closing Off Elements</span></span>

<span data-ttu-id="1b8e3-139">Se um elemento não tiver outros elementos dentro dele, você deverá colocar uma barra no final do nome do elemento logo antes do colchete angular de fechamento.</span><span class="sxs-lookup"><span data-stu-id="1b8e3-139">If an element has no other elements inside it, you must put a forward slash at the end of the element name just before the closing angle bracket.</span></span> <span data-ttu-id="1b8e3-140">Por exemplo, no código acima, cada elemento **buttonelement** tem uma barra "/" para indicar que não há outros elementos aninhados dentro dele.</span><span class="sxs-lookup"><span data-stu-id="1b8e3-140">For example, in the code above, each **BUTTONELEMENT** element has a forward slash to indicate that there are no other elements nested within it.</span></span>

<span data-ttu-id="1b8e3-141">Em outras palavras, você deve ter uma marca de elemento de fechamento ou fechar seu elemento com uma barra.</span><span class="sxs-lookup"><span data-stu-id="1b8e3-141">In other words, you must either have a closing element tag or close off your element with a forward slash.</span></span>

<span data-ttu-id="1b8e3-142">Isso está correto:</span><span class="sxs-lookup"><span data-stu-id="1b8e3-142">This is correct:</span></span>


```C++
<BUTTONGROUP>
    <BUTTONELEMENT/>
    <BUTTONELEMENT/>
</BUTTONGROUP>

```



<span data-ttu-id="1b8e3-143">Isso não está correto:</span><span class="sxs-lookup"><span data-stu-id="1b8e3-143">This is not correct:</span></span>


```C++
<BUTTONGROUP/>
    <BUTTONELEMENT/>
    <BUTTONELEMENT/>
</BUTTONGROUP>

```



<span data-ttu-id="1b8e3-144">Isso também não está correto:</span><span class="sxs-lookup"><span data-stu-id="1b8e3-144">This is also not correct:</span></span>


```C++
<BUTTONGROUP>
    <BUTTONELEMENT>
    <BUTTONELEMENT>
</BUTTONGROUP>

```



<span data-ttu-id="1b8e3-145">A seção a seguir fornece mais informações sobre arquivos de definição de capa:</span><span class="sxs-lookup"><span data-stu-id="1b8e3-145">The following section provides more information about skin definition files:</span></span>

-   [<span data-ttu-id="1b8e3-146">Estrutura do arquivo de definição de capa</span><span class="sxs-lookup"><span data-stu-id="1b8e3-146">Skin Definition File Structure</span></span>](skin-definition-file-structure.md)

## <a name="related-topics"></a><span data-ttu-id="1b8e3-147">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="1b8e3-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1b8e3-148">**Arquivos de capa**</span><span class="sxs-lookup"><span data-stu-id="1b8e3-148">**Skin Files**</span></span>](skin-files.md)
</dt> </dl>

 

 




