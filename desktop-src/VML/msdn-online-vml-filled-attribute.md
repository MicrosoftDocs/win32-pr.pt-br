---
title: Atributo preenchido da VML
description: Atributo preenchido da VML
ms.assetid: c5a71a8d-5310-4e58-9153-c5cc64b0a5e0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 232d8b36b6d272c3a1ee8c17f3ddeca023ab4708
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104454332"
---
# <a name="vml-filled-attribute"></a><span data-ttu-id="db192-103">Atributo preenchido da VML</span><span class="sxs-lookup"><span data-stu-id="db192-103">VML Filled Attribute</span></span>

<span data-ttu-id="db192-104">Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="db192-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="db192-105">As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.</span><span class="sxs-lookup"><span data-stu-id="db192-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="db192-106">A partir de dezembro de 2011, este tópico foi arquivado.</span><span class="sxs-lookup"><span data-stu-id="db192-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="db192-107">Como resultado, ele não é mais mantido ativamente.</span><span class="sxs-lookup"><span data-stu-id="db192-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="db192-108">Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="db192-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="db192-109">Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="db192-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="db192-110">Determina se o caminho fechado será preenchido.</span><span class="sxs-lookup"><span data-stu-id="db192-110">Determines whether the closed path will be filled.</span></span> <span data-ttu-id="db192-111">Leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="db192-111">Read/write.</span></span> <span data-ttu-id="db192-112">**VgTriState**.</span><span class="sxs-lookup"><span data-stu-id="db192-112">**VgTriState**.</span></span>

<span data-ttu-id="db192-113">**Aplica-se a**</span><span class="sxs-lookup"><span data-stu-id="db192-113">**Applies To**</span></span>

[<span data-ttu-id="db192-114">Forma</span><span class="sxs-lookup"><span data-stu-id="db192-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="db192-115">**Sintaxe de marca**</span><span class="sxs-lookup"><span data-stu-id="db192-115">**Tag Syntax**</span></span>

<span data-ttu-id="db192-116"><v: *Element* preenchida = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="db192-116"><v: *element* filled=" *expression* "></span></span>

<span data-ttu-id="db192-117">**Sintaxe do script**</span><span class="sxs-lookup"><span data-stu-id="db192-117">**Script Syntax**</span></span>

<span data-ttu-id="db192-118">*Element* . preenchida = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="db192-118">*element* .filled="*expression*"</span></span>

<span data-ttu-id="db192-119">*expressão* = de *elemento*. preenchido</span><span class="sxs-lookup"><span data-stu-id="db192-119">*expression*=*element*.filled</span></span>

<span data-ttu-id="db192-120">**Comentários**</span><span class="sxs-lookup"><span data-stu-id="db192-120">**Remarks**</span></span>

<span data-ttu-id="db192-121">O valor é duplicado a partir do atributo **on** do elemento [Fill](msdn-online-vml-fill-element.md) .</span><span class="sxs-lookup"><span data-stu-id="db192-121">The value is duplicated from the **On** attribute of the [Fill](msdn-online-vml-fill-element.md) element.</span></span>

<span data-ttu-id="db192-122">*Atributo padrão da VML*</span><span class="sxs-lookup"><span data-stu-id="db192-122">*VML Standard Attribute*</span></span>

<span data-ttu-id="db192-123">**Exemplo**</span><span class="sxs-lookup"><span data-stu-id="db192-123">**Example**</span></span>

<span data-ttu-id="db192-124">O caminho da forma é preenchido.</span><span class="sxs-lookup"><span data-stu-id="db192-124">The shape path is filled.</span></span>


```HTML
   <v:shape id="rect01" filled="True"
   strokecolor="red" fillcolor="white"
   coordorigin="0 0" coordsize="200 200"
   style="position:relative;top:1;left:1;width:20;height:20"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   </v:shape>
```



<span data-ttu-id="db192-125">[Exemplo de atributo preenchido](/previous-versions/bb229669(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="db192-125">[Filled Attribute Example](/previous-versions/bb229669(v=vs.85)).</span></span> <span data-ttu-id="db192-126">(Requer o Microsoft Internet Explorer 5 ou superior.)</span><span class="sxs-lookup"><span data-stu-id="db192-126">(Requires Microsoft Internet Explorer 5 or greater.)</span></span>

 

 