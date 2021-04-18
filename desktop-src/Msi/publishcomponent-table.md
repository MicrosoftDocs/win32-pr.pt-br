---
description: A tabela PublishComponent associa os componentes listados na tabela de componentes com uma cadeia de caracteres de texto de qualificador e um GUID de ID de categoria.
ms.assetid: 4a6be647-3e73-47a1-acfa-7d6d0a2fb2f4
title: Tabela PublishComponent
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bb0edfd811873242629c36257fdce5a80fe9d91
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105759644"
---
# <a name="publishcomponent-table"></a><span data-ttu-id="635aa-103">Tabela PublishComponent</span><span class="sxs-lookup"><span data-stu-id="635aa-103">PublishComponent Table</span></span>

<span data-ttu-id="635aa-104">A tabela PublishComponent associa os componentes listados na [tabela de componentes](component-table.md) com uma cadeia de caracteres de texto de qualificador e um GUID de ID de categoria.</span><span class="sxs-lookup"><span data-stu-id="635aa-104">The PublishComponent table associates components listed in the [Component table](component-table.md) with a qualifier text-string and a category ID GUID.</span></span> <span data-ttu-id="635aa-105">Os componentes com funcionalidade paralela que foram agrupados dessa maneira são chamados de componentes qualificados.</span><span class="sxs-lookup"><span data-stu-id="635aa-105">Components with parallel functionality that have been grouped together in this way are referred to as qualified components.</span></span> <span data-ttu-id="635aa-106">Consulte [componentes qualificados](qualified-components.md).</span><span class="sxs-lookup"><span data-stu-id="635aa-106">See [Qualified Components](qualified-components.md).</span></span> <span data-ttu-id="635aa-107">Isso fornece ao instalador um método de indireção de nível único ao fazer referência aos componentes.</span><span class="sxs-lookup"><span data-stu-id="635aa-107">This provides the installer with a method for single-level indirection when referring to components.</span></span> <span data-ttu-id="635aa-108">Consulte [usando componentes qualificados](using-qualified-components.md).</span><span class="sxs-lookup"><span data-stu-id="635aa-108">See [Using Qualified Components](using-qualified-components.md).</span></span>

<span data-ttu-id="635aa-109">A tabela PublishComponent tem as colunas a seguir.</span><span class="sxs-lookup"><span data-stu-id="635aa-109">The PublishComponent table has the following columns.</span></span>



| <span data-ttu-id="635aa-110">Coluna</span><span class="sxs-lookup"><span data-stu-id="635aa-110">Column</span></span>      | <span data-ttu-id="635aa-111">Tipo</span><span class="sxs-lookup"><span data-stu-id="635aa-111">Type</span></span>                         | <span data-ttu-id="635aa-112">Chave</span><span class="sxs-lookup"><span data-stu-id="635aa-112">Key</span></span> | <span data-ttu-id="635aa-113">Nullable</span><span class="sxs-lookup"><span data-stu-id="635aa-113">Nullable</span></span> |
|-------------|------------------------------|-----|----------|
| <span data-ttu-id="635aa-114">ComponentId</span><span class="sxs-lookup"><span data-stu-id="635aa-114">ComponentId</span></span> | [<span data-ttu-id="635aa-115">GUID</span><span class="sxs-lookup"><span data-stu-id="635aa-115">GUID</span></span>](guid.md)             | <span data-ttu-id="635aa-116">S</span><span class="sxs-lookup"><span data-stu-id="635aa-116">Y</span></span>   | <span data-ttu-id="635aa-117">N</span><span class="sxs-lookup"><span data-stu-id="635aa-117">N</span></span>        |
| <span data-ttu-id="635aa-118">Qualificador</span><span class="sxs-lookup"><span data-stu-id="635aa-118">Qualifier</span></span>   | [<span data-ttu-id="635aa-119">Text</span><span class="sxs-lookup"><span data-stu-id="635aa-119">Text</span></span>](text.md)             | <span data-ttu-id="635aa-120">S</span><span class="sxs-lookup"><span data-stu-id="635aa-120">Y</span></span>   | <span data-ttu-id="635aa-121">N</span><span class="sxs-lookup"><span data-stu-id="635aa-121">N</span></span>        |
| <span data-ttu-id="635aa-122">Componente\_</span><span class="sxs-lookup"><span data-stu-id="635aa-122">Component\_</span></span> | [<span data-ttu-id="635aa-123">Identificador</span><span class="sxs-lookup"><span data-stu-id="635aa-123">Identifier</span></span>](identifier.md) | <span data-ttu-id="635aa-124">S</span><span class="sxs-lookup"><span data-stu-id="635aa-124">Y</span></span>   | <span data-ttu-id="635aa-125">N</span><span class="sxs-lookup"><span data-stu-id="635aa-125">N</span></span>        |
| <span data-ttu-id="635aa-126">AppData</span><span class="sxs-lookup"><span data-stu-id="635aa-126">AppData</span></span>     | [<span data-ttu-id="635aa-127">Text</span><span class="sxs-lookup"><span data-stu-id="635aa-127">Text</span></span>](text.md)             | <span data-ttu-id="635aa-128">N</span><span class="sxs-lookup"><span data-stu-id="635aa-128">N</span></span>   | <span data-ttu-id="635aa-129">S</span><span class="sxs-lookup"><span data-stu-id="635aa-129">Y</span></span>        |
| <span data-ttu-id="635aa-130">Recurso\_</span><span class="sxs-lookup"><span data-stu-id="635aa-130">Feature\_</span></span>   | [<span data-ttu-id="635aa-131">Identificador</span><span class="sxs-lookup"><span data-stu-id="635aa-131">Identifier</span></span>](identifier.md) | <span data-ttu-id="635aa-132">N</span><span class="sxs-lookup"><span data-stu-id="635aa-132">N</span></span>   | <span data-ttu-id="635aa-133">N</span><span class="sxs-lookup"><span data-stu-id="635aa-133">N</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="635aa-134">Colunas</span><span class="sxs-lookup"><span data-stu-id="635aa-134">Columns</span></span>

