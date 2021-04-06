---
description: ICE15 valida que o tipo de conteúdo e as referências de extensão nas tabelas MIME e de extensão são recíprocas. A tabela MIME deve referenciar um tipo de conteúdo para uma extensão que a tabela de extensão faz referência ao mesmo tipo de conteúdo.
ms.assetid: 8a38c8d2-324d-4de9-932b-d188ff5ccbaf
title: ICE15
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb39b3c617db41e9e58a226f1eeb92c3d733ebad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011299"
---
# <a name="ice15"></a><span data-ttu-id="c282b-104">ICE15</span><span class="sxs-lookup"><span data-stu-id="c282b-104">ICE15</span></span>

<span data-ttu-id="c282b-105">ICE15 valida que o tipo de conteúdo e as referências de extensão nas tabelas [MIME](mime-table.md) e de [extensão](extension-table.md) são recíprocas.</span><span class="sxs-lookup"><span data-stu-id="c282b-105">ICE15 validates that content type and extension references in the [MIME](mime-table.md) and [Extension](extension-table.md) tables are reciprocal.</span></span> <span data-ttu-id="c282b-106">A tabela MIME deve referenciar um tipo de conteúdo para uma extensão que a tabela de extensão faz referência ao mesmo tipo de conteúdo.</span><span class="sxs-lookup"><span data-stu-id="c282b-106">The MIME table must reference a content type to an extension that the Extension table references back to the same content type.</span></span>

<span data-ttu-id="c282b-107">Várias extensões podem referenciar o mesmo tipo MIME, desde que o tipo MIME faça referência a uma das extensões.</span><span class="sxs-lookup"><span data-stu-id="c282b-107">Multiple extensions can reference the same MIME type, as long as the MIME type references back to one of the extensions.</span></span> <span data-ttu-id="c282b-108">Vários tipos MIME podem fazer referência à mesma extensão, desde que a extensão faça referência a um dos tipos MIME.</span><span class="sxs-lookup"><span data-stu-id="c282b-108">Multiple MIME types can reference the same extension, as long as the extension references back to one of the MIME types.</span></span>

<span data-ttu-id="c282b-109">Observe que sempre que um MIME faz referência a uma extensão, essa extensão não pode ter a \_ coluna MIME na tabela de extensão definida como NULL.</span><span class="sxs-lookup"><span data-stu-id="c282b-109">Note that whenever a MIME references an extension, that extension cannot have the MIME\_ column in the Extension table set to Null.</span></span>

## <a name="result"></a><span data-ttu-id="c282b-110">Resultado</span><span class="sxs-lookup"><span data-stu-id="c282b-110">Result</span></span>

<span data-ttu-id="c282b-111">ICE15 posta um erro se o tipo de conteúdo e as referências de extensão não forem recíprocos.</span><span class="sxs-lookup"><span data-stu-id="c282b-111">ICE15 posts an error if the content type and extension references are not reciprocal.</span></span>

## <a name="example"></a><span data-ttu-id="c282b-112">Exemplo</span><span class="sxs-lookup"><span data-stu-id="c282b-112">Example</span></span>

<span data-ttu-id="c282b-113">O ICE15 posta duas mensagens de erro para o exemplo mostrado:</span><span class="sxs-lookup"><span data-stu-id="c282b-113">ICE15 posts two error messages for the example shown:</span></span>

-   <span data-ttu-id="c282b-114">O tipo de conteúdo Test/x-flaps na tabela MIME faz referência à extensão TST, mas a extensão TST na tabela de extensão faz referência a flaps/x-flaps.</span><span class="sxs-lookup"><span data-stu-id="c282b-114">The content type test/x-flaps in the MIME table references the extension tst, but the extension tst in the Extension table references flaps/x-flaps.</span></span> <span data-ttu-id="c282b-115">Isso não é recíproco.</span><span class="sxs-lookup"><span data-stu-id="c282b-115">This is not reciprocal.</span></span>
-   <span data-ttu-id="c282b-116">O tipo de conteúdo flaps/x-flaps faz referência à extensão FLP, mas essa extensão tem uma entrada nula na \_ coluna MIME da tabela de extensão.</span><span class="sxs-lookup"><span data-stu-id="c282b-116">The content type flaps/x-flaps references the extension flp, but that extension has a Null entry in the MIME\_ column of the Extension table.</span></span>

<span data-ttu-id="c282b-117">[Tabela MIME](mime-table.md) (parcial)</span><span class="sxs-lookup"><span data-stu-id="c282b-117">[MIME Table](mime-table.md) (partial)</span></span>



| <span data-ttu-id="c282b-118">ContentType</span><span class="sxs-lookup"><span data-stu-id="c282b-118">ContentType</span></span>   | <span data-ttu-id="c282b-119">Extensão\_</span><span class="sxs-lookup"><span data-stu-id="c282b-119">Extension\_</span></span> |
|---------------|-------------|
| <span data-ttu-id="c282b-120">teste/x-teste</span><span class="sxs-lookup"><span data-stu-id="c282b-120">test/x-test</span></span>   | <span data-ttu-id="c282b-121">TST</span><span class="sxs-lookup"><span data-stu-id="c282b-121">tst</span></span>         |
| <span data-ttu-id="c282b-122">flaps/x-flaps</span><span class="sxs-lookup"><span data-stu-id="c282b-122">flaps/x-flaps</span></span> | <span data-ttu-id="c282b-123">FLP</span><span class="sxs-lookup"><span data-stu-id="c282b-123">flp</span></span>         |



 

<span data-ttu-id="c282b-124">[Tabela de extensão](extension-table.md) (parcial)</span><span class="sxs-lookup"><span data-stu-id="c282b-124">[Extension Table](extension-table.md) (partial)</span></span>



| <span data-ttu-id="c282b-125">Extensão</span><span class="sxs-lookup"><span data-stu-id="c282b-125">Extension</span></span> | <span data-ttu-id="c282b-126">MIME\_</span><span class="sxs-lookup"><span data-stu-id="c282b-126">MIME\_</span></span>        |
|-----------|---------------|
| <span data-ttu-id="c282b-127">TST</span><span class="sxs-lookup"><span data-stu-id="c282b-127">tst</span></span>       | <span data-ttu-id="c282b-128">flaps/x-flaps</span><span class="sxs-lookup"><span data-stu-id="c282b-128">flaps/x-flaps</span></span> |
| <span data-ttu-id="c282b-129">FLP</span><span class="sxs-lookup"><span data-stu-id="c282b-129">flp</span></span>       | <span data-ttu-id="c282b-130">Nulo</span><span class="sxs-lookup"><span data-stu-id="c282b-130">Null</span></span>          |



 

## <a name="related-topics"></a><span data-ttu-id="c282b-131">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="c282b-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c282b-132">Referência de ICE</span><span class="sxs-lookup"><span data-stu-id="c282b-132">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



