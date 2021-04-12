---
title: Atributo OnEd de VML
description: Atributo OnEd de VML
ms.assetid: d24137c3-73cb-4b92-bf25-ffe4aa8b0069
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1892d5ed185358c4abc5fa6fdaf6448ac5b6317c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104294445"
---
# <a name="vml-oned-attribute"></a><span data-ttu-id="3d2d0-103">Atributo OnEd de VML</span><span class="sxs-lookup"><span data-stu-id="3d2d0-103">VML OnEd Attribute</span></span>

<span data-ttu-id="3d2d0-104">Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="3d2d0-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="3d2d0-105">As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.</span><span class="sxs-lookup"><span data-stu-id="3d2d0-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="3d2d0-106">A partir de dezembro de 2011, este tópico foi arquivado.</span><span class="sxs-lookup"><span data-stu-id="3d2d0-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="3d2d0-107">Como resultado, ele não é mais mantido ativamente.</span><span class="sxs-lookup"><span data-stu-id="3d2d0-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="3d2d0-108">Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="3d2d0-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="3d2d0-109">Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="3d2d0-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="3d2d0-110">Determina se os identificadores extras de uma forma ficam ocultos.</span><span class="sxs-lookup"><span data-stu-id="3d2d0-110">Determines whether the extra handles of a shape are hidden.</span></span> <span data-ttu-id="3d2d0-111">Leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="3d2d0-111">Read/write.</span></span> <span data-ttu-id="3d2d0-112">**VgTriState**.</span><span class="sxs-lookup"><span data-stu-id="3d2d0-112">**VgTriState**.</span></span>

<span data-ttu-id="3d2d0-113">**Aplica-se a**</span><span class="sxs-lookup"><span data-stu-id="3d2d0-113">**Applies To**</span></span>

[<span data-ttu-id="3d2d0-114">Forma</span><span class="sxs-lookup"><span data-stu-id="3d2d0-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="3d2d0-115">**Sintaxe de marca**</span><span class="sxs-lookup"><span data-stu-id="3d2d0-115">**Tag Syntax**</span></span>

<span data-ttu-id="3d2d0-116"><v: *Element* o:oned = " *expressão* " ></span><span class="sxs-lookup"><span data-stu-id="3d2d0-116"><v: *element* o:oned=" *expression* "></span></span>

<span data-ttu-id="3d2d0-117">**Comentários**</span><span class="sxs-lookup"><span data-stu-id="3d2d0-117">**Remarks**</span></span>

<span data-ttu-id="3d2d0-118">Oculta todas as alças de forma, exceto as partes superior esquerda e inferior direita; ou seja, os mesmos identificadores que são usados para um segmento de linha reta.</span><span class="sxs-lookup"><span data-stu-id="3d2d0-118">Hides all shape handles except the top left and bottom right; that is, the same handles that are used for a straight line segment.</span></span> <span data-ttu-id="3d2d0-119">O padrão é **False**.</span><span class="sxs-lookup"><span data-stu-id="3d2d0-119">The default is **False**.</span></span>

<span data-ttu-id="3d2d0-120">*Atributo de extensões de Microsoft Office*</span><span class="sxs-lookup"><span data-stu-id="3d2d0-120">*Microsoft Office Extensions Attribute*</span></span>

<span data-ttu-id="3d2d0-121">**Exemplo**</span><span class="sxs-lookup"><span data-stu-id="3d2d0-121">**Example**</span></span>

<span data-ttu-id="3d2d0-122">Todos, exceto os identificadores esquerdo superior e inferior direito da forma ficam ocultos.</span><span class="sxs-lookup"><span data-stu-id="3d2d0-122">All but the top left and bottom right handles of the shape are hidden.</span></span>


```HTML
   <v:shape id="rect01" OnEd="True"
   fillcolor="red" strokecolor="red"
   coordorigin="-500 -500" coordsize="1000 1000"
   style="position:relative;top:0;left:0;width:100pt;height:100pt;mso-wrap-distance-top:10pt"
   path="m 5,5 l 5,195, 195,195, 195,5 x e">
   </v:shape>
```



 

 