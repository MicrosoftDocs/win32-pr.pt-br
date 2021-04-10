---
title: Atributo FillOK de VML
description: Atributo FillOK de VML
ms.assetid: 6855544d-0f12-4e21-8101-1bbf45795777
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 667524be103b7c641643a52a85368a82a1289e5d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104294485"
---
# <a name="vml-fillok-attribute"></a><span data-ttu-id="a0a73-103">Atributo FillOK de VML</span><span class="sxs-lookup"><span data-stu-id="a0a73-103">VML FillOK Attribute</span></span>

<span data-ttu-id="a0a73-104">Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="a0a73-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="a0a73-105">As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.</span><span class="sxs-lookup"><span data-stu-id="a0a73-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="a0a73-106">A partir de dezembro de 2011, este tópico foi arquivado.</span><span class="sxs-lookup"><span data-stu-id="a0a73-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="a0a73-107">Como resultado, ele não é mais mantido ativamente.</span><span class="sxs-lookup"><span data-stu-id="a0a73-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="a0a73-108">Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="a0a73-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="a0a73-109">Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="a0a73-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="a0a73-110">Determina se um preenchimento será exibido.</span><span class="sxs-lookup"><span data-stu-id="a0a73-110">Determines whether a fill will be displayed.</span></span> <span data-ttu-id="a0a73-111">Leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="a0a73-111">Read/write.</span></span> <span data-ttu-id="a0a73-112">**VgTriState**.</span><span class="sxs-lookup"><span data-stu-id="a0a73-112">**VgTriState**.</span></span>

<span data-ttu-id="a0a73-113">**Aplica-se a**</span><span class="sxs-lookup"><span data-stu-id="a0a73-113">**Applies To**</span></span>

[<span data-ttu-id="a0a73-114">Caminho</span><span class="sxs-lookup"><span data-stu-id="a0a73-114">Path</span></span>](msdn-online-vml-path-element.md)

<span data-ttu-id="a0a73-115">**Sintaxe de marca**</span><span class="sxs-lookup"><span data-stu-id="a0a73-115">**Tag Syntax**</span></span>

<span data-ttu-id="a0a73-116"><v: *Element* fillok = " *expressão* " ></span><span class="sxs-lookup"><span data-stu-id="a0a73-116"><v: *element* fillok=" *expression* "></span></span>

<span data-ttu-id="a0a73-117">**Sintaxe do script**</span><span class="sxs-lookup"><span data-stu-id="a0a73-117">**Script Syntax**</span></span>

<span data-ttu-id="a0a73-118">*Element* . fillok = "*expressão*"</span><span class="sxs-lookup"><span data-stu-id="a0a73-118">*element* .fillok="*expression*"</span></span>

<span data-ttu-id="a0a73-119">*expressão* = de *elemento*. fillok</span><span class="sxs-lookup"><span data-stu-id="a0a73-119">*expression*=*element*.fillok</span></span>

<span data-ttu-id="a0a73-120">**Comentários**</span><span class="sxs-lookup"><span data-stu-id="a0a73-120">**Remarks**</span></span>

<span data-ttu-id="a0a73-121">Se **for false**, o caminho não poderá ser preenchido.</span><span class="sxs-lookup"><span data-stu-id="a0a73-121">If **False**, the path cannot be filled.</span></span> <span data-ttu-id="a0a73-122">O padrão é **True**.</span><span class="sxs-lookup"><span data-stu-id="a0a73-122">The default is **True**.</span></span> <span data-ttu-id="a0a73-123">Esse atributo substitui todos os outros atributos de preenchimento no elemento pai ou **Fill** .</span><span class="sxs-lookup"><span data-stu-id="a0a73-123">This attribute overrides all other fill attributes in the parent or **Fill** element.</span></span>

<span data-ttu-id="a0a73-124">*Atributo padrão da VML*</span><span class="sxs-lookup"><span data-stu-id="a0a73-124">*VML Standard Attribute*</span></span>

<span data-ttu-id="a0a73-125">**Exemplo**</span><span class="sxs-lookup"><span data-stu-id="a0a73-125">**Example**</span></span>

<span data-ttu-id="a0a73-126">O caminho não será preenchido.</span><span class="sxs-lookup"><span data-stu-id="a0a73-126">The path will not be filled.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red" fillcolor="red"
   style="top:1;left:1;width:50;height:50">
   <v:path id="myPath" fillok="False" v="m 1,1 l 1,200, 200,200, 200,1 x e"/>
   </v:shape>
```



 

 