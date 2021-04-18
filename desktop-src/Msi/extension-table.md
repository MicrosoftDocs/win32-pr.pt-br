---
description: A tabela de extensão contém informações sobre servidores de extensão de nome de arquivo que devem ser gerados como parte do anúncio do produto. Cada linha gera um conjunto de valores e chaves do registro.
ms.assetid: 924858b7-8956-4636-b7c7-c902aa822ee1
title: Tabela de extensão
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ef52f7248f44dcb63255244bbd8abd4ac8181d8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105752654"
---
# <a name="extension-table"></a><span data-ttu-id="811c9-104">Tabela de extensão</span><span class="sxs-lookup"><span data-stu-id="811c9-104">Extension Table</span></span>

<span data-ttu-id="811c9-105">A tabela de extensão contém informações sobre servidores de extensão de nome de arquivo que devem ser gerados como parte do anúncio do produto.</span><span class="sxs-lookup"><span data-stu-id="811c9-105">The Extension table contains information about file name extension servers that must be generated as a part of product advertisement.</span></span> <span data-ttu-id="811c9-106">Cada linha gera um conjunto de valores e chaves do registro.</span><span class="sxs-lookup"><span data-stu-id="811c9-106">Each row generates a set of registry keys and values.</span></span>

<span data-ttu-id="811c9-107">A tabela de extensão contém as colunas mostradas na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="811c9-107">The Extension table contains the columns shown in the following table.</span></span>



| <span data-ttu-id="811c9-108">Coluna</span><span class="sxs-lookup"><span data-stu-id="811c9-108">Column</span></span>      | <span data-ttu-id="811c9-109">Tipo</span><span class="sxs-lookup"><span data-stu-id="811c9-109">Type</span></span>                         | <span data-ttu-id="811c9-110">Chave</span><span class="sxs-lookup"><span data-stu-id="811c9-110">Key</span></span> | <span data-ttu-id="811c9-111">Nullable</span><span class="sxs-lookup"><span data-stu-id="811c9-111">Nullable</span></span> |
|-------------|------------------------------|-----|----------|
| <span data-ttu-id="811c9-112">Extensão</span><span class="sxs-lookup"><span data-stu-id="811c9-112">Extension</span></span>   | [<span data-ttu-id="811c9-113">Text</span><span class="sxs-lookup"><span data-stu-id="811c9-113">Text</span></span>](text.md)             | <span data-ttu-id="811c9-114">S</span><span class="sxs-lookup"><span data-stu-id="811c9-114">Y</span></span>   | <span data-ttu-id="811c9-115">N</span><span class="sxs-lookup"><span data-stu-id="811c9-115">N</span></span>        |
| <span data-ttu-id="811c9-116">Componente\_</span><span class="sxs-lookup"><span data-stu-id="811c9-116">Component\_</span></span> | [<span data-ttu-id="811c9-117">Identificador</span><span class="sxs-lookup"><span data-stu-id="811c9-117">Identifier</span></span>](identifier.md) | <span data-ttu-id="811c9-118">S</span><span class="sxs-lookup"><span data-stu-id="811c9-118">Y</span></span>   | <span data-ttu-id="811c9-119">N</span><span class="sxs-lookup"><span data-stu-id="811c9-119">N</span></span>        |
| <span data-ttu-id="811c9-120">ProgId\_</span><span class="sxs-lookup"><span data-stu-id="811c9-120">ProgId\_</span></span>    | [<span data-ttu-id="811c9-121">Text</span><span class="sxs-lookup"><span data-stu-id="811c9-121">Text</span></span>](text.md)             | <span data-ttu-id="811c9-122">N</span><span class="sxs-lookup"><span data-stu-id="811c9-122">N</span></span>   | <span data-ttu-id="811c9-123">S</span><span class="sxs-lookup"><span data-stu-id="811c9-123">Y</span></span>        |
| <span data-ttu-id="811c9-124">MIME\_</span><span class="sxs-lookup"><span data-stu-id="811c9-124">MIME\_</span></span>      | [<span data-ttu-id="811c9-125">Text</span><span class="sxs-lookup"><span data-stu-id="811c9-125">Text</span></span>](text.md)             | <span data-ttu-id="811c9-126">N</span><span class="sxs-lookup"><span data-stu-id="811c9-126">N</span></span>   | <span data-ttu-id="811c9-127">S</span><span class="sxs-lookup"><span data-stu-id="811c9-127">Y</span></span>        |
| <span data-ttu-id="811c9-128">Recurso\_</span><span class="sxs-lookup"><span data-stu-id="811c9-128">Feature\_</span></span>   | [<span data-ttu-id="811c9-129">Identificador</span><span class="sxs-lookup"><span data-stu-id="811c9-129">Identifier</span></span>](identifier.md) | <span data-ttu-id="811c9-130">N</span><span class="sxs-lookup"><span data-stu-id="811c9-130">N</span></span>   | <span data-ttu-id="811c9-131">N</span><span class="sxs-lookup"><span data-stu-id="811c9-131">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="811c9-132">Colunas</span><span class="sxs-lookup"><span data-stu-id="811c9-132">Columns</span></span>

<dl> <dt>

<span data-ttu-id="811c9-133"><span id="Extension"></span><span id="extension"></span><span id="EXTENSION"></span>Extensão</span><span class="sxs-lookup"><span data-stu-id="811c9-133"><span id="Extension"></span><span id="extension"></span><span id="EXTENSION"></span>Extension</span></span>
</dt> <dd>

