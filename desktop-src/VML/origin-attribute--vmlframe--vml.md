---
title: Atributo Origin (VMLFrame) (VML)
description: Atributo Origin (VMLFrame) (VML)
ms.assetid: 317c027e-5054-4543-ad98-2c21d1cf7154
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae9341eecea9ec1eae8aaf1d7b1ad729986a8249
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103641772"
---
# <a name="origin-attribute-vmlframevml"></a><span data-ttu-id="4b87f-103">Atributo Origin (VMLFrame) (VML)</span><span class="sxs-lookup"><span data-stu-id="4b87f-103">Origin Attribute (VMLFrame)(VML)</span></span>

<span data-ttu-id="4b87f-104">Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="4b87f-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="4b87f-105">As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.</span><span class="sxs-lookup"><span data-stu-id="4b87f-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="4b87f-106">A partir de dezembro de 2011, este tópico foi arquivado.</span><span class="sxs-lookup"><span data-stu-id="4b87f-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="4b87f-107">Como resultado, ele não é mais mantido ativamente.</span><span class="sxs-lookup"><span data-stu-id="4b87f-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="4b87f-108">Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="4b87f-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="4b87f-109">Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="4b87f-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="4b87f-110">Define a origem da região de recorte do quadro.</span><span class="sxs-lookup"><span data-stu-id="4b87f-110">Defines the origin of the clipping region of the frame.</span></span> <span data-ttu-id="4b87f-111">Leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="4b87f-111">Read/write.</span></span> <span data-ttu-id="4b87f-112">**VgVector2D**.</span><span class="sxs-lookup"><span data-stu-id="4b87f-112">**VgVector2D**.</span></span>

<span data-ttu-id="4b87f-113">**Aplica-se a**</span><span class="sxs-lookup"><span data-stu-id="4b87f-113">**Applies To**</span></span>

[<span data-ttu-id="4b87f-114">VMLFrame</span><span class="sxs-lookup"><span data-stu-id="4b87f-114">VMLFrame</span></span>](msdn-online-vml-vmlframe-element.md)

<span data-ttu-id="4b87f-115">**Sintaxe de marca**</span><span class="sxs-lookup"><span data-stu-id="4b87f-115">**Tag Syntax**</span></span>

<span data-ttu-id="4b87f-116"><v: *elemento* Origin = " *expressão* " ></span><span class="sxs-lookup"><span data-stu-id="4b87f-116"><v: *element* origin=" *expression* "></span></span>

<span data-ttu-id="4b87f-117">**Sintaxe do script**</span><span class="sxs-lookup"><span data-stu-id="4b87f-117">**Script Syntax**</span></span>

<span data-ttu-id="4b87f-118">*elemento* . Origin = "*expressão*"</span><span class="sxs-lookup"><span data-stu-id="4b87f-118">*element* .origin="*expression*"</span></span>

<span data-ttu-id="4b87f-119">*expressão* = de *elemento*. Origin</span><span class="sxs-lookup"><span data-stu-id="4b87f-119">*expression*=*element*.origin</span></span>

<span data-ttu-id="4b87f-120">**Comentários**</span><span class="sxs-lookup"><span data-stu-id="4b87f-120">**Remarks**</span></span>

<span data-ttu-id="4b87f-121">O valor padrão é 0,0.</span><span class="sxs-lookup"><span data-stu-id="4b87f-121">The default value is 0,0.</span></span> <span data-ttu-id="4b87f-122">Observe que a **origem** só funciona se o [clipe](msdn-online-vml-clip-attribute.md) for **verdadeiro**.</span><span class="sxs-lookup"><span data-stu-id="4b87f-122">Note that **Origin** only works if [Clip](msdn-online-vml-clip-attribute.md) is **True**.</span></span> <span data-ttu-id="4b87f-123">Nesse atributo, a origem é definida como o canto superior esquerdo do quadro.</span><span class="sxs-lookup"><span data-stu-id="4b87f-123">In this attribute, the origin is defined as the upper left corner of the frame.</span></span>

<span data-ttu-id="4b87f-124">*Atributo padrão da VML*</span><span class="sxs-lookup"><span data-stu-id="4b87f-124">*VML Standard Attribute*</span></span>

<span data-ttu-id="4b87f-125">**Exemplo**</span><span class="sxs-lookup"><span data-stu-id="4b87f-125">**Example**</span></span>

<span data-ttu-id="4b87f-126">A origem da região de recorte é 100pt, 100pt.</span><span class="sxs-lookup"><span data-stu-id="4b87f-126">The origin of the clipping region is 100pt,100pt.</span></span>


```HTML
   <v:vmlframe id="frame01" clip="True"
   origin="100pt,100pt" size="50pt,50pt"
   src="external.vml#shape01"
   style='top:160pt; left:100pt; width:50pt; height:50pt'
   </v:vmlframe>
```



 

 