---
title: Atributo Color (Fill) (VML)
description: Atributo Color (Fill) (VML)
ms.assetid: 38e75bf5-4da9-4c58-af86-3554d03a6b7b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8480b3a013add36533a82b31338fba301e8353db
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104454091"
---
# <a name="color-attribute-fillvml"></a><span data-ttu-id="74621-103">Atributo Color (Fill) (VML)</span><span class="sxs-lookup"><span data-stu-id="74621-103">Color Attribute (Fill)(VML)</span></span>

<span data-ttu-id="74621-104">Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="74621-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="74621-105">As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.</span><span class="sxs-lookup"><span data-stu-id="74621-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="74621-106">A partir de dezembro de 2011, este tópico foi arquivado.</span><span class="sxs-lookup"><span data-stu-id="74621-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="74621-107">Como resultado, ele não é mais mantido ativamente.</span><span class="sxs-lookup"><span data-stu-id="74621-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="74621-108">Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="74621-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="74621-109">Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="74621-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="74621-110">Define a cor de um preenchimento.</span><span class="sxs-lookup"><span data-stu-id="74621-110">Defines the color of a fill.</span></span> <span data-ttu-id="74621-111">Leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="74621-111">Read/write.</span></span> <span data-ttu-id="74621-112">**VgColor**.</span><span class="sxs-lookup"><span data-stu-id="74621-112">**VgColor**.</span></span>

<span data-ttu-id="74621-113">**Aplica-se a**</span><span class="sxs-lookup"><span data-stu-id="74621-113">**Applies To**</span></span>

[<span data-ttu-id="74621-114">Preencher</span><span class="sxs-lookup"><span data-stu-id="74621-114">Fill</span></span>](msdn-online-vml-fill-element.md)

<span data-ttu-id="74621-115">**Sintaxe de marca**</span><span class="sxs-lookup"><span data-stu-id="74621-115">**Tag Syntax**</span></span>

<span data-ttu-id="74621-116"><v: *Element* Color = " *expressão* " ></span><span class="sxs-lookup"><span data-stu-id="74621-116"><v: *element* color=" *expression* "></span></span>

<span data-ttu-id="74621-117">**Sintaxe do script**</span><span class="sxs-lookup"><span data-stu-id="74621-117">**Script Syntax**</span></span>

<span data-ttu-id="74621-118">*Element* . Color = "*expressão*"</span><span class="sxs-lookup"><span data-stu-id="74621-118">*element* .color="*expression*"</span></span>

<span data-ttu-id="74621-119">*expressão* = de *elemento*. Color</span><span class="sxs-lookup"><span data-stu-id="74621-119">*expression*=*element*.color</span></span>

<span data-ttu-id="74621-120">**Comentários**</span><span class="sxs-lookup"><span data-stu-id="74621-120">**Remarks**</span></span>

<span data-ttu-id="74621-121">Substitui o atributo **FillColor** de uma forma.</span><span class="sxs-lookup"><span data-stu-id="74621-121">Overrides the **FillColor** attribute of a shape.</span></span> <span data-ttu-id="74621-122">O valor padrão é **branco**.</span><span class="sxs-lookup"><span data-stu-id="74621-122">The default value is **White**.</span></span>

<span data-ttu-id="74621-123">*Atributo padrão da VML*</span><span class="sxs-lookup"><span data-stu-id="74621-123">*VML Standard Attribute*</span></span>

<span data-ttu-id="74621-124">**Exemplo**</span><span class="sxs-lookup"><span data-stu-id="74621-124">**Example**</span></span>

<span data-ttu-id="74621-125">A cor de preenchimento da forma é verde.</span><span class="sxs-lookup"><span data-stu-id="74621-125">The fill color of the shape is green.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill color="green"/>
   </v:shape>
```



 

 