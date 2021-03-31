---
description: 'Este exemplo ilustra o layout de um arquivo. Cub contendo duas ICEs. O instalador executa as ações personalizadas na sequência: ICE01 e ICE08.'
ms.assetid: 609cd16a-4421-4082-855d-229f5ba7117b
title: Arquivo. Cub de exemplo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e937b779e2a620ffc17cf936e37f74867f3dfdd4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920866"
---
# <a name="sample-cub-file"></a><span data-ttu-id="ee72e-104">Arquivo. Cub de exemplo</span><span class="sxs-lookup"><span data-stu-id="ee72e-104">Sample .cub File</span></span>

<span data-ttu-id="ee72e-105">Este exemplo ilustra o layout de um arquivo. Cub contendo duas [ICES](internal-consistency-evaluators-ices.md).</span><span class="sxs-lookup"><span data-stu-id="ee72e-105">This sample illustrates the layout of a .cub file containing two [ICEs](internal-consistency-evaluators-ices.md).</span></span> <span data-ttu-id="ee72e-106">O instalador executa as ações personalizadas na sequência: ICE01 e ICE08.</span><span class="sxs-lookup"><span data-stu-id="ee72e-106">The installer executes the custom actions in the sequence: ICE01 and ICE08.</span></span>

<span data-ttu-id="ee72e-107">A ação personalizada ICE01 é um [tipo de ação personalizada 1](custom-action-type-1.md).</span><span class="sxs-lookup"><span data-stu-id="ee72e-107">The custom action ICE01 is a [Custom Action Type 1](custom-action-type-1.md).</span></span> <span data-ttu-id="ee72e-108">É um ponto de entrada para uma DLL que é armazenada como um fluxo no arquivo. cub.</span><span class="sxs-lookup"><span data-stu-id="ee72e-108">It is an entry point to a DLL that is stored as a stream in the .cub file.</span></span> <span data-ttu-id="ee72e-109">Esse fluxo é listado na tabela binária ice.dll.</span><span class="sxs-lookup"><span data-stu-id="ee72e-109">This stream is listed in the Binary Table ice.dll.</span></span>

<span data-ttu-id="ee72e-110">A ação personalizada ICE08 é um [tipo de ação personalizada 6](custom-action-type-6.md).</span><span class="sxs-lookup"><span data-stu-id="ee72e-110">The custom action ICE08 is a [Custom Action Type 6](custom-action-type-6.md).</span></span> <span data-ttu-id="ee72e-111">É um ponto de entrada para uma função no VBScript que é armazenada como um fluxo no arquivo. cub.</span><span class="sxs-lookup"><span data-stu-id="ee72e-111">It is an entry point to a function in VBScript that is stored as a stream in the .cub file.</span></span> <span data-ttu-id="ee72e-112">Esse fluxo é listado na tabela binária como ice.vbs.</span><span class="sxs-lookup"><span data-stu-id="ee72e-112">This stream is listed in the Binary Table as ice.vbs.</span></span>

[<span data-ttu-id="ee72e-113">Tabela binária</span><span class="sxs-lookup"><span data-stu-id="ee72e-113">Binary Table</span></span>](binary-table.md)



| <span data-ttu-id="ee72e-114">Name</span><span class="sxs-lookup"><span data-stu-id="ee72e-114">Name</span></span>    | <span data-ttu-id="ee72e-115">Dados</span><span class="sxs-lookup"><span data-stu-id="ee72e-115">Data</span></span>                               |
|---------|------------------------------------|
| <span data-ttu-id="ee72e-116">ice.vbs</span><span class="sxs-lookup"><span data-stu-id="ee72e-116">ice.vbs</span></span> | <span data-ttu-id="ee72e-117">Dados binários não formatados de ice.vbs</span><span class="sxs-lookup"><span data-stu-id="ee72e-117">Unformatted binary data of ice.vbs</span></span> |
| <span data-ttu-id="ee72e-118">ice.dll</span><span class="sxs-lookup"><span data-stu-id="ee72e-118">ice.dll</span></span> | <span data-ttu-id="ee72e-119">Dados binários não formatados de ice.dll</span><span class="sxs-lookup"><span data-stu-id="ee72e-119">Unformatted binary data of ice.dll</span></span> |



 

