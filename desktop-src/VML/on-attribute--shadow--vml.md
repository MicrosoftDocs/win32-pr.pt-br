---
title: Em atributo (sombra) (VML)
description: Em atributo (sombra) (VML)
ms.assetid: 234fe63e-8a4a-4067-9d05-a8990d1cee5c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83df69d8c90c99839f55836941746717a205d07a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103917512"
---
# <a name="on-attribute-shadowvml"></a><span data-ttu-id="ec703-103">Em atributo (sombra) (VML)</span><span class="sxs-lookup"><span data-stu-id="ec703-103">On Attribute (Shadow)(VML)</span></span>

<span data-ttu-id="ec703-104">Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="ec703-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="ec703-105">As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.</span><span class="sxs-lookup"><span data-stu-id="ec703-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="ec703-106">A partir de dezembro de 2011, este tópico foi arquivado.</span><span class="sxs-lookup"><span data-stu-id="ec703-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="ec703-107">Como resultado, ele não é mais mantido ativamente.</span><span class="sxs-lookup"><span data-stu-id="ec703-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="ec703-108">Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="ec703-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="ec703-109">Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="ec703-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="ec703-110">Determina se uma sombra será exibida.</span><span class="sxs-lookup"><span data-stu-id="ec703-110">Determines whether a shadow will be displayed.</span></span> <span data-ttu-id="ec703-111">Leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="ec703-111">Read/write.</span></span> <span data-ttu-id="ec703-112">**VgTriState**.</span><span class="sxs-lookup"><span data-stu-id="ec703-112">**VgTriState**.</span></span>

<span data-ttu-id="ec703-113">**Aplica-se a**</span><span class="sxs-lookup"><span data-stu-id="ec703-113">**Applies To**</span></span>

[<span data-ttu-id="ec703-114">Shadow</span><span class="sxs-lookup"><span data-stu-id="ec703-114">Shadow</span></span>](msdn-online-vml-shadow-element.md)

<span data-ttu-id="ec703-115">**Sintaxe de marca**</span><span class="sxs-lookup"><span data-stu-id="ec703-115">**Tag Syntax**</span></span>

<span data-ttu-id="ec703-116"><v: *Element* em = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="ec703-116"><v: *element* on=" *expression* "></span></span>

<span data-ttu-id="ec703-117">**Sintaxe do script**</span><span class="sxs-lookup"><span data-stu-id="ec703-117">**Script Syntax**</span></span>

<span data-ttu-id="ec703-118">*elemento* . on = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="ec703-118">*element* .on="*expression*"</span></span>

<span data-ttu-id="ec703-119">*expressão* = de *elemento*. on</span><span class="sxs-lookup"><span data-stu-id="ec703-119">*expression*=*element*.on</span></span>

<span data-ttu-id="ec703-120">**Comentários**</span><span class="sxs-lookup"><span data-stu-id="ec703-120">**Remarks**</span></span>

<span data-ttu-id="ec703-121">Se **for true**, a sombra será exibida.</span><span class="sxs-lookup"><span data-stu-id="ec703-121">If **True**, the shadow will be displayed.</span></span> <span data-ttu-id="ec703-122">O valor padrão é **Falso**.</span><span class="sxs-lookup"><span data-stu-id="ec703-122">The default value is **False**.</span></span>

<span data-ttu-id="ec703-123">*Atributo padrão da VML*</span><span class="sxs-lookup"><span data-stu-id="ec703-123">*VML Standard Attribute*</span></span>

<span data-ttu-id="ec703-124">**Exemplo**</span><span class="sxs-lookup"><span data-stu-id="ec703-124">**Example**</span></span>

<span data-ttu-id="ec703-125">A sombra será exibida.</span><span class="sxs-lookup"><span data-stu-id="ec703-125">The shadow will be displayed.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:shadow on="True"/>
   </v:shape>
```





 

 