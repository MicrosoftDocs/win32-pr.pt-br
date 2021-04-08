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
# <a name="sample-cub-file"></a><span data-ttu-id="05189-104">Arquivo. Cub de exemplo</span><span class="sxs-lookup"><span data-stu-id="05189-104">Sample .cub File</span></span>

<span data-ttu-id="05189-105">Este exemplo ilustra o layout de um arquivo. Cub contendo duas [ICES](internal-consistency-evaluators-ices.md).</span><span class="sxs-lookup"><span data-stu-id="05189-105">This sample illustrates the layout of a .cub file containing two [ICEs](internal-consistency-evaluators-ices.md).</span></span> <span data-ttu-id="05189-106">O instalador executa as ações personalizadas na sequência: ICE01 e ICE08.</span><span class="sxs-lookup"><span data-stu-id="05189-106">The installer executes the custom actions in the sequence: ICE01 and ICE08.</span></span>

<span data-ttu-id="05189-107">A ação personalizada ICE01 é um [tipo de ação personalizada 1](custom-action-type-1.md).</span><span class="sxs-lookup"><span data-stu-id="05189-107">The custom action ICE01 is a [Custom Action Type 1](custom-action-type-1.md).</span></span> <span data-ttu-id="05189-108">É um ponto de entrada para uma DLL que é armazenada como um fluxo no arquivo. cub.</span><span class="sxs-lookup"><span data-stu-id="05189-108">It is an entry point to a DLL that is stored as a stream in the .cub file.</span></span> <span data-ttu-id="05189-109">Esse fluxo é listado na tabela binária ice.dll.</span><span class="sxs-lookup"><span data-stu-id="05189-109">This stream is listed in the Binary Table ice.dll.</span></span>

<span data-ttu-id="05189-110">A ação personalizada ICE08 é um [tipo de ação personalizada 6](custom-action-type-6.md).</span><span class="sxs-lookup"><span data-stu-id="05189-110">The custom action ICE08 is a [Custom Action Type 6](custom-action-type-6.md).</span></span> <span data-ttu-id="05189-111">É um ponto de entrada para uma função no VBScript que é armazenada como um fluxo no arquivo. cub.</span><span class="sxs-lookup"><span data-stu-id="05189-111">It is an entry point to a function in VBScript that is stored as a stream in the .cub file.</span></span> <span data-ttu-id="05189-112">Esse fluxo é listado na tabela binária como ice.vbs.</span><span class="sxs-lookup"><span data-stu-id="05189-112">This stream is listed in the Binary Table as ice.vbs.</span></span>

[<span data-ttu-id="05189-113">Tabela binária</span><span class="sxs-lookup"><span data-stu-id="05189-113">Binary Table</span></span>](binary-table.md)



| <span data-ttu-id="05189-114">Nome</span><span class="sxs-lookup"><span data-stu-id="05189-114">Name</span></span>    | <span data-ttu-id="05189-115">Dados</span><span class="sxs-lookup"><span data-stu-id="05189-115">Data</span></span>                               |
|---------|------------------------------------|
| <span data-ttu-id="05189-116">ice.vbs</span><span class="sxs-lookup"><span data-stu-id="05189-116">ice.vbs</span></span> | <span data-ttu-id="05189-117">Dados binários não formatados de ice.vbs</span><span class="sxs-lookup"><span data-stu-id="05189-117">Unformatted binary data of ice.vbs</span></span> |
| <span data-ttu-id="05189-118">ice.dll</span><span class="sxs-lookup"><span data-stu-id="05189-118">ice.dll</span></span> | <span data-ttu-id="05189-119">Dados binários não formatados de ice.dll</span><span class="sxs-lookup"><span data-stu-id="05189-119">Unformatted binary data of ice.dll</span></span> |



 

[<span data-ttu-id="05189-120">Tabela CustomAction</span><span class="sxs-lookup"><span data-stu-id="05189-120">CustomAction Table</span></span>](customaction-table.md)



| <span data-ttu-id="05189-121">Ação</span><span class="sxs-lookup"><span data-stu-id="05189-121">Action</span></span> | <span data-ttu-id="05189-122">Tipo</span><span class="sxs-lookup"><span data-stu-id="05189-122">Type</span></span> | <span data-ttu-id="05189-123">Fonte</span><span class="sxs-lookup"><span data-stu-id="05189-123">Source</span></span>  | <span data-ttu-id="05189-124">Destino</span><span class="sxs-lookup"><span data-stu-id="05189-124">Target</span></span> |
|--------|------|---------|--------|
| <span data-ttu-id="05189-125">ICE01</span><span class="sxs-lookup"><span data-stu-id="05189-125">ICE01</span></span>  | <span data-ttu-id="05189-126">1</span><span class="sxs-lookup"><span data-stu-id="05189-126">1</span></span>    | <span data-ttu-id="05189-127">ice.dll</span><span class="sxs-lookup"><span data-stu-id="05189-127">ice.dll</span></span> | <span data-ttu-id="05189-128">ICE01</span><span class="sxs-lookup"><span data-stu-id="05189-128">ICE01</span></span>  |
| <span data-ttu-id="05189-129">ICE08</span><span class="sxs-lookup"><span data-stu-id="05189-129">ICE08</span></span>  | <span data-ttu-id="05189-130">6</span><span class="sxs-lookup"><span data-stu-id="05189-130">6</span></span>    | <span data-ttu-id="05189-131">ice.vbs</span><span class="sxs-lookup"><span data-stu-id="05189-131">ice.vbs</span></span> | <span data-ttu-id="05189-132">ICE02</span><span class="sxs-lookup"><span data-stu-id="05189-132">ICE02</span></span>  |



 

