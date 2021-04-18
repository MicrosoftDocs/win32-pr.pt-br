---
title: Atributo de tabela da VML
description: Atributo de tabela da VML
ms.assetid: 10355742-13b9-4c08-bff7-f7f7501762e9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f0f010f673b2663764814150f7a38fc06f23e11
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "105784960"
---
# <a name="vml-tableproperties-attribute"></a><span data-ttu-id="62ccb-103">Atributo de tabela da VML</span><span class="sxs-lookup"><span data-stu-id="62ccb-103">VML TableProperties Attribute</span></span>

<span data-ttu-id="62ccb-104">Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9.</span><span class="sxs-lookup"><span data-stu-id="62ccb-104">This topic describes VML, a feature that is deprecated as of Windows Internet Explorer 9.</span></span> <span data-ttu-id="62ccb-105">As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.</span><span class="sxs-lookup"><span data-stu-id="62ccb-105">Webpages and applications that rely on VML should be migrated to SVG or other widely supported standards.</span></span>

> [!Note]  
> <span data-ttu-id="62ccb-106">A partir de dezembro de 2011, este tópico foi arquivado.</span><span class="sxs-lookup"><span data-stu-id="62ccb-106">As of December 2011, this topic has been archived.</span></span> <span data-ttu-id="62ccb-107">Como resultado, ele não é mais mantido ativamente.</span><span class="sxs-lookup"><span data-stu-id="62ccb-107">As a result, it is no longer actively maintained.</span></span> <span data-ttu-id="62ccb-108">Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/).</span><span class="sxs-lookup"><span data-stu-id="62ccb-108">For more information, see [Archived Content](/previous-versions/windows/internet-explorer/ie-developer/).</span></span> <span data-ttu-id="62ccb-109">Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span><span class="sxs-lookup"><span data-stu-id="62ccb-109">For information, recommendations, and guidance regarding the current version of Windows Internet Explorer, see [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).</span></span>

 

<span data-ttu-id="62ccb-110">Determina as propriedades da tabela.</span><span class="sxs-lookup"><span data-stu-id="62ccb-110">Determines table properties.</span></span> <span data-ttu-id="62ccb-111">Leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="62ccb-111">Read/write.</span></span> <span data-ttu-id="62ccb-112">**Integer**.</span><span class="sxs-lookup"><span data-stu-id="62ccb-112">**Integer**.</span></span>

<span data-ttu-id="62ccb-113">**Aplica-se a**</span><span class="sxs-lookup"><span data-stu-id="62ccb-113">**Applies To**</span></span>

[<span data-ttu-id="62ccb-114">Forma</span><span class="sxs-lookup"><span data-stu-id="62ccb-114">Shape</span></span>](shape-element--vml.md)

<span data-ttu-id="62ccb-115">**Sintaxe de marca**</span><span class="sxs-lookup"><span data-stu-id="62ccb-115">**Tag Syntax**</span></span>

<span data-ttu-id="62ccb-116"><v: *Element* o:TableProperties = " *expressão* " ></span><span class="sxs-lookup"><span data-stu-id="62ccb-116"><v: *element* o:tableproperties=" *expression* "></span></span>

<span data-ttu-id="62ccb-117">**Comentários**</span><span class="sxs-lookup"><span data-stu-id="62ccb-117">**Remarks**</span></span>

<span data-ttu-id="62ccb-118">Usado pelo Microsoft PowerPoint para tabelas nativas.</span><span class="sxs-lookup"><span data-stu-id="62ccb-118">Used by Microsoft PowerPoint for native tables.</span></span> <span data-ttu-id="62ccb-119">O valor padrão é 0.</span><span class="sxs-lookup"><span data-stu-id="62ccb-119">Default value is 0.</span></span> <span data-ttu-id="62ccb-120">Somente os três primeiros bits deste inteiro são usados.</span><span class="sxs-lookup"><span data-stu-id="62ccb-120">Only the first three bits of this integer are used.</span></span>

<span data-ttu-id="62ccb-121">Embora o valor seja armazenado em uma forma, o atributo só é útil quando a tabela é composta de formas agrupadas. Os bits podem ser combinados.</span><span class="sxs-lookup"><span data-stu-id="62ccb-121">Even though the value is stored in a shape, the attribute is only useful when the table is made up of shapes that are grouped.Bits may be combined.</span></span>

<span data-ttu-id="62ccb-122">Os valores de bit a seguir estão incluídos.</span><span class="sxs-lookup"><span data-stu-id="62ccb-122">The following bit values are included.</span></span>



| <span data-ttu-id="62ccb-123">bit</span><span class="sxs-lookup"><span data-stu-id="62ccb-123">Bit</span></span> | <span data-ttu-id="62ccb-124">Descrição</span><span class="sxs-lookup"><span data-stu-id="62ccb-124">Description</span></span>                              |
|-----|------------------------------------------|
| <span data-ttu-id="62ccb-125">1</span><span class="sxs-lookup"><span data-stu-id="62ccb-125">1</span></span>   | <span data-ttu-id="62ccb-126">Defina se o grupo de formas é uma tabela.</span><span class="sxs-lookup"><span data-stu-id="62ccb-126">Set if the group of shapes is a table.</span></span>   |
| <span data-ttu-id="62ccb-127">2</span><span class="sxs-lookup"><span data-stu-id="62ccb-127">2</span></span>   | <span data-ttu-id="62ccb-128">Defina se a forma é um espaço reservado.</span><span class="sxs-lookup"><span data-stu-id="62ccb-128">Set if the shape is a placeholder.</span></span>       |
| <span data-ttu-id="62ccb-129">3</span><span class="sxs-lookup"><span data-stu-id="62ccb-129">3</span></span>   | <span data-ttu-id="62ccb-130">Defina se o texto da tabela é bidirecional.</span><span class="sxs-lookup"><span data-stu-id="62ccb-130">Set if the table text is bi-directional.</span></span> |



 

<span data-ttu-id="62ccb-131">*Atributo de extensões de Microsoft Office*</span><span class="sxs-lookup"><span data-stu-id="62ccb-131">*Microsoft Office Extensions Attribute*</span></span>

 

 