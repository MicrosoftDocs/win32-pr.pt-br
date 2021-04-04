---
description: Especifica uma operação para a qual o código deve ser gerado.
ms.assetid: d198197e-d146-4f1b-99df-944822e83357
title: elemento Operation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0bdd8324553e046000f467c103afd6ac0464cbc0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010810"
---
# <a name="operation-element"></a><span data-ttu-id="6f8d4-103">elemento Operation</span><span class="sxs-lookup"><span data-stu-id="6f8d4-103">operation element</span></span>

<span data-ttu-id="6f8d4-104">Especifica uma operação para a qual o código deve ser gerado.</span><span class="sxs-lookup"><span data-stu-id="6f8d4-104">Specifies an operation for which code is to be generated.</span></span>

## <a name="usage"></a><span data-ttu-id="6f8d4-105">Uso</span><span class="sxs-lookup"><span data-stu-id="6f8d4-105">Usage</span></span>

``` syntax
<operation/>
```

## <a name="attributes"></a><span data-ttu-id="6f8d4-106">Atributos</span><span class="sxs-lookup"><span data-stu-id="6f8d4-106">Attributes</span></span>

<span data-ttu-id="6f8d4-107">Não há atributos.</span><span class="sxs-lookup"><span data-stu-id="6f8d4-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="6f8d4-108">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="6f8d4-108">Child elements</span></span>

<span data-ttu-id="6f8d4-109">Não há elementos filho.</span><span class="sxs-lookup"><span data-stu-id="6f8d4-109">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="6f8d4-110">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="6f8d4-110">Parent elements</span></span>



