---
title: Atributo HRef (forma) (VML)
description: Atributo HRef (forma) (VML)
ms.assetid: c44b3099-df3f-42e5-ad0c-10400630e884
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ecbc0f97ca2fb9c1565b712d3677d007a62b035
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104008074"
---
# <a name="href-attribute-shapevml"></a><span data-ttu-id="17b7e-103">Atributo HRef (forma) (VML)</span><span class="sxs-lookup"><span data-stu-id="17b7e-103">HRef Attribute (Shape)(VML)</span></span>

<span data-ttu-id="17b7e-104">Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="17b7e-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="17b7e-105">As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.</span><span class="sxs-lookup"><span data-stu-id="17b7e-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="17b7e-106">A partir de dezembro de 2011, este tópico foi arquivado.</span><span class="sxs-lookup"><span data-stu-id="17b7e-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="17b7e-107">Como resultado, ele não é mais mantido ativamente.</span><span class="sxs-lookup"><span data-stu-id="17b7e-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="17b7e-108">Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="17b7e-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="17b7e-109">Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="17b7e-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="17b7e-110">Define uma URL para uma forma.</span><span class="sxs-lookup"><span data-stu-id="17b7e-110">Defines a URL for a shape.</span></span> <span data-ttu-id="17b7e-111">Quando a forma é clicada, o navegador carregará a URL.</span><span class="sxs-lookup"><span data-stu-id="17b7e-111">When the shape is clicked, the browser will load the URL.</span></span> <span data-ttu-id="17b7e-112">Leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="17b7e-112">Read/write.</span></span> <span data-ttu-id="17b7e-113">**Cadeia de caracteres**.</span><span class="sxs-lookup"><span data-stu-id="17b7e-113">**String**.</span></span>

<span data-ttu-id="17b7e-114">**Aplica-se a**</span><span class="sxs-lookup"><span data-stu-id="17b7e-114">**Applies To**</span></span>

[<span data-ttu-id="17b7e-115">Forma</span><span class="sxs-lookup"><span data-stu-id="17b7e-115">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="17b7e-116">**Sintaxe de marca**</span><span class="sxs-lookup"><span data-stu-id="17b7e-116">**Tag Syntax**</span></span>

<span data-ttu-id="17b7e-117"><v: *Element* href = " *expressão* " ></span><span class="sxs-lookup"><span data-stu-id="17b7e-117"><v: *element* href=" *expression* "></span></span>

<span data-ttu-id="17b7e-118">**Sintaxe do script**</span><span class="sxs-lookup"><span data-stu-id="17b7e-118">**Script Syntax**</span></span>

<span data-ttu-id="17b7e-119">*Element* . href = "*expressão*"</span><span class="sxs-lookup"><span data-stu-id="17b7e-119">*element* .href="*expression*"</span></span>

<span data-ttu-id="17b7e-120">*expressão* = de *Element*. href</span><span class="sxs-lookup"><span data-stu-id="17b7e-120">*expression*=*element*.href</span></span>

<span data-ttu-id="17b7e-121">**Comentários**</span><span class="sxs-lookup"><span data-stu-id="17b7e-121">**Remarks**</span></span>

<span data-ttu-id="17b7e-122">O atributo **href** é semelhante ao atributo HTML **href** padrão de âncoras.</span><span class="sxs-lookup"><span data-stu-id="17b7e-122">The **HRef** attribute is similar to the standard HTML **HRef** attribute of anchors.</span></span>

<span data-ttu-id="17b7e-123">Usar **href** torna mais fácil criar botões interessantes em uma página da Web.</span><span class="sxs-lookup"><span data-stu-id="17b7e-123">Using **HRef** makes it easy to create interesting buttons on a Web page.</span></span>

<span data-ttu-id="17b7e-124">*Atributo padrão da VML*</span><span class="sxs-lookup"><span data-stu-id="17b7e-124">*VML Standard Attribute*</span></span>

<span data-ttu-id="17b7e-125">**Exemplo**</span><span class="sxs-lookup"><span data-stu-id="17b7e-125">**Example**</span></span>

<span data-ttu-id="17b7e-126">Quando o retângulo for clicado, o navegador carregará o home page da Microsoft Corporation.</span><span class="sxs-lookup"><span data-stu-id="17b7e-126">When the rectangle is clicked, the browser will load the Microsoft Corporation home page.</span></span>


```HTML
   <v:rect id=myrect fillcolor="red"
   href="https://www.microsoft.com"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
   
```



<span data-ttu-id="17b7e-127">[Exemplo de atributo href](/previous-versions/bb229672(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="17b7e-127">[HRef Attribute Example](/previous-versions/bb229672(v=vs.85)).</span></span> <span data-ttu-id="17b7e-128">(Requer o Microsoft Internet Explorer 5 ou superior.)</span><span class="sxs-lookup"><span data-stu-id="17b7e-128">(Requires Microsoft Internet Explorer 5 or greater.)</span></span>

 

 