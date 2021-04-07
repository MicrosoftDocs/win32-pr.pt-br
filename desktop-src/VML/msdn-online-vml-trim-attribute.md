---
title: Atributo de corte de VML
description: Atributo de corte de VML
ms.assetid: c8038361-00bd-4787-9759-506a8a47b19a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25f7aa2ce17d5b2b8df772954cee323e3d5ea2db
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103823948"
---
# <a name="vml-trim-attribute"></a><span data-ttu-id="bb44e-103">Atributo de corte de VML</span><span class="sxs-lookup"><span data-stu-id="bb44e-103">VML Trim Attribute</span></span>

<span data-ttu-id="bb44e-104">Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="bb44e-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="bb44e-105">As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.</span><span class="sxs-lookup"><span data-stu-id="bb44e-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="bb44e-106">A partir de dezembro de 2011, este tópico foi arquivado.</span><span class="sxs-lookup"><span data-stu-id="bb44e-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="bb44e-107">Como resultado, ele não é mais mantido ativamente.</span><span class="sxs-lookup"><span data-stu-id="bb44e-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="bb44e-108">Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="bb44e-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="bb44e-109">Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="bb44e-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="bb44e-110">Determina se o espaço extra é removido acima e abaixo do texto.</span><span class="sxs-lookup"><span data-stu-id="bb44e-110">Determines whether extra space is removed above and below the text.</span></span> <span data-ttu-id="bb44e-111">Leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="bb44e-111">Read/write.</span></span> <span data-ttu-id="bb44e-112">**VgTriState**.</span><span class="sxs-lookup"><span data-stu-id="bb44e-112">**VgTriState**.</span></span>

<span data-ttu-id="bb44e-113">**Aplica-se a**</span><span class="sxs-lookup"><span data-stu-id="bb44e-113">**Applies To**</span></span>

[<span data-ttu-id="bb44e-114">TextPath</span><span class="sxs-lookup"><span data-stu-id="bb44e-114">TextPath</span></span>](msdn-online-vml-textpath-element.md)

<span data-ttu-id="bb44e-115">**Sintaxe de marca**</span><span class="sxs-lookup"><span data-stu-id="bb44e-115">**Tag Syntax**</span></span>

<span data-ttu-id="bb44e-116"><v: *Element* Style = "arrumar: *expression* " ></span><span class="sxs-lookup"><span data-stu-id="bb44e-116"><v: *element* style="trim: *expression* "></span></span>

<span data-ttu-id="bb44e-117">**Sintaxe do script**</span><span class="sxs-lookup"><span data-stu-id="bb44e-117">**Script Syntax**</span></span>

<span data-ttu-id="bb44e-118">*elemento* . Style. Trim = "*expressão*"</span><span class="sxs-lookup"><span data-stu-id="bb44e-118">*element* .style.trim="*expression*"</span></span>

<span data-ttu-id="bb44e-119">*expressão* = de *elemento*. Style. Trim</span><span class="sxs-lookup"><span data-stu-id="bb44e-119">*expression*=*element*.style.trim</span></span>

<span data-ttu-id="bb44e-120">**Comentários**</span><span class="sxs-lookup"><span data-stu-id="bb44e-120">**Remarks**</span></span>

<span data-ttu-id="bb44e-121">Se **for true**, o espaço reservado para ascendentes e descendentes será removido.</span><span class="sxs-lookup"><span data-stu-id="bb44e-121">If **True**, space reserved for ascenders and descenders is removed.</span></span> <span data-ttu-id="bb44e-122">O valor padrão é **Falso**.</span><span class="sxs-lookup"><span data-stu-id="bb44e-122">The default value is **False**.</span></span>

<span data-ttu-id="bb44e-123">*Atributo padrão da VML*</span><span class="sxs-lookup"><span data-stu-id="bb44e-123">*VML Standard Attribute*</span></span>

<span data-ttu-id="bb44e-124">**Exemplo**</span><span class="sxs-lookup"><span data-stu-id="bb44e-124">**Example**</span></span>

<span data-ttu-id="bb44e-125">O espaço extra acima e abaixo é cortado.</span><span class="sxs-lookup"><span data-stu-id="bb44e-125">The extra space above and below is trimmed.</span></span>


```HTML
   <v:line from="50 100" to="400 100">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text"
   style="trim:True;font:normal normal normal 36pt Arial"/>
   </v:line>
```



 

 