| <span data-ttu-id="6f8d4-111">Elemento</span><span class="sxs-lookup"><span data-stu-id="6f8d4-111">Element</span></span>                                                                                                 | <span data-ttu-id="6f8d4-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="6f8d4-112">Description</span></span>                                                                                                                                   |
|---------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6f8d4-113">**functionDeclarations**</span><span class="sxs-lookup"><span data-stu-id="6f8d4-113">**functionDeclarations**</span></span>](functiondeclarations.md)<br/>                                         | <span data-ttu-id="6f8d4-114">Gera declarações de implementação para funções de proxy para operações de tipo de porta.</span><span class="sxs-lookup"><span data-stu-id="6f8d4-114">Generates implementation declarations for proxy functions for port type operations.</span></span><br/> <br/>                                    |
| [<span data-ttu-id="6f8d4-115">**idlFunctionDeclarations**</span><span class="sxs-lookup"><span data-stu-id="6f8d4-115">**idlFunctionDeclarations**</span></span>](idlfunctiondeclarations.md)<br/>                                   | <span data-ttu-id="6f8d4-116">Gera declarações IDL para funções de proxy para operações de tipo de porta.</span><span class="sxs-lookup"><span data-stu-id="6f8d4-116">Generates IDL declarations for proxy functions for port type operations.</span></span><br/> <br/>                                               |
| [<span data-ttu-id="6f8d4-117">**messageStructureDefinitions**</span><span class="sxs-lookup"><span data-stu-id="6f8d4-117">**messageStructureDefinitions**</span></span>](messagestructuredefinitions.md)<br/>                           | <span data-ttu-id="6f8d4-118">Gera definições de estrutura C para tipos de mensagem.</span><span class="sxs-lookup"><span data-stu-id="6f8d4-118">Generates C structure definitions for message types.</span></span><br/> <br/>                                                                   |
| [<span data-ttu-id="6f8d4-119">**messageTypeDeclarations**</span><span class="sxs-lookup"><span data-stu-id="6f8d4-119">**messageTypeDeclarations**</span></span>](messagetypedeclarations.md)<br/>                                   | <span data-ttu-id="6f8d4-120">Gera declarações de constante C para tabelas de esquema XML para tipos de mensagem.</span><span class="sxs-lookup"><span data-stu-id="6f8d4-120">Generates C constant declarations for XML schema tables for message types.</span></span><br/> <br/>                                             |
| [<span data-ttu-id="6f8d4-121">**messageTypeDefinitions**</span><span class="sxs-lookup"><span data-stu-id="6f8d4-121">**messageTypeDefinitions**</span></span>](messagetypedefinitions.md)<br/>                                     | <span data-ttu-id="6f8d4-122">Gera constantes C para tabelas de esquema XML para tipos de mensagem.</span><span class="sxs-lookup"><span data-stu-id="6f8d4-122">Generates C constants for XML schema tables for message types.</span></span><br/> <br/>                                                         |
| [<span data-ttu-id="6f8d4-123">**portTypeDeclarations**</span><span class="sxs-lookup"><span data-stu-id="6f8d4-123">**portTypeDeclarations**</span></span>](porttypedeclarations.md)<br/>                                         | <span data-ttu-id="6f8d4-124">Gera declarações de constante C para tipos de porta.</span><span class="sxs-lookup"><span data-stu-id="6f8d4-124">Generates C constant declarations for port types.</span></span><br/> <br/>                                                                      |
| [<span data-ttu-id="6f8d4-125">**portTypeDefinitions**</span><span class="sxs-lookup"><span data-stu-id="6f8d4-125">**portTypeDefinitions**</span></span>](porttypedefinitions.md)<br/>                                           | <span data-ttu-id="6f8d4-126">Gera constantes C para tipos de porta.</span><span class="sxs-lookup"><span data-stu-id="6f8d4-126">Generates C constants for port types.</span></span><br/> <br/>                                                                                  |
| [<span data-ttu-id="6f8d4-127">**proxyFunctionImplementations**</span><span class="sxs-lookup"><span data-stu-id="6f8d4-127">**proxyFunctionImplementations**</span></span>](proxyfunctionimplementations.md)<br/>                         | <span data-ttu-id="6f8d4-128">Gera implementações para funções de proxy para operações de tipo de porta.</span><span class="sxs-lookup"><span data-stu-id="6f8d4-128">Generates implementations for proxy functions for port type operations.</span></span><br/> <br/>                                                |
| [<span data-ttu-id="6f8d4-129">**stubDeclarations**</span><span class="sxs-lookup"><span data-stu-id="6f8d4-129">**stubDeclarations**</span></span>](stubdeclarations.md)<br/>                                                 | <span data-ttu-id="6f8d4-130">Gera declarações para funções de stub para operações de tipo de porta.</span><span class="sxs-lookup"><span data-stu-id="6f8d4-130">Generates declarations for stub functions for port type operations.</span></span><br/> <br/>                                                    |
| [<span data-ttu-id="6f8d4-131">**stubDefinitions**</span><span class="sxs-lookup"><span data-stu-id="6f8d4-131">**stubDefinitions**</span></span>](stubdefinitions.md)<br/>                                                   | <span data-ttu-id="6f8d4-132">Gera implementações para funções de stub para operações de tipo de porta.</span><span class="sxs-lookup"><span data-stu-id="6f8d4-132">Generates implementations for stub functions for port type operations.</span></span><br/> <br/>                                                 |
| [<span data-ttu-id="6f8d4-133">**subscriptionFunctionDeclarations**</span><span class="sxs-lookup"><span data-stu-id="6f8d4-133">**subscriptionFunctionDeclarations**</span></span>](subscriptionfunctiondeclarations.md)<br/>                 | <span data-ttu-id="6f8d4-134">Gera declarações de implementação para funções de proxy de assinatura/cancelamento de assinatura para operações de notificação de tipo de porta.</span><span class="sxs-lookup"><span data-stu-id="6f8d4-134">Generates implementation declarations for subscribe/unsubscribe proxy functions for port type notification operations.</span></span><br/> <br/> |
| [<span data-ttu-id="6f8d4-135">**subscriptionIdlFunctionDeclarations**</span><span class="sxs-lookup"><span data-stu-id="6f8d4-135">**subscriptionIdlFunctionDeclarations**</span></span>](subscriptionidlfunctiondeclarations.md)<br/>           | <span data-ttu-id="6f8d4-136">Gera declarações IDL para funções de proxy de assinatura/cancelamento de assinatura para operações de notificação de tipo de porta.</span><span class="sxs-lookup"><span data-stu-id="6f8d4-136">Generates IDL declarations for subscribe/unsubscribe proxy functions for port type notification operations.</span></span><br/> <br/>            |
| [<span data-ttu-id="6f8d4-137">**subscriptionProxyFunctionImplementations**</span><span class="sxs-lookup"><span data-stu-id="6f8d4-137">**subscriptionProxyFunctionImplementations**</span></span>](subscriptionproxyfunctionimplementations.md)<br/> | <span data-ttu-id="6f8d4-138">Gera implementações para funções de proxy de assinatura/cancelamento de assinatura para operações de notificação de tipo de porta.</span><span class="sxs-lookup"><span data-stu-id="6f8d4-138">Generates implementations for subscribe/unsubscribe proxy functions for port type notification operations.</span></span><br/> <br/>             |



## <a name="remarks"></a><span data-ttu-id="6f8d4-139">Comentários</span><span class="sxs-lookup"><span data-stu-id="6f8d4-139">Remarks</span></span>

