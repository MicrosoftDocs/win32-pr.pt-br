---
title: Atributo Color2 (Fill) (VML)
description: Atributo Color2 (Fill) (VML)
ms.assetid: 971c8783-8c7b-43c7-8b94-01159336eef6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5689bba52277b4056f57a171f3ffc1e197aa4c8b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "105782289"
---
# <a name="color2-attribute-fillvml"></a><span data-ttu-id="b397f-103">Atributo Color2 (Fill) (VML)</span><span class="sxs-lookup"><span data-stu-id="b397f-103">Color2 Attribute (Fill)(VML)</span></span>

<span data-ttu-id="b397f-104">Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="b397f-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="b397f-105">As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.</span><span class="sxs-lookup"><span data-stu-id="b397f-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="b397f-106">A partir de dezembro de 2011, este tópico foi arquivado.</span><span class="sxs-lookup"><span data-stu-id="b397f-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="b397f-107">Como resultado, ele não é mais mantido ativamente.</span><span class="sxs-lookup"><span data-stu-id="b397f-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="b397f-108">Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="b397f-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="b397f-109">Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="b397f-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="b397f-110">Define uma segunda cor para preenchimentos.</span><span class="sxs-lookup"><span data-stu-id="b397f-110">Defines a second color for fills.</span></span> <span data-ttu-id="b397f-111">Leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="b397f-111">Read/write.</span></span> <span data-ttu-id="b397f-112">[VgColor](msdn-online-vml-ivgcolor.md) .</span><span class="sxs-lookup"><span data-stu-id="b397f-112">[VgColor](msdn-online-vml-ivgcolor.md) .</span></span>

<span data-ttu-id="b397f-113">**Aplica-se a**</span><span class="sxs-lookup"><span data-stu-id="b397f-113">**Applies To**</span></span>

[<span data-ttu-id="b397f-114">Preencher</span><span class="sxs-lookup"><span data-stu-id="b397f-114">Fill</span></span>](msdn-online-vml-fill-element.md)

<span data-ttu-id="b397f-115">**Sintaxe de marca**</span><span class="sxs-lookup"><span data-stu-id="b397f-115">**Tag Syntax**</span></span>

<span data-ttu-id="b397f-116"><v: *Element* color2 = " *expressão* " ></span><span class="sxs-lookup"><span data-stu-id="b397f-116"><v: *element* color2=" *expression* "></span></span>

<span data-ttu-id="b397f-117">**Sintaxe do script**</span><span class="sxs-lookup"><span data-stu-id="b397f-117">**Script Syntax**</span></span>

<span data-ttu-id="b397f-118">*Element* . color2 = "*expressão*"</span><span class="sxs-lookup"><span data-stu-id="b397f-118">*element* .color2="*expression*"</span></span>

<span data-ttu-id="b397f-119">*expressão* = de *elemento*. color2</span><span class="sxs-lookup"><span data-stu-id="b397f-119">*expression*=*element*.color2</span></span>

<span data-ttu-id="b397f-120">**Comentários**</span><span class="sxs-lookup"><span data-stu-id="b397f-120">**Remarks**</span></span>

<span data-ttu-id="b397f-121">Uma segunda cor é usada quando um tipo de preenchimento é um padrão ou um gradiente.</span><span class="sxs-lookup"><span data-stu-id="b397f-121">A second color is used when a fill type is a pattern or a gradient.</span></span> <span data-ttu-id="b397f-122">O valor padrão é **branco**.</span><span class="sxs-lookup"><span data-stu-id="b397f-122">The default value is **White**.</span></span>

<span data-ttu-id="b397f-123">*Atributo padrão da VML*</span><span class="sxs-lookup"><span data-stu-id="b397f-123">*VML Standard Attribute*</span></span>

<span data-ttu-id="b397f-124">**Exemplo**</span><span class="sxs-lookup"><span data-stu-id="b397f-124">**Example**</span></span>

<span data-ttu-id="b397f-125">O tipo de preenchimento da forma é um padrão em que o preenchimento em primeiro plano é definido pela imagem de origem, mas o plano de fundo transparente é definido pela segunda cor.</span><span class="sxs-lookup"><span data-stu-id="b397f-125">The shape's fill type is a pattern where the foreground fill is defined by the source image but the transparent background is defined by the second color.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill type="pattern" color2="green" src="myimage.gif"/>
   </v:shape>
```



 

 