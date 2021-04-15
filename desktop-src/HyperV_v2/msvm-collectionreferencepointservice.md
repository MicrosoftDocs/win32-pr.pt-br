---
description: Serviço para criar, destruir e exportar pontos de referência.
ms.assetid: 88a76319-b5a7-44a3-8a31-83ade999b255
title: Classe Msvm_CollectionReferencePointService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionReferencePointService
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: f6ba56fcb75a177521b8f3ea3ae0675cfdd8a8dc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105760856"
---
# <a name="msvm_collectionreferencepointservice-class"></a><span data-ttu-id="e4071-103">\_Classe Msvm CollectionReferencePointService</span><span class="sxs-lookup"><span data-stu-id="e4071-103">Msvm\_CollectionReferencePointService class</span></span>

<span data-ttu-id="e4071-104">Serviço para criar, destruir e exportar pontos de referência</span><span class="sxs-lookup"><span data-stu-id="e4071-104">Service to create, destroy and export reference points</span></span>

<span data-ttu-id="e4071-105">de coleções de sistemas virtuais.</span><span class="sxs-lookup"><span data-stu-id="e4071-105">of virtual system collections.</span></span>

<span data-ttu-id="e4071-106">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="e4071-106">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="e4071-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e4071-107">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_CollectionReferencePointService : CIM_Service
{
};
```

## <a name="members"></a><span data-ttu-id="e4071-108">Membros</span><span class="sxs-lookup"><span data-stu-id="e4071-108">Members</span></span>

<span data-ttu-id="e4071-109">A classe **Msvm \_ CollectionReferencePointService** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="e4071-109">The **Msvm\_CollectionReferencePointService** class has these types of members:</span></span>

-   [<span data-ttu-id="e4071-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="e4071-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="e4071-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="e4071-111">Methods</span></span>

<span data-ttu-id="e4071-112">A classe **Msvm \_ CollectionReferencePointService** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="e4071-112">The **Msvm\_CollectionReferencePointService** class has these methods.</span></span>



| <span data-ttu-id="e4071-113">Método</span><span class="sxs-lookup"><span data-stu-id="e4071-113">Method</span></span>                                                                                      | <span data-ttu-id="e4071-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="e4071-114">Description</span></span>                                                                                                                                                                                                     |
|:--------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e4071-115">**CreateReferencePoint**</span><span class="sxs-lookup"><span data-stu-id="e4071-115">**CreateReferencePoint**</span></span>](msvm-collectionreferencepointservice-createreferencepoint.md)   | <span data-ttu-id="e4071-116">Cria um ponto de referência de uma coleção de sistemas virtuais.</span><span class="sxs-lookup"><span data-stu-id="e4071-116">Creates a reference point of a virtual system collection.</span></span><br/>                                                                                                                                            |
| [<span data-ttu-id="e4071-117">**DestroyReferencePoint**</span><span class="sxs-lookup"><span data-stu-id="e4071-117">**DestroyReferencePoint**</span></span>](msvm-collectionreferencepointservice-destroyreferencepoint.md) | <span data-ttu-id="e4071-118">Destrói uma coleção de pontos de referência existente.</span><span class="sxs-lookup"><span data-stu-id="e4071-118">Destroys an existing reference point collection.</span></span> <span data-ttu-id="e4071-119">Esse método pode, como efeito colateral, destruir outros pontos de referência que dependem da coleção de pontos de referência afetada.</span><span class="sxs-lookup"><span data-stu-id="e4071-119">This method may as a side effect destroy other reference points that are dependent on the affected reference point collection.</span></span><br/>                      |
| [<span data-ttu-id="e4071-120">**ExportReferencePoint**</span><span class="sxs-lookup"><span data-stu-id="e4071-120">**ExportReferencePoint**</span></span>](msvm-collectionreferencepointservice-exportreferencepoint.md)   | <span data-ttu-id="e4071-121">Exporta uma coleção de pontos de referência para um arquivo.</span><span class="sxs-lookup"><span data-stu-id="e4071-121">Exports a reference point collection to a file.</span></span> <span data-ttu-id="e4071-122">A coleção de pontos de referência, suas definições de configuração associadas e suas configurações de recursos associadas serão preservadas no arquivo resultante.</span><span class="sxs-lookup"><span data-stu-id="e4071-122">The reference point collection, its associated configuration settings, and its associated resource settings will be preserved in the resulting file.</span></span><br/> |
| [<span data-ttu-id="e4071-123">**RemoveAssociatedData**</span><span class="sxs-lookup"><span data-stu-id="e4071-123">**RemoveAssociatedData**</span></span>](msvm-collectionreferencepointservice-removeassociateddata.md)   | <span data-ttu-id="e4071-124">Remove o log de dados associado ao ponto de referência.</span><span class="sxs-lookup"><span data-stu-id="e4071-124">Removes the data log associated with the reference point.</span></span><br/>                                                                                                                                            |



 

## <a name="requirements"></a><span data-ttu-id="e4071-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e4071-125">Requirements</span></span>



| <span data-ttu-id="e4071-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="e4071-126">Requirement</span></span> | <span data-ttu-id="e4071-127">Valor</span><span class="sxs-lookup"><span data-stu-id="e4071-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e4071-128">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e4071-128">Minimum supported client</span></span><br/> | <span data-ttu-id="e4071-129">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="e4071-129">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="e4071-130">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e4071-130">Minimum supported server</span></span><br/> | <span data-ttu-id="e4071-131">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="e4071-131">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="e4071-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="e4071-132">Namespace</span></span><br/>                | <span data-ttu-id="e4071-133">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="e4071-133">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="e4071-134">MOF</span><span class="sxs-lookup"><span data-stu-id="e4071-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e4071-135"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e4071-135"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="e4071-136">DLL</span><span class="sxs-lookup"><span data-stu-id="e4071-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e4071-137"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="e4071-137"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="e4071-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="e4071-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e4071-139">**\_Serviço CIM**</span><span class="sxs-lookup"><span data-stu-id="e4071-139">**CIM\_Service**</span></span>](cim-service.md)
</dt> </dl>

 

 




