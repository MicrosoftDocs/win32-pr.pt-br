---
title: Atributo de aspecto da VML
description: Atributo de aspecto da VML
ms.assetid: 5486ed48-d28f-4bbb-b8ed-fc5a5aa12f25
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45f7cf666e9bb8d4bf3cfe0e47190a8127415ac1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103641358"
---
# <a name="vml-aspect-attribute"></a><span data-ttu-id="406ae-103">Atributo de aspecto da VML</span><span class="sxs-lookup"><span data-stu-id="406ae-103">VML Aspect Attribute</span></span>

<span data-ttu-id="406ae-104">Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="406ae-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="406ae-105">As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.</span><span class="sxs-lookup"><span data-stu-id="406ae-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="406ae-106">A partir de dezembro de 2011, este tópico foi arquivado.</span><span class="sxs-lookup"><span data-stu-id="406ae-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="406ae-107">Como resultado, ele não é mais mantido ativamente.</span><span class="sxs-lookup"><span data-stu-id="406ae-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="406ae-108">Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="406ae-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="406ae-109">Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="406ae-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="406ae-110">Especifica como a taxa de proporção da imagem de preenchimento será preservada.</span><span class="sxs-lookup"><span data-stu-id="406ae-110">Specifies how the fill image aspect ratio will be preserved.</span></span> <span data-ttu-id="406ae-111">Leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="406ae-111">Read/write.</span></span> <span data-ttu-id="406ae-112">**Cadeia de caracteres**.</span><span class="sxs-lookup"><span data-stu-id="406ae-112">**String**.</span></span>

<span data-ttu-id="406ae-113">**Aplica-se a**</span><span class="sxs-lookup"><span data-stu-id="406ae-113">**Applies To**</span></span>

[<span data-ttu-id="406ae-114">Preencher</span><span class="sxs-lookup"><span data-stu-id="406ae-114">Fill</span></span>](msdn-online-vml-fill-element.md)

<span data-ttu-id="406ae-115">**Sintaxe de marca**</span><span class="sxs-lookup"><span data-stu-id="406ae-115">**Tag Syntax**</span></span>

<span data-ttu-id="406ae-116"><v: *Element* aspecto = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="406ae-116"><v: *element* aspect=" *expression* "></span></span>

<span data-ttu-id="406ae-117">**Sintaxe do script**</span><span class="sxs-lookup"><span data-stu-id="406ae-117">**Script Syntax**</span></span>

<span data-ttu-id="406ae-118">*elemento* . Aspect = "*expressão*"</span><span class="sxs-lookup"><span data-stu-id="406ae-118">*element* .aspect="*expression*"</span></span>

<span data-ttu-id="406ae-119">*expressão* = de *elemento*. Aspect</span><span class="sxs-lookup"><span data-stu-id="406ae-119">*expression*=*element*.aspect</span></span>

<span data-ttu-id="406ae-120">**Comentários**</span><span class="sxs-lookup"><span data-stu-id="406ae-120">**Remarks**</span></span>

<span data-ttu-id="406ae-121">Os valores são:</span><span class="sxs-lookup"><span data-stu-id="406ae-121">Values include:</span></span>



| <span data-ttu-id="406ae-122">Valor</span><span class="sxs-lookup"><span data-stu-id="406ae-122">Value</span></span>   | <span data-ttu-id="406ae-123">Descrição</span><span class="sxs-lookup"><span data-stu-id="406ae-123">Description</span></span>                           |
|---------|---------------------------------------|
| <span data-ttu-id="406ae-124">ignore</span><span class="sxs-lookup"><span data-stu-id="406ae-124">ignore</span></span>  | <span data-ttu-id="406ae-125">Ignorar problemas de aspecto.</span><span class="sxs-lookup"><span data-stu-id="406ae-125">Ignore aspect issues.</span></span> <span data-ttu-id="406ae-126">Padrão.</span><span class="sxs-lookup"><span data-stu-id="406ae-126">Default.</span></span>        |
| <span data-ttu-id="406ae-127">mínimo</span><span class="sxs-lookup"><span data-stu-id="406ae-127">atleast</span></span> | <span data-ttu-id="406ae-128">A imagem é pelo menos tão grande quanto o **tamanho**.</span><span class="sxs-lookup"><span data-stu-id="406ae-128">Image is at least as big as **Size**.</span></span> |
| <span data-ttu-id="406ae-129">atmost</span><span class="sxs-lookup"><span data-stu-id="406ae-129">atmost</span></span>  | <span data-ttu-id="406ae-130">A imagem não é maior que o **tamanho**.</span><span class="sxs-lookup"><span data-stu-id="406ae-130">Image is no bigger than **Size**.</span></span>     |



 

<span data-ttu-id="406ae-131">*Atributo padrão da VML*</span><span class="sxs-lookup"><span data-stu-id="406ae-131">*VML Standard Attribute*</span></span>

<span data-ttu-id="406ae-132">**Exemplo**</span><span class="sxs-lookup"><span data-stu-id="406ae-132">**Example**</span></span>

<span data-ttu-id="406ae-133">A imagem que compõe o preenchimento é maior ou igual a um tamanho de 10 pontos em 10 pontos.</span><span class="sxs-lookup"><span data-stu-id="406ae-133">The image that makes up the fill is greater than or equal to a size of 10 points by 10 points.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill aspect="atleast" size="10pt,10pt" src="myimage.gif"/>
   </v:shape>
```



 

 