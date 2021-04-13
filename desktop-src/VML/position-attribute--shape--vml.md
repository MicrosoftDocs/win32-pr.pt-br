---
title: Atributo Position (forma) (VML)
description: Atributo Position (forma) (VML)
ms.assetid: 64ffe754-298b-4cf1-a236-6a4bdcd27123
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 866c14817ff6ac741b7fb41b1331f6d9ae32d069
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366663"
---
# <a name="position-attribute-shapevml"></a><span data-ttu-id="1beb0-103">Atributo Position (forma) (VML)</span><span class="sxs-lookup"><span data-stu-id="1beb0-103">Position Attribute (Shape)(VML)</span></span>

<span data-ttu-id="1beb0-104">Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="1beb0-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="1beb0-105">As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.</span><span class="sxs-lookup"><span data-stu-id="1beb0-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="1beb0-106">A partir de dezembro de 2011, este tópico foi arquivado.</span><span class="sxs-lookup"><span data-stu-id="1beb0-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="1beb0-107">Como resultado, ele não é mais mantido ativamente.</span><span class="sxs-lookup"><span data-stu-id="1beb0-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="1beb0-108">Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="1beb0-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="1beb0-109">Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="1beb0-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="1beb0-110">Define o tipo de posicionamento usado para posicionar um elemento.</span><span class="sxs-lookup"><span data-stu-id="1beb0-110">Defines the type of positioning used to place an element.</span></span> <span data-ttu-id="1beb0-111">Leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="1beb0-111">Read/write.</span></span> <span data-ttu-id="1beb0-112">**Cadeia de caracteres**.</span><span class="sxs-lookup"><span data-stu-id="1beb0-112">**String**.</span></span>

<span data-ttu-id="1beb0-113">**Aplica-se a**</span><span class="sxs-lookup"><span data-stu-id="1beb0-113">**Applies To**</span></span>

