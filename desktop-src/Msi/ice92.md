---
description: ICE92 verifica se um componente sem um GUID de ID de componente também não foi especificado como um componente permanente.
ms.assetid: 5fe8a844-3f96-4b19-baa6-24e2405aff30
title: ICE92
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63c9cffdfd7ac30313ed24182d8b4cc94f25900f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103828874"
---
# <a name="ice92"></a><span data-ttu-id="d2181-103">ICE92</span><span class="sxs-lookup"><span data-stu-id="d2181-103">ICE92</span></span>

<span data-ttu-id="d2181-104">ICE92 verifica se um componente sem um GUID de ID de componente também não foi especificado como um componente permanente.</span><span class="sxs-lookup"><span data-stu-id="d2181-104">ICE92 verifies that a component without a Component Id GUID is not also specified as a permanent component.</span></span> <span data-ttu-id="d2181-105">Essa ação personalizada de ICE verifica a tabela de componentes em busca de [componente](component-table.md) sem um [GUID](guid.md) especificado no campo ComponentID e verifica se o sinalizador **msidbComponentAttributesPermanent** não foi definido no campo atributos.</span><span class="sxs-lookup"><span data-stu-id="d2181-105">This ICE custom action checks the [Component Table](component-table.md) for components without a [GUID](guid.md) specified in the ComponentId field and verifies that the **msidbComponentAttributesPermanent** flag has not been set in the Attributes field.</span></span> <span data-ttu-id="d2181-106">ICE92 também verifica se nenhum componente tem os atributos **msidbComponentAttributesPermanent** e **msidbComponentAttributesUninstallOnSupersedence** .</span><span class="sxs-lookup"><span data-stu-id="d2181-106">ICE92 also verifies that no component has both the **msidbComponentAttributesPermanent** and **msidbComponentAttributesUninstallOnSupersedence** attributes.</span></span>

<span data-ttu-id="d2181-107">Se a coluna ComponentID for nula, o instalador não registrará o componente e o componente não poderá ser removido ou reparado pelo instalador.</span><span class="sxs-lookup"><span data-stu-id="d2181-107">If the ComponentId column is null, the installer does not register the component and the component cannot be removed or repaired by the installer.</span></span>

## <a name="result"></a><span data-ttu-id="d2181-108">Resultado</span><span class="sxs-lookup"><span data-stu-id="d2181-108">Result</span></span>

<span data-ttu-id="d2181-109">ICE92 posta o erro a seguir.</span><span class="sxs-lookup"><span data-stu-id="d2181-109">ICE92 posts the following error.</span></span>



| <span data-ttu-id="d2181-110">Erro de ICE92</span><span class="sxs-lookup"><span data-stu-id="d2181-110">ICE92 error</span></span>                                                          | <span data-ttu-id="d2181-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="d2181-111">Description</span></span>                                                                                                                                                    |
|----------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d2181-112">O componente ' \[ 1 \] ' não tem ComponentID e está marcado como permanente.</span><span class="sxs-lookup"><span data-stu-id="d2181-112">The Component '\[1\]' has no ComponentId and is marked as permanent.</span></span> | <span data-ttu-id="d2181-113">A entrada deste componente na tabela de componentes tem nulo na coluna ComponentID e tem **msidbComponentAttributesPermanent** na coluna atributos.</span><span class="sxs-lookup"><span data-stu-id="d2181-113">The entry for this component in the Component table has null in the ComponentId column and has **msidbComponentAttributesPermanent** in the Attributes column.</span></span> |



 

<span data-ttu-id="d2181-114">ICE92 posta o aviso a seguir.</span><span class="sxs-lookup"><span data-stu-id="d2181-114">ICE92 posts the following warning.</span></span>



| <span data-ttu-id="d2181-115">Aviso de ICE92</span><span class="sxs-lookup"><span data-stu-id="d2181-115">ICE92 warning</span></span>                                                                                                                                                           | <span data-ttu-id="d2181-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="d2181-116">Description</span></span>                                                                                                                                                                                                 |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d2181-117">O componente ' \[ 1 \] ' está marcado como permanente e como desinstalar-on-substituition.</span><span class="sxs-lookup"><span data-stu-id="d2181-117">The Component '\[1\]' is marked as permanent and uninstall-on-supersedence.</span></span> <span data-ttu-id="d2181-118">O atributo Uninstall-on-substituition será ignorado porque o componente é permanente.</span><span class="sxs-lookup"><span data-stu-id="d2181-118">The uninstall-on-supersedence attribute will be ignored because the component is permanent.</span></span> | <span data-ttu-id="d2181-119">A entrada para esse componente na [tabela de componentes](component-table.md) tem os atributos **msidbComponentAttributesPermanent** e **msidbComponentAttributesUninstallOnSupersedence** especificados.</span><span class="sxs-lookup"><span data-stu-id="d2181-119">The entry for this component in the [Component table](component-table.md) has both the **msidbComponentAttributesPermanent** and **msidbComponentAttributesUninstallOnSupersedence** attributes specified.</span></span> |



 

## <a name="example"></a><span data-ttu-id="d2181-120">Exemplo</span><span class="sxs-lookup"><span data-stu-id="d2181-120">Example</span></span>

<span data-ttu-id="d2181-121">ICE92 relata o seguinte erro para o exemplo:</span><span class="sxs-lookup"><span data-stu-id="d2181-121">ICE92 reports the following error for the example:</span></span>

``` syntax
The Component 'Component1' has no ComponentId and is marked as permanent.
```

<span data-ttu-id="d2181-122">[Tabela de componentes](component-table.md) (parcial)</span><span class="sxs-lookup"><span data-stu-id="d2181-122">[Component Table](component-table.md) (partial)</span></span>



| <span data-ttu-id="d2181-123">Componente</span><span class="sxs-lookup"><span data-stu-id="d2181-123">Component</span></span>  | <span data-ttu-id="d2181-124">ComponentId</span><span class="sxs-lookup"><span data-stu-id="d2181-124">ComponentId</span></span> | <span data-ttu-id="d2181-125">Diretório\_</span><span class="sxs-lookup"><span data-stu-id="d2181-125">Directory\_</span></span> | <span data-ttu-id="d2181-126">Atributos</span><span class="sxs-lookup"><span data-stu-id="d2181-126">Attributes</span></span> | <span data-ttu-id="d2181-127">KeyPath</span><span class="sxs-lookup"><span data-stu-id="d2181-127">KeyPath</span></span> |
|------------|-------------|-------------|------------|---------|
| <span data-ttu-id="d2181-128">Component1</span><span class="sxs-lookup"><span data-stu-id="d2181-128">Component1</span></span> |             | <span data-ttu-id="d2181-129">Directorya</span><span class="sxs-lookup"><span data-stu-id="d2181-129">DirectoryA</span></span>  | <span data-ttu-id="d2181-130">16</span><span class="sxs-lookup"><span data-stu-id="d2181-130">16</span></span>         | <span data-ttu-id="d2181-131">FileA</span><span class="sxs-lookup"><span data-stu-id="d2181-131">FileA</span></span>   |



 

## <a name="related-topics"></a><span data-ttu-id="d2181-132">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="d2181-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d2181-133">Referência de ICE</span><span class="sxs-lookup"><span data-stu-id="d2181-133">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



