---
title: Atributo VML MSO-Wrap-Distance-Left
description: Atributo VML MSO-Wrap-Distance-Left
ms.assetid: 25dcb5d0-a839-4a4b-8969-8e5dcf1baa47
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87d1e47fff0f9dceff5fd98ad526208bf487d851
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104294158"
---
# <a name="vml-mso-wrap-distance-left-attribute"></a><span data-ttu-id="3d722-103">Atributo VML MSO-Wrap-Distance-Left</span><span class="sxs-lookup"><span data-stu-id="3d722-103">VML MSO-Wrap-Distance-Left Attribute</span></span>

<span data-ttu-id="3d722-104">Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="3d722-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="3d722-105">As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.</span><span class="sxs-lookup"><span data-stu-id="3d722-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="3d722-106">A partir de dezembro de 2011, este tópico foi arquivado.</span><span class="sxs-lookup"><span data-stu-id="3d722-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="3d722-107">Como resultado, ele não é mais mantido ativamente.</span><span class="sxs-lookup"><span data-stu-id="3d722-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="3d722-108">Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="3d722-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="3d722-109">Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="3d722-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="3d722-110">Define a distância do lado esquerdo da forma com o texto que quebra ao seu respeito.</span><span class="sxs-lookup"><span data-stu-id="3d722-110">Defines the distance from the left side of the shape to the text that wraps around it.</span></span> <span data-ttu-id="3d722-111">Leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="3d722-111">Read/write.</span></span> <span data-ttu-id="3d722-112">**Cadeia de caracteres**.</span><span class="sxs-lookup"><span data-stu-id="3d722-112">**String**.</span></span>

<span data-ttu-id="3d722-113">**Aplica-se a**</span><span class="sxs-lookup"><span data-stu-id="3d722-113">**Applies To**</span></span>

[<span data-ttu-id="3d722-114">Forma</span><span class="sxs-lookup"><span data-stu-id="3d722-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="3d722-115">**Sintaxe de marca**</span><span class="sxs-lookup"><span data-stu-id="3d722-115">**Tag Syntax**</span></span>

<span data-ttu-id="3d722-116"><v: *elemento* Style = "Die-Wrap-Distance-left: *expression* " ></span><span class="sxs-lookup"><span data-stu-id="3d722-116"><v: *element* style="mso-wrap-distance-left: *expression* "></span></span>

<span data-ttu-id="3d722-117">**Comentários**</span><span class="sxs-lookup"><span data-stu-id="3d722-117">**Remarks**</span></span>

<span data-ttu-id="3d722-118">Observe que esse atributo é diferente do atributo de **margem** CSS.</span><span class="sxs-lookup"><span data-stu-id="3d722-118">Note that this attribute is different from the CSS **Margin** attribute.</span></span> <span data-ttu-id="3d722-119">**Margin** altera a origem da forma para incluir as áreas de margem, mas a distância de ajuste em Microsoft Office não altera a origem da forma.</span><span class="sxs-lookup"><span data-stu-id="3d722-119">**Margin** changes the origin of the shape to include the margin areas, but the wrap-distance in Microsoft Office does not change the origin of the shape.</span></span>

<span data-ttu-id="3d722-120">*Atributo de extensões de Microsoft Office*</span><span class="sxs-lookup"><span data-stu-id="3d722-120">*Microsoft Office Extensions Attribute*</span></span>

<span data-ttu-id="3d722-121">**Exemplo**</span><span class="sxs-lookup"><span data-stu-id="3d722-121">**Example**</span></span>

<span data-ttu-id="3d722-122">A forma tem uma distância de ajuste à esquerda de 10 pontos.</span><span class="sxs-lookup"><span data-stu-id="3d722-122">The shape has a left wrap-distance of 10 points.</span></span>


```HTML
   <v:shape id="rect01"
   fillcolor="red" strokecolor="red"
   coordorigin="-500 -500" coordsize="1000 1000"
   style="position:relative;top:0;left:0;width:100pt;height:100pt;mso-wrap-distance-left:10pt"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   </v:shape>
```



 

 