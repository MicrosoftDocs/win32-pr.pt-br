---
description: ICE23 valida a ordem de tabulação de controle para cada caixa de diálogo.
ms.assetid: d425f8c6-4615-439d-8194-3a0325eb3cc3
title: ICE23
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c1823a70e50d7dd3c42c2e90d6a2d0f11f2fa5b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105811843"
---
# <a name="ice23"></a><span data-ttu-id="d0ac8-103">ICE23</span><span class="sxs-lookup"><span data-stu-id="d0ac8-103">ICE23</span></span>

<span data-ttu-id="d0ac8-104">ICE23 valida a ordem de tabulação de controle para cada caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="d0ac8-104">ICE23 validates the control tab order for each dialog box.</span></span>

<span data-ttu-id="d0ac8-105">ICE23 valida o seguinte na tabela de [diálogo](dialog-table.md) e na [tabela de controle](control-table.md):</span><span class="sxs-lookup"><span data-stu-id="d0ac8-105">ICE23 validates the following in the [Dialog table](dialog-table.md) and [Control table](control-table.md):</span></span>

-   <span data-ttu-id="d0ac8-106">Cada registro na tabela de diálogo especifica um controle na \_ primeira coluna de controle que existe na caixa de diálogo especificada pela coluna de caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="d0ac8-106">That every record in the Dialog table specifies a control in the Control\_First column that exists in the dialog box specified by the Dialog column.</span></span>
-   <span data-ttu-id="d0ac8-107">Cada registro na tabela de controle Especifica um controle na \_ próxima coluna de controle que está na mesma caixa de diálogo que o controle listado na coluna de controle, ou \_ o controle a seguir contém o valor nulo.</span><span class="sxs-lookup"><span data-stu-id="d0ac8-107">That every record in the Control table specifies a control in the Control\_Next column that is on the same dialog as the control listed in the Control column, or Control\_Next contains the Null value.</span></span>
-   <span data-ttu-id="d0ac8-108">Que seguir o controle \_ próximo entradas do controle para o controle na tabela de controle faz um loop único, fechado, que retorna ao controle inicial.</span><span class="sxs-lookup"><span data-stu-id="d0ac8-108">That following the Control\_Next entries from control to control in the Control table makes a single, closed, loop that comes back to the initial control.</span></span> <span data-ttu-id="d0ac8-109">Nem todo controle precisa estar no loop, mas o loop deve passar por cada controle que tenha uma entrada na próxima coluna de controle \_ .</span><span class="sxs-lookup"><span data-stu-id="d0ac8-109">Not every control needs to be in the loop, but the loop must pass through every control that has an entry in the Control\_Next column.</span></span>

## <a name="result"></a><span data-ttu-id="d0ac8-110">Resultado</span><span class="sxs-lookup"><span data-stu-id="d0ac8-110">Result</span></span>

<span data-ttu-id="d0ac8-111">ICE23 posta uma mensagem de erro se a ordem de tabulação dos controles não formar um loop fechado único na caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="d0ac8-111">ICE23 posts an error message if the tab order of controls does not form a single closed loop in the dialog box.</span></span>

## <a name="example"></a><span data-ttu-id="d0ac8-112">Exemplo</span><span class="sxs-lookup"><span data-stu-id="d0ac8-112">Example</span></span>

<span data-ttu-id="d0ac8-113">ICE23 postaria as seguintes mensagens de erro para o exemplo mostrado.</span><span class="sxs-lookup"><span data-stu-id="d0ac8-113">ICE23 would post the following error messages for the example shown.</span></span>

