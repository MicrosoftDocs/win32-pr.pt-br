---
title: Atributo CoordSize de VML
description: Atributo CoordSize de VML
ms.assetid: 4e7a7eca-7db2-4522-be8e-e817601625ed
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a0e1fee484071c04c7184e0f200aed9b52aadf9
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "105788855"
---
# <a name="vml-coordsize-attribute"></a><span data-ttu-id="2cc66-103">Atributo CoordSize de VML</span><span class="sxs-lookup"><span data-stu-id="2cc66-103">VML CoordSize Attribute</span></span>

<span data-ttu-id="2cc66-104">Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="2cc66-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="2cc66-105">As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.</span><span class="sxs-lookup"><span data-stu-id="2cc66-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="2cc66-106">A partir de dezembro de 2011, este tópico foi arquivado.</span><span class="sxs-lookup"><span data-stu-id="2cc66-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="2cc66-107">Como resultado, ele não é mais mantido ativamente.</span><span class="sxs-lookup"><span data-stu-id="2cc66-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="2cc66-108">Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="2cc66-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="2cc66-109">Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="2cc66-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="2cc66-110">Especifica as unidades horizontais e verticais do retângulo que limita uma forma.</span><span class="sxs-lookup"><span data-stu-id="2cc66-110">Specifies the horizontal and vertical units of the rectangle that bounds a shape.</span></span> <span data-ttu-id="2cc66-111">Leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="2cc66-111">Read/write.</span></span> <span data-ttu-id="2cc66-112">[IVgVector2D](msdn-online-vml-ivgvector2d-data-type.md).</span><span class="sxs-lookup"><span data-stu-id="2cc66-112">[IVgVector2D](msdn-online-vml-ivgvector2d-data-type.md).</span></span>

<span data-ttu-id="2cc66-113">**Aplica-se a**</span><span class="sxs-lookup"><span data-stu-id="2cc66-113">**Applies To**</span></span>

[<span data-ttu-id="2cc66-114">Forma</span><span class="sxs-lookup"><span data-stu-id="2cc66-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="2cc66-115">**Sintaxe de marca**</span><span class="sxs-lookup"><span data-stu-id="2cc66-115">**Tag Syntax**</span></span>

<span data-ttu-id="2cc66-116"><v: *Element* coordsize = " *expressão* " ></span><span class="sxs-lookup"><span data-stu-id="2cc66-116"><v: *element* coordsize=" *expression* "></span></span>

<span data-ttu-id="2cc66-117">**Sintaxe do script**</span><span class="sxs-lookup"><span data-stu-id="2cc66-117">**Script Syntax**</span></span>

<span data-ttu-id="2cc66-118">*Element* . coordsize = "*expressão*"</span><span class="sxs-lookup"><span data-stu-id="2cc66-118">*element* .coordsize="*expression*"</span></span>

<span data-ttu-id="2cc66-119">*expressão* = de *elemento*. coordsize</span><span class="sxs-lookup"><span data-stu-id="2cc66-119">*expression*=*element*.coordsize</span></span>

<span data-ttu-id="2cc66-120">**Comentários**</span><span class="sxs-lookup"><span data-stu-id="2cc66-120">**Remarks**</span></span>

<span data-ttu-id="2cc66-121">Se não for especificado, o tamanho da coordenada será o mesmo da caixa delimitadora da forma.</span><span class="sxs-lookup"><span data-stu-id="2cc66-121">If not specified, the coordinate size is the same as the bounding box of the shape.</span></span>

<span data-ttu-id="2cc66-122">Observe que esse atributo é um vetor e que as unidades são relativas ao comprimento e à largura do retângulo delimitador.</span><span class="sxs-lookup"><span data-stu-id="2cc66-122">Note that this attribute is a vector and that the units are relative to the length and width of the bounding rectangle.</span></span>

<span data-ttu-id="2cc66-123">Observe também que o mapeamento entre **coordsize** e a caixa delimitadora pode se tornar anisotropic.</span><span class="sxs-lookup"><span data-stu-id="2cc66-123">Also note that mapping between **coordsize** and the bounding box can be made anisotropic.</span></span> <span data-ttu-id="2cc66-124">Verifique se a **largura de coordsize** e a **altura de coordsize** são iguais à **largura** e **altura** do estilo se você não quiser distorcer a forma.</span><span class="sxs-lookup"><span data-stu-id="2cc66-124">Make sure that the **coordsize width** and **coordsize height** is the same as the **style width** and **height** if you don't want to distort the shape.</span></span>

<span data-ttu-id="2cc66-125">No script, como esse é um vetor 2D, você pode acessar os valores x e y separadamente e também pode determinar o tipo de unidades esperado.</span><span class="sxs-lookup"><span data-stu-id="2cc66-125">In scripting, because this is a 2-D vector, you can access the x and y values separately, and can also determine the type of units expected.</span></span>

<span data-ttu-id="2cc66-126">*Atributo padrão da VML*</span><span class="sxs-lookup"><span data-stu-id="2cc66-126">*VML Standard Attribute*</span></span>

<span data-ttu-id="2cc66-127">**Exemplo**</span><span class="sxs-lookup"><span data-stu-id="2cc66-127">**Example**</span></span>

<span data-ttu-id="2cc66-128">A forma tem 100 pontos de altura alta e 100 pontos, mas cada unidade horizontal e vertical no espaço de coordenadas é 1/10 de um ponto.</span><span class="sxs-lookup"><span data-stu-id="2cc66-128">The shape is 100 points high and 100 points wide, but each horizontal and vertical unit in the coordinate space is 1/10 of a point.</span></span>


```HTML
   <v:shape id="rect01"
   fillcolor="red" strokecolor="red"
   coordorigin="0 0" coordsize="1000 1000"
   style="position:relative;top:0;left:0;width:100pt;height:100pt"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   </v:shape>
```



<span data-ttu-id="2cc66-129">[Exemplo do atributo CoordSize](/previous-versions/bb229665(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="2cc66-129">[CoordSize Attribute Example](/previous-versions/bb229665(v=vs.85)).</span></span> <span data-ttu-id="2cc66-130">(Requer o Microsoft Internet Explorer 5 ou superior.)</span><span class="sxs-lookup"><span data-stu-id="2cc66-130">(Requires Microsoft Internet Explorer 5 or greater.)</span></span>

 

 