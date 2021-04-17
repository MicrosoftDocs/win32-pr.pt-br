---
title: Atributo do método VML
description: Atributo do método VML
ms.assetid: 42ab9d78-f004-4571-a566-03edd8341d19
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2f7440e1e793e7ad34860524f63a3bfc38456f1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "105789620"
---
# <a name="vml-method-attribute"></a><span data-ttu-id="e3c1b-103">Atributo do método VML</span><span class="sxs-lookup"><span data-stu-id="e3c1b-103">VML Method Attribute</span></span>

<span data-ttu-id="e3c1b-104">Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="e3c1b-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="e3c1b-105">As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.</span><span class="sxs-lookup"><span data-stu-id="e3c1b-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="e3c1b-106">A partir de dezembro de 2011, este tópico foi arquivado.</span><span class="sxs-lookup"><span data-stu-id="e3c1b-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="e3c1b-107">Como resultado, ele não é mais mantido ativamente.</span><span class="sxs-lookup"><span data-stu-id="e3c1b-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="e3c1b-108">Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="e3c1b-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="e3c1b-109">Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="e3c1b-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="e3c1b-110">Define o método usado para gerar um preenchimento gradual.</span><span class="sxs-lookup"><span data-stu-id="e3c1b-110">Defines the method used to generate a gradient fill.</span></span> <span data-ttu-id="e3c1b-111">Leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="e3c1b-111">Read/write.</span></span> <span data-ttu-id="e3c1b-112">**VgSigmaType**.</span><span class="sxs-lookup"><span data-stu-id="e3c1b-112">**VgSigmaType**.</span></span>

<span data-ttu-id="e3c1b-113">**Aplica-se a**</span><span class="sxs-lookup"><span data-stu-id="e3c1b-113">**Applies To**</span></span>

[<span data-ttu-id="e3c1b-114">Preencher</span><span class="sxs-lookup"><span data-stu-id="e3c1b-114">Fill</span></span>](msdn-online-vml-fill-element.md)

<span data-ttu-id="e3c1b-115">**Sintaxe de marca**</span><span class="sxs-lookup"><span data-stu-id="e3c1b-115">**Tag Syntax**</span></span>

<span data-ttu-id="e3c1b-116"><v: *Element* Method = " *expression* " ></span><span class="sxs-lookup"><span data-stu-id="e3c1b-116"><v: *element* method=" *expression* "></span></span>

<span data-ttu-id="e3c1b-117">**Sintaxe do script**</span><span class="sxs-lookup"><span data-stu-id="e3c1b-117">**Script Syntax**</span></span>

<span data-ttu-id="e3c1b-118">*elemento* . Method = "*expression*"</span><span class="sxs-lookup"><span data-stu-id="e3c1b-118">*element* .method="*expression*"</span></span>

<span data-ttu-id="e3c1b-119">*expressão* = de *elemento*. Method</span><span class="sxs-lookup"><span data-stu-id="e3c1b-119">*expression*=*element*.method</span></span>

<span data-ttu-id="e3c1b-120">**Comentários**</span><span class="sxs-lookup"><span data-stu-id="e3c1b-120">**Remarks**</span></span>

<span data-ttu-id="e3c1b-121">Os valores são:</span><span class="sxs-lookup"><span data-stu-id="e3c1b-121">Values include:</span></span>



| <span data-ttu-id="e3c1b-122">Valor</span><span class="sxs-lookup"><span data-stu-id="e3c1b-122">Value</span></span>  | <span data-ttu-id="e3c1b-123">Descrição</span><span class="sxs-lookup"><span data-stu-id="e3c1b-123">Description</span></span>          |
|--------|----------------------|
| <span data-ttu-id="e3c1b-124">Nenhum</span><span class="sxs-lookup"><span data-stu-id="e3c1b-124">None</span></span>   | <span data-ttu-id="e3c1b-125">Nenhum preenchimento Sigma.</span><span class="sxs-lookup"><span data-stu-id="e3c1b-125">No sigma fill.</span></span>       |
| <span data-ttu-id="e3c1b-126">Linear</span><span class="sxs-lookup"><span data-stu-id="e3c1b-126">Linear</span></span> | <span data-ttu-id="e3c1b-127">Preenchimento Sigma linear.</span><span class="sxs-lookup"><span data-stu-id="e3c1b-127">Linear sigma fill.</span></span>   |
| <span data-ttu-id="e3c1b-128">Sigma</span><span class="sxs-lookup"><span data-stu-id="e3c1b-128">Sigma</span></span>  | <span data-ttu-id="e3c1b-129">Preenchimento Sigma.</span><span class="sxs-lookup"><span data-stu-id="e3c1b-129">Sigma fill.</span></span> <span data-ttu-id="e3c1b-130">Padrão.</span><span class="sxs-lookup"><span data-stu-id="e3c1b-130">Default.</span></span> |
| <span data-ttu-id="e3c1b-131">Qualquer</span><span class="sxs-lookup"><span data-stu-id="e3c1b-131">Any</span></span>    | <span data-ttu-id="e3c1b-132">Qualquer preenchimento Sigma.</span><span class="sxs-lookup"><span data-stu-id="e3c1b-132">Any sigma fill.</span></span>      |



 

<span data-ttu-id="e3c1b-133">*Atributo padrão da VML*</span><span class="sxs-lookup"><span data-stu-id="e3c1b-133">*VML Standard Attribute*</span></span>

<span data-ttu-id="e3c1b-134">**Exemplo**</span><span class="sxs-lookup"><span data-stu-id="e3c1b-134">**Example**</span></span>

<span data-ttu-id="e3c1b-135">A forma terá um preenchimento de gradiente linear vermelho.</span><span class="sxs-lookup"><span data-stu-id="e3c1b-135">The shape will have a red linear gradient fill.</span></span>


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill color="red" type="gradient" method="linear"/>
   </v:shape>
```



 

 