-   <span data-ttu-id="d0ac8-114">Dialog1 não tem controle \_ primeiro.</span><span class="sxs-lookup"><span data-stu-id="d0ac8-114">Dialog1 has no Control\_First.</span></span>
-   <span data-ttu-id="d0ac8-115">O controle \_ primeiro da caixa de diálogo Dialog2 refere-se a um ControlX de controle inexistente.</span><span class="sxs-lookup"><span data-stu-id="d0ac8-115">Control\_First of dialog Dialog2 refers to nonexistent control ControlX.</span></span>
-   <span data-ttu-id="d0ac8-116">Dialog3 tem uma ordem de tabulação de inatividade no controle ControlB.</span><span class="sxs-lookup"><span data-stu-id="d0ac8-116">Dialog3 has dead-end tab order at control ControlB.</span></span>
-   <span data-ttu-id="d0ac8-117">Dialog4 tem ordem de tabulação malformada no controle ControlC</span><span class="sxs-lookup"><span data-stu-id="d0ac8-117">Dialog4 has malformed tab order at control ControlC</span></span>
-   <span data-ttu-id="d0ac8-118">Dialog5 tem uma ordem de tabulação malformada no controle ControlC.</span><span class="sxs-lookup"><span data-stu-id="d0ac8-118">Dialog5 has malformed tab order at control ControlC.</span></span>
-   <span data-ttu-id="d0ac8-119">Controle o \_ próximo do controle Dialog6. ControlC vincula-se a um controle desconhecido.</span><span class="sxs-lookup"><span data-stu-id="d0ac8-119">Control\_Next of control Dialog6.ControlC links to unknown control.</span></span>

<span data-ttu-id="d0ac8-120">[Tabela de diálogo](dialog-table.md) (parcial)</span><span class="sxs-lookup"><span data-stu-id="d0ac8-120">[Dialog Table](dialog-table.md) (partial)</span></span>



| <span data-ttu-id="d0ac8-121">caixa de diálogo</span><span class="sxs-lookup"><span data-stu-id="d0ac8-121">Dialog</span></span>  | <span data-ttu-id="d0ac8-122">Controlar \_ primeiro</span><span class="sxs-lookup"><span data-stu-id="d0ac8-122">Control\_First</span></span> |
|---------|----------------|
| <span data-ttu-id="d0ac8-123">Dialog1</span><span class="sxs-lookup"><span data-stu-id="d0ac8-123">Dialog1</span></span> |                |
| <span data-ttu-id="d0ac8-124">Dialog2</span><span class="sxs-lookup"><span data-stu-id="d0ac8-124">Dialog2</span></span> | <span data-ttu-id="d0ac8-125">ControlX</span><span class="sxs-lookup"><span data-stu-id="d0ac8-125">ControlX</span></span>       |
| <span data-ttu-id="d0ac8-126">Dialog3</span><span class="sxs-lookup"><span data-stu-id="d0ac8-126">Dialog3</span></span> | <span data-ttu-id="d0ac8-127">ControlA</span><span class="sxs-lookup"><span data-stu-id="d0ac8-127">ControlA</span></span>       |
| <span data-ttu-id="d0ac8-128">Dialog4</span><span class="sxs-lookup"><span data-stu-id="d0ac8-128">Dialog4</span></span> | <span data-ttu-id="d0ac8-129">ControlA</span><span class="sxs-lookup"><span data-stu-id="d0ac8-129">ControlA</span></span>       |
| <span data-ttu-id="d0ac8-130">Dialog5</span><span class="sxs-lookup"><span data-stu-id="d0ac8-130">Dialog5</span></span> | <span data-ttu-id="d0ac8-131">ControlA</span><span class="sxs-lookup"><span data-stu-id="d0ac8-131">ControlA</span></span>       |



 

<span data-ttu-id="d0ac8-132">[Tabela de controle](control-table.md) (parcial)</span><span class="sxs-lookup"><span data-stu-id="d0ac8-132">[Control Table](control-table.md) (partial)</span></span>



