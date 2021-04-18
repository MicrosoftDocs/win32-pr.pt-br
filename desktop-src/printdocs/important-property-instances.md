---
description: Este tópico não é atual. Para obter as informações mais atuais, consulte a especificação do esquema de impressão.
ms.assetid: 8169b74f-13e0-4f6b-81e2-1824d932ee50
title: Instâncias de propriedade importantes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ad3f58c099913b129ee7be0337ecab3343a5e5e
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/05/2021
ms.locfileid: "105791085"
---
# <a name="important-property-instances"></a><span data-ttu-id="4b80e-104">Instâncias de propriedade importantes</span><span class="sxs-lookup"><span data-stu-id="4b80e-104">Important Property Instances</span></span>

<span data-ttu-id="4b80e-105">Este tópico não é atual.</span><span class="sxs-lookup"><span data-stu-id="4b80e-105">This topic is not current.</span></span> <span data-ttu-id="4b80e-106">Para obter as informações mais atuais, consulte a [especificação do esquema de impressão](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span><span class="sxs-lookup"><span data-stu-id="4b80e-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="4b80e-107">Para que um cliente de PrintCapabilities possa construir um PrintTicket razoável, o documento PrintCapabilities deve fornecer certas propriedades de instâncias de recursos, bem como instâncias de opção dentro do recurso.</span><span class="sxs-lookup"><span data-stu-id="4b80e-107">In order for a PrintCapabilities client to be able to construct a reasonable PrintTicket, the PrintCapabilities document must provide certain properties of Feature instances as well as Option instances within the Feature.</span></span> <span data-ttu-id="4b80e-108">Um módulo de interface do usuário genérica (IU) requer essas informações para construir uma interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="4b80e-108">A generic user interface (UI) module requires such information to construct a UI.</span></span> <span data-ttu-id="4b80e-109">Isso, por sua vez, requer que as palavras-chave do esquema de impressão definam algumas instâncias de propriedade que aparecem como filhos dos elementos Feature e Option.</span><span class="sxs-lookup"><span data-stu-id="4b80e-109">This in turn requires that the Print Schema Keywords define a few Property instances that appear as children of Feature and Option elements.</span></span>

<span data-ttu-id="4b80e-110">Os elementos de recurso podem conter a seguinte propriedade.</span><span class="sxs-lookup"><span data-stu-id="4b80e-110">Feature elements can contain the following Property.</span></span>



| <span data-ttu-id="4b80e-111">Propriedade</span><span class="sxs-lookup"><span data-stu-id="4b80e-111">Property</span></span>                  | <span data-ttu-id="4b80e-112">Valores</span><span class="sxs-lookup"><span data-stu-id="4b80e-112">Values</span></span>                                 | <span data-ttu-id="4b80e-113">Finalidade</span><span class="sxs-lookup"><span data-stu-id="4b80e-113">Purpose</span></span>                                                                                                                                                                                                                                                                                                       |
|---------------------------|----------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4b80e-114">SelectionType</span><span class="sxs-lookup"><span data-stu-id="4b80e-114">SelectionType</span></span> <br/> | <span data-ttu-id="4b80e-115">PickOne</span><span class="sxs-lookup"><span data-stu-id="4b80e-115">PickOne</span></span><br/> <span data-ttu-id="4b80e-116">PickMany</span><span class="sxs-lookup"><span data-stu-id="4b80e-116">PickMany</span></span><br/> | <span data-ttu-id="4b80e-117">Especifica o número de opções que podem ser selecionadas para esse recurso em um determinado momento, qualquer um (PickOne) ou mais de um (PickMany).</span><span class="sxs-lookup"><span data-stu-id="4b80e-117">Specifies the number of Options that can be selected for this Feature at a given time, either one (PickOne), or more than one (PickMany).</span></span> <span data-ttu-id="4b80e-118">O cliente pode usar essas informações para construir um PrintTicket.</span><span class="sxs-lookup"><span data-stu-id="4b80e-118">The client can use this information to construct a PrintTicket.</span></span> <span data-ttu-id="4b80e-119">Essas informações afetam o comportamento da interface do usuário, bem como a validação de PrintTicket pelo provedor.</span><span class="sxs-lookup"><span data-stu-id="4b80e-119">This information affects UI behavior, as well as PrintTicket validation by the provider.</span></span><br/> |



 

<span data-ttu-id="4b80e-120">Os elementos de opção podem conter a propriedade a seguir.</span><span class="sxs-lookup"><span data-stu-id="4b80e-120">Option elements can contain the following Property.</span></span>



| <span data-ttu-id="4b80e-121">Propriedade</span><span class="sxs-lookup"><span data-stu-id="4b80e-121">Property</span></span>                   | <span data-ttu-id="4b80e-122">Valores</span><span class="sxs-lookup"><span data-stu-id="4b80e-122">Values</span></span>                           | <span data-ttu-id="4b80e-123">Finalidade</span><span class="sxs-lookup"><span data-stu-id="4b80e-123">Purpose</span></span>                                                                                                                                                                                                                                                                                                                                                                 |
|----------------------------|----------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4b80e-124">IdentityOption</span><span class="sxs-lookup"><span data-stu-id="4b80e-124">IdentityOption</span></span> <br/> | <span data-ttu-id="4b80e-125">True</span><span class="sxs-lookup"><span data-stu-id="4b80e-125">True</span></span><br/> <span data-ttu-id="4b80e-126">Falso</span><span class="sxs-lookup"><span data-stu-id="4b80e-126">False</span></span><br/> | <span data-ttu-id="4b80e-127">A seleção da propriedade IdentityOption é interpretada para significar "desabilitar este recurso".</span><span class="sxs-lookup"><span data-stu-id="4b80e-127">Selecting the IdentityOption Property is interpreted to mean "disable this feature".</span></span> <span data-ttu-id="4b80e-128">Um recurso que contém uma Propriedade SelectionType cujo valor é PickMany também deve conter uma opção que tem uma propriedade IdentityOption.</span><span class="sxs-lookup"><span data-stu-id="4b80e-128">A Feature that contains a SelectionType Property whose value is PickMany must also contain an Option that has an IdentityOption Property.</span></span> <span data-ttu-id="4b80e-129">O código da interface do usuário (ou cliente construindo um PrintTicket) deve anular a seleção de qualquer outra opção se a propriedade IdentityOption estiver selecionada.</span><span class="sxs-lookup"><span data-stu-id="4b80e-129">The UI code (or client constructing a PrintTicket) must deselect any other Option if the IdentityOption Property is selected.</span></span><br/> |



 

<span data-ttu-id="4b80e-130">Os elementos Feature, Option e ParameterDef podem conter a propriedade a seguir.</span><span class="sxs-lookup"><span data-stu-id="4b80e-130">Feature, Option, and ParameterDef elements can contain the following Property.</span></span>



| <span data-ttu-id="4b80e-131">Propriedade</span><span class="sxs-lookup"><span data-stu-id="4b80e-131">Property</span></span>              | <span data-ttu-id="4b80e-132">Valores</span><span class="sxs-lookup"><span data-stu-id="4b80e-132">Values</span></span>                          | <span data-ttu-id="4b80e-133">Finalidade</span><span class="sxs-lookup"><span data-stu-id="4b80e-133">Purpose</span></span>                                                                                                                                                                                                                                                                                                                                     |
|-----------------------|---------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4b80e-134">DisplayUI</span><span class="sxs-lookup"><span data-stu-id="4b80e-134">DisplayUI</span></span> <br/> | <span data-ttu-id="4b80e-135">Mostrar</span><span class="sxs-lookup"><span data-stu-id="4b80e-135">Show</span></span><br/> <span data-ttu-id="4b80e-136">Ocultar</span><span class="sxs-lookup"><span data-stu-id="4b80e-136">Hide</span></span><br/> | <span data-ttu-id="4b80e-137">Especifica se o elemento pai deve ser exibido na interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="4b80e-137">Specifies whether the parent element should be displayed in the UI.</span></span> <span data-ttu-id="4b80e-138">Mostrar indica que o elemento deve ser exibido na interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="4b80e-138">Show indicates that the element should be displayed in the UI.</span></span> <span data-ttu-id="4b80e-139">Ocultar indica que o elemento não deve ser exibido na interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="4b80e-139">Hide indicates that the element should not be displayed in the UI.</span></span> <span data-ttu-id="4b80e-140">Se essa propriedade não for definida para um elemento, a interpretação padrão será mostrada, o que significa que o elemento é exibido.</span><span class="sxs-lookup"><span data-stu-id="4b80e-140">If this Property is not defined for an element, the default interpretation is Show, meaning that the element is displayed.</span></span><br/> |



 

<span data-ttu-id="4b80e-141">Os elementos Feature, Option e ParameterDef podem conter a propriedade a seguir.</span><span class="sxs-lookup"><span data-stu-id="4b80e-141">Feature, Option, and ParameterDef elements can contain the following Property.</span></span>



| <span data-ttu-id="4b80e-142">Propriedade</span><span class="sxs-lookup"><span data-stu-id="4b80e-142">Property</span></span>                | <span data-ttu-id="4b80e-143">Valor</span><span class="sxs-lookup"><span data-stu-id="4b80e-143">Value</span></span>             | <span data-ttu-id="4b80e-144">Finalidade</span><span class="sxs-lookup"><span data-stu-id="4b80e-144">Purpose</span></span>                                                                                                                                                                                                                                                                                                                                                                                                               |
|-------------------------|-------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4b80e-145">DisplayName</span><span class="sxs-lookup"><span data-stu-id="4b80e-145">DisplayName</span></span> <br/> | <span data-ttu-id="4b80e-146">String</span><span class="sxs-lookup"><span data-stu-id="4b80e-146">String</span></span><br/> | <span data-ttu-id="4b80e-147">Especifica a cadeia de caracteres de exibição para o elemento pai, substituindo o nome de exibição padrão.</span><span class="sxs-lookup"><span data-stu-id="4b80e-147">Specifies the display string for the parent element, overriding the default display name.</span></span> <span data-ttu-id="4b80e-148">Pode ser usado por provedores de PrintCapabilities para apresentar um nome de exibição localizado e amigável.</span><span class="sxs-lookup"><span data-stu-id="4b80e-148">Can be used by PrintCapabilities providers to present a localized and user friendly display name.</span></span> <span data-ttu-id="4b80e-149">O valor do nome de exibição padrão é o atributo Name para o elemento pai.</span><span class="sxs-lookup"><span data-stu-id="4b80e-149">The default display name value is the name attribute for the parent element.</span></span> <br/> <span data-ttu-id="4b80e-150">No caso de elementos Option, se o atributo Name não for fornecido, a propriedade DisplayName deverá estar presente.</span><span class="sxs-lookup"><span data-stu-id="4b80e-150">In the case of Option elements, if the name attribute is not provided, then the DisplayName Property must be present.</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="4b80e-151">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="4b80e-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4b80e-152">Especificação de esquema de impressão</span><span class="sxs-lookup"><span data-stu-id="4b80e-152">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




