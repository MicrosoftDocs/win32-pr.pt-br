---
title: Atributo Conectortype da VML
description: Atributo Conectortype da VML
ms.assetid: acb9050d-c9e4-4d87-96c2-0bd2a1cf6e6b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0be0309e478970b93324b98a5efaaae54964435
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "105785390"
---
# <a name="vml-connectortype-attribute"></a><span data-ttu-id="b7635-103">Atributo Conectortype da VML</span><span class="sxs-lookup"><span data-stu-id="b7635-103">VML ConnectorType Attribute</span></span>

<span data-ttu-id="b7635-104">Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="b7635-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="b7635-105">As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.</span><span class="sxs-lookup"><span data-stu-id="b7635-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="b7635-106">A partir de dezembro de 2011, este tópico foi arquivado.</span><span class="sxs-lookup"><span data-stu-id="b7635-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="b7635-107">Como resultado, ele não é mais mantido ativamente.</span><span class="sxs-lookup"><span data-stu-id="b7635-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="b7635-108">Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="b7635-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="b7635-109">Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="b7635-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="b7635-110">Indica o tipo de conector usado para unir formas.</span><span class="sxs-lookup"><span data-stu-id="b7635-110">Indicates the type of connector used for joining shapes.</span></span> <span data-ttu-id="b7635-111">Leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="b7635-111">Read/write.</span></span> <span data-ttu-id="b7635-112">**Cadeia de caracteres**.</span><span class="sxs-lookup"><span data-stu-id="b7635-112">**String**.</span></span>

<span data-ttu-id="b7635-113">**Aplica-se a**</span><span class="sxs-lookup"><span data-stu-id="b7635-113">**Applies To**</span></span>

[<span data-ttu-id="b7635-114">Forma</span><span class="sxs-lookup"><span data-stu-id="b7635-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="b7635-115">**Sintaxe de marca**</span><span class="sxs-lookup"><span data-stu-id="b7635-115">**Tag Syntax**</span></span>

<span data-ttu-id="b7635-116"><v: *Element* o:ConnectorType = " *expressão* " ></span><span class="sxs-lookup"><span data-stu-id="b7635-116"><v: *element* o:connectortype=" *expression* "></span></span>

<span data-ttu-id="b7635-117">**Comentários**</span><span class="sxs-lookup"><span data-stu-id="b7635-117">**Remarks**</span></span>

<span data-ttu-id="b7635-118">Os valores são:</span><span class="sxs-lookup"><span data-stu-id="b7635-118">Values include:</span></span>



| <span data-ttu-id="b7635-119">Valor</span><span class="sxs-lookup"><span data-stu-id="b7635-119">Value</span></span>    | <span data-ttu-id="b7635-120">Descrição</span><span class="sxs-lookup"><span data-stu-id="b7635-120">Description</span></span>                    |
|----------|--------------------------------|
| <span data-ttu-id="b7635-121">none</span><span class="sxs-lookup"><span data-stu-id="b7635-121">none</span></span>     | <span data-ttu-id="b7635-122">Nenhum conector.</span><span class="sxs-lookup"><span data-stu-id="b7635-122">No connector.</span></span>                  |
| <span data-ttu-id="b7635-123">simples</span><span class="sxs-lookup"><span data-stu-id="b7635-123">straight</span></span> | <span data-ttu-id="b7635-124">Padrão.</span><span class="sxs-lookup"><span data-stu-id="b7635-124">Default.</span></span> <span data-ttu-id="b7635-125">Um conector reto.</span><span class="sxs-lookup"><span data-stu-id="b7635-125">A straight connector.</span></span> |
| <span data-ttu-id="b7635-126">angular</span><span class="sxs-lookup"><span data-stu-id="b7635-126">elbow</span></span>    | <span data-ttu-id="b7635-127">Um conector em forma de ângulo.</span><span class="sxs-lookup"><span data-stu-id="b7635-127">An elbow-shaped connector.</span></span>     |
| <span data-ttu-id="b7635-128">curva</span><span class="sxs-lookup"><span data-stu-id="b7635-128">curved</span></span>   | <span data-ttu-id="b7635-129">Um conector curvo.</span><span class="sxs-lookup"><span data-stu-id="b7635-129">A curved connector.</span></span>            |



 

<span data-ttu-id="b7635-130">Esse atributo também pode ser usado por um mecanismo de regras de um editor gráfico.</span><span class="sxs-lookup"><span data-stu-id="b7635-130">This attribute may also be used by a rules engine of a graphical editor.</span></span>

<span data-ttu-id="b7635-131">*Atributo de extensões de Microsoft Office*</span><span class="sxs-lookup"><span data-stu-id="b7635-131">*Microsoft Office Extensions Attribute*</span></span>

<span data-ttu-id="b7635-132">**Exemplo**</span><span class="sxs-lookup"><span data-stu-id="b7635-132">**Example**</span></span>

<span data-ttu-id="b7635-133">A forma usa uma linha reta como um conector.</span><span class="sxs-lookup"><span data-stu-id="b7635-133">The shape uses a straight line as a connector.</span></span>


```HTML
   <v:rect id=myrect fillcolor="red" o:connectortype="straight"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
```



 

 