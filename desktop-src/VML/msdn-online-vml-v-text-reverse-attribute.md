---
title: Atributo de inversão de texto V de VML
description: Atributo de inversão de texto V de VML
ms.assetid: ad302b0f-5d93-457d-a8df-c9fce184475e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d2625439d4b7a767a21de3578a7b15d3115a8f5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104007853"
---
# <a name="vml-v-text-reverse-attribute"></a><span data-ttu-id="e71a1-103">Atributo de inversão de texto V de VML</span><span class="sxs-lookup"><span data-stu-id="e71a1-103">VML V-Text-Reverse Attribute</span></span>

<span data-ttu-id="e71a1-104">Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="e71a1-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="e71a1-105">As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.</span><span class="sxs-lookup"><span data-stu-id="e71a1-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="e71a1-106">A partir de dezembro de 2011, este tópico foi arquivado.</span><span class="sxs-lookup"><span data-stu-id="e71a1-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="e71a1-107">Como resultado, ele não é mais mantido ativamente.</span><span class="sxs-lookup"><span data-stu-id="e71a1-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="e71a1-108">Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="e71a1-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="e71a1-109">Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="e71a1-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="e71a1-110">Determina se a ordem de layout das linhas é invertida.</span><span class="sxs-lookup"><span data-stu-id="e71a1-110">Determines whether the layout order of rows is reversed.</span></span> <span data-ttu-id="e71a1-111">Leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="e71a1-111">Read/write.</span></span> <span data-ttu-id="e71a1-112">**VgTriState**.</span><span class="sxs-lookup"><span data-stu-id="e71a1-112">**VgTriState**.</span></span>

<span data-ttu-id="e71a1-113">**Aplica-se a**</span><span class="sxs-lookup"><span data-stu-id="e71a1-113">**Applies To**</span></span>

[<span data-ttu-id="e71a1-114">TextPath</span><span class="sxs-lookup"><span data-stu-id="e71a1-114">TextPath</span></span>](msdn-online-vml-textpath-element.md)

<span data-ttu-id="e71a1-115">**Sintaxe de marca**</span><span class="sxs-lookup"><span data-stu-id="e71a1-115">**Tag Syntax**</span></span>

<span data-ttu-id="e71a1-116"><v: *elemento* Style = "v-Text-Reverse: *expression* " ></span><span class="sxs-lookup"><span data-stu-id="e71a1-116"><v: *element* style="v-text-reverse: *expression* "></span></span>

<span data-ttu-id="e71a1-117">**Sintaxe do script**</span><span class="sxs-lookup"><span data-stu-id="e71a1-117">**Script Syntax**</span></span>

<span data-ttu-id="e71a1-118">*elemento* . Style. v-Text-Reverse = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="e71a1-118">*element* .style.v-text-reverse="*expression*"</span></span>

<span data-ttu-id="e71a1-119">*expressão* = de *elemento*. Style. v-texto-reverso</span><span class="sxs-lookup"><span data-stu-id="e71a1-119">*expression*=*element*.style.v-text-reverse</span></span>

<span data-ttu-id="e71a1-120">**Comentários**</span><span class="sxs-lookup"><span data-stu-id="e71a1-120">**Remarks**</span></span>

<span data-ttu-id="e71a1-121">Se **for true**, a ordem de layout das linhas será invertida.</span><span class="sxs-lookup"><span data-stu-id="e71a1-121">If **True**, the layout order of rows is reversed.</span></span> <span data-ttu-id="e71a1-122">Esse atributo é usado para layout de texto vertical.</span><span class="sxs-lookup"><span data-stu-id="e71a1-122">This attribute is used for vertical text layout.</span></span> <span data-ttu-id="e71a1-123">O valor padrão é **Falso**.</span><span class="sxs-lookup"><span data-stu-id="e71a1-123">The default value is **False**.</span></span>

<span data-ttu-id="e71a1-124">*Atributo padrão da VML*</span><span class="sxs-lookup"><span data-stu-id="e71a1-124">*VML Standard Attribute*</span></span>

<span data-ttu-id="e71a1-125">**Exemplo**</span><span class="sxs-lookup"><span data-stu-id="e71a1-125">**Example**</span></span>

<span data-ttu-id="e71a1-126">A ordem de layout é invertida.</span><span class="sxs-lookup"><span data-stu-id="e71a1-126">The layout order is reversed.</span></span>


```HTML
   <v:line from="50 100" to="400 100">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text"
   style="v-text-reverse:True;font:normal normal normal 36pt Arial"/>
   </v:line>
```



 

 