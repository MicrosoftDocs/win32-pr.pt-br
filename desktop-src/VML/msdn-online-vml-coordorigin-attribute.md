---
title: Atributo CoordOrigin de VML
description: Atributo CoordOrigin de VML
ms.assetid: 0630e670-6ebe-424e-a5e0-545597454283
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb08d35aac7e26cc15aa7699439ea9f7ab4dba94
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103823793"
---
# <a name="vml-coordorigin-attribute"></a><span data-ttu-id="1212d-103">Atributo CoordOrigin de VML</span><span class="sxs-lookup"><span data-stu-id="1212d-103">VML CoordOrigin Attribute</span></span>

<span data-ttu-id="1212d-104">Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="1212d-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="1212d-105">As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.</span><span class="sxs-lookup"><span data-stu-id="1212d-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="1212d-106">A partir de dezembro de 2011, este tópico foi arquivado.</span><span class="sxs-lookup"><span data-stu-id="1212d-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="1212d-107">Como resultado, ele não é mais mantido ativamente.</span><span class="sxs-lookup"><span data-stu-id="1212d-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="1212d-108">Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="1212d-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="1212d-109">Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="1212d-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="1212d-110">Especifica a origem da unidade de coordenadas do retângulo que vincula uma forma.</span><span class="sxs-lookup"><span data-stu-id="1212d-110">Specifies the coordinate unit origin of the rectangle that bounds a shape.</span></span> <span data-ttu-id="1212d-111">Leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="1212d-111">Read/write.</span></span> <span data-ttu-id="1212d-112">[IVgVector2D](msdn-online-vml-ivgvector2d-data-type.md).</span><span class="sxs-lookup"><span data-stu-id="1212d-112">[IVgVector2D](msdn-online-vml-ivgvector2d-data-type.md).</span></span>

<span data-ttu-id="1212d-113">**Aplica-se a**</span><span class="sxs-lookup"><span data-stu-id="1212d-113">**Applies To**</span></span>

