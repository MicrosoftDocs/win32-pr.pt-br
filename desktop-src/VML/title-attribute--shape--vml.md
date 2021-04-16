---
title: Atributo Title (forma) (VML)
description: Atributo Title (forma) (VML)
ms.assetid: 08680706-5274-46d4-9199-4fdbf32f884b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 075b1cf078617abd3486ba55008794e1342efa63
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104454324"
---
# <a name="title-attribute-shapevml"></a><span data-ttu-id="9b935-103">Atributo Title (forma) (VML)</span><span class="sxs-lookup"><span data-stu-id="9b935-103">Title Attribute (Shape)(VML)</span></span>

<span data-ttu-id="9b935-104">Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="9b935-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="9b935-105">As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.</span><span class="sxs-lookup"><span data-stu-id="9b935-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="9b935-106">A partir de dezembro de 2011, este tópico foi arquivado.</span><span class="sxs-lookup"><span data-stu-id="9b935-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="9b935-107">Como resultado, ele não é mais mantido ativamente.</span><span class="sxs-lookup"><span data-stu-id="9b935-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="9b935-108">Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="9b935-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="9b935-109">Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="9b935-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="9b935-110">Define o texto exibido quando o ponteiro do mouse se move sobre a forma.</span><span class="sxs-lookup"><span data-stu-id="9b935-110">Defines the text displayed when the mouse pointer moves over the shape.</span></span> <span data-ttu-id="9b935-111">Leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="9b935-111">Read/write.</span></span> <span data-ttu-id="9b935-112">**Cadeia de caracteres**.</span><span class="sxs-lookup"><span data-stu-id="9b935-112">**String**.</span></span>

<span data-ttu-id="9b935-113">**Aplica-se a**</span><span class="sxs-lookup"><span data-stu-id="9b935-113">**Applies To**</span></span>

[<span data-ttu-id="9b935-114">Forma</span><span class="sxs-lookup"><span data-stu-id="9b935-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="9b935-115">**Sintaxe de marca**</span><span class="sxs-lookup"><span data-stu-id="9b935-115">**Tag Syntax**</span></span>

<span data-ttu-id="9b935-116"><v: *Element* título = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="9b935-116"><v: *element* title=" *expression* "></span></span>

<span data-ttu-id="9b935-117">**Sintaxe do script**</span><span class="sxs-lookup"><span data-stu-id="9b935-117">**Script Syntax**</span></span>

<span data-ttu-id="9b935-118">*elemento* . title = "*expressão*"</span><span class="sxs-lookup"><span data-stu-id="9b935-118">*element* .title="*expression*"</span></span>

<span data-ttu-id="9b935-119">*expressão* = de *elemento*. title</span><span class="sxs-lookup"><span data-stu-id="9b935-119">*expression*=*element*.title</span></span>

<span data-ttu-id="9b935-120">**Comentários**</span><span class="sxs-lookup"><span data-stu-id="9b935-120">**Remarks**</span></span>

<span data-ttu-id="9b935-121">O atributo **título** é semelhante ao atributo padrão de **título** HTML.</span><span class="sxs-lookup"><span data-stu-id="9b935-121">The **Title** attribute is similar to the standard HTML **Title** attribute.</span></span> <span data-ttu-id="9b935-122">O comportamento de um título é semelhante a uma dica de ferramenta do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="9b935-122">The behavior of a title is similar to a Microsoft Windows ToolTip.</span></span>

<span data-ttu-id="9b935-123">**Atributo padrão da VML**</span><span class="sxs-lookup"><span data-stu-id="9b935-123">**VML Standard Attribute**</span></span>

<span data-ttu-id="9b935-124">**Exemplo**</span><span class="sxs-lookup"><span data-stu-id="9b935-124">**Example**</span></span>

<span data-ttu-id="9b935-125">O título da forma é "exibição da dica de ferramenta" e aparecerá quando o ponteiro do mouse se mover sobre a forma.</span><span class="sxs-lookup"><span data-stu-id="9b935-125">The title of the shape is "ToolTip display" and will appear when the mouse pointer moves over the shape.</span></span>


```HTML
   <v:rect id=myrect fillcolor="red" title="ToolTip display"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
```



<span data-ttu-id="9b935-126">[Exemplo de atributo de título](/previous-versions/bb264097(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="9b935-126">[Title Attribute Example](/previous-versions/bb264097(v=vs.85)).</span></span> <span data-ttu-id="9b935-127">(Requer o Microsoft Internet Explorer 5 ou superior.)</span><span class="sxs-lookup"><span data-stu-id="9b935-127">(Requires Microsoft Internet Explorer 5 or greater.)</span></span>

 

 