<dl> <dt>

<span data-ttu-id="635aa-135"><span id="ComponentId"></span><span id="componentid"></span><span id="COMPONENTID"></span>ComponentId</span><span class="sxs-lookup"><span data-stu-id="635aa-135"><span id="ComponentId"></span><span id="componentid"></span><span id="COMPONENTID"></span>ComponentId</span></span>
</dt> <dd>

<span data-ttu-id="635aa-136">Um [GUID](guid.md) de cadeia de caracteres que representa a categoria de componentes agrupados.</span><span class="sxs-lookup"><span data-stu-id="635aa-136">A string [GUID](guid.md) that represents the category of components being grouped together.</span></span> <span data-ttu-id="635aa-137">Observe que o título desta coluna é enganoso.</span><span class="sxs-lookup"><span data-stu-id="635aa-137">Note that this column's title is misleading.</span></span> <span data-ttu-id="635aa-138">Este é o GUID para a categoria de componentes qualificados e não é o mesmo GUID que aparece na coluna ComponentID da [tabela de componentes](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="635aa-138">This is the GUID for the category of qualified components and is not the same GUID appearing in the ComponentId column of the [Component table](component-table.md).</span></span> <span data-ttu-id="635aa-139">Aqui, ele se refere a um servidor que fornece a funcionalidade de um componente para clientes externos em vez do próprio componente.</span><span class="sxs-lookup"><span data-stu-id="635aa-139">Here it refers to a server that provides the functionality of a component to external clients rather than the component itself.</span></span>

</dd> <dt>

<span data-ttu-id="635aa-140"><span id="Qualifier"></span><span id="qualifier"></span><span id="QUALIFIER"></span>Qualificado</span><span class="sxs-lookup"><span data-stu-id="635aa-140"><span id="Qualifier"></span><span id="qualifier"></span><span id="QUALIFIER"></span>Qualifier</span></span>
</dt> <dd>

<span data-ttu-id="635aa-141">Uma cadeia de texto que qualifica o valor na coluna ComponentID.</span><span class="sxs-lookup"><span data-stu-id="635aa-141">A text string that qualifies the value in the ComponentId column.</span></span> <span data-ttu-id="635aa-142">Um qualificador é usado para distinguir várias formas do mesmo componente, como um componente que é implementado em vários idiomas.</span><span class="sxs-lookup"><span data-stu-id="635aa-142">A qualifier is used to distinguish multiple forms of the same component, such as a component that is implemented in multiple languages.</span></span> <span data-ttu-id="635aa-143">Essas são as cadeias de texto do qualificador retornadas por [**MsiEnumComponentQualifiers**](/windows/desktop/api/Msi/nf-msi-msienumcomponentqualifiersa).</span><span class="sxs-lookup"><span data-stu-id="635aa-143">These are the qualifier text-strings returned by [**MsiEnumComponentQualifiers**](/windows/desktop/api/Msi/nf-msi-msienumcomponentqualifiersa).</span></span>

</dd> <dt>

<span data-ttu-id="635aa-144"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Componente\_</span><span class="sxs-lookup"><span data-stu-id="635aa-144"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Component\_</span></span>
</dt> <dd>

<span data-ttu-id="635aa-145">Chave externa na coluna um da [tabela de componentes](component-table.md).</span><span class="sxs-lookup"><span data-stu-id="635aa-145">External key into column one of the [Component table](component-table.md).</span></span> <span data-ttu-id="635aa-146">Esse identificador se refere ao registro do componente qualificado na tabela de componentes.</span><span class="sxs-lookup"><span data-stu-id="635aa-146">This identifier refers to the qualified component's record in the Component table.</span></span>

