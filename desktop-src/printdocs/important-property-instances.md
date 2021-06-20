---
description: Para que um cliente Construa um PrintTicket, o documento PrintCapabilities deve fornecer propriedades de instâncias de recurso e instâncias de opção no recurso.
ms.assetid: 8169b74f-13e0-4f6b-81e2-1824d932ee50
title: Instâncias de propriedade importantes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4691b73b1206ee092c171b213a3815925b7f53c6
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112409119"
---
# <a name="important-property-instances"></a><span data-ttu-id="74a96-103">Instâncias de propriedade importantes</span><span class="sxs-lookup"><span data-stu-id="74a96-103">Important Property Instances</span></span>

<span data-ttu-id="74a96-104">Este tópico não é atual.</span><span class="sxs-lookup"><span data-stu-id="74a96-104">This topic is not current.</span></span> <span data-ttu-id="74a96-105">Para obter as informações mais atuais, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="74a96-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="74a96-106">Para que um cliente de PrintCapabilities possa construir um PrintTicket razoável, o documento PrintCapabilities deve fornecer certas propriedades de instâncias de recursos, bem como instâncias de opção dentro do recurso.</span><span class="sxs-lookup"><span data-stu-id="74a96-106">In order for a PrintCapabilities client to be able to construct a reasonable PrintTicket, the PrintCapabilities document must provide certain properties of Feature instances as well as Option instances within the Feature.</span></span> <span data-ttu-id="74a96-107">Um módulo de interface do usuário genérica (IU) requer essas informações para construir uma interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="74a96-107">A generic user interface (UI) module requires such information to construct a UI.</span></span> <span data-ttu-id="74a96-108">Isso, por sua vez, requer que as palavras-chave do esquema de impressão definam algumas instâncias de propriedade que aparecem como filhos dos elementos Feature e Option.</span><span class="sxs-lookup"><span data-stu-id="74a96-108">This in turn requires that the Print Schema Keywords define a few Property instances that appear as children of Feature and Option elements.</span></span>

<span data-ttu-id="74a96-109">Os elementos de recurso podem conter a seguinte propriedade.</span><span class="sxs-lookup"><span data-stu-id="74a96-109">Feature elements can contain the following Property.</span></span>



| <span data-ttu-id="74a96-110">Propriedade</span><span class="sxs-lookup"><span data-stu-id="74a96-110">Property</span></span>                  | <span data-ttu-id="74a96-111">Valores</span><span class="sxs-lookup"><span data-stu-id="74a96-111">Values</span></span>                                 | <span data-ttu-id="74a96-112">Finalidade</span><span class="sxs-lookup"><span data-stu-id="74a96-112">Purpose</span></span>                                                                                                                                                                                                                                                                                                       |
|---------------------------|----------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="74a96-113">SelectionType</span><span class="sxs-lookup"><span data-stu-id="74a96-113">SelectionType</span></span> <br/> | <span data-ttu-id="74a96-114">PickOne</span><span class="sxs-lookup"><span data-stu-id="74a96-114">PickOne</span></span><br/> <span data-ttu-id="74a96-115">PickMany</span><span class="sxs-lookup"><span data-stu-id="74a96-115">PickMany</span></span><br/> | <span data-ttu-id="74a96-116">Especifica o número de opções que podem ser selecionadas para esse recurso em um determinado momento, qualquer um (PickOne) ou mais de um (PickMany).</span><span class="sxs-lookup"><span data-stu-id="74a96-116">Specifies the number of Options that can be selected for this Feature at a given time, either one (PickOne), or more than one (PickMany).</span></span> <span data-ttu-id="74a96-117">O cliente pode usar essas informações para construir um PrintTicket.</span><span class="sxs-lookup"><span data-stu-id="74a96-117">The client can use this information to construct a PrintTicket.</span></span> <span data-ttu-id="74a96-118">Essas informações afetam o comportamento da interface do usuário, bem como a validação de PrintTicket pelo provedor.</span><span class="sxs-lookup"><span data-stu-id="74a96-118">This information affects UI behavior, as well as PrintTicket validation by the provider.</span></span><br/> |



 

<span data-ttu-id="74a96-119">Os elementos de opção podem conter a propriedade a seguir.</span><span class="sxs-lookup"><span data-stu-id="74a96-119">Option elements can contain the following Property.</span></span>



| <span data-ttu-id="74a96-120">Propriedade</span><span class="sxs-lookup"><span data-stu-id="74a96-120">Property</span></span>                   | <span data-ttu-id="74a96-121">Valores</span><span class="sxs-lookup"><span data-stu-id="74a96-121">Values</span></span>                           | <span data-ttu-id="74a96-122">Finalidade</span><span class="sxs-lookup"><span data-stu-id="74a96-122">Purpose</span></span>                                                                                                                                                                                                                                                                                                                                                                 |
|----------------------------|----------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="74a96-123">IdentityOption</span><span class="sxs-lookup"><span data-stu-id="74a96-123">IdentityOption</span></span> <br/> | <span data-ttu-id="74a96-124">Verdadeiro</span><span class="sxs-lookup"><span data-stu-id="74a96-124">True</span></span><br/> <span data-ttu-id="74a96-125">Falso</span><span class="sxs-lookup"><span data-stu-id="74a96-125">False</span></span><br/> | <span data-ttu-id="74a96-126">A seleção da propriedade IdentityOption é interpretada para significar "desabilitar este recurso".</span><span class="sxs-lookup"><span data-stu-id="74a96-126">Selecting the IdentityOption Property is interpreted to mean "disable this feature".</span></span> <span data-ttu-id="74a96-127">Um recurso que contém uma Propriedade SelectionType cujo valor é PickMany também deve conter uma opção que tem uma propriedade IdentityOption.</span><span class="sxs-lookup"><span data-stu-id="74a96-127">A Feature that contains a SelectionType Property whose value is PickMany must also contain an Option that has an IdentityOption Property.</span></span> <span data-ttu-id="74a96-128">O código da interface do usuário (ou cliente construindo um PrintTicket) deve anular a seleção de qualquer outra opção se a propriedade IdentityOption estiver selecionada.</span><span class="sxs-lookup"><span data-stu-id="74a96-128">The UI code (or client constructing a PrintTicket) must deselect any other Option if the IdentityOption Property is selected.</span></span><br/> |



 

