---
title: Elemento ShapeType de VML
description: Elemento ShapeType de VML
ms.assetid: 4e0288c9-ab0f-4399-982a-97dcf16f4ec4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ebbb35eef0a3c987fe1e6ec35d15701236ae0af1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104162308"
---
# <a name="vml-shapetype-element"></a><span data-ttu-id="f1ed1-103">Elemento ShapeType de VML</span><span class="sxs-lookup"><span data-stu-id="f1ed1-103">VML ShapeType Element</span></span>

<span data-ttu-id="f1ed1-104">Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="f1ed1-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="f1ed1-105">As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.</span><span class="sxs-lookup"><span data-stu-id="f1ed1-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="f1ed1-106">A partir de dezembro de 2011, este tópico foi arquivado.</span><span class="sxs-lookup"><span data-stu-id="f1ed1-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="f1ed1-107">Como resultado, ele não é mais mantido ativamente.</span><span class="sxs-lookup"><span data-stu-id="f1ed1-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="f1ed1-108">Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="f1ed1-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="f1ed1-109">Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="f1ed1-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="f1ed1-110">Define uma forma que pode ser usada para criar outras formas.</span><span class="sxs-lookup"><span data-stu-id="f1ed1-110">Defines a shape that can be used to create other shapes.</span></span>

<span data-ttu-id="f1ed1-111">O atributo a seguir modifica um **ShapeType**.</span><span class="sxs-lookup"><span data-stu-id="f1ed1-111">The following attribute modifies a **ShapeType**.</span></span>



| <span data-ttu-id="f1ed1-112">Atributo</span><span class="sxs-lookup"><span data-stu-id="f1ed1-112">Attribute</span></span>                                      | <span data-ttu-id="f1ed1-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="f1ed1-113">Description</span></span>                                             |
|------------------------------------------------|---------------------------------------------------------|
| [<span data-ttu-id="f1ed1-114">Vários</span><span class="sxs-lookup"><span data-stu-id="f1ed1-114">Master</span></span>](msdn-online-vml-master-attribute.md) | <span data-ttu-id="f1ed1-115">Determina se um **ShapeType** é um elemento mestre.</span><span class="sxs-lookup"><span data-stu-id="f1ed1-115">Determines whether a **ShapeType** is a master element.</span></span> |



 

<span data-ttu-id="f1ed1-116">**Comentários**</span><span class="sxs-lookup"><span data-stu-id="f1ed1-116">**Remarks**</span></span>

<span data-ttu-id="f1ed1-117">**ShapeType** é idêntico ao elemento **Shape** , exceto que não pode fazer referência a outro elemento **ShapeType** .</span><span class="sxs-lookup"><span data-stu-id="f1ed1-117">**ShapeType** is identical to the **Shape** element except it cannot reference another **ShapeType** element.</span></span>

<span data-ttu-id="f1ed1-118">Quando um elemento **Shape** faz referência a um **ShapeType**, a **forma** pode duplicar algumas das propriedades que já foram especificadas no **ShapeType**.</span><span class="sxs-lookup"><span data-stu-id="f1ed1-118">When a **Shape** element makes reference to a **ShapeType**, the **Shape** may duplicate some of the properties that have already been specified in the **ShapeType**.</span></span> <span data-ttu-id="f1ed1-119">Nesses casos, os atributos na **forma** substituem aqueles do **ShapeType**.</span><span class="sxs-lookup"><span data-stu-id="f1ed1-119">In these cases, the attributes in the **Shape** override those of the **ShapeType**.</span></span>

<span data-ttu-id="f1ed1-120">O atributo **Type** não pode ser usado com **ShapeType**.</span><span class="sxs-lookup"><span data-stu-id="f1ed1-120">The **Type** attribute may not be used with **ShapeType**.</span></span>

<span data-ttu-id="f1ed1-121">Os atributos de posicionamento CSS (como **Top**, **Left**, etc.) não são passados para uma **forma** de um **ShapeType**.</span><span class="sxs-lookup"><span data-stu-id="f1ed1-121">CSS positioning attributes (such as **Top**, **Left**, etc.) are not passed to a **Shape** from a **ShapeType**.</span></span>

<span data-ttu-id="f1ed1-122">Para usar esse elemento, crie um **ShapeType** com um atributo de [ID](id-attribute--vml.md) específico.</span><span class="sxs-lookup"><span data-stu-id="f1ed1-122">To use this element, create a **ShapeType** with a specific [ID](id-attribute--vml.md) attribute.</span></span> <span data-ttu-id="f1ed1-123">Em seguida, crie uma **forma** e referencie a **formatype** com o atributo **Type** .</span><span class="sxs-lookup"><span data-stu-id="f1ed1-123">Then create a **Shape** and reference the **ShapeType** with the **Type** attribute.</span></span> <span data-ttu-id="f1ed1-124">Consulte o atributo [Type](type-attribute--shape--vml.md) para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="f1ed1-124">See the [Type](type-attribute--shape--vml.md) attribute for more information.</span></span>

 

 