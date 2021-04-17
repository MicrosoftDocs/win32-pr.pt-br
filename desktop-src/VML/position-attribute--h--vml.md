---
title: Atributo de posição (H) (VML)
description: Atributo de posição (H) (VML)
ms.assetid: 0bae708d-5409-4609-a102-7f799f2c1fbb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac310c0fad457beaf3b9aeb04671b7ffbb1dbd8d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "105811401"
---
# <a name="position-attribute-hvml"></a><span data-ttu-id="43b74-103">Atributo de posição (H) (VML)</span><span class="sxs-lookup"><span data-stu-id="43b74-103">Position Attribute (H)(VML)</span></span>

<span data-ttu-id="43b74-104">Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="43b74-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="43b74-105">As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.</span><span class="sxs-lookup"><span data-stu-id="43b74-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="43b74-106">A partir de dezembro de 2011, este tópico foi arquivado.</span><span class="sxs-lookup"><span data-stu-id="43b74-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="43b74-107">Como resultado, ele não é mais mantido ativamente.</span><span class="sxs-lookup"><span data-stu-id="43b74-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="43b74-108">Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="43b74-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="43b74-109">Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="43b74-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="43b74-110">Especifica os valores de thex e y do identificador.</span><span class="sxs-lookup"><span data-stu-id="43b74-110">Specifies thex and y values of the handle.</span></span> <span data-ttu-id="43b74-111">**VgVector2D** de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="43b74-111">Read/write **VgVector2D**.</span></span>

<span data-ttu-id="43b74-112">**Aplica-se a**</span><span class="sxs-lookup"><span data-stu-id="43b74-112">**Applies To**</span></span>

<span data-ttu-id="43b74-113">[H](msdn-online-vml-h-element.md) (subelemento de [identificadores](msdn-online-vml-handles-element.md))</span><span class="sxs-lookup"><span data-stu-id="43b74-113">[H](msdn-online-vml-h-element.md) (subelement of [Handles](msdn-online-vml-handles-element.md))</span></span>

<span data-ttu-id="43b74-114">**Sintaxe de marca**</span><span class="sxs-lookup"><span data-stu-id="43b74-114">**Tag Syntax**</span></span>

<span data-ttu-id="43b74-115"><v: *elemento* position = " *expressão* " ></span><span class="sxs-lookup"><span data-stu-id="43b74-115"><v: *element* position=" *expression* "></span></span>

<span data-ttu-id="43b74-116">**Comentários**</span><span class="sxs-lookup"><span data-stu-id="43b74-116">**Remarks**</span></span>

<span data-ttu-id="43b74-117">os valores x e y podem ser um dos seguintes tipos:</span><span class="sxs-lookup"><span data-stu-id="43b74-117">x and y values can be one of the following types:</span></span>

-   <span data-ttu-id="43b74-118">constante</span><span class="sxs-lookup"><span data-stu-id="43b74-118">constant</span></span>
-   <span data-ttu-id="43b74-119">fórmula (por exemplo, @2 )</span><span class="sxs-lookup"><span data-stu-id="43b74-119">formula (for example, @2)</span></span>
-   <span data-ttu-id="43b74-120">ajustar (por exemplo, \# 3)</span><span class="sxs-lookup"><span data-stu-id="43b74-120">adjust (for example, \#3)</span></span>
-   <span data-ttu-id="43b74-121">centro</span><span class="sxs-lookup"><span data-stu-id="43b74-121">center</span></span>
-   <span data-ttu-id="43b74-122">topleft</span><span class="sxs-lookup"><span data-stu-id="43b74-122">topleft</span></span>
-   <span data-ttu-id="43b74-123">bottomright</span><span class="sxs-lookup"><span data-stu-id="43b74-123">bottomright</span></span>

<span data-ttu-id="43b74-124">Se qualquer um dos tipos acima, exceto *ajuste* , for especificado, a posição do identificador será corrigida nessa dimensão.</span><span class="sxs-lookup"><span data-stu-id="43b74-124">If any of the above types except *adjust* are specified, the handle position is fixed in that dimension.</span></span> <span data-ttu-id="43b74-125">Se um identificador de ajuste for especificado, o identificador será livre para mover nessa dimensão e o valor de ajuste será determinado pela posição do identificador.</span><span class="sxs-lookup"><span data-stu-id="43b74-125">If an adjust handle is specified, the handle is free to move in that dimension and the adjust value is determined by the position of the handle.</span></span>

<span data-ttu-id="43b74-126">Se um atributo [polar](msdn-online-vml-polar-attribute.md) for especificado, o atributo **Position** representará os valores de raio e ângulo da alça em vez de x e y.</span><span class="sxs-lookup"><span data-stu-id="43b74-126">If a [Polar](msdn-online-vml-polar-attribute.md) attribute is specified, the **Position** attribute represents the radius and angle values of the handle instead of x and y.</span></span>

<span data-ttu-id="43b74-127">O valor padrão é 0,0.</span><span class="sxs-lookup"><span data-stu-id="43b74-127">The default value is 0,0.</span></span>

<span data-ttu-id="43b74-128">*Atributo padrão da VML*</span><span class="sxs-lookup"><span data-stu-id="43b74-128">*VML Standard Attribute*</span></span>

 

 