<span data-ttu-id="74a96-129">Os elementos Feature, Option e ParameterDef podem conter a propriedade a seguir.</span><span class="sxs-lookup"><span data-stu-id="74a96-129">Feature, Option, and ParameterDef elements can contain the following Property.</span></span>



| <span data-ttu-id="74a96-130">Propriedade</span><span class="sxs-lookup"><span data-stu-id="74a96-130">Property</span></span>              | <span data-ttu-id="74a96-131">Valores</span><span class="sxs-lookup"><span data-stu-id="74a96-131">Values</span></span>                          | <span data-ttu-id="74a96-132">Finalidade</span><span class="sxs-lookup"><span data-stu-id="74a96-132">Purpose</span></span>                                                                                                                                                                                                                                                                                                                                     |
|-----------------------|---------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="74a96-133">DisplayUI</span><span class="sxs-lookup"><span data-stu-id="74a96-133">DisplayUI</span></span> <br/> | <span data-ttu-id="74a96-134">Mostrar</span><span class="sxs-lookup"><span data-stu-id="74a96-134">Show</span></span><br/> <span data-ttu-id="74a96-135">Ocultar</span><span class="sxs-lookup"><span data-stu-id="74a96-135">Hide</span></span><br/> | <span data-ttu-id="74a96-136">Especifica se o elemento pai deve ser exibido na interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="74a96-136">Specifies whether the parent element should be displayed in the UI.</span></span> <span data-ttu-id="74a96-137">Mostrar indica que o elemento deve ser exibido na interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="74a96-137">Show indicates that the element should be displayed in the UI.</span></span> <span data-ttu-id="74a96-138">Ocultar indica que o elemento não deve ser exibido na interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="74a96-138">Hide indicates that the element should not be displayed in the UI.</span></span> <span data-ttu-id="74a96-139">Se essa propriedade não for definida para um elemento, a interpretação padrão será mostrada, o que significa que o elemento é exibido.</span><span class="sxs-lookup"><span data-stu-id="74a96-139">If this Property is not defined for an element, the default interpretation is Show, meaning that the element is displayed.</span></span><br/> |



 

<span data-ttu-id="74a96-140">Os elementos Feature, Option e ParameterDef podem conter a propriedade a seguir.</span><span class="sxs-lookup"><span data-stu-id="74a96-140">Feature, Option, and ParameterDef elements can contain the following Property.</span></span>



| <span data-ttu-id="74a96-141">Propriedade</span><span class="sxs-lookup"><span data-stu-id="74a96-141">Property</span></span>                | <span data-ttu-id="74a96-142">Valor</span><span class="sxs-lookup"><span data-stu-id="74a96-142">Value</span></span>             | <span data-ttu-id="74a96-143">Finalidade</span><span class="sxs-lookup"><span data-stu-id="74a96-143">Purpose</span></span>                                                                                                                                                                                                                                                                                                                                                                                                               |
|-------------------------|-------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="74a96-144">DisplayName</span><span class="sxs-lookup"><span data-stu-id="74a96-144">DisplayName</span></span> <br/> | <span data-ttu-id="74a96-145">String</span><span class="sxs-lookup"><span data-stu-id="74a96-145">String</span></span><br/> | <span data-ttu-id="74a96-146">Especifica a cadeia de caracteres de exibição para o elemento pai, substituindo o nome de exibição padrão.</span><span class="sxs-lookup"><span data-stu-id="74a96-146">Specifies the display string for the parent element, overriding the default display name.</span></span> <span data-ttu-id="74a96-147">Pode ser usado por provedores de PrintCapabilities para apresentar um nome de exibição localizado e amigável.</span><span class="sxs-lookup"><span data-stu-id="74a96-147">Can be used by PrintCapabilities providers to present a localized and user friendly display name.</span></span> <span data-ttu-id="74a96-148">O valor do nome de exibição padrão é o atributo Name para o elemento pai.</span><span class="sxs-lookup"><span data-stu-id="74a96-148">The default display name value is the name attribute for the parent element.</span></span> <br/> <span data-ttu-id="74a96-149">No caso de elementos Option, se o atributo Name não for fornecido, a propriedade DisplayName deverá estar presente.</span><span class="sxs-lookup"><span data-stu-id="74a96-149">In the case of Option elements, if the name attribute is not provided, then the DisplayName Property must be present.</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="74a96-150">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="74a96-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="74a96-151">Especificação de esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="74a96-151">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