[<span data-ttu-id="1beb0-114">Forma</span><span class="sxs-lookup"><span data-stu-id="1beb0-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="1beb0-115">**Sintaxe de marca**</span><span class="sxs-lookup"><span data-stu-id="1beb0-115">**Tag Syntax**</span></span>

<span data-ttu-id="1beb0-116"><v: *elemento* Style = "posição: *expressão* " ></span><span class="sxs-lookup"><span data-stu-id="1beb0-116"><v: *element* style="position: *expression* "></span></span>

<span data-ttu-id="1beb0-117">**Sintaxe do script**</span><span class="sxs-lookup"><span data-stu-id="1beb0-117">**Script Syntax**</span></span>

<span data-ttu-id="1beb0-118">*elemento* . Style. Position = "*expressão*"</span><span class="sxs-lookup"><span data-stu-id="1beb0-118">*element* .style.position="*expression*"</span></span>

<span data-ttu-id="1beb0-119">*expressão* = de *elemento*. Style. Position</span><span class="sxs-lookup"><span data-stu-id="1beb0-119">*expression*=*element*.style.position</span></span>

<span data-ttu-id="1beb0-120">**Comentários**</span><span class="sxs-lookup"><span data-stu-id="1beb0-120">**Remarks**</span></span>

<span data-ttu-id="1beb0-121">O atributo **Position** é semelhante ao atributo de **posição** HTML padrão usado com folhas de estilo.</span><span class="sxs-lookup"><span data-stu-id="1beb0-121">The **Position** attribute is similar to the standard HTML **Position** attribute used with style sheets.</span></span>

<span data-ttu-id="1beb0-122">Os valores são:</span><span class="sxs-lookup"><span data-stu-id="1beb0-122">Values include:</span></span>



| <span data-ttu-id="1beb0-123">Valor</span><span class="sxs-lookup"><span data-stu-id="1beb0-123">Value</span></span>    | <span data-ttu-id="1beb0-124">Descrição</span><span class="sxs-lookup"><span data-stu-id="1beb0-124">Description</span></span>                                                                                                                                                                                                               |
|----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1beb0-125">static</span><span class="sxs-lookup"><span data-stu-id="1beb0-125">static</span></span>   | <span data-ttu-id="1beb0-126">Padrão.</span><span class="sxs-lookup"><span data-stu-id="1beb0-126">Default.</span></span> <span data-ttu-id="1beb0-127">O elemento é posicionado de acordo com o fluxo normal da página.</span><span class="sxs-lookup"><span data-stu-id="1beb0-127">The element is positioned according to the normal flow of the page.</span></span> <span data-ttu-id="1beb0-128">Os atributos **superior** e **esquerdo** são ignorados.</span><span class="sxs-lookup"><span data-stu-id="1beb0-128">The **Top** and **Left** attributes are ignored.</span></span> <span data-ttu-id="1beb0-129">Se o objeto for ancorado embutido, o que acontece apenas no Microsoft Word, esse valor será usado.</span><span class="sxs-lookup"><span data-stu-id="1beb0-129">If the object is anchored inline, which only happens in Microsoft Word, this value is used.</span></span> |
| <span data-ttu-id="1beb0-130">absoluto</span><span class="sxs-lookup"><span data-stu-id="1beb0-130">absolute</span></span> | <span data-ttu-id="1beb0-131">O elemento é posicionado em relação ao pai, usando os atributos **superior** e **esquerdo** .</span><span class="sxs-lookup"><span data-stu-id="1beb0-131">The element is positioned relative to the parent, using the **Top** and **Left** attributes.</span></span> <span data-ttu-id="1beb0-132">Esse valor é usado por objetos flutuantes do Microsoft Word e do Microsoft Excel e slides do Microsoft PowerPoint.</span><span class="sxs-lookup"><span data-stu-id="1beb0-132">This value is used by Microsoft Word and Microsoft Excel floating objects, and Microsoft PowerPoint slides.</span></span>                  |
| <span data-ttu-id="1beb0-133">relative</span><span class="sxs-lookup"><span data-stu-id="1beb0-133">relative</span></span> | <span data-ttu-id="1beb0-134">O elemento é posicionado de acordo com o fluxo normal da página, mas os atributos **superior** e **esquerdo** são usados.</span><span class="sxs-lookup"><span data-stu-id="1beb0-134">The element is positioned according to the normal flow of the page, but the **Top** and **Left** attributes are used.</span></span> <span data-ttu-id="1beb0-135">A sobreposição de elementos sobrepostos é regida pelo atributo **Z-index** .</span><span class="sxs-lookup"><span data-stu-id="1beb0-135">The overlap of overlapping elements is governed by the **Z-Index** attribute.</span></span>                       |



 

<span data-ttu-id="1beb0-136">*Atributo padrão da VML*</span><span class="sxs-lookup"><span data-stu-id="1beb0-136">*VML Standard Attribute*</span></span>

<span data-ttu-id="1beb0-137">**Exemplo**</span><span class="sxs-lookup"><span data-stu-id="1beb0-137">**Example**</span></span>

<span data-ttu-id="1beb0-138">A posição do retângulo é exibida usando o estilo *relativo* .</span><span class="sxs-lookup"><span data-stu-id="1beb0-138">The position of the rectangle is displayed using the *relative* style.</span></span>


```HTML
   <v:rect id=myrect fillcolor="red"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
```



<span data-ttu-id="1beb0-139">[Exemplo de atributo de posição](/previous-versions/bb264090(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="1beb0-139">[Position Attribute Example](/previous-versions/bb264090(v=vs.85)).</span></span> <span data-ttu-id="1beb0-140">(Requer o Microsoft Internet Explorer 5 ou superior.)</span><span class="sxs-lookup"><span data-stu-id="1beb0-140">(Requires Microsoft Internet Explorer 5 or greater.)</span></span>

 

 