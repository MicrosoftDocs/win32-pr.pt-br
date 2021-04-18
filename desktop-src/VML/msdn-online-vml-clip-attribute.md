---
title: Atributo de clipe da VML
description: Atributo de clipe da VML
ms.assetid: 8839c10e-96dd-4419-9f02-80033a4633e9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2702355ea93d8e87d173ee4c23406b12557dce4a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "105763436"
---
# <a name="vml-clip-attribute"></a><span data-ttu-id="5bc0b-103">Atributo de clipe da VML</span><span class="sxs-lookup"><span data-stu-id="5bc0b-103">VML Clip Attribute</span></span>

<span data-ttu-id="5bc0b-104">Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="5bc0b-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="5bc0b-105">As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.</span><span class="sxs-lookup"><span data-stu-id="5bc0b-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="5bc0b-106">A partir de dezembro de 2011, este tópico foi arquivado.</span><span class="sxs-lookup"><span data-stu-id="5bc0b-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="5bc0b-107">Como resultado, ele não é mais mantido ativamente.</span><span class="sxs-lookup"><span data-stu-id="5bc0b-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="5bc0b-108">Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="5bc0b-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="5bc0b-109">Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="5bc0b-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="5bc0b-110">Determina se o recorte está ativado.</span><span class="sxs-lookup"><span data-stu-id="5bc0b-110">Determines whether the clipping is on.</span></span> <span data-ttu-id="5bc0b-111">Leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="5bc0b-111">Read/write.</span></span> <span data-ttu-id="5bc0b-112">**VgTriState**.</span><span class="sxs-lookup"><span data-stu-id="5bc0b-112">**VgTriState**.</span></span>

<span data-ttu-id="5bc0b-113">**Aplica-se a**</span><span class="sxs-lookup"><span data-stu-id="5bc0b-113">**Applies To**</span></span>

[<span data-ttu-id="5bc0b-114">VMLFrame</span><span class="sxs-lookup"><span data-stu-id="5bc0b-114">VMLFrame</span></span>](msdn-online-vml-vmlframe-element.md)

<span data-ttu-id="5bc0b-115">**Sintaxe de marca**</span><span class="sxs-lookup"><span data-stu-id="5bc0b-115">**Tag Syntax**</span></span>

<span data-ttu-id="5bc0b-116"><v: *elemento* clip = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="5bc0b-116"><v: *element* clip=" *expression* "></span></span>

<span data-ttu-id="5bc0b-117">**Sintaxe do script**</span><span class="sxs-lookup"><span data-stu-id="5bc0b-117">**Script Syntax**</span></span>

<span data-ttu-id="5bc0b-118">*Element* . Clip = "*expressão*"</span><span class="sxs-lookup"><span data-stu-id="5bc0b-118">*element* .clip="*expression*"</span></span>

<span data-ttu-id="5bc0b-119">*expressão* = de *elemento*. clip</span><span class="sxs-lookup"><span data-stu-id="5bc0b-119">*expression*=*element*.clip</span></span>

<span data-ttu-id="5bc0b-120">**Comentários**</span><span class="sxs-lookup"><span data-stu-id="5bc0b-120">**Remarks**</span></span>

<span data-ttu-id="5bc0b-121">Se **clip** for **false**, a forma será dimensionada para caber no quadro.</span><span class="sxs-lookup"><span data-stu-id="5bc0b-121">If **Clip** is **False**, the shape will scale to fit the frame.</span></span> <span data-ttu-id="5bc0b-122">Se **for true**, qualquer parte da forma que estiver fora do quadro não será exibida.</span><span class="sxs-lookup"><span data-stu-id="5bc0b-122">If **True**, any parts of the shape that are outside the frame will not be displayed.</span></span>

<span data-ttu-id="5bc0b-123">Observe que a [origem](origin-attribute--vmlframe--vml.md) e o [tamanho](size-attribute--vmlframe.md) não serão usados, a menos que o **clipe** seja **verdadeiro**.</span><span class="sxs-lookup"><span data-stu-id="5bc0b-123">Note that [Origin](origin-attribute--vmlframe--vml.md) and [Size](size-attribute--vmlframe.md) won't be used unless **Clip** is **True**.</span></span>

<span data-ttu-id="5bc0b-124">*Atributo padrão da VML*</span><span class="sxs-lookup"><span data-stu-id="5bc0b-124">*VML Standard Attribute*</span></span>

<span data-ttu-id="5bc0b-125">**Exemplo**</span><span class="sxs-lookup"><span data-stu-id="5bc0b-125">**Example**</span></span>

<span data-ttu-id="5bc0b-126">A imagem definida no arquivo externo será recortada.</span><span class="sxs-lookup"><span data-stu-id="5bc0b-126">The image defined in the external file will be clipped.</span></span>


```HTML
   <v:vmlframe id="frame01" clip="True"
   origin="100pt,100pt" size="50pt,50pt"
   src="external.vml#shape01"
   style='top:160pt; left:100pt; width:50pt; height:50pt'>
   </v:vmlframe>
```



 

 