<span data-ttu-id="6f8d4-140">Qualquer quantidade de operações pode ser especificada.</span><span class="sxs-lookup"><span data-stu-id="6f8d4-140">Any number of operations may be specified.</span></span> <span data-ttu-id="6f8d4-141">Se nenhuma operação for especificada, o código será gerado para todas as operações em todos os tipos de porta relevantes.</span><span class="sxs-lookup"><span data-stu-id="6f8d4-141">If no operations are specified, code is generated for all operations in all the relevant port types.</span></span> <span data-ttu-id="6f8d4-142">O uso do elemento **Operation** limitará os métodos gerados àqueles contidos na operação.</span><span class="sxs-lookup"><span data-stu-id="6f8d4-142">Using the **operation** element will limit the methods generated to those contained in the operation.</span></span>

<span data-ttu-id="6f8d4-143">Por exemplo, uma impressora dá suporte a essas operações entre outras:</span><span class="sxs-lookup"><span data-stu-id="6f8d4-143">For example, a printer supports these operations among others:</span></span>

-   <span data-ttu-id="6f8d4-144">**PrintJobByPost**</span><span class="sxs-lookup"><span data-stu-id="6f8d4-144">**PrintJobByPost**</span></span>
-   <span data-ttu-id="6f8d4-145">**PrintJobByReference**</span><span class="sxs-lookup"><span data-stu-id="6f8d4-145">**PrintJobByReference**</span></span>
-   <span data-ttu-id="6f8d4-146">**CancelJob**</span><span class="sxs-lookup"><span data-stu-id="6f8d4-146">**CancelJob**</span></span>
-   <span data-ttu-id="6f8d4-147">**GetJobElements**</span><span class="sxs-lookup"><span data-stu-id="6f8d4-147">**GetJobElements**</span></span>
-   <span data-ttu-id="6f8d4-148">**GetActiveJobs**</span><span class="sxs-lookup"><span data-stu-id="6f8d4-148">**GetActiveJobs**</span></span>
-   <span data-ttu-id="6f8d4-149">**GetJobHistory**</span><span class="sxs-lookup"><span data-stu-id="6f8d4-149">**GetJobHistory**</span></span>
-   <span data-ttu-id="6f8d4-150">**SubscribeToPrinterConfigChange**</span><span class="sxs-lookup"><span data-stu-id="6f8d4-150">**SubscribeToPrinterConfigChange**</span></span>
-   <span data-ttu-id="6f8d4-151">**UnsubscribeToPrinterConfigChange**</span><span class="sxs-lookup"><span data-stu-id="6f8d4-151">**UnsubscribeToPrinterConfigChange**</span></span>

<span data-ttu-id="6f8d4-152">No entanto, para incluir apenas os métodos relacionados às operações **PrintJobByPost** e **GetJobElements** , o script de geração de código usaria os elementos [**idlFunctionDeclarations**](idlfunctiondeclarations.md) da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="6f8d4-152">However, to include only the methods related to the **PrintJobByPost** and **GetJobElements** operations, the code generation script would use the [**idlFunctionDeclarations**](idlfunctiondeclarations.md) elements as follows:</span></span>

``` syntax
<idlFunctionDeclarations>
    <operation>PrintJobByPost</operation>
    <operation>GetJobElements></operation>
</idlFunctionDeclarations>
```

<span data-ttu-id="6f8d4-153">Isso gera declarações de função IDL para todos os métodos associados às duas operações (por exemplo, **BeginPrintJobByPost**, **EndPrintJobByPost**, **BeginGetJobElements** e **EndGetJobElements**).</span><span class="sxs-lookup"><span data-stu-id="6f8d4-153">This generates idl function declarations for all methods associated with the two operations (for example, **BeginPrintJobByPost**, **EndPrintJobByPost**, **BeginGetJobElements** and **EndGetJobElements**).</span></span>

## <a name="element-information"></a><span data-ttu-id="6f8d4-154">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="6f8d4-154">Element information</span></span>



|                                     |               |
|-------------------------------------|---------------|
| <span data-ttu-id="6f8d4-155">Sistema mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6f8d4-155">Minimum supported system</span></span><br/> | <span data-ttu-id="6f8d4-156">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6f8d4-156">Windows Vista</span></span> |
| <span data-ttu-id="6f8d4-157">Pode estar vazio</span><span class="sxs-lookup"><span data-stu-id="6f8d4-157">Can be empty</span></span>                        | <span data-ttu-id="6f8d4-158">Sim</span><span class="sxs-lookup"><span data-stu-id="6f8d4-158">Yes</span></span>           |



 

 




