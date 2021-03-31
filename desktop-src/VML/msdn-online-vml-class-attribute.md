---
title: Atributo de classe VML
description: Atributo de classe VML
ms.assetid: 4030b8b7-fcc9-4153-8004-81935a347a09
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 94bdc723ba9be335afc43023ab89b88834c55474
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103917468"
---
# <a name="vml-class-attribute"></a><span data-ttu-id="e6321-103">Atributo de classe VML</span><span class="sxs-lookup"><span data-stu-id="e6321-103">VML Class Attribute</span></span>

<span data-ttu-id="e6321-104">Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="e6321-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="e6321-105">As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.</span><span class="sxs-lookup"><span data-stu-id="e6321-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="e6321-106">A partir de dezembro de 2011, este tópico foi arquivado.</span><span class="sxs-lookup"><span data-stu-id="e6321-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="e6321-107">Como resultado, ele não é mais mantido ativamente.</span><span class="sxs-lookup"><span data-stu-id="e6321-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="e6321-108">Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="e6321-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="e6321-109">Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="e6321-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="e6321-110">Refere-se a uma definição de um estilo CSS.</span><span class="sxs-lookup"><span data-stu-id="e6321-110">Refers to a definition of a CSS style.</span></span> <span data-ttu-id="e6321-111">Leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="e6321-111">Read/write.</span></span> <span data-ttu-id="e6321-112">**Cadeia de caracteres**.</span><span class="sxs-lookup"><span data-stu-id="e6321-112">**String**.</span></span>

<span data-ttu-id="e6321-113">**Aplica-se a**</span><span class="sxs-lookup"><span data-stu-id="e6321-113">**Applies To**</span></span>

[<span data-ttu-id="e6321-114">Forma</span><span class="sxs-lookup"><span data-stu-id="e6321-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="e6321-115">**Sintaxe de marca**</span><span class="sxs-lookup"><span data-stu-id="e6321-115">**Tag Syntax**</span></span>

<span data-ttu-id="e6321-116"><v: *Element* Class = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="e6321-116"><v: *element* class=" *expression* "></span></span>

<span data-ttu-id="e6321-117">**Sintaxe do script**</span><span class="sxs-lookup"><span data-stu-id="e6321-117">**Script Syntax**</span></span>

<span data-ttu-id="e6321-118">*Element* . ClassName = "*expressão*"</span><span class="sxs-lookup"><span data-stu-id="e6321-118">*element* .classname="*expression*"</span></span>

<span data-ttu-id="e6321-119">*expressão* = de *Element*. ClassName</span><span class="sxs-lookup"><span data-stu-id="e6321-119">*expression*=*element*.classname</span></span>

<span data-ttu-id="e6321-120">**Comentários**</span><span class="sxs-lookup"><span data-stu-id="e6321-120">**Remarks**</span></span>

<span data-ttu-id="e6321-121">O atributo de **classe** é semelhante ao atributo de **classe** HTML padrão usado com folhas de estilo CSS.</span><span class="sxs-lookup"><span data-stu-id="e6321-121">The **class** attribute is similar to the standard HTML **class** attribute used with CSS style sheets.</span></span>

<span data-ttu-id="e6321-122">Observe que **ClassName** é usado em vez de **Class** para scripts.</span><span class="sxs-lookup"><span data-stu-id="e6321-122">Note that **classname** is used instead of **class** for scripting.</span></span> <span data-ttu-id="e6321-123">Observe também que para scripts, o **ClassName** só pode ser lido; a alteração do valor de **ClassName** não alterará a renderização da forma.</span><span class="sxs-lookup"><span data-stu-id="e6321-123">Also note that for scripting, the **classname** can only be read; changing the value of **classname** will not change the rendering of the shape.</span></span>

<span data-ttu-id="e6321-124">*Atributo padrão da VML*</span><span class="sxs-lookup"><span data-stu-id="e6321-124">*VML Standard Attribute*</span></span>

<span data-ttu-id="e6321-125">**Consulte também**</span><span class="sxs-lookup"><span data-stu-id="e6321-125">**See Also**</span></span>

[<span data-ttu-id="e6321-126">Forma</span><span class="sxs-lookup"><span data-stu-id="e6321-126">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="e6321-127">**Exemplo**</span><span class="sxs-lookup"><span data-stu-id="e6321-127">**Example**</span></span>

<span data-ttu-id="e6321-128">Uma classe para **largura** é criada com o estilo</span><span class="sxs-lookup"><span data-stu-id="e6321-128">A class for **width** is created with the style</span></span>


```HTML
   .narrowstyle {width:50;height:100}
```



<span data-ttu-id="e6321-129">Em seguida, a largura é referenciada incluindo o estilo.</span><span class="sxs-lookup"><span data-stu-id="e6321-129">Then the width is referenced by including the style.</span></span> <span data-ttu-id="e6321-130">Observe que a largura andheight não está definida no atributo **Style** , mas será definida pelo estilo.</span><span class="sxs-lookup"><span data-stu-id="e6321-130">Note that the width andheight is not defined in the **style** attribute, but will be defined by the style.</span></span>


```HTML
   <v:shape id="rect01" class="narrowstyle"
   fillcolor="red" strokecolor="red"
   coordorigin="0 0" coordsize="200 200"
   style="position:relative;top:1;left:1"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   </v:shape>
```



<span data-ttu-id="e6321-131">Observe que a **classe** se aplica somente aos atributos do tipo CSS.</span><span class="sxs-lookup"><span data-stu-id="e6321-131">Note that **Class** only applies to CSS-type attributes.</span></span>

 

 