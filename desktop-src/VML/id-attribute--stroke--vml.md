---
title: Atributo de ID (Stroke) (VML)
description: Atributo de ID (Stroke) (VML)
ms.assetid: 584b0e90-9d66-471b-a1d2-33a236c2ed8e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5efc9cfda1b7ddb359812d9ad28b37b851315da8
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103641359"
---
# <a name="id-attribute-strokevml"></a><span data-ttu-id="9c33d-103">Atributo de ID (Stroke) (VML)</span><span class="sxs-lookup"><span data-stu-id="9c33d-103">ID Attribute (Stroke)(VML)</span></span>

<span data-ttu-id="9c33d-104">Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="9c33d-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="9c33d-105">As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.</span><span class="sxs-lookup"><span data-stu-id="9c33d-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="9c33d-106">A partir de dezembro de 2011, este tópico foi arquivado.</span><span class="sxs-lookup"><span data-stu-id="9c33d-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="9c33d-107">Como resultado, ele não é mais mantido ativamente.</span><span class="sxs-lookup"><span data-stu-id="9c33d-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="9c33d-108">Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="9c33d-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="9c33d-109">Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="9c33d-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="9c33d-110">Um nome que fornece um identificador exclusivo para um traço.</span><span class="sxs-lookup"><span data-stu-id="9c33d-110">A name that provides a unique identifier for a stroke.</span></span> <span data-ttu-id="9c33d-111">Leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="9c33d-111">Read/write.</span></span> <span data-ttu-id="9c33d-112">**Cadeia de caracteres**.</span><span class="sxs-lookup"><span data-stu-id="9c33d-112">**String**.</span></span>

<span data-ttu-id="9c33d-113">**Aplica-se a**</span><span class="sxs-lookup"><span data-stu-id="9c33d-113">**Applies To**</span></span>

[<span data-ttu-id="9c33d-114">Pincel</span><span class="sxs-lookup"><span data-stu-id="9c33d-114">Stroke</span></span>](msdn-online-vml-stroke-element.md)

<span data-ttu-id="9c33d-115">**Sintaxe de marca**</span><span class="sxs-lookup"><span data-stu-id="9c33d-115">**Tag Syntax**</span></span>

<span data-ttu-id="9c33d-116"><v: *Element* ID = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="9c33d-116"><v: *element* id=" *expression* "></span></span>

<span data-ttu-id="9c33d-117">**Sintaxe do script**</span><span class="sxs-lookup"><span data-stu-id="9c33d-117">**Script Syntax**</span></span>

<span data-ttu-id="9c33d-118">*Element* . ID = "*expressão*"</span><span class="sxs-lookup"><span data-stu-id="9c33d-118">*element* .id="*expression*"</span></span>

<span data-ttu-id="9c33d-119">*expressão* = de *elemento*. ID</span><span class="sxs-lookup"><span data-stu-id="9c33d-119">*expression*=*element*.id</span></span>

<span data-ttu-id="9c33d-120">**Comentários**</span><span class="sxs-lookup"><span data-stu-id="9c33d-120">**Remarks**</span></span>

<span data-ttu-id="9c33d-121">Use **ID** para se referir a um traço específico.</span><span class="sxs-lookup"><span data-stu-id="9c33d-121">Use **ID** to refer to a specific stroke.</span></span> <span data-ttu-id="9c33d-122">Depois de criar um traço e fornecer a ele uma ID, você poderá usar o nome da ID quando desejar manipular o traço.</span><span class="sxs-lookup"><span data-stu-id="9c33d-122">Once you have created a stroke and given it an ID, you can use the ID name when you want to manipulate the stroke.</span></span>

<span data-ttu-id="9c33d-123">*Atributo padrão da VML*</span><span class="sxs-lookup"><span data-stu-id="9c33d-123">*VML Standard Attribute*</span></span>

<span data-ttu-id="9c33d-124">**Exemplo**</span><span class="sxs-lookup"><span data-stu-id="9c33d-124">**Example**</span></span>

<span data-ttu-id="9c33d-125">A forma tem uma ID de traço chamada "mystroke".</span><span class="sxs-lookup"><span data-stu-id="9c33d-125">The shape has a stroke ID called "mystroke".</span></span>


```HTML
   <v:shape id="rect01"
   strokecolor="red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:stroke id="mystroke"/>
   </v:shape>
```



 

 