<span data-ttu-id="811c9-134">A extensão associada à linha da tabela.</span><span class="sxs-lookup"><span data-stu-id="811c9-134">The extension associated with the table row.</span></span> <span data-ttu-id="811c9-135">A extensão pode ter até 255 caracteres de comprimento.</span><span class="sxs-lookup"><span data-stu-id="811c9-135">The extension can be up to 255 characters long.</span></span> <span data-ttu-id="811c9-136">Insira a extensão neste campo sem o período anterior.</span><span class="sxs-lookup"><span data-stu-id="811c9-136">Enter the extension in this field without the preceding period.</span></span>

</dd> <dt>

<span data-ttu-id="811c9-137"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Componente\_</span><span class="sxs-lookup"><span data-stu-id="811c9-137"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Component\_</span></span>
</dt> <dd>

<span data-ttu-id="811c9-138">Uma chave externa para a primeira coluna da tabela de [componentes](component-table.md) .</span><span class="sxs-lookup"><span data-stu-id="811c9-138">An external key to the first column of the [Component](component-table.md) table.</span></span> <span data-ttu-id="811c9-139">Esta coluna faz referência ao componente que controla a instalação da extensão.</span><span class="sxs-lookup"><span data-stu-id="811c9-139">This column references the component that controls the installation of the extension.</span></span>

</dd> <dt>

<span data-ttu-id="811c9-140"><span id="ProgId_"></span><span id="progid_"></span><span id="PROGID_"></span>ProgId\_</span><span class="sxs-lookup"><span data-stu-id="811c9-140"><span id="ProgId_"></span><span id="progid_"></span><span id="PROGID_"></span>ProgId\_</span></span>
</dt> <dd>

<span data-ttu-id="811c9-141">A ID do programa associada a esta extensão.</span><span class="sxs-lookup"><span data-stu-id="811c9-141">The Program ID associated with this extension.</span></span> <span data-ttu-id="811c9-142">Esta é uma chave estrangeira na tabela [ProgID](progid-table.md) .</span><span class="sxs-lookup"><span data-stu-id="811c9-142">This is a foreign key into the [ProgId](progid-table.md) table.</span></span>

</dd> <dt>

<span data-ttu-id="811c9-143"><span id="MIME_"></span><span id="mime_"></span>MIME\_</span><span class="sxs-lookup"><span data-stu-id="811c9-143"><span id="MIME_"></span><span id="mime_"></span>MIME\_</span></span>
</dt> <dd>

<span data-ttu-id="811c9-144">O tipo de conteúdo a ser gravado para a coluna de extensão.</span><span class="sxs-lookup"><span data-stu-id="811c9-144">The Content Type that is to be written for the Extension column.</span></span>

<span data-ttu-id="811c9-145">Uma chave externa para a primeira coluna da tabela [MIME](mime-table.md) .</span><span class="sxs-lookup"><span data-stu-id="811c9-145">An external key to the first column of the [MIME](mime-table.md) table.</span></span>

</dd> <dt>

<span data-ttu-id="811c9-146"><span id="Feature_"></span><span id="feature_"></span><span id="FEATURE_"></span>Recurso\_</span><span class="sxs-lookup"><span data-stu-id="811c9-146"><span id="Feature_"></span><span id="feature_"></span><span id="FEATURE_"></span>Feature\_</span></span>
</dt> <dd>

<span data-ttu-id="811c9-147">Uma chave externa na primeira coluna da tabela de [recursos](feature-table.md) que especifica o recurso que fornece o servidor de extensão.</span><span class="sxs-lookup"><span data-stu-id="811c9-147">An external key into the first column of the [Feature](feature-table.md) table specifying the feature that provides the extension server.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="811c9-148">Comentários</span><span class="sxs-lookup"><span data-stu-id="811c9-148">Remarks</span></span>

<span data-ttu-id="811c9-149">A tabela de extensão é referenciada quando a ação [RegisterExtensionInfo](registerextensioninfo-action.md) ou a ação [UnRegisterExtensionInfo](unregisterextensioninfo-action.md) é executada.</span><span class="sxs-lookup"><span data-stu-id="811c9-149">The Extension table is referred to when the [RegisterExtensionInfo](registerextensioninfo-action.md) action or the [UnRegisterExtensionInfo](unregisterextensioninfo-action.md) action is executed.</span></span>

## <a name="validation"></a><span data-ttu-id="811c9-150">Validação</span><span class="sxs-lookup"><span data-stu-id="811c9-150">Validation</span></span>

<dl>

[<span data-ttu-id="811c9-151">ICE03</span><span class="sxs-lookup"><span data-stu-id="811c9-151">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="811c9-152">ICE06</span><span class="sxs-lookup"><span data-stu-id="811c9-152">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="811c9-153">ICE15</span><span class="sxs-lookup"><span data-stu-id="811c9-153">ICE15</span></span>](ice15.md)  
[<span data-ttu-id="811c9-154">ICE19</span><span class="sxs-lookup"><span data-stu-id="811c9-154">ICE19</span></span>](ice19.md)  
[<span data-ttu-id="811c9-155">ICE32</span><span class="sxs-lookup"><span data-stu-id="811c9-155">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="811c9-156">ICE41</span><span class="sxs-lookup"><span data-stu-id="811c9-156">ICE41</span></span>](ice41.md)  
[<span data-ttu-id="811c9-157">ICE69</span><span class="sxs-lookup"><span data-stu-id="811c9-157">ICE69</span></span>](ice69.md)  
</dl>

 

 



