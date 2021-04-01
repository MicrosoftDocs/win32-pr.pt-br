---
title: Atributo Connecttype de VML
description: Atributo Connecttype de VML
ms.assetid: 907803c8-687b-4823-8252-b59acbbd9aa4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a54135dcb4ffe0a86f781d68b8babe1259029be
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104084555"
---
# <a name="vml-connecttype-attribute"></a><span data-ttu-id="d215b-103">Atributo Connecttype de VML</span><span class="sxs-lookup"><span data-stu-id="d215b-103">VML ConnectType Attribute</span></span>

<span data-ttu-id="d215b-104">Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="d215b-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="d215b-105">As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.</span><span class="sxs-lookup"><span data-stu-id="d215b-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="d215b-106">A partir de dezembro de 2011, este tópico foi arquivado.</span><span class="sxs-lookup"><span data-stu-id="d215b-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="d215b-107">Como resultado, ele não é mais mantido ativamente.</span><span class="sxs-lookup"><span data-stu-id="d215b-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="d215b-108">Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="d215b-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="d215b-109">Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="d215b-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="d215b-110">Define o tipo de pontos de conexão usados para anexar formas a outras formas.</span><span class="sxs-lookup"><span data-stu-id="d215b-110">Defines the type of connection points used for attaching shapes to other shapes.</span></span> <span data-ttu-id="d215b-111">Leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="d215b-111">Read/write.</span></span> <span data-ttu-id="d215b-112">**Cadeia de caracteres**.</span><span class="sxs-lookup"><span data-stu-id="d215b-112">**String**.</span></span>

<span data-ttu-id="d215b-113">**Aplica-se a**</span><span class="sxs-lookup"><span data-stu-id="d215b-113">**Applies To**</span></span>

[<span data-ttu-id="d215b-114">Caminho</span><span class="sxs-lookup"><span data-stu-id="d215b-114">Path</span></span>](msdn-online-vml-path-element.md)

<span data-ttu-id="d215b-115">**Sintaxe de marca**</span><span class="sxs-lookup"><span data-stu-id="d215b-115">**Tag Syntax**</span></span>

<span data-ttu-id="d215b-116"><v: *Element* o:connecttype = " *expressão* " ></span><span class="sxs-lookup"><span data-stu-id="d215b-116"><v: *element* o:connecttype=" *expression* "></span></span>

<span data-ttu-id="d215b-117">**Comentários**</span><span class="sxs-lookup"><span data-stu-id="d215b-117">**Remarks**</span></span>

<span data-ttu-id="d215b-118">Os valores são:</span><span class="sxs-lookup"><span data-stu-id="d215b-118">Values include:</span></span>



| <span data-ttu-id="d215b-119">Valor</span><span class="sxs-lookup"><span data-stu-id="d215b-119">Value</span></span>    | <span data-ttu-id="d215b-120">Descrição</span><span class="sxs-lookup"><span data-stu-id="d215b-120">Description</span></span>                                                                                                                           |
|----------|---------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d215b-121">none</span><span class="sxs-lookup"><span data-stu-id="d215b-121">none</span></span>     | <span data-ttu-id="d215b-122">Nenhum site de conexão.</span><span class="sxs-lookup"><span data-stu-id="d215b-122">No connection sites.</span></span> <span data-ttu-id="d215b-123">Padrão.</span><span class="sxs-lookup"><span data-stu-id="d215b-123">Default.</span></span>                                                                                                         |
| <span data-ttu-id="d215b-124">rect</span><span class="sxs-lookup"><span data-stu-id="d215b-124">rect</span></span>     | <span data-ttu-id="d215b-125">Os quatro pontos de conexão padrão, em pontos médios, dos lados superior, inferior, esquerdo e direito.</span><span class="sxs-lookup"><span data-stu-id="d215b-125">Standard four connection points at midpoints of top, bottom, left, and right sides.</span></span>                                                   |
| <span data-ttu-id="d215b-126">segmentos</span><span class="sxs-lookup"><span data-stu-id="d215b-126">segments</span></span> | <span data-ttu-id="d215b-127">Os pontos de edição da forma são usados.</span><span class="sxs-lookup"><span data-stu-id="d215b-127">The edit points of the shape are used.</span></span> <span data-ttu-id="d215b-128">Os pontos de edição são os pontos pretos em um editor gráfico que são usados para selecionar partes de uma forma.</span><span class="sxs-lookup"><span data-stu-id="d215b-128">Edit points are the black dots in a graphical editor that are used to select parts of a shape.</span></span> |
| <span data-ttu-id="d215b-129">custom</span><span class="sxs-lookup"><span data-stu-id="d215b-129">custom</span></span>   | <span data-ttu-id="d215b-130">Uma matriz personalizada de locais de conexão.</span><span class="sxs-lookup"><span data-stu-id="d215b-130">A custom array of connection locations.</span></span>                                                                                               |



 

<span data-ttu-id="d215b-131">*Atributo de extensões de Microsoft Office*</span><span class="sxs-lookup"><span data-stu-id="d215b-131">*Microsoft Office Extensions Attribute*</span></span>

 

 