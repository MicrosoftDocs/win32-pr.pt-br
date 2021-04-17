---
title: Atributo de visibilidade de VML
description: Atributo de visibilidade de VML
ms.assetid: 1a15335b-e7e9-4bf1-9c0c-8d2e4704f256
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7325d09f60da13f0c7c44e73b347fa579870fcd0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "105763810"
---
# <a name="vml-visibility-attribute"></a><span data-ttu-id="5db8d-103">Atributo de visibilidade de VML</span><span class="sxs-lookup"><span data-stu-id="5db8d-103">VML Visibility Attribute</span></span>

<span data-ttu-id="5db8d-104">Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="5db8d-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="5db8d-105">As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.</span><span class="sxs-lookup"><span data-stu-id="5db8d-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="5db8d-106">A partir de dezembro de 2011, este tópico foi arquivado.</span><span class="sxs-lookup"><span data-stu-id="5db8d-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="5db8d-107">Como resultado, ele não é mais mantido ativamente.</span><span class="sxs-lookup"><span data-stu-id="5db8d-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="5db8d-108">Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="5db8d-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="5db8d-109">Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="5db8d-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="5db8d-110">Determina se uma forma é exibida.</span><span class="sxs-lookup"><span data-stu-id="5db8d-110">Determines whether a shape is displayed.</span></span> <span data-ttu-id="5db8d-111">Leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="5db8d-111">Read/write.</span></span> <span data-ttu-id="5db8d-112">**Cadeia de caracteres**.</span><span class="sxs-lookup"><span data-stu-id="5db8d-112">**String**.</span></span>

<span data-ttu-id="5db8d-113">**Aplica-se a**</span><span class="sxs-lookup"><span data-stu-id="5db8d-113">**Applies To**</span></span>

