---
title: Atributo de ID (VMLFrame) (VML)
description: Atributo de ID (VMLFrame) (VML)
ms.assetid: 3580fad7-b49e-44d7-b266-90fbfc2a02c9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71f9c5254a2dca186651bb49b677febe747f37c4
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104007762"
---
# <a name="id-attribute-vmlframevml"></a><span data-ttu-id="9a1f5-103">Atributo de ID (VMLFrame) (VML)</span><span class="sxs-lookup"><span data-stu-id="9a1f5-103">ID Attribute (VMLFrame)(VML)</span></span>

<span data-ttu-id="9a1f5-104">Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="9a1f5-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="9a1f5-105">As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.</span><span class="sxs-lookup"><span data-stu-id="9a1f5-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="9a1f5-106">A partir de dezembro de 2011, este tópico foi arquivado.</span><span class="sxs-lookup"><span data-stu-id="9a1f5-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="9a1f5-107">Como resultado, ele não é mais mantido ativamente.</span><span class="sxs-lookup"><span data-stu-id="9a1f5-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="9a1f5-108">Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="9a1f5-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="9a1f5-109">Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="9a1f5-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="9a1f5-110">Define um identificador exclusivo para o quadro.</span><span class="sxs-lookup"><span data-stu-id="9a1f5-110">Defines a unique identifier for the frame.</span></span> <span data-ttu-id="9a1f5-111">Leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="9a1f5-111">Read/write.</span></span> <span data-ttu-id="9a1f5-112">**Cadeia de caracteres**.</span><span class="sxs-lookup"><span data-stu-id="9a1f5-112">**String**.</span></span>

<span data-ttu-id="9a1f5-113">**Aplica-se a**</span><span class="sxs-lookup"><span data-stu-id="9a1f5-113">**Applies To**</span></span>

[<span data-ttu-id="9a1f5-114">VMLFrame</span><span class="sxs-lookup"><span data-stu-id="9a1f5-114">VMLFrame</span></span>](msdn-online-vml-vmlframe-element.md)

<span data-ttu-id="9a1f5-115">**Sintaxe de marca**</span><span class="sxs-lookup"><span data-stu-id="9a1f5-115">**Tag Syntax**</span></span>

<span data-ttu-id="9a1f5-116"><v: *Element* ID = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="9a1f5-116"><v: *element* ID=" *expression* "></span></span>

<span data-ttu-id="9a1f5-117">**Sintaxe do script**</span><span class="sxs-lookup"><span data-stu-id="9a1f5-117">**Script Syntax**</span></span>

<span data-ttu-id="9a1f5-118">*Element* . ID = "*expressão*"</span><span class="sxs-lookup"><span data-stu-id="9a1f5-118">*element* .ID="*expression*"</span></span>

<span data-ttu-id="9a1f5-119">*expressão* = de *elemento*. ID</span><span class="sxs-lookup"><span data-stu-id="9a1f5-119">*expression*=*element*.ID</span></span>

<span data-ttu-id="9a1f5-120">**Comentários**</span><span class="sxs-lookup"><span data-stu-id="9a1f5-120">**Remarks**</span></span>

<span data-ttu-id="9a1f5-121">Use **ID** para fazer referência a um quadro.</span><span class="sxs-lookup"><span data-stu-id="9a1f5-121">Use **ID** to reference a frame.</span></span> <span data-ttu-id="9a1f5-122">Por exemplo, você pode mover o quadro na página alterando a posição do quadro referenciado pela **ID**.</span><span class="sxs-lookup"><span data-stu-id="9a1f5-122">For example, you can move the frame around on the page by changing the frame position referenced by the **ID**.</span></span>

<span data-ttu-id="9a1f5-123">*Atributo padrão da VML*</span><span class="sxs-lookup"><span data-stu-id="9a1f5-123">*VML Standard Attribute*</span></span>

<span data-ttu-id="9a1f5-124">**Exemplo**</span><span class="sxs-lookup"><span data-stu-id="9a1f5-124">**Example**</span></span>

<span data-ttu-id="9a1f5-125">A **ID** do quadro é "frame01".</span><span class="sxs-lookup"><span data-stu-id="9a1f5-125">The **ID** of the frame is "frame01".</span></span>


```HTML
   <v:vmlframe id="frame01" clip="True"
   origin="100pt,100pt" size="50pt,50pt"
   src="external.vml#shape01"
   style='top:160pt; left:100pt; width:50pt; height:50pt'
   </v:vmlframe>
```



 

 