[<span data-ttu-id="ee72e-120">Tabela CustomAction</span><span class="sxs-lookup"><span data-stu-id="ee72e-120">CustomAction Table</span></span>](customaction-table.md)



| <span data-ttu-id="ee72e-121">Ação</span><span class="sxs-lookup"><span data-stu-id="ee72e-121">Action</span></span> | <span data-ttu-id="ee72e-122">Tipo</span><span class="sxs-lookup"><span data-stu-id="ee72e-122">Type</span></span> | <span data-ttu-id="ee72e-123">Fonte</span><span class="sxs-lookup"><span data-stu-id="ee72e-123">Source</span></span>  | <span data-ttu-id="ee72e-124">Destino</span><span class="sxs-lookup"><span data-stu-id="ee72e-124">Target</span></span> |
|--------|------|---------|--------|
| <span data-ttu-id="ee72e-125">ICE01</span><span class="sxs-lookup"><span data-stu-id="ee72e-125">ICE01</span></span>  | <span data-ttu-id="ee72e-126">1</span><span class="sxs-lookup"><span data-stu-id="ee72e-126">1</span></span>    | <span data-ttu-id="ee72e-127">ice.dll</span><span class="sxs-lookup"><span data-stu-id="ee72e-127">ice.dll</span></span> | <span data-ttu-id="ee72e-128">ICE01</span><span class="sxs-lookup"><span data-stu-id="ee72e-128">ICE01</span></span>  |
| <span data-ttu-id="ee72e-129">ICE08</span><span class="sxs-lookup"><span data-stu-id="ee72e-129">ICE08</span></span>  | <span data-ttu-id="ee72e-130">6</span><span class="sxs-lookup"><span data-stu-id="ee72e-130">6</span></span>    | <span data-ttu-id="ee72e-131">ice.vbs</span><span class="sxs-lookup"><span data-stu-id="ee72e-131">ice.vbs</span></span> | <span data-ttu-id="ee72e-132">ICE02</span><span class="sxs-lookup"><span data-stu-id="ee72e-132">ICE02</span></span>  |



 

<span data-ttu-id="ee72e-133">\_Tabela ICESequence</span><span class="sxs-lookup"><span data-stu-id="ee72e-133">\_ICESequence Table</span></span>



| <span data-ttu-id="ee72e-134">Ação</span><span class="sxs-lookup"><span data-stu-id="ee72e-134">Action</span></span> | <span data-ttu-id="ee72e-135">Condição</span><span class="sxs-lookup"><span data-stu-id="ee72e-135">Condition</span></span> | <span data-ttu-id="ee72e-136">Sequência</span><span class="sxs-lookup"><span data-stu-id="ee72e-136">Sequence</span></span> |
|--------|-----------|----------|
| <span data-ttu-id="ee72e-137">ICE01</span><span class="sxs-lookup"><span data-stu-id="ee72e-137">ICE01</span></span>  |           | <span data-ttu-id="ee72e-138">10</span><span class="sxs-lookup"><span data-stu-id="ee72e-138">10</span></span>       |
| <span data-ttu-id="ee72e-139">ICE08</span><span class="sxs-lookup"><span data-stu-id="ee72e-139">ICE08</span></span>  |           | <span data-ttu-id="ee72e-140">20</span><span class="sxs-lookup"><span data-stu-id="ee72e-140">20</span></span>       |



 

<span data-ttu-id="ee72e-141">\_Tabela especial</span><span class="sxs-lookup"><span data-stu-id="ee72e-141">\_Special Table</span></span>

<span data-ttu-id="ee72e-142">ICE01 e ICE08 não exigem a inclusão de tabelas de processamento especiais.</span><span class="sxs-lookup"><span data-stu-id="ee72e-142">ICE01 and ICE08 do not require the inclusion of special processing tables.</span></span> <span data-ttu-id="ee72e-143">Quando o arquivo. Cub contém tabelas especiais, elas também devem ser incluídas na \_ tabela de validação.</span><span class="sxs-lookup"><span data-stu-id="ee72e-143">When the .cub file contains special tables they must also be included in the \_Validation Table.</span></span>

