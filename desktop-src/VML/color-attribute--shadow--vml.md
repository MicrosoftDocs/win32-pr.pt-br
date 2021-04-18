---
title: Atributo Color (Shadow) (VML)
description: Atributo Color (Shadow) (VML)
ms.assetid: 677615b7-b4a4-411f-b04e-3ed0399f4c05
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73df77e65a3ae0f74c6e79b9c179c31da27698f9
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "105764016"
---
# <a name="color-attribute-shadowvml"></a><span data-ttu-id="57da8-103">Atributo Color (Shadow) (VML)</span><span class="sxs-lookup"><span data-stu-id="57da8-103">Color Attribute (Shadow)(VML)</span></span>

<span data-ttu-id="57da8-104">Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="57da8-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="57da8-105">As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.</span><span class="sxs-lookup"><span data-stu-id="57da8-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="57da8-106">A partir de dezembro de 2011, este tópico foi arquivado.</span><span class="sxs-lookup"><span data-stu-id="57da8-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="57da8-107">Como resultado, ele não é mais mantido ativamente.</span><span class="sxs-lookup"><span data-stu-id="57da8-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="57da8-108">Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="57da8-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="57da8-109">Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="57da8-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="57da8-110">Define a cor da sombra.</span><span class="sxs-lookup"><span data-stu-id="57da8-110">Defines the color of the shadow.</span></span> <span data-ttu-id="57da8-111">Leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="57da8-111">Read/write.</span></span> <span data-ttu-id="57da8-112">**VgColor**.</span><span class="sxs-lookup"><span data-stu-id="57da8-112">**VgColor**.</span></span>

<span data-ttu-id="57da8-113">**Aplica-se a**</span><span class="sxs-lookup"><span data-stu-id="57da8-113">**Applies To**</span></span>

[<span data-ttu-id="57da8-114">Shadow</span><span class="sxs-lookup"><span data-stu-id="57da8-114">Shadow</span></span>](msdn-online-vml-shadow-element.md)

<span data-ttu-id="57da8-115">**Sintaxe de marca**</span><span class="sxs-lookup"><span data-stu-id="57da8-115">**Tag Syntax**</span></span>

<span data-ttu-id="57da8-116"><v: *Element* Color = " *expressão* " ></span><span class="sxs-lookup"><span data-stu-id="57da8-116"><v: *element* color=" *expression* "></span></span>

<span data-ttu-id="57da8-117">**Sintaxe do script**</span><span class="sxs-lookup"><span data-stu-id="57da8-117">**Script Syntax**</span></span>

<span data-ttu-id="57da8-118">*Element* . Color = "*expressão*"</span><span class="sxs-lookup"><span data-stu-id="57da8-118">*element* .color="*expression*"</span></span>

<span data-ttu-id="57da8-119">*expressão* = de *elemento*. Color</span><span class="sxs-lookup"><span data-stu-id="57da8-119">*expression*=*element*.color</span></span>

<span data-ttu-id="57da8-120">**Comentários**</span><span class="sxs-lookup"><span data-stu-id="57da8-120">**Remarks**</span></span>

<span data-ttu-id="57da8-121">Use o atributo Color para definir ou obter a cor de uma sombra.</span><span class="sxs-lookup"><span data-stu-id="57da8-121">Use the color attribute to set or get the color of a shadow.</span></span>

<span data-ttu-id="57da8-122">*Atributo padrão da VML*</span><span class="sxs-lookup"><span data-stu-id="57da8-122">*VML Standard Attribute*</span></span>

<span data-ttu-id="57da8-123">**Exemplo**</span><span class="sxs-lookup"><span data-stu-id="57da8-123">**Example**</span></span>

<span data-ttu-id="57da8-124">A sombra está verde.</span><span class="sxs-lookup"><span data-stu-id="57da8-124">The shadow is green.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:shadow on="True" color="green"/>
   </v:shape>
```



 

 