---
title: Atributo InvY de VML
description: Atributo InvY de VML
ms.assetid: 6c8c51ab-88ce-40b2-add7-1152e125ad8b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a728d804d771f79b892ee6616cca527dba42bfa
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104294193"
---
# <a name="vml-invy-attribute"></a><span data-ttu-id="af281-103">Atributo InvY de VML</span><span class="sxs-lookup"><span data-stu-id="af281-103">VML InvY Attribute</span></span>

<span data-ttu-id="af281-104">Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="af281-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="af281-105">As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.</span><span class="sxs-lookup"><span data-stu-id="af281-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="af281-106">A partir de dezembro de 2011, este tópico foi arquivado.</span><span class="sxs-lookup"><span data-stu-id="af281-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="af281-107">Como resultado, ele não é mais mantido ativamente.</span><span class="sxs-lookup"><span data-stu-id="af281-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="af281-108">Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="af281-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="af281-109">Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="af281-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="af281-110">Determina se a posição y do identificador é invertida.</span><span class="sxs-lookup"><span data-stu-id="af281-110">Determines whether the y position of the handle is inverted.</span></span> <span data-ttu-id="af281-111">Leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="af281-111">Read/write.</span></span> <span data-ttu-id="af281-112">**VgTriState**.</span><span class="sxs-lookup"><span data-stu-id="af281-112">**VgTriState**.</span></span>

<span data-ttu-id="af281-113">**Aplica-se a**</span><span class="sxs-lookup"><span data-stu-id="af281-113">**Applies To**</span></span>

<span data-ttu-id="af281-114">[H](msdn-online-vml-h-element.md) (subelemento de [identificadores](msdn-online-vml-handles-element.md))</span><span class="sxs-lookup"><span data-stu-id="af281-114">[H](msdn-online-vml-h-element.md) (subelement of [Handles](msdn-online-vml-handles-element.md))</span></span>

<span data-ttu-id="af281-115">**Sintaxe de marca**</span><span class="sxs-lookup"><span data-stu-id="af281-115">**Tag Syntax**</span></span>

<span data-ttu-id="af281-116"><v: *Element* invy = " *expressão* " ></span><span class="sxs-lookup"><span data-stu-id="af281-116"><v: *element* invy=" *expression* "></span></span>

<span data-ttu-id="af281-117">**Comentários**</span><span class="sxs-lookup"><span data-stu-id="af281-117">**Remarks**</span></span>

<span data-ttu-id="af281-118">Se **for true**, a posição y do identificador será invertida com a subtração do valor y do valor y de **CoordOrigin** adicionado ao valor y de **CoordSize**.</span><span class="sxs-lookup"><span data-stu-id="af281-118">If **True**, the y position of the handle is inverted by subtracting the y value from the y value of **CoordOrigin** added to the y value of **CoordSize**.</span></span> <span data-ttu-id="af281-119">O valor padrão é **Falso**.</span><span class="sxs-lookup"><span data-stu-id="af281-119">The default value is **False**.</span></span>

<span data-ttu-id="af281-120">Este atributo é o equivalente de</span><span class="sxs-lookup"><span data-stu-id="af281-120">This attribute is the equivalent of</span></span>


```HTML
coordorigin.y + coordsize.y - h.position.y
```



<span data-ttu-id="af281-121">*Atributo padrão da VML*</span><span class="sxs-lookup"><span data-stu-id="af281-121">*VML Standard Attribute*</span></span>

 

 