---
title: Atributo de modo de espaçamento da VML V-Text-mode
description: Atributo de modo de espaçamento da VML V-Text-mode
ms.assetid: 2c20e9d7-cb6a-4da7-af7a-9a7b1baa8e1f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a288f89a1405412ba8c582a5c52c7bfe56809c38
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104454328"
---
# <a name="vml-v-text-spacing-mode-attribute"></a><span data-ttu-id="58853-103">Atributo de modo de espaçamento da VML V-Text-mode</span><span class="sxs-lookup"><span data-stu-id="58853-103">VML V-Text-Spacing-Mode Attribute</span></span>

<span data-ttu-id="58853-104">Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="58853-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="58853-105">As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.</span><span class="sxs-lookup"><span data-stu-id="58853-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="58853-106">A partir de dezembro de 2011, este tópico foi arquivado.</span><span class="sxs-lookup"><span data-stu-id="58853-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="58853-107">Como resultado, ele não é mais mantido ativamente.</span><span class="sxs-lookup"><span data-stu-id="58853-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="58853-108">Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="58853-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="58853-109">Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="58853-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="58853-110">Define o modo para espaçamento.</span><span class="sxs-lookup"><span data-stu-id="58853-110">Defines the mode for letterspacing.</span></span> <span data-ttu-id="58853-111">Leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="58853-111">Read/write.</span></span> <span data-ttu-id="58853-112">**Cadeia de caracteres**.</span><span class="sxs-lookup"><span data-stu-id="58853-112">**String**.</span></span>

<span data-ttu-id="58853-113">**Aplica-se a**</span><span class="sxs-lookup"><span data-stu-id="58853-113">**Applies To**</span></span>

[<span data-ttu-id="58853-114">TextPath</span><span class="sxs-lookup"><span data-stu-id="58853-114">TextPath</span></span>](msdn-online-vml-textpath-element.md)

<span data-ttu-id="58853-115">**Sintaxe de marca**</span><span class="sxs-lookup"><span data-stu-id="58853-115">**Tag Syntax**</span></span>

<span data-ttu-id="58853-116"><v: *elemento* Style = "v-texto-Spacing-Mode: *expressão* " ></span><span class="sxs-lookup"><span data-stu-id="58853-116"><v: *element* style="v-text-spacing-mode: *expression* "></span></span>

<span data-ttu-id="58853-117">**Sintaxe do script**</span><span class="sxs-lookup"><span data-stu-id="58853-117">**Script Syntax**</span></span>

<span data-ttu-id="58853-118">*elemento* . Style. v-Text-Spacing-Mode = "*expressão*"</span><span class="sxs-lookup"><span data-stu-id="58853-118">*element* .style.v-text-spacing-mode="*expression*"</span></span>

<span data-ttu-id="58853-119">*expressão* = de *elemento*. Style. v-modo de espaçamento de texto</span><span class="sxs-lookup"><span data-stu-id="58853-119">*expression*=*element*.style.v-text-spacing-mode</span></span>

<span data-ttu-id="58853-120">**Comentários**</span><span class="sxs-lookup"><span data-stu-id="58853-120">**Remarks**</span></span>

<span data-ttu-id="58853-121">Os valores incluem</span><span class="sxs-lookup"><span data-stu-id="58853-121">Values include</span></span>

-   <span data-ttu-id="58853-122">**estreitamento** (padrão)</span><span class="sxs-lookup"><span data-stu-id="58853-122">**tightening** (default)</span></span>
-   <span data-ttu-id="58853-123">**controle alterações**</span><span class="sxs-lookup"><span data-stu-id="58853-123">**tracking**</span></span>

<span data-ttu-id="58853-124">Esse atributo determina se o espaço será removido entre cada letra (apertar) ou adicionado entre cada letra (acompanhamento).</span><span class="sxs-lookup"><span data-stu-id="58853-124">This attribute determines whether space will be removed between each letter (tightening) or added between each letter (tracking).</span></span> <span data-ttu-id="58853-125">A quantidade de alteração de espaçamento é definida pelo atributo [V-Text-Spacing](msdn-online-vml-v-text-spacing-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="58853-125">The amount of letterspacing change is defined by the [V-Text-Spacing](msdn-online-vml-v-text-spacing-attribute.md) attribute.</span></span>

<span data-ttu-id="58853-126">*Atributo padrão da VML*</span><span class="sxs-lookup"><span data-stu-id="58853-126">*VML Standard Attribute*</span></span>

<span data-ttu-id="58853-127">**Exemplo**</span><span class="sxs-lookup"><span data-stu-id="58853-127">**Example**</span></span>

<span data-ttu-id="58853-128">O espaçamento entre cada letra é aumentado em 200 unidades.</span><span class="sxs-lookup"><span data-stu-id="58853-128">The letterspacing between each letter is increased by 200 units.</span></span>


```HTML
   <v:line from="50 100" to="400 100">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text"
   style="v-text-spacing:200;v-text-spacing-mode:tracking;font:normal normal normal 36pt Arial"/>
   </v:line>
```



 

 