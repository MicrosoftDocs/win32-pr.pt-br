---
title: Atributo TextPathOK de VML
description: Atributo TextPathOK de VML
ms.assetid: 5d061258-1c4d-4391-81ce-13af90a4231c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06046a4f29c147ef109f0e4670d9965bab77a9fa
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103823791"
---
# <a name="vml-textpathok-attribute"></a><span data-ttu-id="d2564-103">Atributo TextPathOK de VML</span><span class="sxs-lookup"><span data-stu-id="d2564-103">VML TextPathOK Attribute</span></span>

<span data-ttu-id="d2564-104">Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="d2564-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="d2564-105">As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.</span><span class="sxs-lookup"><span data-stu-id="d2564-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="d2564-106">A partir de dezembro de 2011, este tópico foi arquivado.</span><span class="sxs-lookup"><span data-stu-id="d2564-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="d2564-107">Como resultado, ele não é mais mantido ativamente.</span><span class="sxs-lookup"><span data-stu-id="d2564-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="d2564-108">Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="d2564-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="d2564-109">Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="d2564-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="d2564-110">Determina se um caminho de texto será exibido.</span><span class="sxs-lookup"><span data-stu-id="d2564-110">Determines whether a text path will be displayed.</span></span> <span data-ttu-id="d2564-111">Leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="d2564-111">Read/write.</span></span> <span data-ttu-id="d2564-112">**VgTriState**.</span><span class="sxs-lookup"><span data-stu-id="d2564-112">**VgTriState**.</span></span>

<span data-ttu-id="d2564-113">**Aplica-se a**</span><span class="sxs-lookup"><span data-stu-id="d2564-113">**Applies To**</span></span>

[<span data-ttu-id="d2564-114">Caminho</span><span class="sxs-lookup"><span data-stu-id="d2564-114">Path</span></span>](msdn-online-vml-path-element.md)

<span data-ttu-id="d2564-115">**Sintaxe de marca**</span><span class="sxs-lookup"><span data-stu-id="d2564-115">**Tag Syntax**</span></span>

<span data-ttu-id="d2564-116"><v: *Element* textpathok = " *expressão* " ></span><span class="sxs-lookup"><span data-stu-id="d2564-116"><v: *element* textpathok=" *expression* "></span></span>

<span data-ttu-id="d2564-117">**Sintaxe do script**</span><span class="sxs-lookup"><span data-stu-id="d2564-117">**Script Syntax**</span></span>

<span data-ttu-id="d2564-118">*elemento* .</span><span class="sxs-lookup"><span data-stu-id="d2564-118">*element* .</span></span> <span data-ttu-id="d2564-119">textpathok = "*expressão*"</span><span class="sxs-lookup"><span data-stu-id="d2564-119">textpathok= "*expression*"</span></span>

<span data-ttu-id="d2564-120">*expressão* = de *elemento*.</span><span class="sxs-lookup"><span data-stu-id="d2564-120">*expression*=*element*.</span></span> <span data-ttu-id="d2564-121">textpathok</span><span class="sxs-lookup"><span data-stu-id="d2564-121">textpathok</span></span>

<span data-ttu-id="d2564-122">**Comentários**</span><span class="sxs-lookup"><span data-stu-id="d2564-122">**Remarks**</span></span>

<span data-ttu-id="d2564-123">Se **for false**, o caminho não poderá ter um caminho de texto.</span><span class="sxs-lookup"><span data-stu-id="d2564-123">If **False**, the path cannot have a text path.</span></span> <span data-ttu-id="d2564-124">O padrão é **False**.</span><span class="sxs-lookup"><span data-stu-id="d2564-124">The default is **False**.</span></span> <span data-ttu-id="d2564-125">Você deve ter esse atributo definido como **true** para exibir o texto em um caminho.</span><span class="sxs-lookup"><span data-stu-id="d2564-125">You must have this attribute set to **True** to display text on a path.</span></span>

<span data-ttu-id="d2564-126">*Atributo padrão da VML*</span><span class="sxs-lookup"><span data-stu-id="d2564-126">*VML Standard Attribute*</span></span>

<span data-ttu-id="d2564-127">**Exemplo**</span><span class="sxs-lookup"><span data-stu-id="d2564-127">**Example**</span></span>

<span data-ttu-id="d2564-128">A forma tem um caminho de texto.</span><span class="sxs-lookup"><span data-stu-id="d2564-128">The shape has a text path.</span></span> <span data-ttu-id="d2564-129">O texto "Olá, VML" é exibido ao longo de uma curva em forma de Smiley.</span><span class="sxs-lookup"><span data-stu-id="d2564-129">The text "Hello VML" is displayed along a smile-shaped curve.</span></span>


```HTML
   <v:curve id="tc" style="position:relative"
   from="50px 100px" to="400px 100px"
   control1="200px 200px" control2="300px 200px">
   <v:stroke weight="1pt" color="blue"
   filltype="solid"/>
   <v:fill on="True" color="yellow" color2="green" type="gradient"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" id="mytp"
   style="font:normal normal normal 36pt Arial"
   fitpath="True" string="Hello VML"/>
   </v:curve>
```



 

 