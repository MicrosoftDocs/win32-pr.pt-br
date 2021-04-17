---
description: Essa tabela temporária habilita a opção de desinstalação de patch de ação personalizada para ações personalizadas adicionadas ou atualizadas por um patch.
ms.assetid: 2d4a934f-e245-4d0a-b8bf-52457107ac08
title: MsiTransformView
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7eb50c397c10ede3a21b40600952d50e55a5ba1a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105770185"
---
# <a name="msitransformview"></a><span data-ttu-id="b084c-103">MsiTransformView</span><span class="sxs-lookup"><span data-stu-id="b084c-103">MsiTransformView</span></span>

<span data-ttu-id="b084c-104">Essa tabela temporária habilita a [opção de desinstalação de patch de ação personalizada](custom-action-patch-uninstall-option.md) para ações personalizadas adicionadas ou atualizadas por um patch.</span><span class="sxs-lookup"><span data-stu-id="b084c-104">This temporary table enables the [Custom Action Patch Uninstall Option](custom-action-patch-uninstall-option.md) for custom actions added or updated by a patch.</span></span>

<span data-ttu-id="b084c-105">Se um patch adicionar ou atualizar uma ação personalizada com o atributo **msidbCustomActionTypePatchUninstall** , Windows Installer executará a ação personalizada nova ou atualizada quando o patch for desinstalado.</span><span class="sxs-lookup"><span data-stu-id="b084c-105">If a patch adds or updates a custom action having the **msidbCustomActionTypePatchUninstall** attribute, Windows Installer runs the new or updated custom action when the patch is uninstalled.</span></span> <span data-ttu-id="b084c-106">Windows Installer faz com que as atualizações no patch sejam desinstaladas disponíveis para a ação personalizada de desinstalação do patch.</span><span class="sxs-lookup"><span data-stu-id="b084c-106">Windows Installer makes the updates within the patch being uninstalled available to the patch uninstall custom action.</span></span> <span data-ttu-id="b084c-107">O patch deve incluir uma *<PatchGUID>* tabela MsiTransformView para fornecer essas informações para Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="b084c-107">The patch must include a MsiTransformView *<PatchGUID>* table to provide this information to Windows Installer.</span></span> <span data-ttu-id="b084c-108">As informações nesta tabela estão disponíveis para qualquer ação personalizada imediata e não estão disponíveis para ações personalizadas adiadas.</span><span class="sxs-lookup"><span data-stu-id="b084c-108">The information in this table is available to any immediate custom action, and is unavailable to deferred custom actions.</span></span>

<span data-ttu-id="b084c-109">**[Windows Installer 4,0 e anteriores](not-supported-in-windows-installer-4-0.md):** Sem suporte.</span><span class="sxs-lookup"><span data-stu-id="b084c-109">**[Windows Installer 4.0 and earlier](not-supported-in-windows-installer-4-0.md):** Not supported.</span></span> <span data-ttu-id="b084c-110">A [opção de desinstalação de patch de ação personalizada](custom-action-patch-uninstall-option.md) está disponível a partir do Windows Installer 4,5.</span><span class="sxs-lookup"><span data-stu-id="b084c-110">The [Custom Action Patch Uninstall Option](custom-action-patch-uninstall-option.md) is available beginning with Windows Installer 4.5.</span></span>

<span data-ttu-id="b084c-111">Essa tabela deve ser nomeada como *<PatchGUID>* tabela MsiTransformView, em que *<PatchGUID>* é o GUID que identifica exclusivamente o patch.</span><span class="sxs-lookup"><span data-stu-id="b084c-111">This table should be named MsiTransformView *<PatchGUID>* Table, where *<PatchGUID>* is the GUID that uniquely identifies the patch.</span></span> <span data-ttu-id="b084c-112">A *<PatchGUID>* tabela MsiTransformView tem as colunas a seguir.</span><span class="sxs-lookup"><span data-stu-id="b084c-112">The MsiTransformView *<PatchGUID>* Table has the following columns.</span></span>



