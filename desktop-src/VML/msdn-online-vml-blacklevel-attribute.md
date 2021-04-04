---
title: Atributo BlackLevel de VML
description: Atributo BlackLevel de VML
ms.assetid: b30446c2-f4f3-49f5-aa60-4119f211add2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5394f8b218f2eb577aa63ead5ae940fe2a49029f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104007759"
---
# <a name="vml-blacklevel-attribute"></a><span data-ttu-id="29712-103">Atributo BlackLevel de VML</span><span class="sxs-lookup"><span data-stu-id="29712-103">VML BlackLevel Attribute</span></span>

<span data-ttu-id="29712-104">Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="29712-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="29712-105">As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.</span><span class="sxs-lookup"><span data-stu-id="29712-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="29712-106">A partir de dezembro de 2011, este tópico foi arquivado.</span><span class="sxs-lookup"><span data-stu-id="29712-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="29712-107">Como resultado, ele não é mais mantido ativamente.</span><span class="sxs-lookup"><span data-stu-id="29712-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="29712-108">Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="29712-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="29712-109">Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="29712-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="29712-110">Define a intensidade de preto em uma imagem.</span><span class="sxs-lookup"><span data-stu-id="29712-110">Defines the intensity of black in an image.</span></span> <span data-ttu-id="29712-111">Leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="29712-111">Read/write.</span></span> <span data-ttu-id="29712-112">**VgNumber**.</span><span class="sxs-lookup"><span data-stu-id="29712-112">**VgNumber**.</span></span>

<span data-ttu-id="29712-113">**Aplica-se a**</span><span class="sxs-lookup"><span data-stu-id="29712-113">**Applies To**</span></span>

[<span data-ttu-id="29712-114">ImageData</span><span class="sxs-lookup"><span data-stu-id="29712-114">ImageData</span></span>](msdn-online-vml-imagedata-element.md)

<span data-ttu-id="29712-115">**Sintaxe de marca**</span><span class="sxs-lookup"><span data-stu-id="29712-115">**Tag Syntax**</span></span>

<span data-ttu-id="29712-116"><v: *Element* blacklevel = " *expressão* " ></span><span class="sxs-lookup"><span data-stu-id="29712-116"><v: *element* blacklevel=" *expression* "></span></span>

<span data-ttu-id="29712-117">**Sintaxe do script**</span><span class="sxs-lookup"><span data-stu-id="29712-117">**Script Syntax**</span></span>

<span data-ttu-id="29712-118">*Element* . blacklevel = "*expressão*"</span><span class="sxs-lookup"><span data-stu-id="29712-118">*element* .blacklevel="*expression*"</span></span>

<span data-ttu-id="29712-119">*expressão* = de *elemento*. blacklevel</span><span class="sxs-lookup"><span data-stu-id="29712-119">*expression*=*element*.blacklevel</span></span>

<span data-ttu-id="29712-120">**Comentários**</span><span class="sxs-lookup"><span data-stu-id="29712-120">**Remarks**</span></span>

<span data-ttu-id="29712-121">Permite que o nível de cor seja modificado para que os pretos apareçam como verdadeiros pretos e todas as outras cores fiquem visíveis como sombras acima do preto.</span><span class="sxs-lookup"><span data-stu-id="29712-121">Allows the color level to be modified so that blacks appear as true blacks, and all other colors are visible as shades above black.</span></span> <span data-ttu-id="29712-122">O valor padrão é 0.</span><span class="sxs-lookup"><span data-stu-id="29712-122">The default value is 0.</span></span> <span data-ttu-id="29712-123">Embora qualquer número entre o infinito positivo e negativo seja permitido, valores menores que-0,5 serão exibidos como todos os pretos e valores maiores que 0,5 serão exibidos como todos os brancos.</span><span class="sxs-lookup"><span data-stu-id="29712-123">While any number between positive and negative infinity is permitted, values less than -0.5 will display as all black and values greater than 0.5 will display as all white.</span></span>

<span data-ttu-id="29712-124">*Atributo padrão da VML*</span><span class="sxs-lookup"><span data-stu-id="29712-124">*VML Standard Attribute*</span></span>

<span data-ttu-id="29712-125">**Exemplo**</span><span class="sxs-lookup"><span data-stu-id="29712-125">**Example**</span></span>

<span data-ttu-id="29712-126">A imagem será exibida com tons muito escuros.</span><span class="sxs-lookup"><span data-stu-id="29712-126">The image will be displayed with very dark tones.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:300;height:200"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:imagedata blacklevel="-0.2" src="kids.jpg"/>
   </v:shape>
```



 

 