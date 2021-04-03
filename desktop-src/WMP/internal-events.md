---
title: Eventos internos
description: Eventos internos
ms.assetid: d99e84ec-41db-42e7-ab26-5ca6a3ba610b
keywords:
- Capas do Windows Media Player, eventos internos
- capas, eventos internos
- eventos, internos
- escrevendo código para capas, eventos internos
- eventos internos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f08ed2abca3f23a89ea6fe261a29639d671e0d58
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103916056"
---
# <a name="internal-events"></a><span data-ttu-id="d3a3f-108">Eventos internos</span><span class="sxs-lookup"><span data-stu-id="d3a3f-108">Internal Events</span></span>

<span data-ttu-id="d3a3f-109">Você pode detectar alterações que ocorrem no Windows Media Player ou alterações em sua própria aparência.</span><span class="sxs-lookup"><span data-stu-id="d3a3f-109">You can detect changes that occur in Windows Media Player or changes in your own skin.</span></span> <span data-ttu-id="d3a3f-110">Elas podem ser alterações em métodos ou propriedades de objeto do Windows Media Player, alterações em atributos de capa e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="d3a3f-110">These can be changes in Windows Media Player object properties or methods, changes in skin attributes, and so on.</span></span>

## <a name="windows-media-player-property-changes"></a><span data-ttu-id="d3a3f-111">Alterações de Propriedade do Windows Media Player</span><span class="sxs-lookup"><span data-stu-id="d3a3f-111">Windows Media Player Property Changes</span></span>

<span data-ttu-id="d3a3f-112">Você pode processar alterações no Windows Media Player usando o ouvinte wmpprop.</span><span class="sxs-lookup"><span data-stu-id="d3a3f-112">You can process changes in Windows Media Player by using the wmpprop listener.</span></span> <span data-ttu-id="d3a3f-113">Você deve configurar o ouvinte como um valor de um atributo.</span><span class="sxs-lookup"><span data-stu-id="d3a3f-113">You must set up the listener as a value of an attribute.</span></span> <span data-ttu-id="d3a3f-114">Coloque o valor entre aspas duplas e comece com a palavra "wmpprop" seguida por dois-pontos.</span><span class="sxs-lookup"><span data-stu-id="d3a3f-114">Put the value in double quotes, and start with the word "wmpprop" followed by a colon.</span></span> <span data-ttu-id="d3a3f-115">Em seguida, você inclui a propriedade que deseja escutar.</span><span class="sxs-lookup"><span data-stu-id="d3a3f-115">Then you include the property you want to listen to.</span></span> <span data-ttu-id="d3a3f-116">Quando a propriedade for alterada, o valor do atributo também será alterado.</span><span class="sxs-lookup"><span data-stu-id="d3a3f-116">When the property changes, the value of the attribute will change also.</span></span> <span data-ttu-id="d3a3f-117">Por exemplo, para que um valor do elemento Slider seja alterado sempre que o valor do atributo **CurrentPosition** for alterado, digite o seguinte:</span><span class="sxs-lookup"><span data-stu-id="d3a3f-117">For example, to have a slider element value change whenever the value of the **currentPosition** attribute changes, type the following:</span></span>


```C++
<SLIDER id="mySlider" value="wmpprop:player.Controls.currentPosition" />
```



-   <span data-ttu-id="d3a3f-118">**Importante** Não use wmpprop nos métodos do Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="d3a3f-118">**Important** Do not use wmpprop on Windows Media Player methods.</span></span> <span data-ttu-id="d3a3f-119">Podem ocorrer resultados inesperados.</span><span class="sxs-lookup"><span data-stu-id="d3a3f-119">Unexpected results may occur.</span></span>

## <a name="windows-media-player-method-changes"></a><span data-ttu-id="d3a3f-120">Alterações de método do Windows Media Player</span><span class="sxs-lookup"><span data-stu-id="d3a3f-120">Windows Media Player Method Changes</span></span>

<span data-ttu-id="d3a3f-121">Você pode fazer com que sua capa responda à disponibilidade de métodos no Windows Media Player usando wmpenabled e wmpdisabled.</span><span class="sxs-lookup"><span data-stu-id="d3a3f-121">You can make your skin respond to the availability of methods on Windows Media Player using wmpenabled and wmpdisabled.</span></span> <span data-ttu-id="d3a3f-122">Eles são usados de forma semelhante ao ouvinte wmpprop, exceto que você só pode usá-los em métodos do objeto de **controle** que são suportados pelo método **IsAvailable** .</span><span class="sxs-lookup"><span data-stu-id="d3a3f-122">These are used similarly to the wmpprop listener except that you can only use these on methods of the **Control** object that are supported by the **isAvailable** method.</span></span>

