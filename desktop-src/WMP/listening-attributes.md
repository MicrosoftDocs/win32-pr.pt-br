---
title: Atributos de escuta
description: Atributos de escuta
ms.assetid: 51b10507-5c2e-49ca-b560-6db6a1a7ee87
keywords:
- Capas do Windows Media Player, atributos de escuta
- capas, atributos de escuta
- referência para capas, atributos de escuta
- atributos de escuta
- atributos, ouvindo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 349a549966f7fba5ea152f8f0bb002a92f6dfb8e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104498673"
---
# <a name="listening-attributes"></a><span data-ttu-id="148eb-108">Atributos de escuta</span><span class="sxs-lookup"><span data-stu-id="148eb-108">Listening Attributes</span></span>

<span data-ttu-id="148eb-109">Um atributo de escuta é usado para conectar um atributo a outro para que seu valor seja alterado toda vez que o valor do outro atributo for alterado.</span><span class="sxs-lookup"><span data-stu-id="148eb-109">A listening attribute is used to connect one attribute to another so that its value changes every time the value of the other attribute changes.</span></span>

<span data-ttu-id="148eb-110">O atributo de escuta **wmpprop:** é o mais útil.</span><span class="sxs-lookup"><span data-stu-id="148eb-110">The listening attribute **wmpprop:** is the most useful.</span></span> <span data-ttu-id="148eb-111">Se o valor de um atributo for especificado para ser o **wmpprop:** de um segundo atributo, o primeiro valor será atualizado automaticamente para refletir o segundo valor cada vez que o segundo valor for alterado.</span><span class="sxs-lookup"><span data-stu-id="148eb-111">If the value of one attribute is specified to be the **wmpprop:** of a second attribute, the first value will be automatically updated to reflect the second value each time the second value changes.</span></span>

<span data-ttu-id="148eb-112">**Exemplo:**</span><span class="sxs-lookup"><span data-stu-id="148eb-112">**Example:**</span></span>


```C++
<TEXT
  value="wmpprop:mySlider.value"
/>

```



<span data-ttu-id="148eb-113">Dessa forma, o valor de mydeslizer, mostrado pela posição do controle deslizante, também pode ser mostrado como um número dentro de uma caixa de texto.</span><span class="sxs-lookup"><span data-stu-id="148eb-113">In this way, the value of mySlider, shown by the position of the slider control, can also be shown as a number within a text box.</span></span>

<span data-ttu-id="148eb-114">Os dois outros atributos de escuta, **wmpenabled:** e **wmpdisabled:**, podem ser usados para alterar o atributo **habilitado** de um controle dependendo se sua funcionalidade está disponível no Player no momento.</span><span class="sxs-lookup"><span data-stu-id="148eb-114">The two other listening attributes, **wmpenabled:** and **wmpdisabled:**, can be used to change the **enabled** attribute of a control depending on whether its functionality is currently available in the player.</span></span> <span data-ttu-id="148eb-115">Esses atributos podem escutar somente para métodos do objeto **Controls** .</span><span class="sxs-lookup"><span data-stu-id="148eb-115">These attributes can listen only to methods of the **Controls** object.</span></span>

<span data-ttu-id="148eb-116">**Exemplo:**</span><span class="sxs-lookup"><span data-stu-id="148eb-116">**Example:**</span></span>


```C++
<BUTTON 
  id="play" 
  enabled="wmpenabled:player.controls.play"
/>

```



## <a name="related-topics"></a><span data-ttu-id="148eb-117">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="148eb-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="148eb-118">**Diversos**</span><span class="sxs-lookup"><span data-stu-id="148eb-118">**Miscellaneous**</span></span>](miscellaneous.md)
</dt> </dl>

 

 




