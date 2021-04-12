---
title: Atributo de marcador da VML
description: Atributo de marcador da VML
ms.assetid: 17c24b97-191b-4170-8a2d-9284f500e728
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4edcf1194a234284a70f928adad198ca77f597a9
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366236"
---
# <a name="vml-bullet-attribute"></a><span data-ttu-id="0deb0-103">Atributo de marcador da VML</span><span class="sxs-lookup"><span data-stu-id="0deb0-103">VML Bullet Attribute</span></span>

<span data-ttu-id="0deb0-104">Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="0deb0-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="0deb0-105">As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.</span><span class="sxs-lookup"><span data-stu-id="0deb0-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="0deb0-106">A partir de dezembro de 2011, este tópico foi arquivado.</span><span class="sxs-lookup"><span data-stu-id="0deb0-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="0deb0-107">Como resultado, ele não é mais mantido ativamente.</span><span class="sxs-lookup"><span data-stu-id="0deb0-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="0deb0-108">Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="0deb0-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="0deb0-109">Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="0deb0-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="0deb0-110">Determina se uma forma é um marcador gráfico.</span><span class="sxs-lookup"><span data-stu-id="0deb0-110">Determines whether a shape is a graphical bullet.</span></span> <span data-ttu-id="0deb0-111">**VgTriState** de leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="0deb0-111">Read/write **VgTriState**.</span></span>

<span data-ttu-id="0deb0-112">**Aplica-se a**</span><span class="sxs-lookup"><span data-stu-id="0deb0-112">**Applies To**</span></span>

[<span data-ttu-id="0deb0-113">Forma</span><span class="sxs-lookup"><span data-stu-id="0deb0-113">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="0deb0-114">**Sintaxe de marca**</span><span class="sxs-lookup"><span data-stu-id="0deb0-114">**Tag Syntax**</span></span>

<span data-ttu-id="0deb0-115"><v: *Element* o:Bullet = " *expressão* " ></span><span class="sxs-lookup"><span data-stu-id="0deb0-115"><v: *element* o:bullet=" *expression* "></span></span>

<span data-ttu-id="0deb0-116">**Comentários**</span><span class="sxs-lookup"><span data-stu-id="0deb0-116">**Remarks**</span></span>

<span data-ttu-id="0deb0-117">O padrão é **False**.</span><span class="sxs-lookup"><span data-stu-id="0deb0-117">The default is **False**.</span></span> <span data-ttu-id="0deb0-118">Se for **true**, a forma será um marcador gráfico.</span><span class="sxs-lookup"><span data-stu-id="0deb0-118">If **True**, the shape is a graphical bullet.</span></span>

<span data-ttu-id="0deb0-119">*Atributo de extensões de Microsoft Office*</span><span class="sxs-lookup"><span data-stu-id="0deb0-119">*Microsoft Office Extensions Attribute*</span></span>

<span data-ttu-id="0deb0-120">**Exemplo**</span><span class="sxs-lookup"><span data-stu-id="0deb0-120">**Example**</span></span>

<span data-ttu-id="0deb0-121">A forma é um marcador.</span><span class="sxs-lookup"><span data-stu-id="0deb0-121">The shape is a bullet.</span></span>


```HTML
   <v:rect id=myrect fillcolor="red" o:bullet="True"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
```



 

 