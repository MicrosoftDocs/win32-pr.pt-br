---
title: Atributo de rotação (forma) (VML)
description: Atributo de rotação (forma) (VML)
ms.assetid: e1a648a4-1e87-4bec-90b2-6d3a57c0dba0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f03b114c885cbeaf5392068e79cd7f63bbc1fc52
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104008314"
---
# <a name="rotation-attribute-shapevml"></a><span data-ttu-id="a2301-103">Atributo de rotação (forma) (VML)</span><span class="sxs-lookup"><span data-stu-id="a2301-103">Rotation Attribute (Shape)(VML)</span></span>

<span data-ttu-id="a2301-104">Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="a2301-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="a2301-105">As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.</span><span class="sxs-lookup"><span data-stu-id="a2301-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="a2301-106">A partir de dezembro de 2011, este tópico foi arquivado.</span><span class="sxs-lookup"><span data-stu-id="a2301-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="a2301-107">Como resultado, ele não é mais mantido ativamente.</span><span class="sxs-lookup"><span data-stu-id="a2301-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="a2301-108">Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="a2301-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="a2301-109">Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="a2301-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="a2301-110">Define o ângulo em que uma forma é girada.</span><span class="sxs-lookup"><span data-stu-id="a2301-110">Defines the angle that a shape is rotated.</span></span> <span data-ttu-id="a2301-111">Leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="a2301-111">Read/write.</span></span> <span data-ttu-id="a2301-112">[VgAngleInDegrees](msdn-online-vml-vgangleindegrees-data-type.md).</span><span class="sxs-lookup"><span data-stu-id="a2301-112">[VgAngleInDegrees](msdn-online-vml-vgangleindegrees-data-type.md).</span></span>

<span data-ttu-id="a2301-113">**Aplica-se a**</span><span class="sxs-lookup"><span data-stu-id="a2301-113">**Applies To**</span></span>

[<span data-ttu-id="a2301-114">Forma</span><span class="sxs-lookup"><span data-stu-id="a2301-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="a2301-115">**Sintaxe de marca**</span><span class="sxs-lookup"><span data-stu-id="a2301-115">**Tag Syntax**</span></span>

<span data-ttu-id="a2301-116"><v: *elemento* Style = "rotação: *expressão* " ></span><span class="sxs-lookup"><span data-stu-id="a2301-116"><v: *element* style="rotation: *expression* "></span></span>

<span data-ttu-id="a2301-117">**Sintaxe do script**</span><span class="sxs-lookup"><span data-stu-id="a2301-117">**Script Syntax**</span></span>

<span data-ttu-id="a2301-118">*elemento* . Rotation = "*expressão*"</span><span class="sxs-lookup"><span data-stu-id="a2301-118">*element* .rotation="*expression*"</span></span>

<span data-ttu-id="a2301-119">*expressão* = de *elemento*. Rotation</span><span class="sxs-lookup"><span data-stu-id="a2301-119">*expression*=*element*.rotation</span></span>

<span data-ttu-id="a2301-120">**Comentários**</span><span class="sxs-lookup"><span data-stu-id="a2301-120">**Remarks**</span></span>

<span data-ttu-id="a2301-121">O valor em graus pode ser positivo ou negativo, e valores maiores que 360 são modularizados para um círculo de 360 graus.</span><span class="sxs-lookup"><span data-stu-id="a2301-121">The value in degrees can be positive or negative, and values greater than 360 are modularized to a 360-degree circle.</span></span> <span data-ttu-id="a2301-122">Os ângulos positivos são no sentido horário.</span><span class="sxs-lookup"><span data-stu-id="a2301-122">Positive angles are clockwise.</span></span> <span data-ttu-id="a2301-123">O valor padrão é 0.</span><span class="sxs-lookup"><span data-stu-id="a2301-123">The default value is 0.</span></span>

<span data-ttu-id="a2301-124">Observe que a forma é reposicionada após a rotação para refletir as novas coordenadas da caixa delimitadora.</span><span class="sxs-lookup"><span data-stu-id="a2301-124">Note that the shape is repositioned after the rotation to reflect the new bounding box coordinates.</span></span>

<span data-ttu-id="a2301-125">Observe também que para scripts, o atributo **Style** não é usado e essa **rotação** é tratada como um atributo direto da forma.</span><span class="sxs-lookup"><span data-stu-id="a2301-125">Also note that for scripting, the **style** attribute is not used and that **Rotation** is treated as a direct attribute of the shape.</span></span>

<span data-ttu-id="a2301-126">O atributo de **rotação** é semelhante ao atributo de **rotação** HTML padrão para estilos.</span><span class="sxs-lookup"><span data-stu-id="a2301-126">The **Rotation** attribute is similar to the standard HTML **Rotation** attribute for styles.</span></span>

<span data-ttu-id="a2301-127">*Atributo padrão da VML*</span><span class="sxs-lookup"><span data-stu-id="a2301-127">*VML Standard Attribute*</span></span>

<span data-ttu-id="a2301-128">**Consulte também**</span><span class="sxs-lookup"><span data-stu-id="a2301-128">**See Also**</span></span>

<span data-ttu-id="a2301-129">**Exemplo**</span><span class="sxs-lookup"><span data-stu-id="a2301-129">**Example**</span></span>

<span data-ttu-id="a2301-130">O retângulo será inclinado 45 graus.</span><span class="sxs-lookup"><span data-stu-id="a2301-130">The rectangle will be tilted 45 degrees.</span></span>


```HTML
   <v:rect id=myrect fillcolor="red"
   style="position:relative;top:1;left:1;width:20;height:20;rotation:45">
   </v:rect>
```



<span data-ttu-id="a2301-131">[Exemplo de atributo de rotação](/previous-versions/bb264091(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="a2301-131">[Rotation Attribute Example](/previous-versions/bb264091(v=vs.85)).</span></span> <span data-ttu-id="a2301-132">(Requer o Microsoft Internet Explorer 5 ou superior.)</span><span class="sxs-lookup"><span data-stu-id="a2301-132">(Requires Microsoft Internet Explorer 5 or greater.)</span></span>

 

 