---
title: Atributo Angle (preenchimento) (VML)
description: Atributo Angle (preenchimento) (VML)
ms.assetid: 97203e73-4dae-40c5-bb3d-127110525cff
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4167c52d82fabc5804143966b13f9d24ff7b39d6
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104008076"
---
# <a name="angle-attribute-fillvml"></a><span data-ttu-id="809cf-103">Atributo Angle (preenchimento) (VML)</span><span class="sxs-lookup"><span data-stu-id="809cf-103">Angle Attribute (Fill)(VML)</span></span>

<span data-ttu-id="809cf-104">Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="809cf-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="809cf-105">As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.</span><span class="sxs-lookup"><span data-stu-id="809cf-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="809cf-106">A partir de dezembro de 2011, este tópico foi arquivado.</span><span class="sxs-lookup"><span data-stu-id="809cf-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="809cf-107">Como resultado, ele não é mais mantido ativamente.</span><span class="sxs-lookup"><span data-stu-id="809cf-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="809cf-108">Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="809cf-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="809cf-109">Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="809cf-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="809cf-110">Define o ângulo de um preenchimento gradual.</span><span class="sxs-lookup"><span data-stu-id="809cf-110">Defines the angle of a gradient fill.</span></span> <span data-ttu-id="809cf-111">Leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="809cf-111">Read/write.</span></span> <span data-ttu-id="809cf-112">[VgAngle](msdn-online-vml-vgangleindegrees-data-type.md) .</span><span class="sxs-lookup"><span data-stu-id="809cf-112">[VgAngle](msdn-online-vml-vgangleindegrees-data-type.md) .</span></span>

<span data-ttu-id="809cf-113">**Aplica-se a**</span><span class="sxs-lookup"><span data-stu-id="809cf-113">**Applies To**</span></span>

[<span data-ttu-id="809cf-114">Preencher</span><span class="sxs-lookup"><span data-stu-id="809cf-114">Fill</span></span>](msdn-online-vml-fill-element.md)

<span data-ttu-id="809cf-115">**Sintaxe de marca**</span><span class="sxs-lookup"><span data-stu-id="809cf-115">**Tag Syntax**</span></span>

<span data-ttu-id="809cf-116"><v: *elemento* Angle = " *expressão* " ></span><span class="sxs-lookup"><span data-stu-id="809cf-116"><v: *element* angle=" *expression* "></span></span>

<span data-ttu-id="809cf-117">**Sintaxe do script**</span><span class="sxs-lookup"><span data-stu-id="809cf-117">**Script Syntax**</span></span>

<span data-ttu-id="809cf-118">*elemento* . Angle = "*expressão*"</span><span class="sxs-lookup"><span data-stu-id="809cf-118">*element* .angle="*expression*"</span></span>

<span data-ttu-id="809cf-119">*expressão* = de *elemento*. Angle</span><span class="sxs-lookup"><span data-stu-id="809cf-119">*expression*=*element*.angle</span></span>

<span data-ttu-id="809cf-120">**Comentários**</span><span class="sxs-lookup"><span data-stu-id="809cf-120">**Remarks**</span></span>

<span data-ttu-id="809cf-121">O vetor de um gradiente é perpendicular ao vetor da direção de mistura de uma cor para outra.</span><span class="sxs-lookup"><span data-stu-id="809cf-121">The vector of a gradient is perpendicular to the vector of the blend direction from one color to another.</span></span> <span data-ttu-id="809cf-122">O valor padrão é 0 (zero) graus, que é um vetor horizontal da esquerda para a direita.</span><span class="sxs-lookup"><span data-stu-id="809cf-122">The default value is 0 (zero) degrees, which is a horizontal vector from left to right.</span></span> <span data-ttu-id="809cf-123">Ângulos positivos giram o gradiente em uma direção do sentido anti-horário.</span><span class="sxs-lookup"><span data-stu-id="809cf-123">Positive angles rotate the gradient in a counter-clockwise direction.</span></span>

<span data-ttu-id="809cf-124">*Atributo padrão da VML*</span><span class="sxs-lookup"><span data-stu-id="809cf-124">*VML Standard Attribute*</span></span>

<span data-ttu-id="809cf-125">**Exemplo**</span><span class="sxs-lookup"><span data-stu-id="809cf-125">**Example**</span></span>

<span data-ttu-id="809cf-126">O preenchimento da forma é composto de um gradiente de duas cores, sendo executado de azul para vermelho em um ângulo de 45 graus.</span><span class="sxs-lookup"><span data-stu-id="809cf-126">The fill of the shape is composed of a gradient of two colors, running from blue to red at an angle of 45 degrees.</span></span> <span data-ttu-id="809cf-127">Vermelho estará no canto superior esquerdo e azul estará no canto inferior direito.</span><span class="sxs-lookup"><span data-stu-id="809cf-127">Red will be in the top left corner and blue will be in the bottom right corner.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill type="gradient" color="blue" color2="red" angle="45"/>
   </v:shape>
```



 

 