| <span data-ttu-id="d0ac8-133">caixa de diálogo</span><span class="sxs-lookup"><span data-stu-id="d0ac8-133">Dialog</span></span>  | <span data-ttu-id="d0ac8-134">Control</span><span class="sxs-lookup"><span data-stu-id="d0ac8-134">Control</span></span>  | <span data-ttu-id="d0ac8-135">\_Próximo controle</span><span class="sxs-lookup"><span data-stu-id="d0ac8-135">Control\_Next</span></span> |
|---------|----------|---------------|
| <span data-ttu-id="d0ac8-136">Dialog1</span><span class="sxs-lookup"><span data-stu-id="d0ac8-136">Dialog1</span></span> | <span data-ttu-id="d0ac8-137">ControlA</span><span class="sxs-lookup"><span data-stu-id="d0ac8-137">ControlA</span></span> |               |
| <span data-ttu-id="d0ac8-138">Dialog1</span><span class="sxs-lookup"><span data-stu-id="d0ac8-138">Dialog1</span></span> | <span data-ttu-id="d0ac8-139">ControlB</span><span class="sxs-lookup"><span data-stu-id="d0ac8-139">ControlB</span></span> | <span data-ttu-id="d0ac8-140">ControlA</span><span class="sxs-lookup"><span data-stu-id="d0ac8-140">ControlA</span></span>      |
| <span data-ttu-id="d0ac8-141">Dialog2</span><span class="sxs-lookup"><span data-stu-id="d0ac8-141">Dialog2</span></span> | <span data-ttu-id="d0ac8-142">ControlA</span><span class="sxs-lookup"><span data-stu-id="d0ac8-142">ControlA</span></span> | <span data-ttu-id="d0ac8-143">ControlB</span><span class="sxs-lookup"><span data-stu-id="d0ac8-143">ControlB</span></span>      |
| <span data-ttu-id="d0ac8-144">Dialog2</span><span class="sxs-lookup"><span data-stu-id="d0ac8-144">Dialog2</span></span> | <span data-ttu-id="d0ac8-145">ControlB</span><span class="sxs-lookup"><span data-stu-id="d0ac8-145">ControlB</span></span> | <span data-ttu-id="d0ac8-146">ControlA</span><span class="sxs-lookup"><span data-stu-id="d0ac8-146">ControlA</span></span>      |
| <span data-ttu-id="d0ac8-147">Dialog3</span><span class="sxs-lookup"><span data-stu-id="d0ac8-147">Dialog3</span></span> | <span data-ttu-id="d0ac8-148">ControlA</span><span class="sxs-lookup"><span data-stu-id="d0ac8-148">ControlA</span></span> | <span data-ttu-id="d0ac8-149">ControlB</span><span class="sxs-lookup"><span data-stu-id="d0ac8-149">ControlB</span></span>      |
| <span data-ttu-id="d0ac8-150">Dialog3</span><span class="sxs-lookup"><span data-stu-id="d0ac8-150">Dialog3</span></span> | <span data-ttu-id="d0ac8-151">ControlB</span><span class="sxs-lookup"><span data-stu-id="d0ac8-151">ControlB</span></span> |               |
| <span data-ttu-id="d0ac8-152">Dialog4</span><span class="sxs-lookup"><span data-stu-id="d0ac8-152">Dialog4</span></span> | <span data-ttu-id="d0ac8-153">ControlA</span><span class="sxs-lookup"><span data-stu-id="d0ac8-153">ControlA</span></span> | <span data-ttu-id="d0ac8-154">ControlB</span><span class="sxs-lookup"><span data-stu-id="d0ac8-154">ControlB</span></span>      |
| <span data-ttu-id="d0ac8-155">Dialog4</span><span class="sxs-lookup"><span data-stu-id="d0ac8-155">Dialog4</span></span> | <span data-ttu-id="d0ac8-156">ControlB</span><span class="sxs-lookup"><span data-stu-id="d0ac8-156">ControlB</span></span> | <span data-ttu-id="d0ac8-157">ControlC</span><span class="sxs-lookup"><span data-stu-id="d0ac8-157">ControlC</span></span>      |
| <span data-ttu-id="d0ac8-158">Dialog4</span><span class="sxs-lookup"><span data-stu-id="d0ac8-158">Dialog4</span></span> | <span data-ttu-id="d0ac8-159">ControlC</span><span class="sxs-lookup"><span data-stu-id="d0ac8-159">ControlC</span></span> | <span data-ttu-id="d0ac8-160">ControlB</span><span class="sxs-lookup"><span data-stu-id="d0ac8-160">ControlB</span></span>      |
| <span data-ttu-id="d0ac8-161">Dialog5</span><span class="sxs-lookup"><span data-stu-id="d0ac8-161">Dialog5</span></span> | <span data-ttu-id="d0ac8-162">ControlA</span><span class="sxs-lookup"><span data-stu-id="d0ac8-162">ControlA</span></span> | <span data-ttu-id="d0ac8-163">ControlB</span><span class="sxs-lookup"><span data-stu-id="d0ac8-163">ControlB</span></span>      |
| <span data-ttu-id="d0ac8-164">Dialog5</span><span class="sxs-lookup"><span data-stu-id="d0ac8-164">Dialog5</span></span> | <span data-ttu-id="d0ac8-165">ControlB</span><span class="sxs-lookup"><span data-stu-id="d0ac8-165">ControlB</span></span> | <span data-ttu-id="d0ac8-166">ControlC</span><span class="sxs-lookup"><span data-stu-id="d0ac8-166">ControlC</span></span>      |
| <span data-ttu-id="d0ac8-167">Dialog5</span><span class="sxs-lookup"><span data-stu-id="d0ac8-167">Dialog5</span></span> | <span data-ttu-id="d0ac8-168">ControlC</span><span class="sxs-lookup"><span data-stu-id="d0ac8-168">ControlC</span></span> | <span data-ttu-id="d0ac8-169">ControlA</span><span class="sxs-lookup"><span data-stu-id="d0ac8-169">ControlA</span></span>      |
| <span data-ttu-id="d0ac8-170">Dialog5</span><span class="sxs-lookup"><span data-stu-id="d0ac8-170">Dialog5</span></span> | <span data-ttu-id="d0ac8-171">Controle</span><span class="sxs-lookup"><span data-stu-id="d0ac8-171">ControlD</span></span> | <span data-ttu-id="d0ac8-172">ControlA</span><span class="sxs-lookup"><span data-stu-id="d0ac8-172">ControlA</span></span>      |
| <span data-ttu-id="d0ac8-173">Dialog6</span><span class="sxs-lookup"><span data-stu-id="d0ac8-173">Dialog6</span></span> | <span data-ttu-id="d0ac8-174">ControlA</span><span class="sxs-lookup"><span data-stu-id="d0ac8-174">ControlA</span></span> | <span data-ttu-id="d0ac8-175">ControlB</span><span class="sxs-lookup"><span data-stu-id="d0ac8-175">ControlB</span></span>      |
| <span data-ttu-id="d0ac8-176">Dialog6</span><span class="sxs-lookup"><span data-stu-id="d0ac8-176">Dialog6</span></span> | <span data-ttu-id="d0ac8-177">ControlB</span><span class="sxs-lookup"><span data-stu-id="d0ac8-177">ControlB</span></span> | <span data-ttu-id="d0ac8-178">ControlC</span><span class="sxs-lookup"><span data-stu-id="d0ac8-178">ControlC</span></span>      |
| <span data-ttu-id="d0ac8-179">Dialog6</span><span class="sxs-lookup"><span data-stu-id="d0ac8-179">Dialog6</span></span> | <span data-ttu-id="d0ac8-180">ControlC</span><span class="sxs-lookup"><span data-stu-id="d0ac8-180">ControlC</span></span> | <span data-ttu-id="d0ac8-181">ControlX</span><span class="sxs-lookup"><span data-stu-id="d0ac8-181">ControlX</span></span>      |
| <span data-ttu-id="d0ac8-182">Dialog6</span><span class="sxs-lookup"><span data-stu-id="d0ac8-182">Dialog6</span></span> | <span data-ttu-id="d0ac8-183">Controle</span><span class="sxs-lookup"><span data-stu-id="d0ac8-183">ControlD</span></span> | <span data-ttu-id="d0ac8-184">ControlA</span><span class="sxs-lookup"><span data-stu-id="d0ac8-184">ControlA</span></span>      |



 

