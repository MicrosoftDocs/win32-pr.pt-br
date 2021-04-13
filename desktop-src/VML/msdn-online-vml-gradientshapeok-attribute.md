---
title: Atributo GradientShapeOK de VML
description: Atributo GradientShapeOK de VML
ms.assetid: c26ac4cb-f7f0-4666-b32f-d9fcaf9044a2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d1b7c215fbe0b98c11f7e4d33301e81798bd37f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366618"
---
# <a name="vml-gradientshapeok-attribute"></a><span data-ttu-id="09492-103">Atributo GradientShapeOK de VML</span><span class="sxs-lookup"><span data-stu-id="09492-103">VML GradientShapeOK Attribute</span></span>

<span data-ttu-id="09492-104">Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="09492-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="09492-105">As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.</span><span class="sxs-lookup"><span data-stu-id="09492-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="09492-106">A partir de dezembro de 2011, este tópico foi arquivado.</span><span class="sxs-lookup"><span data-stu-id="09492-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="09492-107">Como resultado, ele não é mais mantido ativamente.</span><span class="sxs-lookup"><span data-stu-id="09492-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="09492-108">Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="09492-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="09492-109">Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="09492-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="09492-110">Determina se um caminho de gradiente será composto de caminhos concêntricos repetidos.</span><span class="sxs-lookup"><span data-stu-id="09492-110">Determines whether a gradient path will be made up of repeated concentric paths.</span></span> <span data-ttu-id="09492-111">Leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="09492-111">Read/write.</span></span> <span data-ttu-id="09492-112">**VgTriState**.</span><span class="sxs-lookup"><span data-stu-id="09492-112">**VgTriState**.</span></span>

<span data-ttu-id="09492-113">**Aplica-se a**</span><span class="sxs-lookup"><span data-stu-id="09492-113">**Applies To**</span></span>

[<span data-ttu-id="09492-114">Caminho</span><span class="sxs-lookup"><span data-stu-id="09492-114">Path</span></span>](msdn-online-vml-path-element.md)

<span data-ttu-id="09492-115">**Sintaxe de marca**</span><span class="sxs-lookup"><span data-stu-id="09492-115">**Tag Syntax**</span></span>

<span data-ttu-id="09492-116"><v: *Element* gradientshapeok = " *expressão* " ></span><span class="sxs-lookup"><span data-stu-id="09492-116"><v: *element* gradientshapeok=" *expression* "></span></span>

<span data-ttu-id="09492-117">**Sintaxe do script**</span><span class="sxs-lookup"><span data-stu-id="09492-117">**Script Syntax**</span></span>

<span data-ttu-id="09492-118">*Element* . gradientshapeok = "*expressão*"</span><span class="sxs-lookup"><span data-stu-id="09492-118">*element* .gradientshapeok="*expression*"</span></span>

<span data-ttu-id="09492-119">*expressão* = de *elemento*. gradientshapeok</span><span class="sxs-lookup"><span data-stu-id="09492-119">*expression*=*element*.gradientshapeok</span></span>

<span data-ttu-id="09492-120">**Comentários**</span><span class="sxs-lookup"><span data-stu-id="09492-120">**Remarks**</span></span>

<span data-ttu-id="09492-121">Se **for true**, o caminho será preenchido com um preenchimento gradiente concêntrico usando o caminho como a forma repetida do gradiente. O padrão é **false**.</span><span class="sxs-lookup"><span data-stu-id="09492-121">If **True**, the path will be filled with a concentric gradient fill using the path as the repeated shape of the gradient.The default is **False**.</span></span>

<span data-ttu-id="09492-122">*Atributo padrão da VML*</span><span class="sxs-lookup"><span data-stu-id="09492-122">*VML Standard Attribute*</span></span>

<span data-ttu-id="09492-123">**Exemplo**</span><span class="sxs-lookup"><span data-stu-id="09492-123">**Example**</span></span>

<span data-ttu-id="09492-124">O caminho será preenchido com um preenchimento gradiente concêntrico formado por retângulos repetidos.</span><span class="sxs-lookup"><span data-stu-id="09492-124">The path will be filled with a concentric gradient fill made up of repeated rectangles.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:path gradientshapeok="True"/>
   </v:shape>
```



 

 