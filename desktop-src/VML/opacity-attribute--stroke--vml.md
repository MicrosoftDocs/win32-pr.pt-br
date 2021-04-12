---
title: Atributo de opacidade (traço) (VML)
description: Atributo de opacidade (traço) (VML)
ms.assetid: 8f1968ba-0d0b-4cd6-9332-74755e891783
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5cc97f445ede54676d73e95a60ec039ab214f4a5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104454325"
---
# <a name="opacity-attribute-strokevml"></a><span data-ttu-id="63a7e-103">Atributo de opacidade (traço) (VML)</span><span class="sxs-lookup"><span data-stu-id="63a7e-103">Opacity Attribute (Stroke)(VML)</span></span>

<span data-ttu-id="63a7e-104">Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="63a7e-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="63a7e-105">As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.</span><span class="sxs-lookup"><span data-stu-id="63a7e-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="63a7e-106">A partir de dezembro de 2011, este tópico foi arquivado.</span><span class="sxs-lookup"><span data-stu-id="63a7e-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="63a7e-107">Como resultado, ele não é mais mantido ativamente.</span><span class="sxs-lookup"><span data-stu-id="63a7e-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="63a7e-108">Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="63a7e-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="63a7e-109">Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="63a7e-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="63a7e-110">Define a quantidade de transparência de um traço.</span><span class="sxs-lookup"><span data-stu-id="63a7e-110">Defines the amount of transparency of a stroke.</span></span> <span data-ttu-id="63a7e-111">Leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="63a7e-111">Read/write.</span></span> <span data-ttu-id="63a7e-112">**VgFraction**.</span><span class="sxs-lookup"><span data-stu-id="63a7e-112">**VgFraction**.</span></span>

<span data-ttu-id="63a7e-113">**Aplica-se a**</span><span class="sxs-lookup"><span data-stu-id="63a7e-113">**Applies To**</span></span>

[<span data-ttu-id="63a7e-114">Pincel</span><span class="sxs-lookup"><span data-stu-id="63a7e-114">Stroke</span></span>](msdn-online-vml-stroke-element.md)

<span data-ttu-id="63a7e-115">**Sintaxe de marca**</span><span class="sxs-lookup"><span data-stu-id="63a7e-115">**Tag Syntax**</span></span>

<span data-ttu-id="63a7e-116"><v: *elemento* Opacity = " *expressão* " ></span><span class="sxs-lookup"><span data-stu-id="63a7e-116"><v: *element* opacity=" *expression* "></span></span>

<span data-ttu-id="63a7e-117">**Sintaxe do script**</span><span class="sxs-lookup"><span data-stu-id="63a7e-117">**Script Syntax**</span></span>

<span data-ttu-id="63a7e-118">*elemento* . Opacity = "*expressão*"</span><span class="sxs-lookup"><span data-stu-id="63a7e-118">*element* .opacity="*expression*"</span></span>

<span data-ttu-id="63a7e-119">*expressão* = de *elemento*. Opacity</span><span class="sxs-lookup"><span data-stu-id="63a7e-119">*expression*=*element*.opacity</span></span>

<span data-ttu-id="63a7e-120">**Comentários**</span><span class="sxs-lookup"><span data-stu-id="63a7e-120">**Remarks**</span></span>

<span data-ttu-id="63a7e-121">O valor padrão é 1.0.</span><span class="sxs-lookup"><span data-stu-id="63a7e-121">The default value is 1.0.</span></span>

<span data-ttu-id="63a7e-122">*Atributo padrão da VML*</span><span class="sxs-lookup"><span data-stu-id="63a7e-122">*VML Standard Attribute*</span></span>

<span data-ttu-id="63a7e-123">**Exemplo**</span><span class="sxs-lookup"><span data-stu-id="63a7e-123">**Example**</span></span>

<span data-ttu-id="63a7e-124">O traço é de 50% transparente.</span><span class="sxs-lookup"><span data-stu-id="63a7e-124">The stroke is 50% transparent.</span></span>


```HTML
   <v:shape id="rect01"
   strokecolor="red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:stroke opacity="50%"/>
   </v:shape>
```



 

 