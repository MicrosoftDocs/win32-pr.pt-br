---
title: Atributo alt da VML
description: Atributo alt da VML
ms.assetid: 6b7e778c-d8e2-432e-b69a-5d80fa62d105
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b420d556e69ed2f987a3a3b10a5709f926dc5c7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104162391"
---
# <a name="vml-alt-attribute"></a><span data-ttu-id="539da-103">Atributo alt da VML</span><span class="sxs-lookup"><span data-stu-id="539da-103">VML Alt Attribute</span></span>

<span data-ttu-id="539da-104">Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="539da-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="539da-105">As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.</span><span class="sxs-lookup"><span data-stu-id="539da-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="539da-106">A partir de dezembro de 2011, este tópico foi arquivado.</span><span class="sxs-lookup"><span data-stu-id="539da-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="539da-107">Como resultado, ele não é mais mantido ativamente.</span><span class="sxs-lookup"><span data-stu-id="539da-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="539da-108">Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="539da-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="539da-109">Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="539da-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="539da-110">Define o texto alternativo a ser exibido em vez de um elemento gráfico.</span><span class="sxs-lookup"><span data-stu-id="539da-110">Defines alternative text to be displayed instead of a graphic.</span></span> <span data-ttu-id="539da-111">Leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="539da-111">Read/write.</span></span> <span data-ttu-id="539da-112">**Cadeia de caracteres**.</span><span class="sxs-lookup"><span data-stu-id="539da-112">**String**.</span></span>

<span data-ttu-id="539da-113">**Aplica-se a**</span><span class="sxs-lookup"><span data-stu-id="539da-113">**Applies To**</span></span>

[<span data-ttu-id="539da-114">Forma</span><span class="sxs-lookup"><span data-stu-id="539da-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="539da-115">**Sintaxe de marca**</span><span class="sxs-lookup"><span data-stu-id="539da-115">**Tag Syntax**</span></span>

<span data-ttu-id="539da-116"><v: *Element* Alt = " *expressão* " ></span><span class="sxs-lookup"><span data-stu-id="539da-116"><v: *element* alt=" *expression* "></span></span>

<span data-ttu-id="539da-117">**Sintaxe do script**</span><span class="sxs-lookup"><span data-stu-id="539da-117">**Script Syntax**</span></span>

<span data-ttu-id="539da-118">*Element* . Alt = "*expressão*"</span><span class="sxs-lookup"><span data-stu-id="539da-118">*element* .alt="*expression*"</span></span>

<span data-ttu-id="539da-119">*expressão* = de *elemento*. Alt</span><span class="sxs-lookup"><span data-stu-id="539da-119">*expression*=*element*.alt</span></span>

<span data-ttu-id="539da-120">**Comentários**</span><span class="sxs-lookup"><span data-stu-id="539da-120">**Remarks**</span></span>

<span data-ttu-id="539da-121">O atributo **ALT** é semelhante ao atributo HTML **ALT** padrão.</span><span class="sxs-lookup"><span data-stu-id="539da-121">The **Alt** attribute is similar to the standard HTML **Alt** attribute.</span></span> <span data-ttu-id="539da-122">Esse atributo fornece uma maneira para os navegadores que convertem texto em fala para descrever elementos gráficos em uma página.</span><span class="sxs-lookup"><span data-stu-id="539da-122">This attribute provides a way for browsers that convert text to speech to describe graphical elements on a page.</span></span>

<span data-ttu-id="539da-123">*Atributo padrão da VML*</span><span class="sxs-lookup"><span data-stu-id="539da-123">*VML Standard Attribute*</span></span>

<span data-ttu-id="539da-124">**Consulte também**</span><span class="sxs-lookup"><span data-stu-id="539da-124">**See Also**</span></span>

[<span data-ttu-id="539da-125">Forma</span><span class="sxs-lookup"><span data-stu-id="539da-125">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="539da-126">**Exemplo**</span><span class="sxs-lookup"><span data-stu-id="539da-126">**Example**</span></span>

<span data-ttu-id="539da-127">O elemento **ALT** abaixo exibirá a frase "retângulo vermelho" em navegadores que convertem páginas da Web em frases faladas.</span><span class="sxs-lookup"><span data-stu-id="539da-127">The **Alt** element below will display the phrase "Red rectangle" in browsers that convert Web pages to spoken phrases.</span></span>


```HTML
   <v:rect id=myrect fillcolor="red" alt="Red rectangle"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
```



<span data-ttu-id="539da-128">[Exemplo do atributo ALT](/previous-versions/bb229663(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="539da-128">[Alt Attribute Example](/previous-versions/bb229663(v=vs.85)).</span></span> <span data-ttu-id="539da-129">(Requer o Microsoft Internet Explorer 5 ou superior.)</span><span class="sxs-lookup"><span data-stu-id="539da-129">(Requires Microsoft Internet Explorer 5 or greater.)</span></span>

 

 