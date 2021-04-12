---
title: Atributo src (Fill) (VML)
description: Atributo src (Fill) (VML)
ms.assetid: 88ad9413-1863-41e2-855b-2bf155ce23cc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fddfcc6bb0ba7b4b026287c1efbbd8a20e09c37a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104454085"
---
# <a name="src-attribute-fillvml"></a><span data-ttu-id="726a0-103">Atributo src (Fill) (VML)</span><span class="sxs-lookup"><span data-stu-id="726a0-103">Src Attribute (Fill)(VML)</span></span>

<span data-ttu-id="726a0-104">Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="726a0-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="726a0-105">As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.</span><span class="sxs-lookup"><span data-stu-id="726a0-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="726a0-106">A partir de dezembro de 2011, este tópico foi arquivado.</span><span class="sxs-lookup"><span data-stu-id="726a0-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="726a0-107">Como resultado, ele não é mais mantido ativamente.</span><span class="sxs-lookup"><span data-stu-id="726a0-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="726a0-108">Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="726a0-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="726a0-109">Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="726a0-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="726a0-110">Define a imagem a ser carregada para um preenchimento.</span><span class="sxs-lookup"><span data-stu-id="726a0-110">Defines the image to load for a fill.</span></span> <span data-ttu-id="726a0-111">Leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="726a0-111">Read/write.</span></span> <span data-ttu-id="726a0-112">**Cadeia de caracteres**.</span><span class="sxs-lookup"><span data-stu-id="726a0-112">**String**.</span></span>

<span data-ttu-id="726a0-113">**Aplica-se a**</span><span class="sxs-lookup"><span data-stu-id="726a0-113">**Applies To**</span></span>

[<span data-ttu-id="726a0-114">Preencher</span><span class="sxs-lookup"><span data-stu-id="726a0-114">Fill</span></span>](msdn-online-vml-fill-element.md)

<span data-ttu-id="726a0-115">**Sintaxe de marca**</span><span class="sxs-lookup"><span data-stu-id="726a0-115">**Tag Syntax**</span></span>

<span data-ttu-id="726a0-116"><v: *Element* src = " *expressão* " ></span><span class="sxs-lookup"><span data-stu-id="726a0-116"><v: *element* src=" *expression* "></span></span>

<span data-ttu-id="726a0-117">**Sintaxe do script**</span><span class="sxs-lookup"><span data-stu-id="726a0-117">**Script Syntax**</span></span>

<span data-ttu-id="726a0-118">*Element* . src = "*expressão \* \* *"**</span><span class="sxs-lookup"><span data-stu-id="726a0-118">*element* .src="*expression\*\*\*"*\*</span></span>

<span data-ttu-id="726a0-119">*expressão* = de *elemento*. src</span><span class="sxs-lookup"><span data-stu-id="726a0-119">*expression*=*element*.src</span></span>

<span data-ttu-id="726a0-120">**Comentários**</span><span class="sxs-lookup"><span data-stu-id="726a0-120">**Remarks**</span></span>

<span data-ttu-id="726a0-121">URL para uma imagem a ser carregada para preenchimentos de imagem e padrão.</span><span class="sxs-lookup"><span data-stu-id="726a0-121">URL to an image to load for image and pattern fills.</span></span> <span data-ttu-id="726a0-122">Esse atributo sempre deve estar presente e apontar para dados de imagem válidos para que uma imagem apareça.</span><span class="sxs-lookup"><span data-stu-id="726a0-122">This attribute must always be present and point to valid image data for a picture to appear.</span></span> <span data-ttu-id="726a0-123">Se esse atributo aparecer sozinho (ou seja, sem **href** ou atributo de **título** ), a imagem será vinculada.</span><span class="sxs-lookup"><span data-stu-id="726a0-123">If this attribute appears alone (that is, no **HRef** or **Title** attribute), then the image is linked.</span></span>

<span data-ttu-id="726a0-124">*Atributo padrão da VML*</span><span class="sxs-lookup"><span data-stu-id="726a0-124">*VML Standard Attribute*</span></span>

<span data-ttu-id="726a0-125">**Exemplo**</span><span class="sxs-lookup"><span data-stu-id="726a0-125">**Example**</span></span>

<span data-ttu-id="726a0-126">É exibida uma imagem ao lado com o arquivo myimage.gif como uma fonte.</span><span class="sxs-lookup"><span data-stu-id="726a0-126">A tiled image using the file myimage.gif as a source is displayed.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill type="tile" src="myimage.gif"/>
   </v:shape>
```



 

 