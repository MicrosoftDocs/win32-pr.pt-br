---
title: Atributo de foco da VML
description: Atributo de foco da VML
ms.assetid: 9ed52203-4142-47cd-851f-74230aac934d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 062b2900c2f980c9a1433e5e790a34d463def9be
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104008343"
---
# <a name="vml-focus-attribute"></a><span data-ttu-id="1407c-103">Atributo de foco da VML</span><span class="sxs-lookup"><span data-stu-id="1407c-103">VML Focus Attribute</span></span>

<span data-ttu-id="1407c-104">Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="1407c-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="1407c-105">As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.</span><span class="sxs-lookup"><span data-stu-id="1407c-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="1407c-106">A partir de dezembro de 2011, este tópico foi arquivado.</span><span class="sxs-lookup"><span data-stu-id="1407c-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="1407c-107">Como resultado, ele não é mais mantido ativamente.</span><span class="sxs-lookup"><span data-stu-id="1407c-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="1407c-108">Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="1407c-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="1407c-109">Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="1407c-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="1407c-110">Define o centro de um preenchimento gradiente linear.</span><span class="sxs-lookup"><span data-stu-id="1407c-110">Defines the center of a linear gradient fill.</span></span> <span data-ttu-id="1407c-111">Leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="1407c-111">Read/write.</span></span> <span data-ttu-id="1407c-112">**VgFraction**.</span><span class="sxs-lookup"><span data-stu-id="1407c-112">**VgFraction**.</span></span>

<span data-ttu-id="1407c-113">**Aplica-se a**</span><span class="sxs-lookup"><span data-stu-id="1407c-113">**Applies To**</span></span>

[<span data-ttu-id="1407c-114">Preencher</span><span class="sxs-lookup"><span data-stu-id="1407c-114">Fill</span></span>](msdn-online-vml-fill-element.md)

<span data-ttu-id="1407c-115">**Sintaxe de marca**</span><span class="sxs-lookup"><span data-stu-id="1407c-115">**Tag Syntax**</span></span>

<span data-ttu-id="1407c-116"><v: *elemento* Focus = " *expressão* " ></span><span class="sxs-lookup"><span data-stu-id="1407c-116"><v: *element* focus=" *expression* "></span></span>

<span data-ttu-id="1407c-117">**Sintaxe do script**</span><span class="sxs-lookup"><span data-stu-id="1407c-117">**Script Syntax**</span></span>

<span data-ttu-id="1407c-118">*elemento* . Focus = "*expressão*"</span><span class="sxs-lookup"><span data-stu-id="1407c-118">*element* .focus="*expression*"</span></span>

<span data-ttu-id="1407c-119">*expressão* = de *elemento*. Focus</span><span class="sxs-lookup"><span data-stu-id="1407c-119">*expression*=*element*.focus</span></span>

<span data-ttu-id="1407c-120">**Comentários**</span><span class="sxs-lookup"><span data-stu-id="1407c-120">**Remarks**</span></span>

<span data-ttu-id="1407c-121">Define a posição inicial do Blend.</span><span class="sxs-lookup"><span data-stu-id="1407c-121">Defines the center starting position of the blend.</span></span> <span data-ttu-id="1407c-122">Os valores variam de 100% a-100%.</span><span class="sxs-lookup"><span data-stu-id="1407c-122">Values range from 100% to -100%.</span></span> <span data-ttu-id="1407c-123">O valor padrão é 0.</span><span class="sxs-lookup"><span data-stu-id="1407c-123">The default value is 0.</span></span> <span data-ttu-id="1407c-124">Um valor de 100% (ou-100%) mudará o foco para que a direção do Blend seja invertida (em vigor, revertendo **Color** e **Color2**).</span><span class="sxs-lookup"><span data-stu-id="1407c-124">A value of 100% (or -100%) will shift the focus so that the direction of the blend will reverse (in effect reversing **Color** and **Color2**).</span></span> <span data-ttu-id="1407c-125">Um valor de 50% alterará o Blend para que a **cor** esteja em ambas as extremidades e **Color2** esteja no meio.</span><span class="sxs-lookup"><span data-stu-id="1407c-125">A value of 50% will change the blend so that **Color** is at both ends and **Color2** is in the middle.</span></span> <span data-ttu-id="1407c-126">Um valor de-50% alterará o Blend para que **Color2** esteja em ambas as extremidades e a **cor** esteja no meio.</span><span class="sxs-lookup"><span data-stu-id="1407c-126">A value of -50% will change the blend so that **Color2** is at both ends and **Color** is in the middle.</span></span>

<span data-ttu-id="1407c-127">*Atributo padrão da VML*</span><span class="sxs-lookup"><span data-stu-id="1407c-127">*VML Standard Attribute*</span></span>

<span data-ttu-id="1407c-128">**Exemplo**</span><span class="sxs-lookup"><span data-stu-id="1407c-128">**Example**</span></span>

<span data-ttu-id="1407c-129">O foco gradiente do preenchimento é deslocado para que o vermelho (**cor**) seja uma faixa no centro da forma e que a parte superior e inferior seja azul (**Color2**).</span><span class="sxs-lookup"><span data-stu-id="1407c-129">The gradient focus of the fill is shifted so that red (**Color**) will be a band in the center of the shape and that the top and bottom will be blue (**Color2**).</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill type="gradient" color="red" color2="blue"
   method="linear" focus="-50%"/>
   </v:shape>
```



 

 