[<span data-ttu-id="1212d-114">Forma</span><span class="sxs-lookup"><span data-stu-id="1212d-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="1212d-115">**Sintaxe de marca**</span><span class="sxs-lookup"><span data-stu-id="1212d-115">**Tag Syntax**</span></span>

<span data-ttu-id="1212d-116"><v: *Element* coordorigin = " *expressão* " ></span><span class="sxs-lookup"><span data-stu-id="1212d-116"><v: *element* coordorigin=" *expression* "></span></span>

<span data-ttu-id="1212d-117">**Sintaxe do script**</span><span class="sxs-lookup"><span data-stu-id="1212d-117">**Script Syntax**</span></span>

<span data-ttu-id="1212d-118">*Element* . coordorigin = "*expressão*"</span><span class="sxs-lookup"><span data-stu-id="1212d-118">*element* .coordorigin="*expression*"</span></span>

<span data-ttu-id="1212d-119">*expressão* = de *elemento*. coordorigin</span><span class="sxs-lookup"><span data-stu-id="1212d-119">*expression*=*element*.coordorigin</span></span>

<span data-ttu-id="1212d-120">**Comentários**</span><span class="sxs-lookup"><span data-stu-id="1212d-120">**Remarks**</span></span>

<span data-ttu-id="1212d-121">Se não for especificado, as coordenadas de origem serão (0, 0) no canto superior esquerdo da caixa delimitadora de forma.</span><span class="sxs-lookup"><span data-stu-id="1212d-121">If not specified, the origin coordinates are (0,0) at the top left corner of the shape bounding box.</span></span>

<span data-ttu-id="1212d-122">O valor x de **CoordSize** é adicionado ao valor x de **CoordOrigin** para determinar o intervalo dos valores horizontais.</span><span class="sxs-lookup"><span data-stu-id="1212d-122">The x value of **CoordSize** is added to the x value of **CoordOrigin** to determine the range of the horizontal values.</span></span> <span data-ttu-id="1212d-123">Por exemplo, se o valor x de **CoordOrigin** for-100 e o valor x de **CoordSize** for 200, as unidades horizontais irão variar de-100 a + 100.</span><span class="sxs-lookup"><span data-stu-id="1212d-123">For example,if the x value of **CoordOrigin** is -100 and the x value of **CoordSize** is 200, the horizontal units will range from -100 to +100.</span></span> <span data-ttu-id="1212d-124">Se o valor x de **CoordOrigin** for 100 e o valor x de **CoordSize** for 200, as unidades horizontais irão variar de 100 a 300, tudo dentro da caixa delimitadora.</span><span class="sxs-lookup"><span data-stu-id="1212d-124">If the x value of **CoordOrigin** is 100 and the x value of **CoordSize** is 200, the horizontal units will range from 100 to 300, all within the bounding box.</span></span> <span data-ttu-id="1212d-125">O mesmo é verdadeiro para os valores y.</span><span class="sxs-lookup"><span data-stu-id="1212d-125">The same is true for the y values.</span></span>

<span data-ttu-id="1212d-126">Observe que esse atributo é um vetor e que as unidades são do mesmo tipo de unidade que [CoordSize](msdn-online-vml-coordsize-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="1212d-126">Note that this attribute is a vector and that the units are the same type of unit as [CoordSize](msdn-online-vml-coordsize-attribute.md) .</span></span>

<span data-ttu-id="1212d-127">No script, como esse é um vetor 2D, você pode acessar os valores x e y separadamente e também pode determinar o tipo de unidades esperado.</span><span class="sxs-lookup"><span data-stu-id="1212d-127">In scripting, because this is a 2-D vector, you can access the x and y values separately, and can also determine the type of units expected.</span></span>

<span data-ttu-id="1212d-128">*Atributo padrão da VML*</span><span class="sxs-lookup"><span data-stu-id="1212d-128">*VML Standard Attribute*</span></span>

<span data-ttu-id="1212d-129">**Exemplo**</span><span class="sxs-lookup"><span data-stu-id="1212d-129">**Example**</span></span>

<span data-ttu-id="1212d-130">O centro da caixa delimitadora será a origem (0, 0) do caminho para a forma.</span><span class="sxs-lookup"><span data-stu-id="1212d-130">The center of the bounding box will be the origin (0,0) of the path for the shape.</span></span> <span data-ttu-id="1212d-131">Como **CoordOrigin** é "-500-500" e **CoordSize** é "1000 1000", as unidades horizontais e verticais vão variar de-500 a + 500.</span><span class="sxs-lookup"><span data-stu-id="1212d-131">Because **CoordOrigin** is "-500 -500" and **CoordSize** is "1000 1000", the horizontal and vertical units will range from -500 to +500.</span></span> <span data-ttu-id="1212d-132">O canto esquerdo e superior do caminho estará no centro da caixa delimitadora definida pelos pontos esquerdo e superior, conforme definido pelo **estilo**.</span><span class="sxs-lookup"><span data-stu-id="1212d-132">The left and top corner of the path will be at the center of the bounding box defined by the left and top points as defined by **Style**.</span></span>


```HTML
   <v:shape id="rect01"
   fillcolor="red" strokecolor="red"
   coordorigin="-500 -500" coordsize="1000 1000"
   style="position:relative;top:0;left:0;width:100pt;height:100pt"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   </v:shape>
```



<span data-ttu-id="1212d-133">[Exemplo do atributo CoordOrigin](/previous-versions/bb229664(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="1212d-133">[CoordOrigin Attribute Example](/previous-versions/bb229664(v=vs.85)).</span></span> <span data-ttu-id="1212d-134">(Requer o Microsoft Internet Explorer 5 ou superior.)</span><span class="sxs-lookup"><span data-stu-id="1212d-134">(Requires Microsoft Internet Explorer 5 or greater.)</span></span>

 

 