[<span data-ttu-id="ee72e-144">\_Tabela de validação</span><span class="sxs-lookup"><span data-stu-id="ee72e-144">\_Validation Table</span></span>](-validation-table.md)



| <span data-ttu-id="ee72e-145">Tabela</span><span class="sxs-lookup"><span data-stu-id="ee72e-145">Table</span></span>         | <span data-ttu-id="ee72e-146">Coluna</span><span class="sxs-lookup"><span data-stu-id="ee72e-146">Column</span></span>    | <span data-ttu-id="ee72e-147">Nullable</span><span class="sxs-lookup"><span data-stu-id="ee72e-147">Nullable</span></span> | <span data-ttu-id="ee72e-148">MinValue</span><span class="sxs-lookup"><span data-stu-id="ee72e-148">MinValue</span></span> | <span data-ttu-id="ee72e-149">MaxValue</span><span class="sxs-lookup"><span data-stu-id="ee72e-149">MaxValue</span></span> | <span data-ttu-id="ee72e-150">KeyTable</span><span class="sxs-lookup"><span data-stu-id="ee72e-150">KeyTable</span></span> | <span data-ttu-id="ee72e-151">KeyColumn</span><span class="sxs-lookup"><span data-stu-id="ee72e-151">KeyColumn</span></span> | <span data-ttu-id="ee72e-152">Categoria</span><span class="sxs-lookup"><span data-stu-id="ee72e-152">Category</span></span>                         | <span data-ttu-id="ee72e-153">Definir</span><span class="sxs-lookup"><span data-stu-id="ee72e-153">Set</span></span> | <span data-ttu-id="ee72e-154">Descrição</span><span class="sxs-lookup"><span data-stu-id="ee72e-154">Description</span></span> |
|---------------|-----------|----------|----------|----------|----------|-----------|----------------------------------|-----|-------------|
| <span data-ttu-id="ee72e-155">Binário</span><span class="sxs-lookup"><span data-stu-id="ee72e-155">Binary</span></span>        | <span data-ttu-id="ee72e-156">Name</span><span class="sxs-lookup"><span data-stu-id="ee72e-156">Name</span></span>      | <span data-ttu-id="ee72e-157">N</span><span class="sxs-lookup"><span data-stu-id="ee72e-157">N</span></span>        |          |          |          |           | [<span data-ttu-id="ee72e-158">Identificador</span><span class="sxs-lookup"><span data-stu-id="ee72e-158">Identifier</span></span>](identifier.md)     |     |             |
| <span data-ttu-id="ee72e-159">Binário</span><span class="sxs-lookup"><span data-stu-id="ee72e-159">Binary</span></span>        | <span data-ttu-id="ee72e-160">Dados</span><span class="sxs-lookup"><span data-stu-id="ee72e-160">Data</span></span>      | <span data-ttu-id="ee72e-161">N</span><span class="sxs-lookup"><span data-stu-id="ee72e-161">N</span></span>        |          |          |          |           | [<span data-ttu-id="ee72e-162">Binary</span><span class="sxs-lookup"><span data-stu-id="ee72e-162">Binary</span></span>](binary.md)             |     |             |
| <span data-ttu-id="ee72e-163">CustomAction</span><span class="sxs-lookup"><span data-stu-id="ee72e-163">CustomAction</span></span>  | <span data-ttu-id="ee72e-164">Ação</span><span class="sxs-lookup"><span data-stu-id="ee72e-164">Action</span></span>    | <span data-ttu-id="ee72e-165">N</span><span class="sxs-lookup"><span data-stu-id="ee72e-165">N</span></span>        |          |          |          |           | [<span data-ttu-id="ee72e-166">Identificador</span><span class="sxs-lookup"><span data-stu-id="ee72e-166">Identifier</span></span>](identifier.md)     |     |             |
| <span data-ttu-id="ee72e-167">CustomAction</span><span class="sxs-lookup"><span data-stu-id="ee72e-167">CustomAction</span></span>  | <span data-ttu-id="ee72e-168">Tipo</span><span class="sxs-lookup"><span data-stu-id="ee72e-168">Type</span></span>      | <span data-ttu-id="ee72e-169">N</span><span class="sxs-lookup"><span data-stu-id="ee72e-169">N</span></span>        |          |          |          |           | [<span data-ttu-id="ee72e-170">Inteiro</span><span class="sxs-lookup"><span data-stu-id="ee72e-170">Integer</span></span>](integer.md)           |     |             |
| <span data-ttu-id="ee72e-171">CustomAction</span><span class="sxs-lookup"><span data-stu-id="ee72e-171">CustomAction</span></span>  | <span data-ttu-id="ee72e-172">Fonte</span><span class="sxs-lookup"><span data-stu-id="ee72e-172">Source</span></span>    | <span data-ttu-id="ee72e-173">S</span><span class="sxs-lookup"><span data-stu-id="ee72e-173">Y</span></span>        |          |          |          |           | [<span data-ttu-id="ee72e-174">CustomSource</span><span class="sxs-lookup"><span data-stu-id="ee72e-174">CustomSource</span></span>](customsource.md) |     |             |
| <span data-ttu-id="ee72e-175">CustomAction</span><span class="sxs-lookup"><span data-stu-id="ee72e-175">CustomAction</span></span>  | <span data-ttu-id="ee72e-176">Destino</span><span class="sxs-lookup"><span data-stu-id="ee72e-176">Target</span></span>    | <span data-ttu-id="ee72e-177">S</span><span class="sxs-lookup"><span data-stu-id="ee72e-177">Y</span></span>        |          |          |          |           | [<span data-ttu-id="ee72e-178">Binário</span><span class="sxs-lookup"><span data-stu-id="ee72e-178">Formatted</span></span>](formatted.md)       |     |             |
| <span data-ttu-id="ee72e-179">\_ICESequence</span><span class="sxs-lookup"><span data-stu-id="ee72e-179">\_ICESequence</span></span> | <span data-ttu-id="ee72e-180">Ação</span><span class="sxs-lookup"><span data-stu-id="ee72e-180">Action</span></span>    | <span data-ttu-id="ee72e-181">N</span><span class="sxs-lookup"><span data-stu-id="ee72e-181">N</span></span>        |          |          |          |           | [<span data-ttu-id="ee72e-182">Identificador</span><span class="sxs-lookup"><span data-stu-id="ee72e-182">Identifier</span></span>](identifier.md)     |     |             |
| <span data-ttu-id="ee72e-183">\_ICESequence</span><span class="sxs-lookup"><span data-stu-id="ee72e-183">\_ICESequence</span></span> | <span data-ttu-id="ee72e-184">Condição</span><span class="sxs-lookup"><span data-stu-id="ee72e-184">Condition</span></span> | <span data-ttu-id="ee72e-185">S</span><span class="sxs-lookup"><span data-stu-id="ee72e-185">Y</span></span>        |          |          |          |           | [<span data-ttu-id="ee72e-186">Condição</span><span class="sxs-lookup"><span data-stu-id="ee72e-186">Condition</span></span>](condition.md)       |     |             |
| <span data-ttu-id="ee72e-187">\_ICESequence</span><span class="sxs-lookup"><span data-stu-id="ee72e-187">\_ICESequence</span></span> | <span data-ttu-id="ee72e-188">Sequência</span><span class="sxs-lookup"><span data-stu-id="ee72e-188">Sequence</span></span>  | <span data-ttu-id="ee72e-189">S</span><span class="sxs-lookup"><span data-stu-id="ee72e-189">Y</span></span>        |          |          |          |           | [<span data-ttu-id="ee72e-190">Inteiro</span><span class="sxs-lookup"><span data-stu-id="ee72e-190">Integer</span></span>](integer.md)           |     |             |



 

 

 