[<span data-ttu-id="5db8d-114">Forma</span><span class="sxs-lookup"><span data-stu-id="5db8d-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="5db8d-115">**Sintaxe de marca**</span><span class="sxs-lookup"><span data-stu-id="5db8d-115">**Tag Syntax**</span></span>

<span data-ttu-id="5db8d-116"><v: *elemento* Style = "visibilidade: *expressão* " ></span><span class="sxs-lookup"><span data-stu-id="5db8d-116"><v: *element* style="visibility: *expression* "></span></span>

<span data-ttu-id="5db8d-117">**Sintaxe do script**</span><span class="sxs-lookup"><span data-stu-id="5db8d-117">**Script Syntax**</span></span>

<span data-ttu-id="5db8d-118">*elemento* . Style. Visibility = "*expressão*"</span><span class="sxs-lookup"><span data-stu-id="5db8d-118">*element* .style.visibility="*expression*"</span></span>

<span data-ttu-id="5db8d-119">*expressão* = de *elemento*. Style. Visibility</span><span class="sxs-lookup"><span data-stu-id="5db8d-119">*expression*=*element*.style.visibility</span></span>

<span data-ttu-id="5db8d-120">**Comentários**</span><span class="sxs-lookup"><span data-stu-id="5db8d-120">**Remarks**</span></span>

<span data-ttu-id="5db8d-121">O atributo de **visibilidade** é semelhante ao atributo de **visibilidade** HTML padrão para estilos.</span><span class="sxs-lookup"><span data-stu-id="5db8d-121">The **Visibility** attribute is similar to the standard HTML **Visibility** attribute for styles.</span></span>

<span data-ttu-id="5db8d-122">Os valores são:</span><span class="sxs-lookup"><span data-stu-id="5db8d-122">Values include:</span></span>



| <span data-ttu-id="5db8d-123">Valor</span><span class="sxs-lookup"><span data-stu-id="5db8d-123">Value</span></span>    | <span data-ttu-id="5db8d-124">Descrição</span><span class="sxs-lookup"><span data-stu-id="5db8d-124">Description</span></span>                                                                                                                                                                             |
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5db8d-125">visible</span><span class="sxs-lookup"><span data-stu-id="5db8d-125">visible</span></span>  | <span data-ttu-id="5db8d-126">A forma está visível.</span><span class="sxs-lookup"><span data-stu-id="5db8d-126">The shape is visible.</span></span>                                                                                                                                                                   |
| <span data-ttu-id="5db8d-127">oculto</span><span class="sxs-lookup"><span data-stu-id="5db8d-127">hidden</span></span>   | <span data-ttu-id="5db8d-128">A forma não é visível, mas ainda faz parte do fluxo dos objetos no navegador.</span><span class="sxs-lookup"><span data-stu-id="5db8d-128">The shape is not visible, but is still part of the flow of the objects in the browser.</span></span> <span data-ttu-id="5db8d-129">Eventos de mouse não são processados.</span><span class="sxs-lookup"><span data-stu-id="5db8d-129">Mouse events are not processed.</span></span>                                                                  |
| <span data-ttu-id="5db8d-130">inherit</span><span class="sxs-lookup"><span data-stu-id="5db8d-130">inherit</span></span>  | <span data-ttu-id="5db8d-131">Padrão.</span><span class="sxs-lookup"><span data-stu-id="5db8d-131">Default.</span></span> <span data-ttu-id="5db8d-132">O estado de visibilidade é herdado do pai da forma.</span><span class="sxs-lookup"><span data-stu-id="5db8d-132">The visibility state is inherited from the parent of the shape.</span></span> <span data-ttu-id="5db8d-133">Microsoft Office aplicativos usam somente **Inherit** e **Hidden**; todos os outros valores são mapeados para **herdar**.</span><span class="sxs-lookup"><span data-stu-id="5db8d-133">Microsoft Office applications only use **inherit** and **hidden**; any other values are mapped to **inherit**.</span></span> |
| <span data-ttu-id="5db8d-134">recolher</span><span class="sxs-lookup"><span data-stu-id="5db8d-134">collapse</span></span> | <span data-ttu-id="5db8d-135">Usado para aplicativos de edição gráfica que podem recolher grupos de formas; por exemplo, contornos.</span><span class="sxs-lookup"><span data-stu-id="5db8d-135">Used for graphical editing applications that can collapse groups of shapes; for example, outliners.</span></span>                                                                                     |



 

<span data-ttu-id="5db8d-136">*Atributo padrão da VML*</span><span class="sxs-lookup"><span data-stu-id="5db8d-136">*VML Standard Attribute*</span></span>

<span data-ttu-id="5db8d-137">**Exemplo**</span><span class="sxs-lookup"><span data-stu-id="5db8d-137">**Example**</span></span>

<span data-ttu-id="5db8d-138">O código a seguir cria uma forma, mas a torna oculta.</span><span class="sxs-lookup"><span data-stu-id="5db8d-138">The following code creates a shape but makes it hidden.</span></span> <span data-ttu-id="5db8d-139">Outros objetos no documento fluirão em lugar dele, deixando um espaço com o mesmo tamanho da forma.</span><span class="sxs-lookup"><span data-stu-id="5db8d-139">Other objects in the document will flow around it, leaving a space the same size as the shape.</span></span>


```HTML
   <v:rect id=myrect fillcolor="red"
   style="position:relative;top:1;left:1;width:20;height:20;visibility:hidden">
   </v:rect>
```



<span data-ttu-id="5db8d-140">[Exemplo de atributo Visibility](/previous-versions/bb264100(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="5db8d-140">[Visibility Attribute Example](/previous-versions/bb264100(v=vs.85)).</span></span> <span data-ttu-id="5db8d-141">(Requer o Microsoft Internet Explorer 5 ou superior.)</span><span class="sxs-lookup"><span data-stu-id="5db8d-141">(Requires Microsoft Internet Explorer 5 or greater.)</span></span>

 

 