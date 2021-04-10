---
title: Atributo DoubleClickNotify de VML
description: Atributo DoubleClickNotify de VML
ms.assetid: 003a87f5-29c1-484e-ac15-2e4cb8e854ad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16be329952cfff23957f961fb6d29198ad173898
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104294093"
---
# <a name="vml-doubleclicknotify-attribute"></a><span data-ttu-id="9518f-103">Atributo DoubleClickNotify de VML</span><span class="sxs-lookup"><span data-stu-id="9518f-103">VML DoubleClickNotify Attribute</span></span>

<span data-ttu-id="9518f-104">Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="9518f-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="9518f-105">As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.</span><span class="sxs-lookup"><span data-stu-id="9518f-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="9518f-106">A partir de dezembro de 2011, este tópico foi arquivado.</span><span class="sxs-lookup"><span data-stu-id="9518f-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="9518f-107">Como resultado, ele não é mais mantido ativamente.</span><span class="sxs-lookup"><span data-stu-id="9518f-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="9518f-108">Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="9518f-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="9518f-109">Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="9518f-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="9518f-110">Envia uma mensagem de evento quando uma forma é clicada duas vezes.</span><span class="sxs-lookup"><span data-stu-id="9518f-110">Sends an event message when a shape is double-clicked.</span></span> <span data-ttu-id="9518f-111">Leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="9518f-111">Read/write.</span></span> <span data-ttu-id="9518f-112">**VgTriState**.</span><span class="sxs-lookup"><span data-stu-id="9518f-112">**VgTriState**.</span></span>

<span data-ttu-id="9518f-113">**Aplica-se a**</span><span class="sxs-lookup"><span data-stu-id="9518f-113">**Applies To**</span></span>

[<span data-ttu-id="9518f-114">Forma</span><span class="sxs-lookup"><span data-stu-id="9518f-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="9518f-115">**Sintaxe de marca**</span><span class="sxs-lookup"><span data-stu-id="9518f-115">**Tag Syntax**</span></span>

<span data-ttu-id="9518f-116"><v: *Element* o:doubleclicknotify = " *expressão* " ></span><span class="sxs-lookup"><span data-stu-id="9518f-116"><v: *element* o:doubleclicknotify=" *expression* "></span></span>

<span data-ttu-id="9518f-117">**Comentários**</span><span class="sxs-lookup"><span data-stu-id="9518f-117">**Remarks**</span></span>

<span data-ttu-id="9518f-118">O valor padrão é **false**, indicando que o evento não será acionado.</span><span class="sxs-lookup"><span data-stu-id="9518f-118">The default value is **False**, indicating that the event will not be fired.</span></span>

<span data-ttu-id="9518f-119">*Atributo de extensões de Microsoft Office*</span><span class="sxs-lookup"><span data-stu-id="9518f-119">*Microsoft Office Extensions Attribute*</span></span>

<span data-ttu-id="9518f-120">**Exemplo**</span><span class="sxs-lookup"><span data-stu-id="9518f-120">**Example**</span></span>

<span data-ttu-id="9518f-121">A forma disparará um evento de clique duplo quando clicado duas vezes.</span><span class="sxs-lookup"><span data-stu-id="9518f-121">The shape will trigger a double-click event when double-clicked.</span></span>


```HTML
   <v:rect id=myrect fillcolor="red" o:doubleclicknotify="True"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
```



 

 