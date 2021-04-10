---
title: Atributo VML MSO-Wrap-Mode
description: Atributo VML MSO-Wrap-Mode
ms.assetid: 51c4e90d-62cc-4646-9c71-8a6bf3366b2f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5657192fcf9da72ff99dc25cff7930b6d2d9b6b9
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104294214"
---
# <a name="vml-mso-wrap-mode-attribute"></a><span data-ttu-id="894b0-103">Atributo VML MSO-Wrap-Mode</span><span class="sxs-lookup"><span data-stu-id="894b0-103">VML MSO-Wrap-Mode Attribute</span></span>

<span data-ttu-id="894b0-104">Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="894b0-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="894b0-105">As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.</span><span class="sxs-lookup"><span data-stu-id="894b0-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="894b0-106">A partir de dezembro de 2011, este tópico foi arquivado.</span><span class="sxs-lookup"><span data-stu-id="894b0-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="894b0-107">Como resultado, ele não é mais mantido ativamente.</span><span class="sxs-lookup"><span data-stu-id="894b0-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="894b0-108">Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="894b0-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="894b0-109">Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="894b0-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="894b0-110">Define o modo de disposição para texto.</span><span class="sxs-lookup"><span data-stu-id="894b0-110">Defines the wrapping mode for text.</span></span> <span data-ttu-id="894b0-111">Leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="894b0-111">Read/write.</span></span> <span data-ttu-id="894b0-112">**Cadeia de caracteres**.</span><span class="sxs-lookup"><span data-stu-id="894b0-112">**String**.</span></span>

<span data-ttu-id="894b0-113">**Aplica-se a**</span><span class="sxs-lookup"><span data-stu-id="894b0-113">**Applies To**</span></span>

[<span data-ttu-id="894b0-114">Forma</span><span class="sxs-lookup"><span data-stu-id="894b0-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="894b0-115">**Sintaxe de marca**</span><span class="sxs-lookup"><span data-stu-id="894b0-115">**Tag Syntax**</span></span>

<span data-ttu-id="894b0-116"><v: *Element* Style = "Die-Wrap-Mode: *expression* " ></span><span class="sxs-lookup"><span data-stu-id="894b0-116"><v: *element* style="mso-wrap-mode: *expression* "></span></span>

<span data-ttu-id="894b0-117">**Comentários**</span><span class="sxs-lookup"><span data-stu-id="894b0-117">**Remarks**</span></span>

<span data-ttu-id="894b0-118">Os valores são:</span><span class="sxs-lookup"><span data-stu-id="894b0-118">Values include:</span></span>



| <span data-ttu-id="894b0-119">Valor</span><span class="sxs-lookup"><span data-stu-id="894b0-119">Value</span></span>          | <span data-ttu-id="894b0-120">Descrição</span><span class="sxs-lookup"><span data-stu-id="894b0-120">Description</span></span>                          |
|----------------|--------------------------------------|
| <span data-ttu-id="894b0-121">square</span><span class="sxs-lookup"><span data-stu-id="894b0-121">square</span></span>         | <span data-ttu-id="894b0-122">Quebra o texto em uma forma em um quadrado.</span><span class="sxs-lookup"><span data-stu-id="894b0-122">Wraps text around shape in a square.</span></span> |
| <span data-ttu-id="894b0-123">rigida</span><span class="sxs-lookup"><span data-stu-id="894b0-123">tight</span></span>          | <span data-ttu-id="894b0-124">O texto é ajustado próximo à forma.</span><span class="sxs-lookup"><span data-stu-id="894b0-124">Text is wrapped close to the shape.</span></span>  |
| <span data-ttu-id="894b0-125">de cima para baixo</span><span class="sxs-lookup"><span data-stu-id="894b0-125">top-and-bottom</span></span> | <span data-ttu-id="894b0-126">O texto salta de cima para baixo.</span><span class="sxs-lookup"><span data-stu-id="894b0-126">Text jumps from top to bottom.</span></span>       |
| <span data-ttu-id="894b0-127">ao</span><span class="sxs-lookup"><span data-stu-id="894b0-127">through</span></span>        | <span data-ttu-id="894b0-128">O texto é exibido por meio da forma.</span><span class="sxs-lookup"><span data-stu-id="894b0-128">Text displays through the shape.</span></span>     |
| <span data-ttu-id="894b0-129">none</span><span class="sxs-lookup"><span data-stu-id="894b0-129">none</span></span>           | <span data-ttu-id="894b0-130">O texto não quebra.</span><span class="sxs-lookup"><span data-stu-id="894b0-130">Text doesn't wrap.</span></span>                   |



 

<span data-ttu-id="894b0-131">Usado pelo Microsoft PowerPoint para salvar em HTML para indicar se a quebra automática de texto dentro de uma AutoForma está ativada (**quadrado**) ou desativada (**nenhuma**).</span><span class="sxs-lookup"><span data-stu-id="894b0-131">Used by Microsoft PowerPoint for saving to HTML to indicate whether word wrap inside an AutoShape is on (**square**) or off (**none**).</span></span>

<span data-ttu-id="894b0-132">*Atributo de extensões de Microsoft Office*</span><span class="sxs-lookup"><span data-stu-id="894b0-132">*Microsoft Office Extensions Attribute*</span></span>

<span data-ttu-id="894b0-133">**Exemplo**</span><span class="sxs-lookup"><span data-stu-id="894b0-133">**Example**</span></span>

<span data-ttu-id="894b0-134">O código a seguir indica que a WordWrap dentro de uma AutoForma está ativada no PowerPoint.</span><span class="sxs-lookup"><span data-stu-id="894b0-134">The following code indicates that wordwrap inside an AutoShape is turned on in PowerPoint.</span></span>


```HTML
   <v:shape id="rect01"
   fillcolor="red" strokecolor="red"
   coordorigin="-500 -500" coordsize="1000 1000"
   style="position:relative;top:0;left:0;width:100pt;height:100pt;mso-wrap-mode:square"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   </v:shape>
```



 

 