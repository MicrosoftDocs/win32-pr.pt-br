---
title: Atributo de opacidade (sombra) (VML)
description: Atributo de opacidade (sombra) (VML)
ms.assetid: 394d755c-72cf-46f5-a258-1844b07a97bc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d09ca038a187c4a4ed1f914f5d05bcfd63e4a4a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366146"
---
# <a name="opacity-attribute-shadowvml"></a><span data-ttu-id="77309-103">Atributo de opacidade (sombra) (VML)</span><span class="sxs-lookup"><span data-stu-id="77309-103">Opacity Attribute (Shadow)(VML)</span></span>

<span data-ttu-id="77309-104">Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="77309-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="77309-105">As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.</span><span class="sxs-lookup"><span data-stu-id="77309-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="77309-106">A partir de dezembro de 2011, este tópico foi arquivado.</span><span class="sxs-lookup"><span data-stu-id="77309-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="77309-107">Como resultado, ele não é mais mantido ativamente.</span><span class="sxs-lookup"><span data-stu-id="77309-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="77309-108">Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="77309-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="77309-109">Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="77309-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="77309-110">Determina a transparência de uma sombra.</span><span class="sxs-lookup"><span data-stu-id="77309-110">Determines the transparency of a shadow.</span></span> <span data-ttu-id="77309-111">Leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="77309-111">Read/write.</span></span> <span data-ttu-id="77309-112">[VgFraction](msdn-online-vml-vgfraction-data-type.md) .</span><span class="sxs-lookup"><span data-stu-id="77309-112">[VgFraction](msdn-online-vml-vgfraction-data-type.md) .</span></span>

<span data-ttu-id="77309-113">**Aplica-se a**</span><span class="sxs-lookup"><span data-stu-id="77309-113">**Applies To**</span></span>

[<span data-ttu-id="77309-114">Shadow</span><span class="sxs-lookup"><span data-stu-id="77309-114">Shadow</span></span>](msdn-online-vml-shadow-element.md)

<span data-ttu-id="77309-115">**Sintaxe de marca**</span><span class="sxs-lookup"><span data-stu-id="77309-115">**Tag Syntax**</span></span>

<span data-ttu-id="77309-116"><v: *elemento* Opacity = " *expressão* " ></span><span class="sxs-lookup"><span data-stu-id="77309-116"><v: *element* opacity=" *expression* "></span></span>

<span data-ttu-id="77309-117">**Sintaxe do script**</span><span class="sxs-lookup"><span data-stu-id="77309-117">**Script Syntax**</span></span>

<span data-ttu-id="77309-118">*elemento* . Opacity = "*expressão*"</span><span class="sxs-lookup"><span data-stu-id="77309-118">*element* .opacity="*expression*"</span></span>

<span data-ttu-id="77309-119">*expressão* = de *elemento*. Opacity</span><span class="sxs-lookup"><span data-stu-id="77309-119">*expression*=*element*.opacity</span></span>

<span data-ttu-id="77309-120">**Comentários**</span><span class="sxs-lookup"><span data-stu-id="77309-120">**Remarks**</span></span>

<span data-ttu-id="77309-121">O valor padrão é 1.</span><span class="sxs-lookup"><span data-stu-id="77309-121">The default value is 1.</span></span> <span data-ttu-id="77309-122">Um valor de 0 fará uma sombra completamente transparente.</span><span class="sxs-lookup"><span data-stu-id="77309-122">A value of 0 will make a completely transparent shadow.</span></span>

<span data-ttu-id="77309-123">*Atributo padrão da VML*</span><span class="sxs-lookup"><span data-stu-id="77309-123">*VML Standard Attribute*</span></span>

<span data-ttu-id="77309-124">**Exemplo**</span><span class="sxs-lookup"><span data-stu-id="77309-124">**Example**</span></span>

<span data-ttu-id="77309-125">A forma tem uma sombra que é de 50% transparente.</span><span class="sxs-lookup"><span data-stu-id="77309-125">The shape has a shadow that is 50% transparent.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor= "red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m  1,1 l 1,200,200,200, 200,1 x e">
   <v:shadow on="True" opacity="50%"/>
   </v:shape>
```



 

 