| <span data-ttu-id="b084c-113">Coluna</span><span class="sxs-lookup"><span data-stu-id="b084c-113">Column</span></span>  | <span data-ttu-id="b084c-114">Tipo</span><span class="sxs-lookup"><span data-stu-id="b084c-114">Type</span></span>                         | <span data-ttu-id="b084c-115">Chave</span><span class="sxs-lookup"><span data-stu-id="b084c-115">Key</span></span> | <span data-ttu-id="b084c-116">Nullable</span><span class="sxs-lookup"><span data-stu-id="b084c-116">Nullable</span></span> |
|---------|------------------------------|-----|----------|
| <span data-ttu-id="b084c-117">Tabela</span><span class="sxs-lookup"><span data-stu-id="b084c-117">Table</span></span>   | [<span data-ttu-id="b084c-118">Identificador</span><span class="sxs-lookup"><span data-stu-id="b084c-118">Identifier</span></span>](identifier.md) | <span data-ttu-id="b084c-119">S</span><span class="sxs-lookup"><span data-stu-id="b084c-119">Y</span></span>   | <span data-ttu-id="b084c-120">N</span><span class="sxs-lookup"><span data-stu-id="b084c-120">N</span></span>        |
| <span data-ttu-id="b084c-121">Coluna</span><span class="sxs-lookup"><span data-stu-id="b084c-121">Column</span></span>  | [<span data-ttu-id="b084c-122">Text</span><span class="sxs-lookup"><span data-stu-id="b084c-122">Text</span></span>](text.md)             | <span data-ttu-id="b084c-123">S</span><span class="sxs-lookup"><span data-stu-id="b084c-123">Y</span></span>   | <span data-ttu-id="b084c-124">N</span><span class="sxs-lookup"><span data-stu-id="b084c-124">N</span></span>        |
| <span data-ttu-id="b084c-125">Linha</span><span class="sxs-lookup"><span data-stu-id="b084c-125">Row</span></span>     | [<span data-ttu-id="b084c-126">Text</span><span class="sxs-lookup"><span data-stu-id="b084c-126">Text</span></span>](text.md)             | <span data-ttu-id="b084c-127">S</span><span class="sxs-lookup"><span data-stu-id="b084c-127">Y</span></span>   | <span data-ttu-id="b084c-128">S</span><span class="sxs-lookup"><span data-stu-id="b084c-128">Y</span></span>        |
| <span data-ttu-id="b084c-129">Dados</span><span class="sxs-lookup"><span data-stu-id="b084c-129">Data</span></span>    | [<span data-ttu-id="b084c-130">Text</span><span class="sxs-lookup"><span data-stu-id="b084c-130">Text</span></span>](text.md)             | <span data-ttu-id="b084c-131">N</span><span class="sxs-lookup"><span data-stu-id="b084c-131">N</span></span>   | <span data-ttu-id="b084c-132">S</span><span class="sxs-lookup"><span data-stu-id="b084c-132">Y</span></span>        |
| <span data-ttu-id="b084c-133">Current</span><span class="sxs-lookup"><span data-stu-id="b084c-133">Current</span></span> | [<span data-ttu-id="b084c-134">Text</span><span class="sxs-lookup"><span data-stu-id="b084c-134">Text</span></span>](text.md)             | <span data-ttu-id="b084c-135">N</span><span class="sxs-lookup"><span data-stu-id="b084c-135">N</span></span>   | <span data-ttu-id="b084c-136">S</span><span class="sxs-lookup"><span data-stu-id="b084c-136">Y</span></span>        |



 

## <a name="column"></a><span data-ttu-id="b084c-137">Coluna</span><span class="sxs-lookup"><span data-stu-id="b084c-137">Column</span></span>

<dl> <dt>

<span data-ttu-id="b084c-138"><span id="Table"></span><span id="table"></span><span id="TABLE"></span>Tabela</span><span class="sxs-lookup"><span data-stu-id="b084c-138"><span id="Table"></span><span id="table"></span><span id="TABLE"></span>Table</span></span>
</dt> <dd>

<span data-ttu-id="b084c-139">Nome de uma tabela de banco de dados alterada.</span><span class="sxs-lookup"><span data-stu-id="b084c-139">Name of an altered database table.</span></span>

</dd> <dt>

<span data-ttu-id="b084c-140"><span id="Column"></span><span id="column"></span><span id="COLUMN"></span>Pilha</span><span class="sxs-lookup"><span data-stu-id="b084c-140"><span id="Column"></span><span id="column"></span><span id="COLUMN"></span>Column</span></span>
</dt> <dd>

