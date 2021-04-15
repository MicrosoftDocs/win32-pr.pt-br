---
title: Em atributo (Stroke) (VML)
description: Em atributo (Stroke) (VML)
ms.assetid: 8a966dc2-826b-4202-9c5c-c6afb00cd501
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1e418857db22ee1ac12a35e9b81840b89e06c00
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "105760936"
---
# <a name="on-attribute-strokevml"></a><span data-ttu-id="cf939-103">Em atributo (Stroke) (VML)</span><span class="sxs-lookup"><span data-stu-id="cf939-103">On Attribute (Stroke)(VML)</span></span>

<span data-ttu-id="cf939-104">Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="cf939-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="cf939-105">As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.</span><span class="sxs-lookup"><span data-stu-id="cf939-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="cf939-106">A partir de dezembro de 2011, este tópico foi arquivado.</span><span class="sxs-lookup"><span data-stu-id="cf939-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="cf939-107">Como resultado, ele não é mais mantido ativamente.</span><span class="sxs-lookup"><span data-stu-id="cf939-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="cf939-108">Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="cf939-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="cf939-109">Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="cf939-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="cf939-110">Determina se o traço será exibido.</span><span class="sxs-lookup"><span data-stu-id="cf939-110">Determines whether the stroke will be displayed.</span></span> <span data-ttu-id="cf939-111">Leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="cf939-111">Read/write.</span></span> <span data-ttu-id="cf939-112">**VgTriState**.</span><span class="sxs-lookup"><span data-stu-id="cf939-112">**VgTriState**.</span></span>

<span data-ttu-id="cf939-113">**Aplica-se a**</span><span class="sxs-lookup"><span data-stu-id="cf939-113">**Applies To**</span></span>

[<span data-ttu-id="cf939-114">Pincel</span><span class="sxs-lookup"><span data-stu-id="cf939-114">Stroke</span></span>](msdn-online-vml-stroke-element.md)

<span data-ttu-id="cf939-115">**Sintaxe de marca**</span><span class="sxs-lookup"><span data-stu-id="cf939-115">**Tag Syntax**</span></span>

<span data-ttu-id="cf939-116"><v: *Element* em = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="cf939-116"><v: *element* on=" *expression* "></span></span>

<span data-ttu-id="cf939-117">**Sintaxe do script**</span><span class="sxs-lookup"><span data-stu-id="cf939-117">**Script Syntax**</span></span>

<span data-ttu-id="cf939-118">*elemento* . on = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="cf939-118">*element* .on="*expression*"</span></span>

<span data-ttu-id="cf939-119">*expressão* = de *elemento*. on</span><span class="sxs-lookup"><span data-stu-id="cf939-119">*expression*=*element*.on</span></span>

<span data-ttu-id="cf939-120">**Comentários**</span><span class="sxs-lookup"><span data-stu-id="cf939-120">**Remarks**</span></span>

<span data-ttu-id="cf939-121">Se for **false**, o traço não será exibido.</span><span class="sxs-lookup"><span data-stu-id="cf939-121">If **False**, the stroke is not displayed.</span></span> <span data-ttu-id="cf939-122">O padrão é **True**.</span><span class="sxs-lookup"><span data-stu-id="cf939-122">The default is **True**.</span></span>

<span data-ttu-id="cf939-123">*Atributo padrão da VML*</span><span class="sxs-lookup"><span data-stu-id="cf939-123">*VML Standard Attribute*</span></span>

<span data-ttu-id="cf939-124">**Exemplo**</span><span class="sxs-lookup"><span data-stu-id="cf939-124">**Example**</span></span>

<span data-ttu-id="cf939-125">O traço não será exibido.</span><span class="sxs-lookup"><span data-stu-id="cf939-125">The stroke will not be displayed.</span></span>


```HTML
   <v:shape id="rect01"
   strokecolor="red" fillcolor="blue"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:stroke on="False"/>
   </v:shape>
```



 

 