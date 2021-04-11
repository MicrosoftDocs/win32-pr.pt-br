---
title: Atributo ext (distorção) (VML)
description: Atributo ext (distorção) (VML)
ms.assetid: ff1dfb2f-9098-4418-a2f7-c7159328bd09
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 153273f613d188ae9e6fe733b2d0337c5010295d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104162334"
---
# <a name="ext-attribute-skewvml"></a><span data-ttu-id="58cf3-103">Atributo ext (distorção) (VML)</span><span class="sxs-lookup"><span data-stu-id="58cf3-103">Ext Attribute (Skew)(VML)</span></span>

<span data-ttu-id="58cf3-104">Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="58cf3-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="58cf3-105">As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.</span><span class="sxs-lookup"><span data-stu-id="58cf3-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="58cf3-106">A partir de dezembro de 2011, este tópico foi arquivado.</span><span class="sxs-lookup"><span data-stu-id="58cf3-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="58cf3-107">Como resultado, ele não é mais mantido ativamente.</span><span class="sxs-lookup"><span data-stu-id="58cf3-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="58cf3-108">Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="58cf3-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="58cf3-109">Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="58cf3-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="58cf3-110">Define a maneira como uma distorção é exibida.</span><span class="sxs-lookup"><span data-stu-id="58cf3-110">Defines the way a skew is displayed.</span></span> <span data-ttu-id="58cf3-111">Leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="58cf3-111">Read/write.</span></span> <span data-ttu-id="58cf3-112">**Cadeia de caracteres**.</span><span class="sxs-lookup"><span data-stu-id="58cf3-112">**String**.</span></span>

<span data-ttu-id="58cf3-113">**Aplica-se a**</span><span class="sxs-lookup"><span data-stu-id="58cf3-113">**Applies To**</span></span>

[<span data-ttu-id="58cf3-114">Inclinar</span><span class="sxs-lookup"><span data-stu-id="58cf3-114">Skew</span></span>](msdn-online-vml-skew-element.md)

<span data-ttu-id="58cf3-115">**Sintaxe de marca**</span><span class="sxs-lookup"><span data-stu-id="58cf3-115">**Tag Syntax**</span></span>

<span data-ttu-id="58cf3-116"><o: *Element* v:ext = " *expressão* " ></span><span class="sxs-lookup"><span data-stu-id="58cf3-116"><o: *element* v:ext=" *expression* "></span></span>

<span data-ttu-id="58cf3-117">**Sintaxe do script**</span><span class="sxs-lookup"><span data-stu-id="58cf3-117">**Script Syntax**</span></span>

<span data-ttu-id="58cf3-118">*Element* . ext = "*expressão*"</span><span class="sxs-lookup"><span data-stu-id="58cf3-118">*element* .ext="*expression*"</span></span>

<span data-ttu-id="58cf3-119">*expressão* = de *elemento*. ext</span><span class="sxs-lookup"><span data-stu-id="58cf3-119">*expression*=*element*.ext</span></span>

<span data-ttu-id="58cf3-120">**Comentários**</span><span class="sxs-lookup"><span data-stu-id="58cf3-120">**Remarks**</span></span>

<span data-ttu-id="58cf3-121">Esse atributo é usado para informar aos editores gráficos como processar o elemento **skew** .</span><span class="sxs-lookup"><span data-stu-id="58cf3-121">This attribute is used to tell graphical editors how to process the **Skew** element.</span></span> <span data-ttu-id="58cf3-122">Os valores são:</span><span class="sxs-lookup"><span data-stu-id="58cf3-122">Values include:</span></span>

-   <span data-ttu-id="58cf3-123">**edit**</span><span class="sxs-lookup"><span data-stu-id="58cf3-123">**edit**</span></span>
-   <span data-ttu-id="58cf3-124">**exibição** (padrão)</span><span class="sxs-lookup"><span data-stu-id="58cf3-124">**view** (default)</span></span>
-   <span data-ttu-id="58cf3-125">**backwardCompatible**</span><span class="sxs-lookup"><span data-stu-id="58cf3-125">**backwardCompatible**</span></span>

<span data-ttu-id="58cf3-126">Se uma extensão for definida como **Editar**, ela poderá ser ignorada por um visualizador de software.</span><span class="sxs-lookup"><span data-stu-id="58cf3-126">If an extension is set to **edit**, it can be ignored by a software viewer.</span></span> <span data-ttu-id="58cf3-127">Se definido como **Exibir**, o visualizador deverá renderizar a representação de bitmap em vez disso.</span><span class="sxs-lookup"><span data-stu-id="58cf3-127">If set to **view**, the viewer must render the bitmap representation instead.</span></span>

<span data-ttu-id="58cf3-128">*Atributo de extensões de Microsoft Office*</span><span class="sxs-lookup"><span data-stu-id="58cf3-128">*Microsoft Office Extensions Attribute*</span></span>

 

 