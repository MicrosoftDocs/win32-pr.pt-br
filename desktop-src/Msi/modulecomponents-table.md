---
description: A tabela ModuleComponents contém uma lista dos componentes encontrados no módulo de mesclagem.
ms.assetid: def96d52-c9fa-4fac-b575-f9de8eb82d1c
title: Tabela ModuleComponents
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ea2f47418b0387c7fa9d289d156fb0369f53adf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105751194"
---
# <a name="modulecomponents-table"></a><span data-ttu-id="abb85-103">Tabela ModuleComponents</span><span class="sxs-lookup"><span data-stu-id="abb85-103">ModuleComponents Table</span></span>

<span data-ttu-id="abb85-104">A tabela ModuleComponents contém uma lista dos componentes encontrados no módulo de mesclagem.</span><span class="sxs-lookup"><span data-stu-id="abb85-104">The ModuleComponents table contains a list of the components found in the merge module.</span></span>

<span data-ttu-id="abb85-105">A tabela ModuleComponents tem as colunas a seguir.</span><span class="sxs-lookup"><span data-stu-id="abb85-105">The ModuleComponents table has the following columns.</span></span>



| <span data-ttu-id="abb85-106">Coluna</span><span class="sxs-lookup"><span data-stu-id="abb85-106">Column</span></span>    | <span data-ttu-id="abb85-107">Tipo</span><span class="sxs-lookup"><span data-stu-id="abb85-107">Type</span></span>                         | <span data-ttu-id="abb85-108">Chave</span><span class="sxs-lookup"><span data-stu-id="abb85-108">Key</span></span> | <span data-ttu-id="abb85-109">Nullable</span><span class="sxs-lookup"><span data-stu-id="abb85-109">Nullable</span></span> |
|-----------|------------------------------|-----|----------|
| <span data-ttu-id="abb85-110">Componente</span><span class="sxs-lookup"><span data-stu-id="abb85-110">Component</span></span> | [<span data-ttu-id="abb85-111">Identificador</span><span class="sxs-lookup"><span data-stu-id="abb85-111">Identifier</span></span>](identifier.md) | <span data-ttu-id="abb85-112">S</span><span class="sxs-lookup"><span data-stu-id="abb85-112">Y</span></span>   | <span data-ttu-id="abb85-113">N</span><span class="sxs-lookup"><span data-stu-id="abb85-113">N</span></span>        |
| <span data-ttu-id="abb85-114">ModuleID</span><span class="sxs-lookup"><span data-stu-id="abb85-114">ModuleID</span></span>  | [<span data-ttu-id="abb85-115">Identificador</span><span class="sxs-lookup"><span data-stu-id="abb85-115">Identifier</span></span>](identifier.md) | <span data-ttu-id="abb85-116">S</span><span class="sxs-lookup"><span data-stu-id="abb85-116">Y</span></span>   | <span data-ttu-id="abb85-117">N</span><span class="sxs-lookup"><span data-stu-id="abb85-117">N</span></span>        |
| <span data-ttu-id="abb85-118">Idioma</span><span class="sxs-lookup"><span data-stu-id="abb85-118">Language</span></span>  | [<span data-ttu-id="abb85-119">Inteiro</span><span class="sxs-lookup"><span data-stu-id="abb85-119">Integer</span></span>](integer.md)       | <span data-ttu-id="abb85-120">S</span><span class="sxs-lookup"><span data-stu-id="abb85-120">Y</span></span>   | <span data-ttu-id="abb85-121">N</span><span class="sxs-lookup"><span data-stu-id="abb85-121">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="abb85-122">Colunas</span><span class="sxs-lookup"><span data-stu-id="abb85-122">Columns</span></span>

<dl> <dt>

<span data-ttu-id="abb85-123"><span id="Component"></span><span id="component"></span><span id="COMPONENT"></span>Componente</span><span class="sxs-lookup"><span data-stu-id="abb85-123"><span id="Component"></span><span id="component"></span><span id="COMPONENT"></span>Component</span></span>
</dt> <dd>

<span data-ttu-id="abb85-124">Um identificador que faz referência a um componente no módulo de mesclagem.</span><span class="sxs-lookup"><span data-stu-id="abb85-124">An identifier referring to a component in the merge module.</span></span> <span data-ttu-id="abb85-125">A coluna de componente é uma chave estrangeira para a [tabela de componentes](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="abb85-125">The Component column is a foreign key to the [Component table](component-table.md).</span></span> <span data-ttu-id="abb85-126">A entrada na coluna componente deve seguir a Convenção de nomenclatura na [nomenclatura de chaves primárias em bancos de dados do módulo de mesclagem](naming-primary-keys-in-merge-module-databases.md).</span><span class="sxs-lookup"><span data-stu-id="abb85-126">The entry in the Component column must follow the naming convention in [Naming Primary Keys in Merge Module Databases](naming-primary-keys-in-merge-module-databases.md).</span></span>

</dd> <dt>

<span data-ttu-id="abb85-127"><span id="ModuleID"></span><span id="moduleid"></span><span id="MODULEID"></span>ModuleID</span><span class="sxs-lookup"><span data-stu-id="abb85-127"><span id="ModuleID"></span><span id="moduleid"></span><span id="MODULEID"></span>ModuleID</span></span>
</dt> <dd>

<span data-ttu-id="abb85-128">O identificador do módulo de mesclagem.</span><span class="sxs-lookup"><span data-stu-id="abb85-128">The identifier for the merge module.</span></span> <span data-ttu-id="abb85-129">Esta é uma chave estrangeira para a [tabela ModuleSignature](modulesignature-table.md).</span><span class="sxs-lookup"><span data-stu-id="abb85-129">This is a foreign key to the [ModuleSignature table](modulesignature-table.md).</span></span>

</dd> <dt>

<span data-ttu-id="abb85-130"><span id="Language"></span><span id="language"></span><span id="LANGUAGE"></span>Idioma</span><span class="sxs-lookup"><span data-stu-id="abb85-130"><span id="Language"></span><span id="language"></span><span id="LANGUAGE"></span>Language</span></span>
</dt> <dd>

<span data-ttu-id="abb85-131">O identificador de idioma descreve o idioma padrão para o módulo de mesclagem.</span><span class="sxs-lookup"><span data-stu-id="abb85-131">The Language identifier describes the default language for the merge module.</span></span> <span data-ttu-id="abb85-132">O identificador de idioma está em formato decimal, por exemplo, o inglês dos EUA é 1033.</span><span class="sxs-lookup"><span data-stu-id="abb85-132">The language identifier is in decimal format, for example, U.S. English is 1033.</span></span> <span data-ttu-id="abb85-133">Chave estrangeira para a [tabela ModuleSignature](modulesignature-table.md).</span><span class="sxs-lookup"><span data-stu-id="abb85-133">Foreign key to the [ModuleSignature table](modulesignature-table.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="abb85-134">Comentários</span><span class="sxs-lookup"><span data-stu-id="abb85-134">Remarks</span></span>

<span data-ttu-id="abb85-135">As transformações de linguagem devem ser capazes de atualizar esta tabela se o módulo de mesclagem oferecer suporte a vários idiomas.</span><span class="sxs-lookup"><span data-stu-id="abb85-135">Language transforms must be able to update this table if the merge module supports multiple languages.</span></span>

 

 