</dd> <dt>

<span data-ttu-id="635aa-147"><span id="AppData"></span><span id="appdata"></span><span id="APPDATA"></span>AppData</span><span class="sxs-lookup"><span data-stu-id="635aa-147"><span id="AppData"></span><span id="appdata"></span><span id="APPDATA"></span>AppData</span></span>
</dt> <dd>

<span data-ttu-id="635aa-148">Um texto localizável opcional que descreve o componente qualificado deste registro.</span><span class="sxs-lookup"><span data-stu-id="635aa-148">An optional localizable text describing the qualified component of this record.</span></span> <span data-ttu-id="635aa-149">A cadeia de caracteres é normalmente analisada pelo aplicativo e pode ser exibida para o usuário.</span><span class="sxs-lookup"><span data-stu-id="635aa-149">The string is commonly parsed by the application and can be displayed to the user.</span></span> <span data-ttu-id="635aa-150">Ele deve descrever o componente qualificado.</span><span class="sxs-lookup"><span data-stu-id="635aa-150">It should describe the qualified component.</span></span> <span data-ttu-id="635aa-151">Isso pode ser recuperado com [**MsiEnumComponentQualifiers**](/windows/desktop/api/Msi/nf-msi-msienumcomponentqualifiersa).</span><span class="sxs-lookup"><span data-stu-id="635aa-151">This can be retrieved with [**MsiEnumComponentQualifiers**](/windows/desktop/api/Msi/nf-msi-msienumcomponentqualifiersa).</span></span>

</dd> <dt>

<span data-ttu-id="635aa-152"><span id="Feature_"></span><span id="feature_"></span><span id="FEATURE_"></span>Recurso\_</span><span class="sxs-lookup"><span data-stu-id="635aa-152"><span id="Feature_"></span><span id="feature_"></span><span id="FEATURE_"></span>Feature\_</span></span>
</dt> <dd>

<span data-ttu-id="635aa-153">Chave externa na coluna um da [tabela de recursos](feature-table.md).</span><span class="sxs-lookup"><span data-stu-id="635aa-153">External key into column one of the [Feature table](feature-table.md).</span></span> <span data-ttu-id="635aa-154">Esse é o recurso que usa esse componente qualificado.</span><span class="sxs-lookup"><span data-stu-id="635aa-154">This is the feature using this qualified component.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="635aa-155">Comentários</span><span class="sxs-lookup"><span data-stu-id="635aa-155">Remarks</span></span>

<span data-ttu-id="635aa-156">Essa tabela é referida quando a ação [PublishComponents](publishcomponents-action.md) ou a [ação UnpublishComponents](unpublishcomponents-action.md) é executada.</span><span class="sxs-lookup"><span data-stu-id="635aa-156">This table is referred to when the [PublishComponents action](publishcomponents-action.md) or the [UnpublishComponents action](unpublishcomponents-action.md) is executed.</span></span>

<span data-ttu-id="635aa-157">Observe que o nome desta tabela é enganoso.</span><span class="sxs-lookup"><span data-stu-id="635aa-157">Note that the name of this table is misleading.</span></span> <span data-ttu-id="635aa-158">Essa tabela não é necessária para criar anúncios.</span><span class="sxs-lookup"><span data-stu-id="635aa-158">This table is not required in order to author advertisement.</span></span> <span data-ttu-id="635aa-159">Consulte a coluna atributos da tabela de [componentes](component-table.md) e a [tabela de recursos](feature-table.md) para obter informações sobre como definir o estado de instalação dos componentes a serem anunciados.</span><span class="sxs-lookup"><span data-stu-id="635aa-159">See the Attributes column of the [Component table](component-table.md) and [Feature table](feature-table.md) for information on how to set the installation state of components to advertise.</span></span>

## <a name="validation"></a><span data-ttu-id="635aa-160">Validação</span><span class="sxs-lookup"><span data-stu-id="635aa-160">Validation</span></span>

<dl>

[<span data-ttu-id="635aa-161">ICE03</span><span class="sxs-lookup"><span data-stu-id="635aa-161">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="635aa-162">ICE06</span><span class="sxs-lookup"><span data-stu-id="635aa-162">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="635aa-163">ICE19</span><span class="sxs-lookup"><span data-stu-id="635aa-163">ICE19</span></span>](ice19.md)  
[<span data-ttu-id="635aa-164">ICE22</span><span class="sxs-lookup"><span data-stu-id="635aa-164">ICE22</span></span>](ice22.md)  
[<span data-ttu-id="635aa-165">ICE32</span><span class="sxs-lookup"><span data-stu-id="635aa-165">ICE32</span></span>](ice32.md)  
</dl>

 

 