<span data-ttu-id="d0ac8-185">Para corrigir esses erros, observe o seguinte nas tabelas acima e faça as alterações indicadas.</span><span class="sxs-lookup"><span data-stu-id="d0ac8-185">To fix these errors note the following in the above tables and make the indicated changes.</span></span>

<span data-ttu-id="d0ac8-186">Nem todas as linhas na tabela de diálogo têm um controle especificado na \_ primeira coluna do controle.</span><span class="sxs-lookup"><span data-stu-id="d0ac8-186">Not every row in the Dialog table has a control specified in the Control\_First column.</span></span> <span data-ttu-id="d0ac8-187">Altere a \_ primeira coluna Control do registro Dialog1 na tabela Dialog para um controle que exista em Dialog1.</span><span class="sxs-lookup"><span data-stu-id="d0ac8-187">Change the Control\_First column of the Dialog1 record in the Dialog table to a control that exists in Dialog1.</span></span>

<span data-ttu-id="d0ac8-188">Nem toda linha na tabela de diálogo tem um controle especificado na \_ primeira coluna de controle que existe na caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="d0ac8-188">Not every row in the Dialog table has a control specified in the Control\_First column that exists on the dialog box.</span></span> <span data-ttu-id="d0ac8-189">Altere a \_ primeira coluna do controle Dialog2 para um controle que exista em Dialog2.</span><span class="sxs-lookup"><span data-stu-id="d0ac8-189">Change the Control\_First column of the Dialog2 to a control that exists in Dialog2.</span></span>

