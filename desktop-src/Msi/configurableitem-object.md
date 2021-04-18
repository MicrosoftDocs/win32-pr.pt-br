---
description: O objeto ConfigurableItem representa uma única linha da Tabela ModuleConfiguration.
ms.assetid: bbd0d9bc-a463-4cd8-93ee-963dcee8efa6
title: Objeto ConfigurableItem (Mergemod. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ConfigurableItem
- IMsmConfigurableItem
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 4436be457adcca37ba40f15bbe0ecd6b0445fb2f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752049"
---
# <a name="configurableitem-object"></a><span data-ttu-id="1ed6a-103">Objeto ConfigurableItem</span><span class="sxs-lookup"><span data-stu-id="1ed6a-103">ConfigurableItem object</span></span>

<span data-ttu-id="1ed6a-104">O **objeto ConfigurableItem** representa uma única linha da [Tabela ModuleConfiguration](moduleconfiguration-table.md).</span><span class="sxs-lookup"><span data-stu-id="1ed6a-104">The **ConfigurableItem object** represents a single row from the [ModuleConfiguration table](moduleconfiguration-table.md).</span></span> <span data-ttu-id="1ed6a-105">Esse é um "atributo" único configurável do módulo.</span><span class="sxs-lookup"><span data-stu-id="1ed6a-105">This is a single configurable "attribute" from the module.</span></span> <span data-ttu-id="1ed6a-106">A interface consiste em propriedades somente leitura, uma para cada coluna na Tabela ModuleConfiguration.</span><span class="sxs-lookup"><span data-stu-id="1ed6a-106">The interface consists read-only properties, one for each column in the ModuleConfiguration table.</span></span> <span data-ttu-id="1ed6a-107">A definição da interface é a seguinte:</span><span class="sxs-lookup"><span data-stu-id="1ed6a-107">The Interface definition is as follows.</span></span>

## <a name="members"></a><span data-ttu-id="1ed6a-108">Membros</span><span class="sxs-lookup"><span data-stu-id="1ed6a-108">Members</span></span>

<span data-ttu-id="1ed6a-109">O objeto **ConfigurableItem** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="1ed6a-109">The **ConfigurableItem** object has these types of members:</span></span>

-   [<span data-ttu-id="1ed6a-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="1ed6a-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="1ed6a-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="1ed6a-111">Properties</span></span>

<span data-ttu-id="1ed6a-112">O objeto **ConfigurableItem** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="1ed6a-112">The **ConfigurableItem** object has these properties.</span></span>



| <span data-ttu-id="1ed6a-113">Propriedade</span><span class="sxs-lookup"><span data-stu-id="1ed6a-113">Property</span></span>                                                         | <span data-ttu-id="1ed6a-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="1ed6a-114">Description</span></span>                                                                                                                               |
|:-----------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1ed6a-115">**Atributos**</span><span class="sxs-lookup"><span data-stu-id="1ed6a-115">**Attributes**</span></span>](configurableitem-attributes.md)<br/>     | <span data-ttu-id="1ed6a-116">Retorna o valor no campo atributos do registro desse objeto na Tabela ModuleConfiguration.</span><span class="sxs-lookup"><span data-stu-id="1ed6a-116">Returns the value in the Attributes field of this object's record in the ModuleConfiguration table.</span></span><br/>                            |
| [<span data-ttu-id="1ed6a-117">**Contexto**</span><span class="sxs-lookup"><span data-stu-id="1ed6a-117">**Context**</span></span>](configurableitem-context.md)<br/>           | <span data-ttu-id="1ed6a-118">Retorna o valor no campo de contexto do registro desse objeto na Tabela ModuleConfiguration.</span><span class="sxs-lookup"><span data-stu-id="1ed6a-118">Returns the value in the Context field of this object's record in the ModuleConfiguration table.</span></span><br/>                               |
| [<span data-ttu-id="1ed6a-119">**DefaultValue**</span><span class="sxs-lookup"><span data-stu-id="1ed6a-119">**DefaultValue**</span></span>](configurableitem-defaultvalue.md)<br/> | <span data-ttu-id="1ed6a-120">Retorna o valor no campo DefaultValue do registro desse objeto na Tabela ModuleConfiguration.</span><span class="sxs-lookup"><span data-stu-id="1ed6a-120">Returns the value in the DefaultValue field of this object's record in the ModuleConfiguration table.</span></span><br/>                          |
| [<span data-ttu-id="1ed6a-121">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="1ed6a-121">**Description**</span></span>](configurableitem-description.md)<br/>   | <span data-ttu-id="1ed6a-122">Retorna o valor no campo Descrição do registro desse objeto na Tabela ModuleConfiguration.</span><span class="sxs-lookup"><span data-stu-id="1ed6a-122">Returns the value in the Description field of this object's record in the ModuleConfiguration table.</span></span><br/>                           |
| [<span data-ttu-id="1ed6a-123">**DisplayName**</span><span class="sxs-lookup"><span data-stu-id="1ed6a-123">**DisplayName**</span></span>](configurableitem-displayname.md)<br/>   | <span data-ttu-id="1ed6a-124">Retorna o valor no campo DisplayName do registro desse objeto na Tabela ModuleConfiguration.</span><span class="sxs-lookup"><span data-stu-id="1ed6a-124">Returns the value in the DisplayName field of this object's record in the ModuleConfiguration table.</span></span><br/>                           |
| [<span data-ttu-id="1ed6a-125">**Formatar**</span><span class="sxs-lookup"><span data-stu-id="1ed6a-125">**Format**</span></span>](configurableitem-format.md)<br/>             | <span data-ttu-id="1ed6a-126">Retorna o valor no campo formato do registro desse objeto na Tabela ModuleConfiguration.</span><span class="sxs-lookup"><span data-stu-id="1ed6a-126">Returns the value in the Format field of this object's record in the ModuleConfiguration table.</span></span><br/>                                |
| [<span data-ttu-id="1ed6a-127">**HelpKeyword**</span><span class="sxs-lookup"><span data-stu-id="1ed6a-127">**HelpKeyword**</span></span>](configurableitem-helpkeyword.md)<br/>   | <span data-ttu-id="1ed6a-128">Retorna o valor no campo HelpKeyword do registro desse objeto na Tabela ModuleConfiguration.</span><span class="sxs-lookup"><span data-stu-id="1ed6a-128">Returns the value in the HelpKeyword field of this object's record in the ModuleConfiguration table.</span></span><br/>                           |
| [<span data-ttu-id="1ed6a-129">**HelpLocation**</span><span class="sxs-lookup"><span data-stu-id="1ed6a-129">**HelpLocation**</span></span>](configurableitem-helplocation.md)<br/> | <span data-ttu-id="1ed6a-130">Retorna o valor no campo HelpLocation do registro desse objeto na Tabela ModuleConfiguration.</span><span class="sxs-lookup"><span data-stu-id="1ed6a-130">Returns the value in the HelpLocation field of this object's record in the ModuleConfiguration table.</span></span><br/>                          |
| [<span data-ttu-id="1ed6a-131">**Nome**</span><span class="sxs-lookup"><span data-stu-id="1ed6a-131">**Name**</span></span>](configurableitem-name.md)<br/>                 | <span data-ttu-id="1ed6a-132">Retorna o valor no campo nome do registro desse objeto na [Tabela ModuleConfiguration](moduleconfiguration-table.md).</span><span class="sxs-lookup"><span data-stu-id="1ed6a-132">Returns the value in the Name field of this object's record in the [ModuleConfiguration table](moduleconfiguration-table.md).</span></span><br/> |
| [<span data-ttu-id="1ed6a-133">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="1ed6a-133">**Type**</span></span>](configurableitem-type.md)<br/>                 | <span data-ttu-id="1ed6a-134">Retorna o valor no campo tipo do registro desse objeto na Tabela ModuleConfiguration.</span><span class="sxs-lookup"><span data-stu-id="1ed6a-134">Returns the value in the Type field of this object's record in the ModuleConfiguration table.</span></span><br/>                                  |



 

## <a name="c"></a><span data-ttu-id="1ed6a-135">C++</span><span class="sxs-lookup"><span data-stu-id="1ed6a-135">C++</span></span>

<span data-ttu-id="1ed6a-136">IMsmConfigurableItem de interface **: IDispatch**</span><span class="sxs-lookup"><span data-stu-id="1ed6a-136">interface **IMsmConfigurableItem : IDispatch**</span></span>

## <a name="interface-id"></a><span data-ttu-id="1ed6a-137">ID da interface</span><span class="sxs-lookup"><span data-stu-id="1ed6a-137">Interface ID</span></span>



| <span data-ttu-id="1ed6a-138">Constante</span><span class="sxs-lookup"><span data-stu-id="1ed6a-138">Constant</span></span>                      | <span data-ttu-id="1ed6a-139">Valor</span><span class="sxs-lookup"><span data-stu-id="1ed6a-139">Value</span></span>                                  |
|-------------------------------|----------------------------------------|
| <span data-ttu-id="1ed6a-140">**IMsmConfigurableItem de IID \_**</span><span class="sxs-lookup"><span data-stu-id="1ed6a-140">**IID\_IMsmConfigurableItem**</span></span> | <span data-ttu-id="1ed6a-141">{4D6E6284-D21D-401E-84F6-909E00B50F71}</span><span class="sxs-lookup"><span data-stu-id="1ed6a-141">{4D6E6284-D21D-401E-84F6-909E00B50F71}</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="1ed6a-142">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1ed6a-142">Requirements</span></span>



| <span data-ttu-id="1ed6a-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="1ed6a-143">Requirement</span></span> | <span data-ttu-id="1ed6a-144">Valor</span><span class="sxs-lookup"><span data-stu-id="1ed6a-144">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1ed6a-145">Versão</span><span class="sxs-lookup"><span data-stu-id="1ed6a-145">Version</span></span><br/> | <span data-ttu-id="1ed6a-146">Mergemod.dll 2,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="1ed6a-146">Mergemod.dll 2.0 or later</span></span><br/>                                                    |
| <span data-ttu-id="1ed6a-147">parâmetro</span><span class="sxs-lookup"><span data-stu-id="1ed6a-147">Header</span></span><br/>  | <dl> <span data-ttu-id="1ed6a-148"><dt>Mergemod. h</dt></span><span class="sxs-lookup"><span data-stu-id="1ed6a-148"><dt>Mergemod.h</dt></span></span> </dl>   |
| <span data-ttu-id="1ed6a-149">DLL</span><span class="sxs-lookup"><span data-stu-id="1ed6a-149">DLL</span></span><br/>     | <dl> <span data-ttu-id="1ed6a-150"><dt>Mergemod.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1ed6a-150"><dt>Mergemod.dll</dt></span></span> </dl> |



 

 




