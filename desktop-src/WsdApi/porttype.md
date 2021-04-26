---
description: Especifica o tipo de porta para o qual o código deve ser gerado.
ms.assetid: 8a7762ae-2e39-46e1-b49f-09cae1af9b0d
title: elemento portType
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a98f02fc5a18e330bb5617b52563adc79a039831
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107996533"
---
# <a name="porttype-element"></a><span data-ttu-id="04c2d-103">elemento portType</span><span class="sxs-lookup"><span data-stu-id="04c2d-103">portType element</span></span>

<span data-ttu-id="04c2d-104">Especifica o tipo de porta para o qual o código deve ser gerado.</span><span class="sxs-lookup"><span data-stu-id="04c2d-104">Specifies the port type for which code is to be generated.</span></span>

## <a name="usage"></a><span data-ttu-id="04c2d-105">Uso</span><span class="sxs-lookup"><span data-stu-id="04c2d-105">Usage</span></span>

``` syntax
<portType/>
```

## <a name="attributes"></a><span data-ttu-id="04c2d-106">Atributos</span><span class="sxs-lookup"><span data-stu-id="04c2d-106">Attributes</span></span>

<span data-ttu-id="04c2d-107">Não há atributos.</span><span class="sxs-lookup"><span data-stu-id="04c2d-107">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="04c2d-108">Elementos filho</span><span class="sxs-lookup"><span data-stu-id="04c2d-108">Child elements</span></span>

<span data-ttu-id="04c2d-109">Não há elementos filho.</span><span class="sxs-lookup"><span data-stu-id="04c2d-109">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="04c2d-110">Elementos pai</span><span class="sxs-lookup"><span data-stu-id="04c2d-110">Parent elements</span></span>



