---
description: O objeto de componente representa uma instância exclusiva de um componente que está disponível para enumeração.
ms.assetid: cdc99bc3-9e2a-49db-8c01-b9634aefac38
title: Objeto de componente
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Component
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 5e31d6a7c3d2422111d0d8c3247e022fa35bdc43
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105748989"
---
# <a name="component-object"></a><span data-ttu-id="53945-103">Objeto de componente</span><span class="sxs-lookup"><span data-stu-id="53945-103">Component object</span></span>

<span data-ttu-id="53945-104">O objeto de componente representa uma instância exclusiva de um componente que está disponível para enumeração.</span><span class="sxs-lookup"><span data-stu-id="53945-104">The Component object represents a unique instance of a component that is available for enumeration.</span></span>

<span data-ttu-id="53945-105">**[Windows Installer 4,5 ou anterior](not-supported-in-windows-installer-4-5.md):** Sem suporte.</span><span class="sxs-lookup"><span data-stu-id="53945-105">**[Windows Installer 4.5 or earlier](not-supported-in-windows-installer-4-5.md):** Not supported.</span></span> <span data-ttu-id="53945-106">Esse objeto está disponível a partir do Windows Installer 5,0.</span><span class="sxs-lookup"><span data-stu-id="53945-106">This object is available beginning with Windows Installer 5.0.</span></span>

## <a name="members"></a><span data-ttu-id="53945-107">Membros</span><span class="sxs-lookup"><span data-stu-id="53945-107">Members</span></span>

<span data-ttu-id="53945-108">O objeto de **componente** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="53945-108">The **Component** object has these types of members:</span></span>

-   [<span data-ttu-id="53945-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="53945-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="53945-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="53945-110">Properties</span></span>

<span data-ttu-id="53945-111">O objeto de **componente** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="53945-111">The **Component** object has these properties.</span></span>



| <span data-ttu-id="53945-112">Propriedade</span><span class="sxs-lookup"><span data-stu-id="53945-112">Property</span></span>                                                    | <span data-ttu-id="53945-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="53945-113">Description</span></span>                                                                               |
|:------------------------------------------------------------|:------------------------------------------------------------------------------------------|
| [<span data-ttu-id="53945-114">**ComponentCode**</span><span class="sxs-lookup"><span data-stu-id="53945-114">**ComponentCode**</span></span>](component-componentcode.md)<br/> | <span data-ttu-id="53945-115">O código do componente em questão.</span><span class="sxs-lookup"><span data-stu-id="53945-115">The component code of the component in question.</span></span><br/>                               |
| [<span data-ttu-id="53945-116">**Contexto**</span><span class="sxs-lookup"><span data-stu-id="53945-116">**Context**</span></span>](component-context.md)<br/>             | <span data-ttu-id="53945-117">O contexto que foi determinado para ser aplicável ao componente em questão.</span><span class="sxs-lookup"><span data-stu-id="53945-117">The context that was determined to be applicable to the component in question.</span></span><br/> |
| [<span data-ttu-id="53945-118">**UserSID**</span><span class="sxs-lookup"><span data-stu-id="53945-118">**UserSID**</span></span>](component-usersid.md)<br/>             | <span data-ttu-id="53945-119">O SID do usuário para o componente enumerado.</span><span class="sxs-lookup"><span data-stu-id="53945-119">The user SID for the enumerated component.</span></span><br/>                                     |



 

## <a name="requirements"></a><span data-ttu-id="53945-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="53945-120">Requirements</span></span>



| <span data-ttu-id="53945-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="53945-121">Requirement</span></span> | <span data-ttu-id="53945-122">Valor</span><span class="sxs-lookup"><span data-stu-id="53945-122">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="53945-123">Versão</span><span class="sxs-lookup"><span data-stu-id="53945-123">Version</span></span><br/> | <span data-ttu-id="53945-124">Windows Installer 5,0 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="53945-124">Windows Installer 5.0 or later.</span></span><br/>                                         |
| <span data-ttu-id="53945-125">DLL</span><span class="sxs-lookup"><span data-stu-id="53945-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="53945-126"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="53945-126"><dt>Msi.dll</dt></span></span> </dl> |
| <span data-ttu-id="53945-127">IID</span><span class="sxs-lookup"><span data-stu-id="53945-127">IID</span></span><br/>     | <span data-ttu-id="53945-128">IID \_ IComponent é definido como 000C1097-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="53945-128">IID\_IComponent is defined as 000C1097-0000-0000-C000-000000000046</span></span><br/>      |



## <a name="see-also"></a><span data-ttu-id="53945-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="53945-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="53945-130">Usando a interface de automação</span><span class="sxs-lookup"><span data-stu-id="53945-130">Using the Automation Interface</span></span>](using-the-automation-interface.md)
</dt> <dt>

[<span data-ttu-id="53945-131">Exemplos de script de Windows Installer</span><span class="sxs-lookup"><span data-stu-id="53945-131">Windows Installer Scripting Examples</span></span>](windows-installer-scripting-examples.md)
</dt> </dl>

 

 