<span data-ttu-id="d0ac8-190">Seguindo o controle \_ próximo entradas na tabela de controle do controle para o controle não faz um loop fechado em todos os casos.</span><span class="sxs-lookup"><span data-stu-id="d0ac8-190">Following the Control\_Next entries in the Control table from control to control does not make a closed loop in every case.</span></span> <span data-ttu-id="d0ac8-191">Altere a \_ próxima coluna do controle para ControlB em Dialog3 para controla.</span><span class="sxs-lookup"><span data-stu-id="d0ac8-191">Change the Control\_Next column for ControlB in Dialog3 to ControlA.</span></span>

<span data-ttu-id="d0ac8-192">Após o controle, \_ as próximas entradas na tabela de controle do controle ao controle não retornam ao controle inicial em todos os casos.</span><span class="sxs-lookup"><span data-stu-id="d0ac8-192">Following the Control\_Next entries in the Control table from control to control does not lead back to the initial control in every case.</span></span> <span data-ttu-id="d0ac8-193">Altere a \_ próxima coluna do controle para ControlC em Dialog4 para fazer referência a controla.</span><span class="sxs-lookup"><span data-stu-id="d0ac8-193">Change the Control\_Next column for ControlC in Dialog4 to refer to ControlA.</span></span>

<span data-ttu-id="d0ac8-194">Após o controle, \_ as próximas entradas na tabela de controle do controle ao controle não passam por todos os controles na caixa de diálogo com uma entrada na \_ próxima coluna do controle.</span><span class="sxs-lookup"><span data-stu-id="d0ac8-194">Following the Control\_Next entries in the Control table from control to control does not pass through every control in the dialog box having an entry in the Control\_Next column.</span></span> <span data-ttu-id="d0ac8-195">Altere a \_ próxima coluna do controle para ControlC em Dialog5 para controle.</span><span class="sxs-lookup"><span data-stu-id="d0ac8-195">Change the Control\_Next column for ControlC in Dialog5 to ControlD.</span></span>

<span data-ttu-id="d0ac8-196">\_O controle Next não se refere a um controle válido que está na mesma caixa de diálogo que o controle listado na coluna Control.</span><span class="sxs-lookup"><span data-stu-id="d0ac8-196">Control\_Next does not refer to a valid control that is in the same dialog as the control listed in the Control column.</span></span> <span data-ttu-id="d0ac8-197">Altere a \_ próxima coluna do controle para ControlC em Dialog6 para referir-se ao controle.</span><span class="sxs-lookup"><span data-stu-id="d0ac8-197">Change the Control\_Next column for ControlC in Dialog6 to refer to ControlD.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d0ac8-198">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="d0ac8-198">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d0ac8-199">Referência de ICE</span><span class="sxs-lookup"><span data-stu-id="d0ac8-199">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



