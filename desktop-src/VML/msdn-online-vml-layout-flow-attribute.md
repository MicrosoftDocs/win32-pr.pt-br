---
title: Atributo Layout-Flow de VML
description: Atributo Layout-Flow de VML
ms.assetid: 63b06dcb-5179-4046-9e02-4441d0d7bcd6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e437e31043afcf7fba4967076a861c9bca86477
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103917466"
---
# <a name="vml-layout-flow-attribute"></a><span data-ttu-id="e12f6-103">Atributo Layout-Flow de VML</span><span class="sxs-lookup"><span data-stu-id="e12f6-103">VML Layout-Flow Attribute</span></span>

<span data-ttu-id="e12f6-104">Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="e12f6-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="e12f6-105">As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.</span><span class="sxs-lookup"><span data-stu-id="e12f6-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="e12f6-106">A partir de dezembro de 2011, este tópico foi arquivado.</span><span class="sxs-lookup"><span data-stu-id="e12f6-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="e12f6-107">Como resultado, ele não é mais mantido ativamente.</span><span class="sxs-lookup"><span data-stu-id="e12f6-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="e12f6-108">Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="e12f6-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="e12f6-109">Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="e12f6-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="e12f6-110">Determina o fluxo do layout de texto em uma caixa de texto.</span><span class="sxs-lookup"><span data-stu-id="e12f6-110">Determines the flow of the text layout in a textbox.</span></span> <span data-ttu-id="e12f6-111">Leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="e12f6-111">Read/write.</span></span> <span data-ttu-id="e12f6-112">**Cadeia de caracteres**.</span><span class="sxs-lookup"><span data-stu-id="e12f6-112">**String**.</span></span>

<span data-ttu-id="e12f6-113">**Aplica-se a**</span><span class="sxs-lookup"><span data-stu-id="e12f6-113">**Applies To**</span></span>

[<span data-ttu-id="e12f6-114">TextBox</span><span class="sxs-lookup"><span data-stu-id="e12f6-114">TextBox</span></span>](msdn-online-vml-textbox-element.md)

<span data-ttu-id="e12f6-115">**Sintaxe de marca**</span><span class="sxs-lookup"><span data-stu-id="e12f6-115">**Tag Syntax**</span></span>

<span data-ttu-id="e12f6-116"><v: *Element* estilo = "layout-Flow: *expressão* " ></span><span class="sxs-lookup"><span data-stu-id="e12f6-116"><v: *element* style="layout-flow: *expression* "></span></span>

<span data-ttu-id="e12f6-117">**Comentários**</span><span class="sxs-lookup"><span data-stu-id="e12f6-117">**Remarks**</span></span>

<span data-ttu-id="e12f6-118">Os valores são:</span><span class="sxs-lookup"><span data-stu-id="e12f6-118">Values include:</span></span>



| <span data-ttu-id="e12f6-119">Valor</span><span class="sxs-lookup"><span data-stu-id="e12f6-119">Value</span></span>                  | <span data-ttu-id="e12f6-120">Descrição</span><span class="sxs-lookup"><span data-stu-id="e12f6-120">Description</span></span>                                 |
|------------------------|---------------------------------------------|
| <span data-ttu-id="e12f6-121">horizontal</span><span class="sxs-lookup"><span data-stu-id="e12f6-121">horizontal</span></span>             | <span data-ttu-id="e12f6-122">O texto é exibido horizontalmente.</span><span class="sxs-lookup"><span data-stu-id="e12f6-122">Text is displayed horizontally.</span></span> <span data-ttu-id="e12f6-123">Padrão.</span><span class="sxs-lookup"><span data-stu-id="e12f6-123">Default.</span></span>    |
| <span data-ttu-id="e12f6-124">vertical</span><span class="sxs-lookup"><span data-stu-id="e12f6-124">vertical</span></span>               | <span data-ttu-id="e12f6-125">O texto é exibido verticalmente.</span><span class="sxs-lookup"><span data-stu-id="e12f6-125">Text is displayed vertically.</span></span>               |
| <span data-ttu-id="e12f6-126">vertical-Ideograma</span><span class="sxs-lookup"><span data-stu-id="e12f6-126">vertical-ideographic</span></span>   | <span data-ttu-id="e12f6-127">O texto ideográficar é exibido verticalmente.</span><span class="sxs-lookup"><span data-stu-id="e12f6-127">Ideographic text is displayed vertically.</span></span>   |
| <span data-ttu-id="e12f6-128">Ideograma horizontal</span><span class="sxs-lookup"><span data-stu-id="e12f6-128">horizontal-ideographic</span></span> | <span data-ttu-id="e12f6-129">O texto ideográficar é exibido horizontalmente.</span><span class="sxs-lookup"><span data-stu-id="e12f6-129">Ideographic text is displayed horizontally.</span></span> |



 

<span data-ttu-id="e12f6-130">*Atributo padrão da VML*</span><span class="sxs-lookup"><span data-stu-id="e12f6-130">*VML Standard Attribute*</span></span>

<span data-ttu-id="e12f6-131">**Exemplo**</span><span class="sxs-lookup"><span data-stu-id="e12f6-131">**Example**</span></span>

<span data-ttu-id="e12f6-132">O fluxo de texto na TextBox fluirá verticalmente.</span><span class="sxs-lookup"><span data-stu-id="e12f6-132">The text flow in the textbox will flow vertically.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red" fillcolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <textbox string="VML text" layout-flow="vertical"/>
   </v:shape>
```



 

 