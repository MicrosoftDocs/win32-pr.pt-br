---
title: Atributo de obter VML
description: Atributo de obter VML
ms.assetid: 2ac034ff-f3dd-4e98-ad9d-4d9cdad28f3c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5675503def2f48d4c5fbf7154f0d0d05b2fe417d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366368"
---
# <a name="vml-gain-attribute"></a><span data-ttu-id="dcd9f-103">Atributo de obter VML</span><span class="sxs-lookup"><span data-stu-id="dcd9f-103">VML Gain Attribute</span></span>

<span data-ttu-id="dcd9f-104">Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="dcd9f-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="dcd9f-105">As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.</span><span class="sxs-lookup"><span data-stu-id="dcd9f-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="dcd9f-106">A partir de dezembro de 2011, este tópico foi arquivado.</span><span class="sxs-lookup"><span data-stu-id="dcd9f-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="dcd9f-107">Como resultado, ele não é mais mantido ativamente.</span><span class="sxs-lookup"><span data-stu-id="dcd9f-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="dcd9f-108">Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="dcd9f-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="dcd9f-109">Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="dcd9f-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="dcd9f-110">Define a intensidade de todas as cores em uma imagem.</span><span class="sxs-lookup"><span data-stu-id="dcd9f-110">Defines the intensity of all colors in an image.</span></span> <span data-ttu-id="dcd9f-111">Leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="dcd9f-111">Read/write.</span></span> <span data-ttu-id="dcd9f-112">**VgNumber**.</span><span class="sxs-lookup"><span data-stu-id="dcd9f-112">**VgNumber**.</span></span>

<span data-ttu-id="dcd9f-113">**Aplica-se a**</span><span class="sxs-lookup"><span data-stu-id="dcd9f-113">**Applies To**</span></span>

[<span data-ttu-id="dcd9f-114">ImageData</span><span class="sxs-lookup"><span data-stu-id="dcd9f-114">ImageData</span></span>](msdn-online-vml-imagedata-element.md)

<span data-ttu-id="dcd9f-115">**Sintaxe de marca**</span><span class="sxs-lookup"><span data-stu-id="dcd9f-115">**Tag Syntax**</span></span>

<span data-ttu-id="dcd9f-116"><v: *Element* saiba = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="dcd9f-116"><v: *element* gain=" *expression* "></span></span>

<span data-ttu-id="dcd9f-117">**Sintaxe do script**</span><span class="sxs-lookup"><span data-stu-id="dcd9f-117">**Script Syntax**</span></span>

<span data-ttu-id="dcd9f-118">*Element* . obter = "*expressão*"</span><span class="sxs-lookup"><span data-stu-id="dcd9f-118">*element* .gain="*expression*"</span></span>

<span data-ttu-id="dcd9f-119">*expressão* = de *elemento*. obter</span><span class="sxs-lookup"><span data-stu-id="dcd9f-119">*expression*=*element*.gain</span></span>

<span data-ttu-id="dcd9f-120">**Comentários**</span><span class="sxs-lookup"><span data-stu-id="dcd9f-120">**Remarks**</span></span>

<span data-ttu-id="dcd9f-121">Esse atributo define a claridade da cor branca, afetando todas as outras cores.</span><span class="sxs-lookup"><span data-stu-id="dcd9f-121">This attribute defines how bright the color white is, affecting all other colors.</span></span> <span data-ttu-id="dcd9f-122">Os valores variam de 0 a infinito.</span><span class="sxs-lookup"><span data-stu-id="dcd9f-122">Values range from 0 to infinity.</span></span> <span data-ttu-id="dcd9f-123">O valor padrão é 1.0.</span><span class="sxs-lookup"><span data-stu-id="dcd9f-123">The default value is 1.0.</span></span> <span data-ttu-id="dcd9f-124">Um valor de 0 não exibe nenhuma imagem.</span><span class="sxs-lookup"><span data-stu-id="dcd9f-124">A value of 0 displays no image.</span></span> <span data-ttu-id="dcd9f-125">Valores maiores que 1 claream a imagem e os valores menores que 1 fazem com que a imagem pareça Grayer.</span><span class="sxs-lookup"><span data-stu-id="dcd9f-125">Values greater than 1 lighten the picture and values less than 1 make the picture seem grayer.</span></span>

<span data-ttu-id="dcd9f-126">Esse atributo pode ser usado para criar efeitos interessantes.</span><span class="sxs-lookup"><span data-stu-id="dcd9f-126">This attribute can be used to create interesting effects.</span></span>

<span data-ttu-id="dcd9f-127">*Atributo padrão da VML*</span><span class="sxs-lookup"><span data-stu-id="dcd9f-127">*VML Standard Attribute*</span></span>

<span data-ttu-id="dcd9f-128">**Exemplo**</span><span class="sxs-lookup"><span data-stu-id="dcd9f-128">**Example**</span></span>

<span data-ttu-id="dcd9f-129">A imagem será exibida com todas as cores que tendem a ficar cinza.</span><span class="sxs-lookup"><span data-stu-id="dcd9f-129">The image will be displayed with all the colors tending toward gray.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:300;height:200"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:imagedata gain=".5" src="kids.jpg"/>
   </v:shape>
```





 

 