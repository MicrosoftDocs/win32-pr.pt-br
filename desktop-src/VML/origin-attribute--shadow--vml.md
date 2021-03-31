---
title: Atributo de origem (sombra) (VML)
description: Atributo de origem (sombra) (VML)
ms.assetid: acef5134-dad6-4ba6-9d70-a9f56cd8c5ef
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 481c3df832ec08bc193db021244049fae96d9e34
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103641773"
---
# <a name="origin-attribute-shadowvml"></a><span data-ttu-id="7acd1-103">Atributo de origem (sombra) (VML)</span><span class="sxs-lookup"><span data-stu-id="7acd1-103">Origin Attribute (Shadow)(VML)</span></span>

<span data-ttu-id="7acd1-104">Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="7acd1-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="7acd1-105">As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.</span><span class="sxs-lookup"><span data-stu-id="7acd1-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="7acd1-106">A partir de dezembro de 2011, este tópico foi arquivado.</span><span class="sxs-lookup"><span data-stu-id="7acd1-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="7acd1-107">Como resultado, ele não é mais mantido ativamente.</span><span class="sxs-lookup"><span data-stu-id="7acd1-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="7acd1-108">Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="7acd1-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="7acd1-109">Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="7acd1-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="7acd1-110">Define o centro da sombra.</span><span class="sxs-lookup"><span data-stu-id="7acd1-110">Defines the center of the shadow.</span></span> <span data-ttu-id="7acd1-111">Leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="7acd1-111">Read/write.</span></span> <span data-ttu-id="7acd1-112">**VgVector2D**.</span><span class="sxs-lookup"><span data-stu-id="7acd1-112">**VgVector2D**.</span></span>

<span data-ttu-id="7acd1-113">**Aplica-se a**</span><span class="sxs-lookup"><span data-stu-id="7acd1-113">**Applies To**</span></span>

[<span data-ttu-id="7acd1-114">Shadow</span><span class="sxs-lookup"><span data-stu-id="7acd1-114">Shadow</span></span>](msdn-online-vml-shadow-element.md)

<span data-ttu-id="7acd1-115">**Sintaxe de marca**</span><span class="sxs-lookup"><span data-stu-id="7acd1-115">**Tag Syntax**</span></span>

<span data-ttu-id="7acd1-116"><v: *elemento* Origin = " *expressão* " ></span><span class="sxs-lookup"><span data-stu-id="7acd1-116"><v: *element* origin=" *expression* "></span></span>

<span data-ttu-id="7acd1-117">**Sintaxe do script**</span><span class="sxs-lookup"><span data-stu-id="7acd1-117">**Script Syntax**</span></span>

<span data-ttu-id="7acd1-118">*elemento* . Origin = "*expressão*"</span><span class="sxs-lookup"><span data-stu-id="7acd1-118">*element* .origin="*expression*"</span></span>

<span data-ttu-id="7acd1-119">*expressão* = de *elemento*. Origin</span><span class="sxs-lookup"><span data-stu-id="7acd1-119">*expression*=*element*.origin</span></span>

<span data-ttu-id="7acd1-120">**Comentários**</span><span class="sxs-lookup"><span data-stu-id="7acd1-120">**Remarks**</span></span>

<span data-ttu-id="7acd1-121">Um par de valores fracionários da forma, variando de 50% a-50%.</span><span class="sxs-lookup"><span data-stu-id="7acd1-121">A pair of fractional values of the shape, ranging from 50% to -50%.</span></span> <span data-ttu-id="7acd1-122">O valor padrão é 0,0.</span><span class="sxs-lookup"><span data-stu-id="7acd1-122">The default value is 0,0.</span></span>

<span data-ttu-id="7acd1-123">*Atributo padrão da VML*</span><span class="sxs-lookup"><span data-stu-id="7acd1-123">*VML Standard Attribute*</span></span>

<span data-ttu-id="7acd1-124">**Exemplo**</span><span class="sxs-lookup"><span data-stu-id="7acd1-124">**Example**</span></span>

<span data-ttu-id="7acd1-125">A sombra tem uma origem que está de 20% abaixo e 20% à direita da origem da forma.</span><span class="sxs-lookup"><span data-stu-id="7acd1-125">The shadow has an origin that is 20% down and 20% to the right of the shape's origin.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:shadow on="True" origin="20%,20%"/>
   </v:shape>
```



 

 