---
description: A tabela UIText contém as versões localizadas de algumas das cadeias de caracteres usadas na interface do usuário. Essas cadeias de caracteres não fazem parte de nenhuma outra tabela. A tabela UIText é para cadeias de caracteres que não têm nenhum local lógico em nenhuma outra tabela.
ms.assetid: 2965e3a8-2cbf-4445-963b-ec2040692106
title: Tabela UIText
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5fe8bbdec694511103636508d229ab0d2e40afc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089846"
---
# <a name="uitext-table"></a><span data-ttu-id="60fbb-105">Tabela UIText</span><span class="sxs-lookup"><span data-stu-id="60fbb-105">UIText Table</span></span>

<span data-ttu-id="60fbb-106">A tabela UIText contém as versões localizadas de algumas das cadeias de caracteres usadas na interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="60fbb-106">The UIText table contains the localized versions of some of the strings used in the user interface.</span></span> <span data-ttu-id="60fbb-107">Essas cadeias de caracteres não fazem parte de nenhuma outra tabela.</span><span class="sxs-lookup"><span data-stu-id="60fbb-107">These strings are not part of any other table.</span></span> <span data-ttu-id="60fbb-108">A tabela UIText é para cadeias de caracteres que não têm nenhum local lógico em nenhuma outra tabela.</span><span class="sxs-lookup"><span data-stu-id="60fbb-108">The UIText table is for strings that have no logical place in any other table.</span></span>

<span data-ttu-id="60fbb-109">A tabela UIText tem as colunas a seguir.</span><span class="sxs-lookup"><span data-stu-id="60fbb-109">The UIText table has the following columns.</span></span>



| <span data-ttu-id="60fbb-110">Coluna</span><span class="sxs-lookup"><span data-stu-id="60fbb-110">Column</span></span> | <span data-ttu-id="60fbb-111">Type</span><span class="sxs-lookup"><span data-stu-id="60fbb-111">Type</span></span>                         | <span data-ttu-id="60fbb-112">Chave</span><span class="sxs-lookup"><span data-stu-id="60fbb-112">Key</span></span> | <span data-ttu-id="60fbb-113">Nullable</span><span class="sxs-lookup"><span data-stu-id="60fbb-113">Nullable</span></span> |
|--------|------------------------------|-----|----------|
| <span data-ttu-id="60fbb-114">Chave</span><span class="sxs-lookup"><span data-stu-id="60fbb-114">Key</span></span>    | [<span data-ttu-id="60fbb-115">Identificador</span><span class="sxs-lookup"><span data-stu-id="60fbb-115">Identifier</span></span>](identifier.md) | <span data-ttu-id="60fbb-116">S</span><span class="sxs-lookup"><span data-stu-id="60fbb-116">Y</span></span>   | <span data-ttu-id="60fbb-117">N</span><span class="sxs-lookup"><span data-stu-id="60fbb-117">N</span></span>        |
| <span data-ttu-id="60fbb-118">Texto</span><span class="sxs-lookup"><span data-stu-id="60fbb-118">Text</span></span>   | [<span data-ttu-id="60fbb-119">Text</span><span class="sxs-lookup"><span data-stu-id="60fbb-119">Text</span></span>](text.md)             | <span data-ttu-id="60fbb-120">N</span><span class="sxs-lookup"><span data-stu-id="60fbb-120">N</span></span>   | <span data-ttu-id="60fbb-121">S</span><span class="sxs-lookup"><span data-stu-id="60fbb-121">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="60fbb-122">Colunas</span><span class="sxs-lookup"><span data-stu-id="60fbb-122">Columns</span></span>

<dl> <dt>

<span data-ttu-id="60fbb-123"><span id="Key"></span><span id="key"></span><span id="KEY"></span>Chaves</span><span class="sxs-lookup"><span data-stu-id="60fbb-123"><span id="Key"></span><span id="key"></span><span id="KEY"></span>Key</span></span>
</dt> <dd>

<span data-ttu-id="60fbb-124">Uma chave exclusiva que identifica a cadeia de caracteres específica.</span><span class="sxs-lookup"><span data-stu-id="60fbb-124">A unique key that identifies the particular string.</span></span>

</dd> <dt>

<span data-ttu-id="60fbb-125"><span id="Text"></span><span id="text"></span><span id="TEXT"></span>Texto</span><span class="sxs-lookup"><span data-stu-id="60fbb-125"><span id="Text"></span><span id="text"></span><span id="TEXT"></span>Text</span></span>
</dt> <dd>

<span data-ttu-id="60fbb-126">A versão localizada da cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="60fbb-126">The localized version of the string.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="60fbb-127">Comentários</span><span class="sxs-lookup"><span data-stu-id="60fbb-127">Remarks</span></span>

<span data-ttu-id="60fbb-128">Alguns controles usam a tabela UIText como uma fonte de cadeias de caracteres.</span><span class="sxs-lookup"><span data-stu-id="60fbb-128">Some controls use the UIText table as a source of strings.</span></span> <span data-ttu-id="60fbb-129">Para obter informações sobre quais cadeias de caracteres são necessárias nesta tabela para cada controle específico, consulte os controles individuais na [referência da interface do usuário](user-interface-reference.md).</span><span class="sxs-lookup"><span data-stu-id="60fbb-129">For information about which strings are required in this table for each particular control, see the individual controls in the [User Interface Reference](user-interface-reference.md).</span></span>

## <a name="validation"></a><span data-ttu-id="60fbb-130">Validação</span><span class="sxs-lookup"><span data-stu-id="60fbb-130">Validation</span></span>

<dl>

[<span data-ttu-id="60fbb-131">ICE03</span><span class="sxs-lookup"><span data-stu-id="60fbb-131">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="60fbb-132">ICE06</span><span class="sxs-lookup"><span data-stu-id="60fbb-132">ICE06</span></span>](ice06.md)  
</dl>

 

 



