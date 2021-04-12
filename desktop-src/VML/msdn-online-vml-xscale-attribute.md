---
title: Atributo XScale de VML
description: Atributo XScale de VML
ms.assetid: b876201d-87d1-4795-8f7f-33712a8bf493
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3221ab44cad9eb9f422ce451f618eb8eeba55bcf
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104294116"
---
# <a name="vml-xscale-attribute"></a><span data-ttu-id="2973a-103">Atributo XScale de VML</span><span class="sxs-lookup"><span data-stu-id="2973a-103">VML XScale Attribute</span></span>

<span data-ttu-id="2973a-104">Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="2973a-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="2973a-105">As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.</span><span class="sxs-lookup"><span data-stu-id="2973a-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="2973a-106">A partir de dezembro de 2011, este tópico foi arquivado.</span><span class="sxs-lookup"><span data-stu-id="2973a-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="2973a-107">Como resultado, ele não é mais mantido ativamente.</span><span class="sxs-lookup"><span data-stu-id="2973a-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="2973a-108">Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="2973a-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="2973a-109">Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="2973a-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="2973a-110">Determina se um TextPath direto será usado em vez do caminho da forma.</span><span class="sxs-lookup"><span data-stu-id="2973a-110">Determines whether a straight textpath will be used instead of the shape path.</span></span> <span data-ttu-id="2973a-111">Leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="2973a-111">Read/write.</span></span> <span data-ttu-id="2973a-112">**VgTriState**.</span><span class="sxs-lookup"><span data-stu-id="2973a-112">**VgTriState**.</span></span>

<span data-ttu-id="2973a-113">**Aplica-se a**</span><span class="sxs-lookup"><span data-stu-id="2973a-113">**Applies To**</span></span>

[<span data-ttu-id="2973a-114">TextPath</span><span class="sxs-lookup"><span data-stu-id="2973a-114">TextPath</span></span>](msdn-online-vml-textpath-element.md)

<span data-ttu-id="2973a-115">**Sintaxe de marca**</span><span class="sxs-lookup"><span data-stu-id="2973a-115">**Tag Syntax**</span></span>

<span data-ttu-id="2973a-116"><v: *Element* Style = "XScale: *expression* " ></span><span class="sxs-lookup"><span data-stu-id="2973a-116"><v: *element* style="xscale: *expression* "></span></span>

<span data-ttu-id="2973a-117">**Sintaxe do script**</span><span class="sxs-lookup"><span data-stu-id="2973a-117">**Script Syntax**</span></span>

<span data-ttu-id="2973a-118">*elemento* . Style. XScale = "*expressão*"</span><span class="sxs-lookup"><span data-stu-id="2973a-118">*element* .style.xscale="*expression*"</span></span>

<span data-ttu-id="2973a-119">*expressão* = de *elemento*. Style. XScale</span><span class="sxs-lookup"><span data-stu-id="2973a-119">*expression*=*element*.style.xscale</span></span>

<span data-ttu-id="2973a-120">**Comentários**</span><span class="sxs-lookup"><span data-stu-id="2973a-120">**Remarks**</span></span>

<span data-ttu-id="2973a-121">Se **for true**, o texto será executado ao longo do apath da esquerda para a direita ao longo do valor x do limite inferior da forma.</span><span class="sxs-lookup"><span data-stu-id="2973a-121">If **True**, the text runs along apath from left to right along the x value of the lower boundary of the shape.</span></span> <span data-ttu-id="2973a-122">O valor padrão é **Falso**.</span><span class="sxs-lookup"><span data-stu-id="2973a-122">The default value is **False**.</span></span>

<span data-ttu-id="2973a-123">*Atributo padrão da VML*</span><span class="sxs-lookup"><span data-stu-id="2973a-123">*VML Standard Attribute*</span></span>

<span data-ttu-id="2973a-124">**Exemplo**</span><span class="sxs-lookup"><span data-stu-id="2973a-124">**Example**</span></span>

<span data-ttu-id="2973a-125">O texto será exibido como se fosse desenhado em uma linha horizontal, embora o caminho da forma seja uma diagonal.</span><span class="sxs-lookup"><span data-stu-id="2973a-125">The text will appear as if it were drawn on a horizontal line, even though the shape path is a diagonal.</span></span>


```HTML
   <v:line from="100 100" to="400 400">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text"
   style="xscale:true;font:normal normal normal 36pt Arial"/>
   </v:line>
```



 

 