<span data-ttu-id="05189-133">\_Tabela ICESequence</span><span class="sxs-lookup"><span data-stu-id="05189-133">\_ICESequence Table</span></span>



| <span data-ttu-id="05189-134">Ação</span><span class="sxs-lookup"><span data-stu-id="05189-134">Action</span></span> | <span data-ttu-id="05189-135">Condição</span><span class="sxs-lookup"><span data-stu-id="05189-135">Condition</span></span> | <span data-ttu-id="05189-136">Sequência</span><span class="sxs-lookup"><span data-stu-id="05189-136">Sequence</span></span> |
|--------|-----------|----------|
| <span data-ttu-id="05189-137">ICE01</span><span class="sxs-lookup"><span data-stu-id="05189-137">ICE01</span></span>  |           | <span data-ttu-id="05189-138">10</span><span class="sxs-lookup"><span data-stu-id="05189-138">10</span></span>       |
| <span data-ttu-id="05189-139">ICE08</span><span class="sxs-lookup"><span data-stu-id="05189-139">ICE08</span></span>  |           | <span data-ttu-id="05189-140">20</span><span class="sxs-lookup"><span data-stu-id="05189-140">20</span></span>       |



 

<span data-ttu-id="05189-141">\_Tabela especial</span><span class="sxs-lookup"><span data-stu-id="05189-141">\_Special Table</span></span>

<span data-ttu-id="05189-142">ICE01 e ICE08 não exigem a inclusão de tabelas de processamento especiais.</span><span class="sxs-lookup"><span data-stu-id="05189-142">ICE01 and ICE08 do not require the inclusion of special processing tables.</span></span> <span data-ttu-id="05189-143">Quando o arquivo. Cub contém tabelas especiais, elas também devem ser incluídas na \_ tabela de validação.</span><span class="sxs-lookup"><span data-stu-id="05189-143">When the .cub file contains special tables they must also be included in the \_Validation Table.</span></span>

[<span data-ttu-id="05189-144">\_Tabela de validação</span><span class="sxs-lookup"><span data-stu-id="05189-144">\_Validation Table</span></span>](-validation-table.md)



