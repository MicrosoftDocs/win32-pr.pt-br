---
title: Atributo oculto de VML
description: Atributo oculto de VML
ms.assetid: b8cdb066-e4fc-4dd6-a55a-7c2488f89e61
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3e383061d3210c9c52dc8c89322bd617257555e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104007752"
---
# <a name="vml-obscured-attribute"></a><span data-ttu-id="c5328-103">Atributo oculto de VML</span><span class="sxs-lookup"><span data-stu-id="c5328-103">VML Obscured Attribute</span></span>

<span data-ttu-id="c5328-104">Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="c5328-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="c5328-105">As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.</span><span class="sxs-lookup"><span data-stu-id="c5328-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="c5328-106">A partir de dezembro de 2011, este tópico foi arquivado.</span><span class="sxs-lookup"><span data-stu-id="c5328-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="c5328-107">Como resultado, ele não é mais mantido ativamente.</span><span class="sxs-lookup"><span data-stu-id="c5328-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="c5328-108">Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="c5328-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="c5328-109">Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="c5328-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="c5328-110">Determina se uma sombra é transparente.</span><span class="sxs-lookup"><span data-stu-id="c5328-110">Determines whether a shadow is transparent.</span></span> <span data-ttu-id="c5328-111">Leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="c5328-111">Read/write.</span></span> <span data-ttu-id="c5328-112">**VgTriState**.</span><span class="sxs-lookup"><span data-stu-id="c5328-112">**VgTriState**.</span></span>

<span data-ttu-id="c5328-113">**Aplica-se a**</span><span class="sxs-lookup"><span data-stu-id="c5328-113">**Applies To**</span></span>

[<span data-ttu-id="c5328-114">Shadow</span><span class="sxs-lookup"><span data-stu-id="c5328-114">Shadow</span></span>](msdn-online-vml-shadow-element.md)

<span data-ttu-id="c5328-115">**Sintaxe de marca**</span><span class="sxs-lookup"><span data-stu-id="c5328-115">**Tag Syntax**</span></span>

<span data-ttu-id="c5328-116"><v: *Element* obscurecido = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="c5328-116"><v: *element* obscured=" *expression* "></span></span>

<span data-ttu-id="c5328-117">**Sintaxe do script**</span><span class="sxs-lookup"><span data-stu-id="c5328-117">**Script Syntax**</span></span>

<span data-ttu-id="c5328-118">*elemento* . obscurecido = "*expressão*"</span><span class="sxs-lookup"><span data-stu-id="c5328-118">*element* .obscured="*expression*"</span></span>

<span data-ttu-id="c5328-119">*expressão* = de *elemento*. obscurecido</span><span class="sxs-lookup"><span data-stu-id="c5328-119">*expression*=*element*.obscured</span></span>

<span data-ttu-id="c5328-120">**Comentários**</span><span class="sxs-lookup"><span data-stu-id="c5328-120">**Remarks**</span></span>

<span data-ttu-id="c5328-121">Se for **true**, permitirá que você veja por meio da sombra se não houver preenchimento da forma.</span><span class="sxs-lookup"><span data-stu-id="c5328-121">If **True**, lets you see through the shadow if there is no fill on the shape.</span></span> <span data-ttu-id="c5328-122">O padrão é **False**.</span><span class="sxs-lookup"><span data-stu-id="c5328-122">Default is **False**.</span></span>

<span data-ttu-id="c5328-123">*Atributo padrão da VML*</span><span class="sxs-lookup"><span data-stu-id="c5328-123">*VML Standard Attribute*</span></span>

<span data-ttu-id="c5328-124">**Exemplo**</span><span class="sxs-lookup"><span data-stu-id="c5328-124">**Example**</span></span>

<span data-ttu-id="c5328-125">O plano de fundo mostra a sombra.</span><span class="sxs-lookup"><span data-stu-id="c5328-125">The background shows through the shadow.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m1,1 l 1,200,200,200, 200,1 x e">
   <v:shadow on="True" obscured="True"/>
   </v:shape>
```



 

 