<span data-ttu-id="b084c-141">Nome de uma coluna de tabela alterada ou inserir, excluir, criar ou descartar.</span><span class="sxs-lookup"><span data-stu-id="b084c-141">Name of an altered table column or INSERT, DELETE, CREATE, or DROP.</span></span>

</dd> <dt>

<span data-ttu-id="b084c-142"><span id="Row"></span><span id="row"></span><span id="ROW"></span>Fila</span><span class="sxs-lookup"><span data-stu-id="b084c-142"><span id="Row"></span><span id="row"></span><span id="ROW"></span>Row</span></span>
</dt> <dd>

<span data-ttu-id="b084c-143">Uma lista dos valores de chave primária separados por tabulações.</span><span class="sxs-lookup"><span data-stu-id="b084c-143">A list of the primary key values separated by tabs.</span></span> <span data-ttu-id="b084c-144">Valores nulos de chave primária são representados por um único caractere de espaço.</span><span class="sxs-lookup"><span data-stu-id="b084c-144">Null primary key values are represented by a single space character.</span></span> <span data-ttu-id="b084c-145">Um valor nulo nesta coluna indica uma alteração de esquema.</span><span class="sxs-lookup"><span data-stu-id="b084c-145">A Null value in this column indicates a schema change.</span></span>

</dd> <dt>

<span data-ttu-id="b084c-146"><span id="Data"></span><span id="data"></span><span id="DATA"></span>Dado</span><span class="sxs-lookup"><span data-stu-id="b084c-146"><span id="Data"></span><span id="data"></span><span id="DATA"></span>Data</span></span>
</dt> <dd>

<span data-ttu-id="b084c-147">Dados, nome de um fluxo de dados ou uma definição de coluna.</span><span class="sxs-lookup"><span data-stu-id="b084c-147">Data, name of a data stream, or a column definition.</span></span>

</dd> <dt>

<span data-ttu-id="b084c-148"><span id="Current"></span><span id="current"></span><span id="CURRENT"></span>Atualizados</span><span class="sxs-lookup"><span data-stu-id="b084c-148"><span id="Current"></span><span id="current"></span><span id="CURRENT"></span>Current</span></span>
</dt> <dd>

<span data-ttu-id="b084c-149">Valor atual do banco de dados de referência ou de um número de coluna.</span><span class="sxs-lookup"><span data-stu-id="b084c-149">Current value from reference database, or column a number.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b084c-150">Comentários</span><span class="sxs-lookup"><span data-stu-id="b084c-150">Remarks</span></span>

<span data-ttu-id="b084c-151">O patch de desinstalação de ações personalizadas é executado quando o patch é desinstalado.</span><span class="sxs-lookup"><span data-stu-id="b084c-151">Patch uninstall custom actions run when the patch is uninstalled.</span></span> <span data-ttu-id="b084c-152">Eles não são executados quando o produto é desinstalado.</span><span class="sxs-lookup"><span data-stu-id="b084c-152">They do not run when the product is uninstalled.</span></span> <span data-ttu-id="b084c-153">Use a [opção de desinstalação de patch de ação personalizada](custom-action-patch-uninstall-option.md) e esta tabela para executar um personalizado somente quando o patch estiver sendo desinstalado.</span><span class="sxs-lookup"><span data-stu-id="b084c-153">Use the [Custom Action Patch Uninstall Option](custom-action-patch-uninstall-option.md) and this table to run a custom only when the patch is being uninstalled.</span></span>

<span data-ttu-id="b084c-154">Um patch pode atualizar uma ação personalizada fornecida no pacote original (arquivo. msi). Para executar a versão atualizada da ação personalizada quando o patch for desinstalado, marque a ação personalizada com o atributo **msidbCustomActionTypePatchUninstall** no pacote original.</span><span class="sxs-lookup"><span data-stu-id="b084c-154">A patch can update a custom action provided in the original package (.msi file.) To run the updated version of the custom action when the patch is uninstalled, mark the custom action with the **msidbCustomActionTypePatchUninstall** attribute in the original package.</span></span>

 

 



