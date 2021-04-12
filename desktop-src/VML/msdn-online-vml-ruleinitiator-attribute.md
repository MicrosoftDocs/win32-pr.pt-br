---
title: Atributo RuleInitiator de VML
description: Atributo RuleInitiator de VML
ms.assetid: 2c9b1131-b088-4b70-b132-bdb4296433ae
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80201ad80fbb8dc5bbff2e8ed4e0b8db2863fdad
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104294467"
---
# <a name="vml-ruleinitiator-attribute"></a><span data-ttu-id="c6ae9-103">Atributo RuleInitiator de VML</span><span class="sxs-lookup"><span data-stu-id="c6ae9-103">VML RuleInitiator Attribute</span></span>

<span data-ttu-id="c6ae9-104">Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="c6ae9-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="c6ae9-105">As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.</span><span class="sxs-lookup"><span data-stu-id="c6ae9-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="c6ae9-106">A partir de dezembro de 2011, este tópico foi arquivado.</span><span class="sxs-lookup"><span data-stu-id="c6ae9-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="c6ae9-107">Como resultado, ele não é mais mantido ativamente.</span><span class="sxs-lookup"><span data-stu-id="c6ae9-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="c6ae9-108">Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="c6ae9-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="c6ae9-109">Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="c6ae9-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="c6ae9-110">Determina se um mecanismo de regras será usado.</span><span class="sxs-lookup"><span data-stu-id="c6ae9-110">Determines whether a rules engine will be used.</span></span> <span data-ttu-id="c6ae9-111">Leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="c6ae9-111">Read/write.</span></span> <span data-ttu-id="c6ae9-112">**VgTriState**.</span><span class="sxs-lookup"><span data-stu-id="c6ae9-112">**VgTriState**.</span></span>

<span data-ttu-id="c6ae9-113">**Aplica-se a**</span><span class="sxs-lookup"><span data-stu-id="c6ae9-113">**Applies To**</span></span>

[<span data-ttu-id="c6ae9-114">Forma</span><span class="sxs-lookup"><span data-stu-id="c6ae9-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="c6ae9-115">**Sintaxe de marca**</span><span class="sxs-lookup"><span data-stu-id="c6ae9-115">**Tag Syntax**</span></span>

<span data-ttu-id="c6ae9-116"><v: *Element* o:ruleinitiator = " *expressão* " ></span><span class="sxs-lookup"><span data-stu-id="c6ae9-116"><v: *element* o:ruleinitiator=" *expression* "></span></span>

<span data-ttu-id="c6ae9-117">**Comentários**</span><span class="sxs-lookup"><span data-stu-id="c6ae9-117">**Remarks**</span></span>

<span data-ttu-id="c6ae9-118">O valor padrão é **Falso**.</span><span class="sxs-lookup"><span data-stu-id="c6ae9-118">The default value is **False**.</span></span> <span data-ttu-id="c6ae9-119">Se o valor for **true**, um mecanismo de regras será usado.</span><span class="sxs-lookup"><span data-stu-id="c6ae9-119">If the value is **True**, a rules engine is used.</span></span>

<span data-ttu-id="c6ae9-120">*Atributo de extensões de Microsoft Office*</span><span class="sxs-lookup"><span data-stu-id="c6ae9-120">*Microsoft Office Extensions Attribute*</span></span>

<span data-ttu-id="c6ae9-121">**Exemplo**</span><span class="sxs-lookup"><span data-stu-id="c6ae9-121">**Example**</span></span>

<span data-ttu-id="c6ae9-122">A forma será processada por um mecanismo de regras.</span><span class="sxs-lookup"><span data-stu-id="c6ae9-122">The shape will be processed by a rules engine.</span></span>


```HTML
   <v:rect id=myrect fillcolor="red" rulesinitiator="True"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
```



 

 