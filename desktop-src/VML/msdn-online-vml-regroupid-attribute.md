---
title: Atributo regroupid da VML
description: Atributo regroupid da VML
ms.assetid: 2fbcc8c5-6e31-4301-9fb8-c2618bb17a1b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 384703d3fc5675013de09c4e3b5dec7505cf4164
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366129"
---
# <a name="vml-regroupid-attribute"></a><span data-ttu-id="b0f1a-103">Atributo regroupid da VML</span><span class="sxs-lookup"><span data-stu-id="b0f1a-103">VML ReGroupID Attribute</span></span>

<span data-ttu-id="b0f1a-104">Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="b0f1a-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="b0f1a-105">As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.</span><span class="sxs-lookup"><span data-stu-id="b0f1a-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="b0f1a-106">A partir de dezembro de 2011, este tópico foi arquivado.</span><span class="sxs-lookup"><span data-stu-id="b0f1a-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="b0f1a-107">Como resultado, ele não é mais mantido ativamente.</span><span class="sxs-lookup"><span data-stu-id="b0f1a-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="b0f1a-108">Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="b0f1a-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="b0f1a-109">Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="b0f1a-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="b0f1a-110">Define um grupo anterior para uma forma.</span><span class="sxs-lookup"><span data-stu-id="b0f1a-110">Defines a previous group for a shape.</span></span> <span data-ttu-id="b0f1a-111">Leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="b0f1a-111">Read/write.</span></span> <span data-ttu-id="b0f1a-112">**VgInteger**.</span><span class="sxs-lookup"><span data-stu-id="b0f1a-112">**VgInteger**.</span></span>

<span data-ttu-id="b0f1a-113">**Aplica-se a**</span><span class="sxs-lookup"><span data-stu-id="b0f1a-113">**Applies To**</span></span>

[<span data-ttu-id="b0f1a-114">Forma</span><span class="sxs-lookup"><span data-stu-id="b0f1a-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="b0f1a-115">**Sintaxe de marca**</span><span class="sxs-lookup"><span data-stu-id="b0f1a-115">**Tag Syntax**</span></span>

<span data-ttu-id="b0f1a-116"><v: *Element* o:regroupid = " *expressão* " ></span><span class="sxs-lookup"><span data-stu-id="b0f1a-116"><v: *element* o:regroupid=" *expression* "></span></span>

<span data-ttu-id="b0f1a-117">**Comentários**</span><span class="sxs-lookup"><span data-stu-id="b0f1a-117">**Remarks**</span></span>

<span data-ttu-id="b0f1a-118">Um número de ID é usado para identificar grupos de formas que não são mais agrupados.</span><span class="sxs-lookup"><span data-stu-id="b0f1a-118">An ID number is used to identify groups of shapes that are no longer grouped.</span></span> <span data-ttu-id="b0f1a-119">Permite que as formas sejam reagrupadas programaticamente.</span><span class="sxs-lookup"><span data-stu-id="b0f1a-119">Allows shapes to be regrouped programmatically.</span></span>

<span data-ttu-id="b0f1a-120">*Atributo de extensões de Microsoft Office*</span><span class="sxs-lookup"><span data-stu-id="b0f1a-120">*Microsoft Office Extensions Attribute*</span></span>

<span data-ttu-id="b0f1a-121">**Exemplo**</span><span class="sxs-lookup"><span data-stu-id="b0f1a-121">**Example**</span></span>

<span data-ttu-id="b0f1a-122">A forma era parte de um grupo indicado pela ID de grupo 040754.</span><span class="sxs-lookup"><span data-stu-id="b0f1a-122">The shape was part of a group denoted by the group ID 040754.</span></span>


```HTML
   <v:shape id="rect01" ReGroupID="040754"
   fillcolor="red" strokecolor="red"
   coordorigin="-500 -500" coordsize="1000 1000"
   style="position:relative;top:0;left:0;width:100pt;height:100pt;mso-wrap-distance-top:10pt"
   path="m 5,5 l 5,195, 195,195, 195,5 x e">
   </v:shape>
```



 

 