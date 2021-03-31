---
title: Atributo de tipo (Fill) (VML)
description: Atributo de tipo (Fill) (VML)
ms.assetid: 5dcc53cd-a156-48cd-ae32-951660d91556
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb40999b9596a41a8469e586dcc8a7f934577e36
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103641476"
---
# <a name="type-attribute-fillvml"></a><span data-ttu-id="3ec49-103">Atributo de tipo (Fill) (VML)</span><span class="sxs-lookup"><span data-stu-id="3ec49-103">Type Attribute (Fill)(VML)</span></span>

<span data-ttu-id="3ec49-104">Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="3ec49-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="3ec49-105">As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.</span><span class="sxs-lookup"><span data-stu-id="3ec49-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="3ec49-106">A partir de dezembro de 2011, este tópico foi arquivado.</span><span class="sxs-lookup"><span data-stu-id="3ec49-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="3ec49-107">Como resultado, ele não é mais mantido ativamente.</span><span class="sxs-lookup"><span data-stu-id="3ec49-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="3ec49-108">Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="3ec49-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="3ec49-109">Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="3ec49-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="3ec49-110">Determina o tipo de preenchimento.</span><span class="sxs-lookup"><span data-stu-id="3ec49-110">Determines the type of fill.</span></span> <span data-ttu-id="3ec49-111">Leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="3ec49-111">Read/write.</span></span> <span data-ttu-id="3ec49-112">**VgFillType**.</span><span class="sxs-lookup"><span data-stu-id="3ec49-112">**VgFillType**.</span></span>

<span data-ttu-id="3ec49-113">**Aplica-se a**</span><span class="sxs-lookup"><span data-stu-id="3ec49-113">**Applies To**</span></span>

[<span data-ttu-id="3ec49-114">Preencher</span><span class="sxs-lookup"><span data-stu-id="3ec49-114">Fill</span></span>](msdn-online-vml-fill-element.md)

<span data-ttu-id="3ec49-115">**Sintaxe de marca**</span><span class="sxs-lookup"><span data-stu-id="3ec49-115">**Tag Syntax**</span></span>

<span data-ttu-id="3ec49-116"><v: tipo de *elemento* = " *expressão* " ></span><span class="sxs-lookup"><span data-stu-id="3ec49-116"><v: *element* type=" *expression* "></span></span>

<span data-ttu-id="3ec49-117">**Sintaxe do script**</span><span class="sxs-lookup"><span data-stu-id="3ec49-117">**Script Syntax**</span></span>

<span data-ttu-id="3ec49-118">*elemento* . Type = "*expressão*"</span><span class="sxs-lookup"><span data-stu-id="3ec49-118">*element* .type="*expression*"</span></span>

<span data-ttu-id="3ec49-119">*expressão* = de *elemento*. Type</span><span class="sxs-lookup"><span data-stu-id="3ec49-119">*expression*=*element*.type</span></span>

<span data-ttu-id="3ec49-120">**Comentários**</span><span class="sxs-lookup"><span data-stu-id="3ec49-120">**Remarks**</span></span>

<span data-ttu-id="3ec49-121">Os valores são:</span><span class="sxs-lookup"><span data-stu-id="3ec49-121">Values include:</span></span>



| <span data-ttu-id="3ec49-122">Tipo</span><span class="sxs-lookup"><span data-stu-id="3ec49-122">Type</span></span>           | <span data-ttu-id="3ec49-123">Descrição</span><span class="sxs-lookup"><span data-stu-id="3ec49-123">Description</span></span>                                                             |
|----------------|-------------------------------------------------------------------------|
| <span data-ttu-id="3ec49-124">consolidou</span><span class="sxs-lookup"><span data-stu-id="3ec49-124">solid</span></span>          | <span data-ttu-id="3ec49-125">O padrão de preenchimento é sólido.</span><span class="sxs-lookup"><span data-stu-id="3ec49-125">The fill pattern is solid.</span></span> <span data-ttu-id="3ec49-126">Padrão.</span><span class="sxs-lookup"><span data-stu-id="3ec49-126">Default.</span></span>                                     |
| <span data-ttu-id="3ec49-127">gradiente</span><span class="sxs-lookup"><span data-stu-id="3ec49-127">gradient</span></span>       | <span data-ttu-id="3ec49-128">As cores de preenchimento se misturam em um gradiente linear de baixo para cima.</span><span class="sxs-lookup"><span data-stu-id="3ec49-128">The fill colors blend together in a linear gradient from bottom to top.</span></span> |
| <span data-ttu-id="3ec49-129">gradientradial</span><span class="sxs-lookup"><span data-stu-id="3ec49-129">gradientradial</span></span> | <span data-ttu-id="3ec49-130">As cores de preenchimento mesclam juntas em um gradiente radial.</span><span class="sxs-lookup"><span data-stu-id="3ec49-130">The fill colors blend together in a radial gradient.</span></span>                    |
| <span data-ttu-id="3ec49-131">bloco</span><span class="sxs-lookup"><span data-stu-id="3ec49-131">tile</span></span>           | <span data-ttu-id="3ec49-132">A imagem de preenchimento é disposta lado a lado.</span><span class="sxs-lookup"><span data-stu-id="3ec49-132">The fill image is tiled.</span></span>                                                |
| <span data-ttu-id="3ec49-133">pattern</span><span class="sxs-lookup"><span data-stu-id="3ec49-133">pattern</span></span>        | <span data-ttu-id="3ec49-134">A imagem é usada para criar um padrão usando as cores de preenchimento.</span><span class="sxs-lookup"><span data-stu-id="3ec49-134">The image is used to create a pattern using the fill colors.</span></span>            |
| <span data-ttu-id="3ec49-135">frame</span><span class="sxs-lookup"><span data-stu-id="3ec49-135">frame</span></span>          | <span data-ttu-id="3ec49-136">A imagem é ampliada para preencher a forma.</span><span class="sxs-lookup"><span data-stu-id="3ec49-136">The image is stretched to fill the shape.</span></span>                               |



 

<span data-ttu-id="3ec49-137">**Atributo padrão da VML**</span><span class="sxs-lookup"><span data-stu-id="3ec49-137">**VML Standard Attribute**</span></span>

<span data-ttu-id="3ec49-138">**Exemplo**</span><span class="sxs-lookup"><span data-stu-id="3ec49-138">**Example**</span></span>

<span data-ttu-id="3ec49-139">Um preenchimento de primeiro plano vermelho e plano de fundo azul é criado usando o padrão da imagem myimage.gif.</span><span class="sxs-lookup"><span data-stu-id="3ec49-139">A red foreground and blue background fill is created using the pattern of the image myimage.gif.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill color="red" color2="blue" type="pattern" src="myimage.gif"/>
   </v:shape>
```



 

 