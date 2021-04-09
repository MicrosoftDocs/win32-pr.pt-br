---
title: Atributo ForceDash de VML
description: Atributo ForceDash de VML
ms.assetid: 659e99bb-16d9-425a-97b1-7767c065ec41
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5bcec4a694a6449412aa07ec69aa9a817aa917c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104007858"
---
# <a name="vml-forcedash-attribute"></a><span data-ttu-id="a4bf1-103">Atributo ForceDash de VML</span><span class="sxs-lookup"><span data-stu-id="a4bf1-103">VML ForceDash Attribute</span></span>

<span data-ttu-id="a4bf1-104">Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="a4bf1-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="a4bf1-105">As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.</span><span class="sxs-lookup"><span data-stu-id="a4bf1-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="a4bf1-106">A partir de dezembro de 2011, este tópico foi arquivado.</span><span class="sxs-lookup"><span data-stu-id="a4bf1-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="a4bf1-107">Como resultado, ele não é mais mantido ativamente.</span><span class="sxs-lookup"><span data-stu-id="a4bf1-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="a4bf1-108">Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="a4bf1-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="a4bf1-109">Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="a4bf1-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="a4bf1-110">Determina se um contorno tracejado é usado para desenhar uma forma quando uma forma não tem linha ou preenchimento.</span><span class="sxs-lookup"><span data-stu-id="a4bf1-110">Determines whether a dashed outline is used to draw a shape when a shape has no line or fill.</span></span> <span data-ttu-id="a4bf1-111">Leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="a4bf1-111">Read/write.</span></span> <span data-ttu-id="a4bf1-112">**VgTriState**.</span><span class="sxs-lookup"><span data-stu-id="a4bf1-112">**VgTriState**.</span></span>

<span data-ttu-id="a4bf1-113">**Aplica-se a**</span><span class="sxs-lookup"><span data-stu-id="a4bf1-113">**Applies To**</span></span>

[<span data-ttu-id="a4bf1-114">Forma</span><span class="sxs-lookup"><span data-stu-id="a4bf1-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="a4bf1-115">**Sintaxe de marca**</span><span class="sxs-lookup"><span data-stu-id="a4bf1-115">**Tag Syntax**</span></span>

<span data-ttu-id="a4bf1-116"><v: *Element* o:forcedash = " *expressão* " ></span><span class="sxs-lookup"><span data-stu-id="a4bf1-116"><v: *element* o:forcedash=" *expression* "></span></span>

<span data-ttu-id="a4bf1-117">**Comentários**</span><span class="sxs-lookup"><span data-stu-id="a4bf1-117">**Remarks**</span></span>

<span data-ttu-id="a4bf1-118">Usado pelos espaços reservados do Microsoft PowerPoint para desenhar um contorno tracejado quando não há nenhuma linha e nenhum preenchimento para uma forma.</span><span class="sxs-lookup"><span data-stu-id="a4bf1-118">Used by Microsoft PowerPoint placeholders to draw a dashed outline when there is no line and no fill for a shape.</span></span> <span data-ttu-id="a4bf1-119">O padrão é **False**.</span><span class="sxs-lookup"><span data-stu-id="a4bf1-119">Default is **False**.</span></span> <span data-ttu-id="a4bf1-120">Se **for true**, um contorno tracejado será usado para indicar um espaço reservado.</span><span class="sxs-lookup"><span data-stu-id="a4bf1-120">If **True**, a dashed outline will be used to indicate a placeholder.</span></span>

<span data-ttu-id="a4bf1-121">*Atributo de extensões de Microsoft Office*</span><span class="sxs-lookup"><span data-stu-id="a4bf1-121">*Microsoft Office Extensions Attribute*</span></span>

<span data-ttu-id="a4bf1-122">**Exemplo**</span><span class="sxs-lookup"><span data-stu-id="a4bf1-122">**Example**</span></span>

<span data-ttu-id="a4bf1-123">Uma linha tracejada será usada para renderizar a forma se não houver nenhuma linha ou preenchimento.</span><span class="sxs-lookup"><span data-stu-id="a4bf1-123">A dashed line will be used to render the shape if there is no line or fill.</span></span>


```HTML
   <v:rect id=myrect fillcolor="red" o:forcedash="True"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
```



 

 