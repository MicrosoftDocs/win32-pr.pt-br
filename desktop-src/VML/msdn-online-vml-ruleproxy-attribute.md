---
title: Atributo RuleProxy de VML
description: Atributo RuleProxy de VML
ms.assetid: 040e80f8-65b6-491d-812d-421800801374
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50c76116fc1f31c379f15c3229fcbe70dc7938f7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "105760799"
---
# <a name="vml-ruleproxy-attribute"></a><span data-ttu-id="0865c-103">Atributo RuleProxy de VML</span><span class="sxs-lookup"><span data-stu-id="0865c-103">VML RuleProxy Attribute</span></span>

<span data-ttu-id="0865c-104">Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="0865c-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="0865c-105">As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.</span><span class="sxs-lookup"><span data-stu-id="0865c-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="0865c-106">A partir de dezembro de 2011, este tópico foi arquivado.</span><span class="sxs-lookup"><span data-stu-id="0865c-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="0865c-107">Como resultado, ele não é mais mantido ativamente.</span><span class="sxs-lookup"><span data-stu-id="0865c-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="0865c-108">Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="0865c-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="0865c-109">Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="0865c-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="0865c-110">Determina se um proxy para o mecanismo de regras será usado.</span><span class="sxs-lookup"><span data-stu-id="0865c-110">Determines whether a proxy for the rules engine will be used.</span></span> <span data-ttu-id="0865c-111">Leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="0865c-111">Read/write.</span></span> <span data-ttu-id="0865c-112">**VgTriState**.</span><span class="sxs-lookup"><span data-stu-id="0865c-112">**VgTriState**.</span></span>

<span data-ttu-id="0865c-113">**Aplica-se a**</span><span class="sxs-lookup"><span data-stu-id="0865c-113">**Applies To**</span></span>

[<span data-ttu-id="0865c-114">Forma</span><span class="sxs-lookup"><span data-stu-id="0865c-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="0865c-115">**Sintaxe de marca**</span><span class="sxs-lookup"><span data-stu-id="0865c-115">**Tag Syntax**</span></span>

<span data-ttu-id="0865c-116"><v: *Element* ruleproxy = " *expressão* " ></span><span class="sxs-lookup"><span data-stu-id="0865c-116"><v: *element* ruleproxy=" *expression* "></span></span>

<span data-ttu-id="0865c-117">**Comentários**</span><span class="sxs-lookup"><span data-stu-id="0865c-117">**Remarks**</span></span>

<span data-ttu-id="0865c-118">O valor padrão é **Falso**.</span><span class="sxs-lookup"><span data-stu-id="0865c-118">The default value is **False**.</span></span> <span data-ttu-id="0865c-119">Se for **true**, um proxy será usado.</span><span class="sxs-lookup"><span data-stu-id="0865c-119">If **True**, a proxy is used.</span></span>

<span data-ttu-id="0865c-120">*Atributo de extensões de Microsoft Office*</span><span class="sxs-lookup"><span data-stu-id="0865c-120">*Microsoft Office Extensions Attribute*</span></span>

<span data-ttu-id="0865c-121">**Exemplo**</span><span class="sxs-lookup"><span data-stu-id="0865c-121">**Example**</span></span>

<span data-ttu-id="0865c-122">Um proxy é usado para processar a forma.</span><span class="sxs-lookup"><span data-stu-id="0865c-122">A proxy is used to process the shape.</span></span>


```HTML
   <v:rect id=myrect fillcolor="red" ruleproxy="True"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
```



 

 