---
title: Atributo StrokeOK de VML
description: Atributo StrokeOK de VML
ms.assetid: f150f87b-1ed9-4c53-bf7f-ebe1e81642fd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7a2875e3e6e8374238340ff2a596852e5ebce7c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103917514"
---
# <a name="vml-strokeok-attribute"></a><span data-ttu-id="d61db-103">Atributo StrokeOK de VML</span><span class="sxs-lookup"><span data-stu-id="d61db-103">VML StrokeOK Attribute</span></span>

<span data-ttu-id="d61db-104">Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="d61db-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="d61db-105">As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.</span><span class="sxs-lookup"><span data-stu-id="d61db-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="d61db-106">A partir de dezembro de 2011, este tópico foi arquivado.</span><span class="sxs-lookup"><span data-stu-id="d61db-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="d61db-107">Como resultado, ele não é mais mantido ativamente.</span><span class="sxs-lookup"><span data-stu-id="d61db-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="d61db-108">Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="d61db-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="d61db-109">Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="d61db-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="d61db-110">Determina se um traço será exibido.</span><span class="sxs-lookup"><span data-stu-id="d61db-110">Determines whether a stroke will be displayed.</span></span> <span data-ttu-id="d61db-111">Leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="d61db-111">Read/write.</span></span> <span data-ttu-id="d61db-112">**VgTriState**.</span><span class="sxs-lookup"><span data-stu-id="d61db-112">**VgTriState**.</span></span>

<span data-ttu-id="d61db-113">**Aplica-se a**</span><span class="sxs-lookup"><span data-stu-id="d61db-113">**Applies To**</span></span>

[<span data-ttu-id="d61db-114">Caminho</span><span class="sxs-lookup"><span data-stu-id="d61db-114">Path</span></span>](msdn-online-vml-path-element.md)

<span data-ttu-id="d61db-115">**Sintaxe de marca**</span><span class="sxs-lookup"><span data-stu-id="d61db-115">**Tag Syntax**</span></span>

<span data-ttu-id="d61db-116"><v: *Element* strokeok = " *expressão* " ></span><span class="sxs-lookup"><span data-stu-id="d61db-116"><v: *element* strokeok=" *expression* "></span></span>

<span data-ttu-id="d61db-117">**Sintaxe do script**</span><span class="sxs-lookup"><span data-stu-id="d61db-117">**Script Syntax**</span></span>

<span data-ttu-id="d61db-118">*Element* . strokeok = "*expressão*"</span><span class="sxs-lookup"><span data-stu-id="d61db-118">*element* .strokeok="*expression*"</span></span>

<span data-ttu-id="d61db-119">*expressão* = de *elemento*. strokeok</span><span class="sxs-lookup"><span data-stu-id="d61db-119">*expression*=*element*.strokeok</span></span>

<span data-ttu-id="d61db-120">**Comentários**</span><span class="sxs-lookup"><span data-stu-id="d61db-120">**Remarks**</span></span>

<span data-ttu-id="d61db-121">Se **for false**, o caminho não poderá ser traçado.</span><span class="sxs-lookup"><span data-stu-id="d61db-121">If **False**, the path cannot be stroked.</span></span> <span data-ttu-id="d61db-122">O padrão é **True**.</span><span class="sxs-lookup"><span data-stu-id="d61db-122">The default is **True**.</span></span> <span data-ttu-id="d61db-123">Esse atributo substitui todos os outros atributos de traço no elemento pai ou **Stroke** .</span><span class="sxs-lookup"><span data-stu-id="d61db-123">This attribute overrides all other stroke attributes in the parent or **Stroke** element.</span></span>

<span data-ttu-id="d61db-124">*Atributo padrão da VML*</span><span class="sxs-lookup"><span data-stu-id="d61db-124">*VML Standard Attribute*</span></span>

<span data-ttu-id="d61db-125">**Exemplo**</span><span class="sxs-lookup"><span data-stu-id="d61db-125">**Example**</span></span>

<span data-ttu-id="d61db-126">O caminho não será traçado.</span><span class="sxs-lookup"><span data-stu-id="d61db-126">The path will not be stroked.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50">
   <v:path id="myPath" strokeok="False" v="m 1,1 l 1,200, 200,200, 200,1 x e"/>
   </v:shape>
```



 

 