| <span data-ttu-id="04c2d-111">Elemento</span><span class="sxs-lookup"><span data-stu-id="04c2d-111">Element</span></span>                                                                                                 | <span data-ttu-id="04c2d-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="04c2d-112">Description</span></span>                                                                                                                                   |
|---------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="04c2d-113">**functionDeclarations**</span><span class="sxs-lookup"><span data-stu-id="04c2d-113">**functionDeclarations**</span></span>](functiondeclarations.md)<br/>                                         | <span data-ttu-id="04c2d-114">Gera declarações de implementação para funções de proxy para operações de tipo de porta.</span><span class="sxs-lookup"><span data-stu-id="04c2d-114">Generates implementation declarations for proxy functions for port type operations.</span></span><br/> <br/>                                    |
| [<span data-ttu-id="04c2d-115">**idlFunctionDeclarations**</span><span class="sxs-lookup"><span data-stu-id="04c2d-115">**idlFunctionDeclarations**</span></span>](idlfunctiondeclarations.md)<br/>                                   | <span data-ttu-id="04c2d-116">Gera declarações IDL para funções de proxy para operações de tipo de porta.</span><span class="sxs-lookup"><span data-stu-id="04c2d-116">Generates IDL declarations for proxy functions for port type operations.</span></span><br/> <br/>                                               |
| [<span data-ttu-id="04c2d-117">**messageStructureDefinitions**</span><span class="sxs-lookup"><span data-stu-id="04c2d-117">**messageStructureDefinitions**</span></span>](messagestructuredefinitions.md)<br/>                           | <span data-ttu-id="04c2d-118">Gera definições de estrutura C para tipos de mensagem.</span><span class="sxs-lookup"><span data-stu-id="04c2d-118">Generates C structure definitions for message types.</span></span><br/> <br/>                                                                   |
| [<span data-ttu-id="04c2d-119">**messageTypeDeclarations**</span><span class="sxs-lookup"><span data-stu-id="04c2d-119">**messageTypeDeclarations**</span></span>](messagetypedeclarations.md)<br/>                                   | <span data-ttu-id="04c2d-120">Gera declarações de constante C para tabelas de esquema XML para tipos de mensagem.</span><span class="sxs-lookup"><span data-stu-id="04c2d-120">Generates C constant declarations for XML schema tables for message types.</span></span><br/> <br/>                                             |
| [<span data-ttu-id="04c2d-121">**messageTypeDefinitions**</span><span class="sxs-lookup"><span data-stu-id="04c2d-121">**messageTypeDefinitions**</span></span>](messagetypedefinitions.md)<br/>                                     | <span data-ttu-id="04c2d-122">Gera constantes C para tabelas de esquema XML para tipos de mensagem.</span><span class="sxs-lookup"><span data-stu-id="04c2d-122">Generates C constants for XML schema tables for message types.</span></span><br/> <br/>                                                         |
| [<span data-ttu-id="04c2d-123">**portTypeDeclarations**</span><span class="sxs-lookup"><span data-stu-id="04c2d-123">**portTypeDeclarations**</span></span>](porttypedeclarations.md)<br/>                                         | <span data-ttu-id="04c2d-124">Gera declarações de constante C para tipos de porta.</span><span class="sxs-lookup"><span data-stu-id="04c2d-124">Generates C constant declarations for port types.</span></span><br/> <br/>                                                                      |
| [<span data-ttu-id="04c2d-125">**portTypeDefinitions**</span><span class="sxs-lookup"><span data-stu-id="04c2d-125">**portTypeDefinitions**</span></span>](porttypedefinitions.md)<br/>                                           | <span data-ttu-id="04c2d-126">Gera constantes C para tipos de porta.</span><span class="sxs-lookup"><span data-stu-id="04c2d-126">Generates C constants for port types.</span></span><br/> <br/>                                                                                  |
| [<span data-ttu-id="04c2d-127">**proxyFunctionImplementations**</span><span class="sxs-lookup"><span data-stu-id="04c2d-127">**proxyFunctionImplementations**</span></span>](proxyfunctionimplementations.md)<br/>                         | <span data-ttu-id="04c2d-128">Gera implementações para funções de proxy para operações de tipo de porta.</span><span class="sxs-lookup"><span data-stu-id="04c2d-128">Generates implementations for proxy functions for port type operations.</span></span><br/> <br/>                                                |
| [<span data-ttu-id="04c2d-129">**stubDeclarations**</span><span class="sxs-lookup"><span data-stu-id="04c2d-129">**stubDeclarations**</span></span>](stubdeclarations.md)<br/>                                                 | <span data-ttu-id="04c2d-130">Gera declarações para funções de stub para operações de tipo de porta.</span><span class="sxs-lookup"><span data-stu-id="04c2d-130">Generates declarations for stub functions for port type operations.</span></span><br/> <br/>                                                    |
| [<span data-ttu-id="04c2d-131">**stubDefinitions**</span><span class="sxs-lookup"><span data-stu-id="04c2d-131">**stubDefinitions**</span></span>](stubdefinitions.md)<br/>                                                   | <span data-ttu-id="04c2d-132">Gera implementações para funções de stub para operações de tipo de porta.</span><span class="sxs-lookup"><span data-stu-id="04c2d-132">Generates implementations for stub functions for port type operations.</span></span><br/> <br/>                                                 |
| [<span data-ttu-id="04c2d-133">**subscriptionFunctionDeclarations**</span><span class="sxs-lookup"><span data-stu-id="04c2d-133">**subscriptionFunctionDeclarations**</span></span>](subscriptionfunctiondeclarations.md)<br/>                 | <span data-ttu-id="04c2d-134">Gera declarações de implementação para funções de proxy de assinatura/cancelamento de assinatura para operações de notificação de tipo de porta.</span><span class="sxs-lookup"><span data-stu-id="04c2d-134">Generates implementation declarations for subscribe/unsubscribe proxy functions for port type notification operations.</span></span><br/> <br/> |
| [<span data-ttu-id="04c2d-135">**subscriptionIdlFunctionDeclarations**</span><span class="sxs-lookup"><span data-stu-id="04c2d-135">**subscriptionIdlFunctionDeclarations**</span></span>](subscriptionidlfunctiondeclarations.md)<br/>           | <span data-ttu-id="04c2d-136">Gera declarações IDL para funções de proxy de assinatura/cancelamento de assinatura para operações de notificação de tipo de porta.</span><span class="sxs-lookup"><span data-stu-id="04c2d-136">Generates IDL declarations for subscribe/unsubscribe proxy functions for port type notification operations.</span></span><br/> <br/>            |
| [<span data-ttu-id="04c2d-137">**subscriptionProxyFunctionImplementations**</span><span class="sxs-lookup"><span data-stu-id="04c2d-137">**subscriptionProxyFunctionImplementations**</span></span>](subscriptionproxyfunctionimplementations.md)<br/> | <span data-ttu-id="04c2d-138">Gera implementações para funções de proxy de assinatura/cancelamento de assinatura para operações de notificação de tipo de porta.</span><span class="sxs-lookup"><span data-stu-id="04c2d-138">Generates implementations for subscribe/unsubscribe proxy functions for port type notification operations.</span></span><br/> <br/>             |



## <a name="remarks"></a><span data-ttu-id="04c2d-139">Comentários</span><span class="sxs-lookup"><span data-stu-id="04c2d-139">Remarks</span></span>

<span data-ttu-id="04c2d-140">Por padrão, o código é gerado para todos os tipos de porta nos arquivos de entrada WSDL.</span><span class="sxs-lookup"><span data-stu-id="04c2d-140">By default, code is generated for all port types in WSDL input files.</span></span>

## <a name="element-information"></a><span data-ttu-id="04c2d-141">Informações do elemento</span><span class="sxs-lookup"><span data-stu-id="04c2d-141">Element information</span></span>



| <span data-ttu-id="04c2d-142">Label</span><span class="sxs-lookup"><span data-stu-id="04c2d-142">Label</span></span> | <span data-ttu-id="04c2d-143">Valor</span><span class="sxs-lookup"><span data-stu-id="04c2d-143">Value</span></span> |
|-------------------------------------|---------------|
| <span data-ttu-id="04c2d-144">Sistema mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="04c2d-144">Minimum supported system</span></span><br/> | <span data-ttu-id="04c2d-145">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="04c2d-145">Windows Vista</span></span> |
| <span data-ttu-id="04c2d-146">Pode estar vazio</span><span class="sxs-lookup"><span data-stu-id="04c2d-146">Can be empty</span></span>                        | <span data-ttu-id="04c2d-147">Sim</span><span class="sxs-lookup"><span data-stu-id="04c2d-147">Yes</span></span>           |



 

 




