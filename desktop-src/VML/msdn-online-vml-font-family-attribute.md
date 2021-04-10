---
title: Atributo Font-Family de VML
description: Atributo Font-Family de VML
ms.assetid: 10586ae0-1480-4ffe-a690-ce8464e9bf41
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a29aa72775e8f00e195462cf3df06097d267b908
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104008342"
---
# <a name="vml-font-family-attribute"></a><span data-ttu-id="d89cf-103">Atributo Font-Family de VML</span><span class="sxs-lookup"><span data-stu-id="d89cf-103">VML Font-Family Attribute</span></span>

<span data-ttu-id="d89cf-104">Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="d89cf-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="d89cf-105">As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.</span><span class="sxs-lookup"><span data-stu-id="d89cf-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="d89cf-106">A partir de dezembro de 2011, este tópico foi arquivado.</span><span class="sxs-lookup"><span data-stu-id="d89cf-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="d89cf-107">Como resultado, ele não é mais mantido ativamente.</span><span class="sxs-lookup"><span data-stu-id="d89cf-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="d89cf-108">Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="d89cf-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="d89cf-109">Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="d89cf-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="d89cf-110">Define a família da fonte TextPath.</span><span class="sxs-lookup"><span data-stu-id="d89cf-110">Defines the family of the textpath font.</span></span> <span data-ttu-id="d89cf-111">Leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="d89cf-111">Read/write.</span></span> <span data-ttu-id="d89cf-112">**Cadeia de caracteres**.</span><span class="sxs-lookup"><span data-stu-id="d89cf-112">**String**.</span></span>

<span data-ttu-id="d89cf-113">**Aplica-se a**</span><span class="sxs-lookup"><span data-stu-id="d89cf-113">**Applies To**</span></span>

[<span data-ttu-id="d89cf-114">TextPath</span><span class="sxs-lookup"><span data-stu-id="d89cf-114">TextPath</span></span>](msdn-online-vml-textpath-element.md)

<span data-ttu-id="d89cf-115">**Sintaxe de marca**</span><span class="sxs-lookup"><span data-stu-id="d89cf-115">**Tag Syntax**</span></span>

<span data-ttu-id="d89cf-116"><v: *Element* Style = "font-family: *expression* " ></span><span class="sxs-lookup"><span data-stu-id="d89cf-116"><v: *element* style="font-family: *expression* "></span></span>

<span data-ttu-id="d89cf-117">**Sintaxe do script**</span><span class="sxs-lookup"><span data-stu-id="d89cf-117">**Script Syntax**</span></span>

<span data-ttu-id="d89cf-118">*elemento* . Style. FontFamily = "*expressão*"</span><span class="sxs-lookup"><span data-stu-id="d89cf-118">*element* .style.fontfamily="*expression*"</span></span>

<span data-ttu-id="d89cf-119">*expressão* = de *elemento*. Style. FontFamily</span><span class="sxs-lookup"><span data-stu-id="d89cf-119">*expression*=*element*.style.fontfamily</span></span>

<span data-ttu-id="d89cf-120">**Comentários**</span><span class="sxs-lookup"><span data-stu-id="d89cf-120">**Remarks**</span></span>

<span data-ttu-id="d89cf-121">Define o nome da fonte.</span><span class="sxs-lookup"><span data-stu-id="d89cf-121">Defines the font name.</span></span> <span data-ttu-id="d89cf-122">Nomes específicos como Arial podem ser usados ou tipos genéricos como serif, sans-serif, cursivo, fantasia ou monospace.</span><span class="sxs-lookup"><span data-stu-id="d89cf-122">Specific names such as Arial can be used or generic types such as serif, sans-serif, cursive, fantasy, or monospace.</span></span> <span data-ttu-id="d89cf-123">Os valores são os mesmos que os atributos de estilo HTML padrão.</span><span class="sxs-lookup"><span data-stu-id="d89cf-123">The values are the same as the standard HTML style attributes.</span></span>

<span data-ttu-id="d89cf-124">*Atributo padrão da VML*</span><span class="sxs-lookup"><span data-stu-id="d89cf-124">*VML Standard Attribute*</span></span>

<span data-ttu-id="d89cf-125">**Exemplo**</span><span class="sxs-lookup"><span data-stu-id="d89cf-125">**Example**</span></span>

<span data-ttu-id="d89cf-126">A família de fontes do texto é Arial.</span><span class="sxs-lookup"><span data-stu-id="d89cf-126">The font family of the text is Arial.</span></span>


```HTML
   <v:line from="50 100" to="400 100">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text"
   style="font:normal normal normal 36pt Arial"/>
   </v:line>
```



 

 