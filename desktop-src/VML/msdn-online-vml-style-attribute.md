---
title: Atributo de estilo da VML
description: Atributo de estilo da VML
ms.assetid: 1695d2b2-cf60-48f1-b47e-f0f43696b5b5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f291fad75bf14e06f40ad0a1446bd0418bba46b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104454087"
---
# <a name="vml-style-attribute"></a><span data-ttu-id="1e496-103">Atributo de estilo da VML</span><span class="sxs-lookup"><span data-stu-id="1e496-103">VML Style Attribute</span></span>

<span data-ttu-id="1e496-104">Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="1e496-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="1e496-105">As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.</span><span class="sxs-lookup"><span data-stu-id="1e496-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="1e496-106">A partir de dezembro de 2011, este tópico foi arquivado.</span><span class="sxs-lookup"><span data-stu-id="1e496-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="1e496-107">Como resultado, ele não é mais mantido ativamente.</span><span class="sxs-lookup"><span data-stu-id="1e496-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="1e496-108">Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="1e496-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="1e496-109">Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="1e496-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="1e496-110">Define o estilo do quadro.</span><span class="sxs-lookup"><span data-stu-id="1e496-110">Defines the style of the frame.</span></span> <span data-ttu-id="1e496-111">Leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="1e496-111">Read/write.</span></span> <span data-ttu-id="1e496-112">**Cadeia de caracteres**.</span><span class="sxs-lookup"><span data-stu-id="1e496-112">**String**.</span></span>

<span data-ttu-id="1e496-113">**Aplica-se a**</span><span class="sxs-lookup"><span data-stu-id="1e496-113">**Applies To**</span></span>

[<span data-ttu-id="1e496-114">VMLFrame</span><span class="sxs-lookup"><span data-stu-id="1e496-114">VMLFrame</span></span>](msdn-online-vml-vmlframe-element.md)

<span data-ttu-id="1e496-115">**Sintaxe de marca**</span><span class="sxs-lookup"><span data-stu-id="1e496-115">**Tag Syntax**</span></span>

<span data-ttu-id="1e496-116"><v: *elemento* Style = " *expressão* " ></span><span class="sxs-lookup"><span data-stu-id="1e496-116"><v: *element* style=" *expression* "></span></span>

<span data-ttu-id="1e496-117">**Sintaxe do script**</span><span class="sxs-lookup"><span data-stu-id="1e496-117">**Script Syntax**</span></span>

<span data-ttu-id="1e496-118">*elemento* . Style = "*expressão*"</span><span class="sxs-lookup"><span data-stu-id="1e496-118">*element* .style="*expression*"</span></span>

<span data-ttu-id="1e496-119">*expressão* = de *elemento*. Style</span><span class="sxs-lookup"><span data-stu-id="1e496-119">*expression*=*element*.style</span></span>

<span data-ttu-id="1e496-120">**Comentários**</span><span class="sxs-lookup"><span data-stu-id="1e496-120">**Remarks**</span></span>

<span data-ttu-id="1e496-121">Esse atributo usa os atributos normais de estilo CSS para posicionamento.</span><span class="sxs-lookup"><span data-stu-id="1e496-121">This attribute uses the normal CSS style attributes for positioning.</span></span>

<span data-ttu-id="1e496-122">*Atributo padrão da VML*</span><span class="sxs-lookup"><span data-stu-id="1e496-122">*VML Standard Attribute*</span></span>

<span data-ttu-id="1e496-123">**Exemplo**</span><span class="sxs-lookup"><span data-stu-id="1e496-123">**Example**</span></span>

<span data-ttu-id="1e496-124">O estilo define a posição real do quadro.</span><span class="sxs-lookup"><span data-stu-id="1e496-124">The style defines the actual position of the frame.</span></span>


```HTML
   <v:vmlframe id="frame01" clip="True"
   origin="100pt,100pt" size="50pt,50pt"
   src="external.vml#shape01"
   style='top:160pt; left:100pt; width:50pt; height:50pt'>
   </v:vmlframe>
```



 

 