<span data-ttu-id="d3a3f-123">Por exemplo, você pode habilitar um botão somente quando o método **Play** está habilitado, usando um código como este:</span><span class="sxs-lookup"><span data-stu-id="d3a3f-123">For example, you could enable a button only when the **Play** method is enabled, using code like this:</span></span>


```C++
<BUTTON ... enabled="wmpenabled:player.Controls.Play();" />

```



-   <span data-ttu-id="d3a3f-124">**Importante** Não use wmpenabled ou wmpdisabled nas propriedades do Windows Media Player.</span><span class="sxs-lookup"><span data-stu-id="d3a3f-124">**Important** Do not use wmpenabled or wmpdisabled on Windows Media Player properties.</span></span> <span data-ttu-id="d3a3f-125">Podem ocorrer resultados inesperados.</span><span class="sxs-lookup"><span data-stu-id="d3a3f-125">Unexpected results may occur.</span></span>

## <a name="skin-attribute-changes"></a><span data-ttu-id="d3a3f-126">Alterações de atributo de aparência</span><span class="sxs-lookup"><span data-stu-id="d3a3f-126">Skin Attribute Changes</span></span>

<span data-ttu-id="d3a3f-127">Você pode responder às alterações nos atributos de capa de uma das duas maneiras, usando wmpprop ou o evento **\_ onChange** .</span><span class="sxs-lookup"><span data-stu-id="d3a3f-127">You can respond to changes in your skin attributes in one of two ways, by using wmpprop or the **\_onchange** event.</span></span>

<span data-ttu-id="d3a3f-128">Você pode usar o wmpprop para escutar alterações em sua própria aparência.</span><span class="sxs-lookup"><span data-stu-id="d3a3f-128">You can use wmpprop to listen for changes in your own skin.</span></span> <span data-ttu-id="d3a3f-129">Por exemplo, para mostrar o valor do controle deslizante em uma caixa de texto, você pode digitar o seguinte:</span><span class="sxs-lookup"><span data-stu-id="d3a3f-129">For example, to show the Slider value in a text box, you could type the following:</span></span>


```C++
<TEXT ... value="wmpprop:mySlider.value">

```



<span data-ttu-id="d3a3f-130">Você pode usar o evento **\_ onChange** para processar eventos dentro de um elemento.</span><span class="sxs-lookup"><span data-stu-id="d3a3f-130">You can use the **\_onchange** event to process events inside an element.</span></span> <span data-ttu-id="d3a3f-131">Você deve anexar o nome do atributo que deseja rastrear para **\_ onChange**.</span><span class="sxs-lookup"><span data-stu-id="d3a3f-131">You must attach the name of the attribute you want to track to **\_onchange**.</span></span> <span data-ttu-id="d3a3f-132">Por exemplo, se você quiser acompanhar o valor de uma caixa de texto, digite:</span><span class="sxs-lookup"><span data-stu-id="d3a3f-132">For example, if you want to track the value of a text box, you would type:</span></span>


```C++
value_onchange

```



<span data-ttu-id="d3a3f-133">Em seguida, você atribuiria uma cadeia de caracteres JScript que você deseja executar quando o valor for alterado.</span><span class="sxs-lookup"><span data-stu-id="d3a3f-133">You would then assign a JScript string that you want to run when the value changes.</span></span> <span data-ttu-id="d3a3f-134">Por exemplo, para responder a uma alteração no valor de uma caixa de texto que pode ser usada para ajustar o volume do Windows Media Player, digite o seguinte dentro de seu elemento de **texto** como um atributo:</span><span class="sxs-lookup"><span data-stu-id="d3a3f-134">For example, to respond to a change in the value of a text box that can be used to adjust the volume of Windows Media Player, type the following inside your **TEXT** element as an attribute:</span></span>


```C++
value_onchange = "JScript: player.Settings.Volume = myText.value"

```



## <a name="related-topics"></a><span data-ttu-id="d3a3f-135">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="d3a3f-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d3a3f-136">**Manipulando eventos**</span><span class="sxs-lookup"><span data-stu-id="d3a3f-136">**Handling Events**</span></span>](handling-events.md)
</dt> </dl>

 

 




