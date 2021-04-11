---
title: Atributo Chromakey de VML
description: Atributo Chromakey de VML
ms.assetid: 937ced3f-2e55-4a22-a9e0-83dc198104d4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22b69b10fe617de23783cf5e2e69b8b1a97b82fa
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104294226"
---
# <a name="vml-chromakey-attribute"></a><span data-ttu-id="3ae04-103">Atributo Chromakey de VML</span><span class="sxs-lookup"><span data-stu-id="3ae04-103">VML Chromakey Attribute</span></span>

<span data-ttu-id="3ae04-104">Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="3ae04-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="3ae04-105">As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.</span><span class="sxs-lookup"><span data-stu-id="3ae04-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="3ae04-106">A partir de dezembro de 2011, este tópico foi arquivado.</span><span class="sxs-lookup"><span data-stu-id="3ae04-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="3ae04-107">Como resultado, ele não é mais mantido ativamente.</span><span class="sxs-lookup"><span data-stu-id="3ae04-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="3ae04-108">Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="3ae04-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="3ae04-109">Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="3ae04-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="3ae04-110">Define o valor de cor da imagem que será tratada como transparente.</span><span class="sxs-lookup"><span data-stu-id="3ae04-110">Defines the color value of the image that will be treated as transparent.</span></span> <span data-ttu-id="3ae04-111">Leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="3ae04-111">Read/write.</span></span> <span data-ttu-id="3ae04-112">**VgColor**.</span><span class="sxs-lookup"><span data-stu-id="3ae04-112">**VgColor**.</span></span>

<span data-ttu-id="3ae04-113">**Aplica-se a**</span><span class="sxs-lookup"><span data-stu-id="3ae04-113">**Applies To**</span></span>

[<span data-ttu-id="3ae04-114">ImageData</span><span class="sxs-lookup"><span data-stu-id="3ae04-114">ImageData</span></span>](msdn-online-vml-imagedata-element.md)

<span data-ttu-id="3ae04-115">**Sintaxe de marca**</span><span class="sxs-lookup"><span data-stu-id="3ae04-115">**Tag Syntax**</span></span>

<span data-ttu-id="3ae04-116"><v: *Element* Chromakey = " *expressão* " ></span><span class="sxs-lookup"><span data-stu-id="3ae04-116"><v: *element* chromakey=" *expression* "></span></span>

<span data-ttu-id="3ae04-117">**Sintaxe do script**</span><span class="sxs-lookup"><span data-stu-id="3ae04-117">**Script Syntax**</span></span>

<span data-ttu-id="3ae04-118">*Element* . Chromakey = "*expressão*"</span><span class="sxs-lookup"><span data-stu-id="3ae04-118">*element* .chromakey="*expression*"</span></span>

<span data-ttu-id="3ae04-119">*expressão* = de *elemento*. Chromakey</span><span class="sxs-lookup"><span data-stu-id="3ae04-119">*expression*=*element*.chromakey</span></span>

<span data-ttu-id="3ae04-120">**Comentários**</span><span class="sxs-lookup"><span data-stu-id="3ae04-120">**Remarks**</span></span>

<span data-ttu-id="3ae04-121">Use esse atributo para tornar partes de uma imagem transparentes, inserindo a transparência em uma cor específica.</span><span class="sxs-lookup"><span data-stu-id="3ae04-121">Use this attribute to make parts of an image transparent by keying the transparency to a specific color.</span></span> <span data-ttu-id="3ae04-122">Por exemplo, se você tornar o  valor Chromakey **preto**, qualquer parte da imagem preta será transparente e a cor de preenchimento será "mostrada" nessa parte da imagem.</span><span class="sxs-lookup"><span data-stu-id="3ae04-122">For example, if you make the **Chromakey** value **black**, then any portion of the image that is black will be transparent, and the fill color will "show through" that portion of the image.</span></span>

<span data-ttu-id="3ae04-123">*Atributo padrão da VML*</span><span class="sxs-lookup"><span data-stu-id="3ae04-123">*VML Standard Attribute*</span></span>

<span data-ttu-id="3ae04-124">**Exemplo**</span><span class="sxs-lookup"><span data-stu-id="3ae04-124">**Example**</span></span>

<span data-ttu-id="3ae04-125">As áreas da imagem que são pretas sólidas ficarão transparentes, permitindo que a cor de preenchimento verde apareça nessas áreas.</span><span class="sxs-lookup"><span data-stu-id="3ae04-125">The areas of the image that are solid black will become transparent, allowing the green fill color to show through those areas instead.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red" fillcolor="green"
   style="top:1;left:1;width:300;height:200"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:imagedata chromakey="black" src="kids.jpg"/>
   </v:shape>
```



 

 