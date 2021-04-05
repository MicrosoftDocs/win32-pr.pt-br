---
title: Atributo de ID (caminho) (VML)
description: Atributo de ID (caminho) (VML)
ms.assetid: f0f3a526-d0e1-46f8-a85c-b99d27c3fdeb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfbd5d8d9acdcafaf015354dc4c99f3703034e89
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104084556"
---
# <a name="id-attribute-pathvml"></a><span data-ttu-id="f20f8-103">Atributo de ID (caminho) (VML)</span><span class="sxs-lookup"><span data-stu-id="f20f8-103">ID Attribute (Path)(VML)</span></span>

<span data-ttu-id="f20f8-104">Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="f20f8-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="f20f8-105">As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.</span><span class="sxs-lookup"><span data-stu-id="f20f8-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="f20f8-106">A partir de dezembro de 2011, este tópico foi arquivado.</span><span class="sxs-lookup"><span data-stu-id="f20f8-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="f20f8-107">Como resultado, ele não é mais mantido ativamente.</span><span class="sxs-lookup"><span data-stu-id="f20f8-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="f20f8-108">Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="f20f8-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="f20f8-109">Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="f20f8-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="f20f8-110">Um nome que fornece um identificador exclusivo para um caminho.</span><span class="sxs-lookup"><span data-stu-id="f20f8-110">A name that provides a unique identifier for a path.</span></span> <span data-ttu-id="f20f8-111">Leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="f20f8-111">Read/write.</span></span> <span data-ttu-id="f20f8-112">**Cadeia de caracteres**.</span><span class="sxs-lookup"><span data-stu-id="f20f8-112">**String**.</span></span>

<span data-ttu-id="f20f8-113">**Aplica-se a**</span><span class="sxs-lookup"><span data-stu-id="f20f8-113">**Applies To**</span></span>

[<span data-ttu-id="f20f8-114">Caminho</span><span class="sxs-lookup"><span data-stu-id="f20f8-114">Path</span></span>](msdn-online-vml-path-element.md)

<span data-ttu-id="f20f8-115">**Sintaxe de marca**</span><span class="sxs-lookup"><span data-stu-id="f20f8-115">**Tag Syntax**</span></span>

<span data-ttu-id="f20f8-116"><v: *Element* ID = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="f20f8-116"><v: *element* id=" *expression* "></span></span>

<span data-ttu-id="f20f8-117">**Sintaxe do script**</span><span class="sxs-lookup"><span data-stu-id="f20f8-117">**Script Syntax**</span></span>

<span data-ttu-id="f20f8-118">*Element* . ID = "*expressão*"</span><span class="sxs-lookup"><span data-stu-id="f20f8-118">*element* .id="*expression*"</span></span>

<span data-ttu-id="f20f8-119">*expressão* = de *elemento*. ID</span><span class="sxs-lookup"><span data-stu-id="f20f8-119">*expression*=*element*.id</span></span>

<span data-ttu-id="f20f8-120">**Comentários**</span><span class="sxs-lookup"><span data-stu-id="f20f8-120">**Remarks**</span></span>

<span data-ttu-id="f20f8-121">Use **ID** para se referir a um caminho específico.</span><span class="sxs-lookup"><span data-stu-id="f20f8-121">Use **ID** to refer to a specific path.</span></span> <span data-ttu-id="f20f8-122">Depois de criar um caminho e fornecer a ele uma ID, você poderá usar o nome da ID quando desejar manipular o caminho.</span><span class="sxs-lookup"><span data-stu-id="f20f8-122">Once you have created a path and given it an ID, you can use the ID name when you want to manipulate the path.</span></span>

<span data-ttu-id="f20f8-123">*Atributo padrão da VML*</span><span class="sxs-lookup"><span data-stu-id="f20f8-123">*VML Standard Attribute*</span></span>

<span data-ttu-id="f20f8-124">**Exemplo**</span><span class="sxs-lookup"><span data-stu-id="f20f8-124">**Example**</span></span>

<span data-ttu-id="f20f8-125">A forma tem uma ID de caminho chamada "MYPATH".</span><span class="sxs-lookup"><span data-stu-id="f20f8-125">The shape has a path ID called "myPath".</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50">
   <v:path id= "myPath" v="m 1,1 l 1,200, 200,200, 200,1 x e"/>
   </v:shape>
```



 

 