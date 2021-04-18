---
title: Atributo userhidden da VML
description: Atributo userhidden da VML
ms.assetid: 0e4616c7-a456-4157-b77a-56cd289e913c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 519857d53cbec985afae31a5e7dea8811773dc43
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "105789619"
---
# <a name="vml-userhidden-attribute"></a><span data-ttu-id="0adfe-103">Atributo userhidden da VML</span><span class="sxs-lookup"><span data-stu-id="0adfe-103">VML UserHidden Attribute</span></span>

<span data-ttu-id="0adfe-104">Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="0adfe-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="0adfe-105">As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.</span><span class="sxs-lookup"><span data-stu-id="0adfe-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="0adfe-106">A partir de dezembro de 2011, este tópico foi arquivado.</span><span class="sxs-lookup"><span data-stu-id="0adfe-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="0adfe-107">Como resultado, ele não é mais mantido ativamente.</span><span class="sxs-lookup"><span data-stu-id="0adfe-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="0adfe-108">Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="0adfe-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="0adfe-109">Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="0adfe-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="0adfe-110">Determina se uma âncora de script está oculta.</span><span class="sxs-lookup"><span data-stu-id="0adfe-110">Determines whether a script anchor is hidden.</span></span> <span data-ttu-id="0adfe-111">Leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="0adfe-111">Read/write.</span></span> <span data-ttu-id="0adfe-112">**VgTriState**.</span><span class="sxs-lookup"><span data-stu-id="0adfe-112">**VgTriState**.</span></span>

<span data-ttu-id="0adfe-113">**Aplica-se a**</span><span class="sxs-lookup"><span data-stu-id="0adfe-113">**Applies To**</span></span>

[<span data-ttu-id="0adfe-114">Forma</span><span class="sxs-lookup"><span data-stu-id="0adfe-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="0adfe-115">**Sintaxe de marca**</span><span class="sxs-lookup"><span data-stu-id="0adfe-115">**Tag Syntax**</span></span>

<span data-ttu-id="0adfe-116"><v: *Element* o:userhidden = " *expressão* " ></span><span class="sxs-lookup"><span data-stu-id="0adfe-116"><v: *element* o:userhidden=" *expression* "></span></span>

<span data-ttu-id="0adfe-117">**Comentários**</span><span class="sxs-lookup"><span data-stu-id="0adfe-117">**Remarks**</span></span>

<span data-ttu-id="0adfe-118">O padrão é **False**.</span><span class="sxs-lookup"><span data-stu-id="0adfe-118">The default is **False**.</span></span> <span data-ttu-id="0adfe-119">Se **for true**, as âncoras de script permanecerão ocultas mesmo se a forma estiver visível.</span><span class="sxs-lookup"><span data-stu-id="0adfe-119">If **True**, script anchors stay hidden even if the shape is otherwise visible.</span></span>

<span data-ttu-id="0adfe-120">*Atributo de extensões de Microsoft Office*</span><span class="sxs-lookup"><span data-stu-id="0adfe-120">*Microsoft Office Extensions Attribute*</span></span>

<span data-ttu-id="0adfe-121">**Exemplo**</span><span class="sxs-lookup"><span data-stu-id="0adfe-121">**Example**</span></span>

<span data-ttu-id="0adfe-122">A âncora do script da forma está oculta.</span><span class="sxs-lookup"><span data-stu-id="0adfe-122">The script anchor of the shape is hidden.</span></span>


```HTML
   <v:rect id=myrect fillcolor="red" userhidden="True"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
```



 

 