| <span data-ttu-id="05189-145">Tabela</span><span class="sxs-lookup"><span data-stu-id="05189-145">Table</span></span>         | <span data-ttu-id="05189-146">Coluna</span><span class="sxs-lookup"><span data-stu-id="05189-146">Column</span></span>    | <span data-ttu-id="05189-147">Nullable</span><span class="sxs-lookup"><span data-stu-id="05189-147">Nullable</span></span> | <span data-ttu-id="05189-148">MinValue</span><span class="sxs-lookup"><span data-stu-id="05189-148">MinValue</span></span> | <span data-ttu-id="05189-149">MaxValue</span><span class="sxs-lookup"><span data-stu-id="05189-149">MaxValue</span></span> | <span data-ttu-id="05189-150">KeyTable</span><span class="sxs-lookup"><span data-stu-id="05189-150">KeyTable</span></span> | <span data-ttu-id="05189-151">KeyColumn</span><span class="sxs-lookup"><span data-stu-id="05189-151">KeyColumn</span></span> | <span data-ttu-id="05189-152">Categoria</span><span class="sxs-lookup"><span data-stu-id="05189-152">Category</span></span>                         | <span data-ttu-id="05189-153">Definir</span><span class="sxs-lookup"><span data-stu-id="05189-153">Set</span></span> | <span data-ttu-id="05189-154">Descrição</span><span class="sxs-lookup"><span data-stu-id="05189-154">Description</span></span> |
|---------------|-----------|----------|----------|----------|----------|-----------|----------------------------------|-----|-------------|
| <span data-ttu-id="05189-155">Binário</span><span class="sxs-lookup"><span data-stu-id="05189-155">Binary</span></span>        | <span data-ttu-id="05189-156">Nome</span><span class="sxs-lookup"><span data-stu-id="05189-156">Name</span></span>      | <span data-ttu-id="05189-157">N</span><span class="sxs-lookup"><span data-stu-id="05189-157">N</span></span>        |          |          |          |           | [<span data-ttu-id="05189-158">Identificador</span><span class="sxs-lookup"><span data-stu-id="05189-158">Identifier</span></span>](identifier.md)     |     |             |
| <span data-ttu-id="05189-159">Binário</span><span class="sxs-lookup"><span data-stu-id="05189-159">Binary</span></span>        | <span data-ttu-id="05189-160">Dados</span><span class="sxs-lookup"><span data-stu-id="05189-160">Data</span></span>      | <span data-ttu-id="05189-161">N</span><span class="sxs-lookup"><span data-stu-id="05189-161">N</span></span>        |          |          |          |           | [<span data-ttu-id="05189-162">Binary</span><span class="sxs-lookup"><span data-stu-id="05189-162">Binary</span></span>](binary.md)             |     |             |
| <span data-ttu-id="05189-163">CustomAction</span><span class="sxs-lookup"><span data-stu-id="05189-163">CustomAction</span></span>  | <span data-ttu-id="05189-164">Ação</span><span class="sxs-lookup"><span data-stu-id="05189-164">Action</span></span>    | <span data-ttu-id="05189-165">N</span><span class="sxs-lookup"><span data-stu-id="05189-165">N</span></span>        |          |          |          |           | [<span data-ttu-id="05189-166">Identificador</span><span class="sxs-lookup"><span data-stu-id="05189-166">Identifier</span></span>](identifier.md)     |     |             |
| <span data-ttu-id="05189-167">CustomAction</span><span class="sxs-lookup"><span data-stu-id="05189-167">CustomAction</span></span>  | <span data-ttu-id="05189-168">Tipo</span><span class="sxs-lookup"><span data-stu-id="05189-168">Type</span></span>      | <span data-ttu-id="05189-169">N</span><span class="sxs-lookup"><span data-stu-id="05189-169">N</span></span>        |          |          |          |           | [<span data-ttu-id="05189-170">Inteiro</span><span class="sxs-lookup"><span data-stu-id="05189-170">Integer</span></span>](integer.md)           |     |             |
| <span data-ttu-id="05189-171">CustomAction</span><span class="sxs-lookup"><span data-stu-id="05189-171">CustomAction</span></span>  | <span data-ttu-id="05189-172">Fonte</span><span class="sxs-lookup"><span data-stu-id="05189-172">Source</span></span>    | <span data-ttu-id="05189-173">S</span><span class="sxs-lookup"><span data-stu-id="05189-173">Y</span></span>        |          |          |          |           | [<span data-ttu-id="05189-174">CustomSource</span><span class="sxs-lookup"><span data-stu-id="05189-174">CustomSource</span></span>](customsource.md) |     |             |
| <span data-ttu-id="05189-175">CustomAction</span><span class="sxs-lookup"><span data-stu-id="05189-175">CustomAction</span></span>  | <span data-ttu-id="05189-176">Destino</span><span class="sxs-lookup"><span data-stu-id="05189-176">Target</span></span>    | <span data-ttu-id="05189-177">S</span><span class="sxs-lookup"><span data-stu-id="05189-177">Y</span></span>        |          |          |          |           | [<span data-ttu-id="05189-178">Binário</span><span class="sxs-lookup"><span data-stu-id="05189-178">Formatted</span></span>](formatted.md)       |     |             |
| <span data-ttu-id="05189-179">\_ICESequence</span><span class="sxs-lookup"><span data-stu-id="05189-179">\_ICESequence</span></span> | <span data-ttu-id="05189-180">Ação</span><span class="sxs-lookup"><span data-stu-id="05189-180">Action</span></span>    | <span data-ttu-id="05189-181">N</span><span class="sxs-lookup"><span data-stu-id="05189-181">N</span></span>        |          |          |          |           | [<span data-ttu-id="05189-182">Identificador</span><span class="sxs-lookup"><span data-stu-id="05189-182">Identifier</span></span>](identifier.md)     |     |             |
| <span data-ttu-id="05189-183">\_ICESequence</span><span class="sxs-lookup"><span data-stu-id="05189-183">\_ICESequence</span></span> | <span data-ttu-id="05189-184">Condição</span><span class="sxs-lookup"><span data-stu-id="05189-184">Condition</span></span> | <span data-ttu-id="05189-185">S</span><span class="sxs-lookup"><span data-stu-id="05189-185">Y</span></span>        |          |          |          |           | [<span data-ttu-id="05189-186">Condição</span><span class="sxs-lookup"><span data-stu-id="05189-186">Condition</span></span>](condition.md)       |     |             |
| <span data-ttu-id="05189-187">\_ICESequence</span><span class="sxs-lookup"><span data-stu-id="05189-187">\_ICESequence</span></span> | <span data-ttu-id="05189-188">Sequência</span><span class="sxs-lookup"><span data-stu-id="05189-188">Sequence</span></span>  | <span data-ttu-id="05189-189">S</span><span class="sxs-lookup"><span data-stu-id="05189-189">Y</span></span>        |          |          |          |           | [<span data-ttu-id="05189-190">Inteiro</span><span class="sxs-lookup"><span data-stu-id="05189-190">Integer</span></span>](integer.md)           |     |             |



 

 

 



