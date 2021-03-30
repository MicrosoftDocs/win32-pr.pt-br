---
title: Atributo InvX de VML
description: Atributo InvX de VML
ms.assetid: 59fbd4c0-ae31-4198-a9e7-be12cd50288f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37d244b5feff319112959d3093927f11d1e92164
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103641293"
---
# <a name="vml-invx-attribute"></a><span data-ttu-id="c69fa-103">Atributo InvX de VML</span><span class="sxs-lookup"><span data-stu-id="c69fa-103">VML InvX Attribute</span></span>

<span data-ttu-id="c69fa-104">Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="c69fa-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="c69fa-105">As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.</span><span class="sxs-lookup"><span data-stu-id="c69fa-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="c69fa-106">A partir de dezembro de 2011, este tópico foi arquivado.</span><span class="sxs-lookup"><span data-stu-id="c69fa-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="c69fa-107">Como resultado, ele não é mais mantido ativamente.</span><span class="sxs-lookup"><span data-stu-id="c69fa-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="c69fa-108">Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="c69fa-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="c69fa-109">Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="c69fa-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="c69fa-110">Determina se a posição x do identificador é invertida.</span><span class="sxs-lookup"><span data-stu-id="c69fa-110">Determines whether the x position of the handle is inverted.</span></span> <span data-ttu-id="c69fa-111">Leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="c69fa-111">Read/write.</span></span> <span data-ttu-id="c69fa-112">**VgTriState**.</span><span class="sxs-lookup"><span data-stu-id="c69fa-112">**VgTriState**.</span></span>

<span data-ttu-id="c69fa-113">**Aplica-se a**</span><span class="sxs-lookup"><span data-stu-id="c69fa-113">**Applies To**</span></span>

<span data-ttu-id="c69fa-114">[H](msdn-online-vml-h-element.md) (subelemento de [identificadores](msdn-online-vml-handles-element.md))</span><span class="sxs-lookup"><span data-stu-id="c69fa-114">[H](msdn-online-vml-h-element.md) (subelement of [Handles](msdn-online-vml-handles-element.md))</span></span>

<span data-ttu-id="c69fa-115">**Sintaxe de marca**</span><span class="sxs-lookup"><span data-stu-id="c69fa-115">**Tag Syntax**</span></span>

<span data-ttu-id="c69fa-116"><v: *Element* invx = " *expressão* " ></span><span class="sxs-lookup"><span data-stu-id="c69fa-116"><v: *element* invx=" *expression* "></span></span>

<span data-ttu-id="c69fa-117">**Comentários**</span><span class="sxs-lookup"><span data-stu-id="c69fa-117">**Remarks**</span></span>

<span data-ttu-id="c69fa-118">Se **for true**, a posição x do identificador será invertida com a subtração do valor x do valor x de **CoordOrigin** adicionado ao valor x de **CoordSize**.</span><span class="sxs-lookup"><span data-stu-id="c69fa-118">If **True**, the x position of the handle is inverted by subtracting the x value from the x value of **CoordOrigin** added to the x value of **CoordSize**.</span></span> <span data-ttu-id="c69fa-119">O valor padrão é **Falso**.</span><span class="sxs-lookup"><span data-stu-id="c69fa-119">The default value is **False**.</span></span>

<span data-ttu-id="c69fa-120">Este atributo é o equivalente de</span><span class="sxs-lookup"><span data-stu-id="c69fa-120">This attribute is the equivalent of</span></span>

<span data-ttu-id="c69fa-121">coordorigin. x + coordsize. x-h. Position. x</span><span class="sxs-lookup"><span data-stu-id="c69fa-121">coordorigin.x + coordsize.x - h.position.x</span></span>

<span data-ttu-id="c69fa-122">*Atributo padrão da VML*</span><span class="sxs-lookup"><span data-stu-id="c69fa-122">*VML Standard Attribute*</span></span>

 

 