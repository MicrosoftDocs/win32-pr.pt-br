---
title: Atributo ArrowOK de VML
description: Atributo ArrowOK de VML
ms.assetid: 19b23544-4a72-4273-b48a-6aee39addcf6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8807b802370f81ddd084df8a171f95e8496c7ff0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366242"
---
# <a name="vml-arrowok-attribute"></a><span data-ttu-id="05067-103">Atributo ArrowOK de VML</span><span class="sxs-lookup"><span data-stu-id="05067-103">VML ArrowOK Attribute</span></span>

<span data-ttu-id="05067-104">Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="05067-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="05067-105">As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.</span><span class="sxs-lookup"><span data-stu-id="05067-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="05067-106">A partir de dezembro de 2011, este tópico foi arquivado.</span><span class="sxs-lookup"><span data-stu-id="05067-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="05067-107">Como resultado, ele não é mais mantido ativamente.</span><span class="sxs-lookup"><span data-stu-id="05067-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="05067-108">Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="05067-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="05067-109">Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="05067-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="05067-110">Determina se as pontas de seta serão exibidas.</span><span class="sxs-lookup"><span data-stu-id="05067-110">Determines whether arrowheads will be displayed.</span></span> <span data-ttu-id="05067-111">Leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="05067-111">Read/write.</span></span> <span data-ttu-id="05067-112">**VgTriState**.</span><span class="sxs-lookup"><span data-stu-id="05067-112">**VgTriState**.</span></span>

<span data-ttu-id="05067-113">**Aplica-se a**</span><span class="sxs-lookup"><span data-stu-id="05067-113">**Applies To**</span></span>

[<span data-ttu-id="05067-114">Caminho</span><span class="sxs-lookup"><span data-stu-id="05067-114">Path</span></span>](msdn-online-vml-path-element.md)

<span data-ttu-id="05067-115">**Sintaxe de marca**</span><span class="sxs-lookup"><span data-stu-id="05067-115">**Tag Syntax**</span></span>

<span data-ttu-id="05067-116"><v: *Element* arrowok = " *expressão* " ></span><span class="sxs-lookup"><span data-stu-id="05067-116"><v: *element* arrowok=" *expression* "></span></span>

<span data-ttu-id="05067-117">**Sintaxe do script**</span><span class="sxs-lookup"><span data-stu-id="05067-117">**Script Syntax**</span></span>

<span data-ttu-id="05067-118">*Element* . arrowok = "*expressão*"</span><span class="sxs-lookup"><span data-stu-id="05067-118">*element* .arrowok="*expression*"</span></span>

<span data-ttu-id="05067-119">*expressão* = de *elemento*. arrowok</span><span class="sxs-lookup"><span data-stu-id="05067-119">*expression*=*element*.arrowok</span></span>

<span data-ttu-id="05067-120">**Comentários**</span><span class="sxs-lookup"><span data-stu-id="05067-120">**Remarks**</span></span>

<span data-ttu-id="05067-121">Se **for false**, o caminho não terá pontas de seta.</span><span class="sxs-lookup"><span data-stu-id="05067-121">If **False**, the path will not have arrowheads.</span></span> <span data-ttu-id="05067-122">O padrão é **False**.</span><span class="sxs-lookup"><span data-stu-id="05067-122">The default is **False**.</span></span> <span data-ttu-id="05067-123">Esse atributo substitui todos os outros atributos de ponta de seta no elemento pai ou **Stroke** .</span><span class="sxs-lookup"><span data-stu-id="05067-123">This attribute overrides all other arrowhead attributes in the parent or **Stroke** element.</span></span>

<span data-ttu-id="05067-124">*Atributo padrão da VML*</span><span class="sxs-lookup"><span data-stu-id="05067-124">*VML Standard Attribute*</span></span>

<span data-ttu-id="05067-125">**Exemplo**</span><span class="sxs-lookup"><span data-stu-id="05067-125">**Example**</span></span>

<span data-ttu-id="05067-126">O caminho não terá uma ponta de seta.</span><span class="sxs-lookup"><span data-stu-id="05067-126">The path will not have an arrowhead.</span></span>


```HTML
   <v:line id="whatsmyline"
   style="position:relative"
   from="114pt,66pt" to="402pt,66pt"
   strokecolor="black">
   <v:stroke startarrow="block" endarrow="block"/>
   <v:path arrowok="False"/>
   </v:line>
```



 

 