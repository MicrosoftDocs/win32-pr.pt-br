---
title: Interface IMsRdpDriveCollection
description: Representa uma coleção de objetos de unidade.
ms.assetid: 26926b85-021d-4678-845f-93ba62b2b4a3
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota de interface IMsRdpDriveCollection
- Serviços de Área de Trabalho Remota da interface IMsRdpDriveCollection, descrita
topic_type:
- apiref
api_name:
- IMsRdpDriveCollection
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e7b2588ddb0945ba1fcab8fbb4c5b9b078a1af9a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104455486"
---
# <a name="imsrdpdrivecollection-interface"></a><span data-ttu-id="05504-105">Interface IMsRdpDriveCollection</span><span class="sxs-lookup"><span data-stu-id="05504-105">IMsRdpDriveCollection interface</span></span>

<span data-ttu-id="05504-106">Representa uma coleção de objetos de unidade.</span><span class="sxs-lookup"><span data-stu-id="05504-106">Represents a collection of drive objects.</span></span>

## <a name="members"></a><span data-ttu-id="05504-107">Membros</span><span class="sxs-lookup"><span data-stu-id="05504-107">Members</span></span>

<span data-ttu-id="05504-108">A interface **IMsRdpDriveCollection** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="05504-108">The **IMsRdpDriveCollection** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="05504-109">**IMsRdpDriveCollection** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="05504-109">**IMsRdpDriveCollection** also has these types of members:</span></span>

-   [<span data-ttu-id="05504-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="05504-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="05504-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="05504-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="05504-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="05504-112">Methods</span></span>

<span data-ttu-id="05504-113">A interface **IMsRdpDriveCollection** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="05504-113">The **IMsRdpDriveCollection** interface has these methods.</span></span>



| <span data-ttu-id="05504-114">Método</span><span class="sxs-lookup"><span data-stu-id="05504-114">Method</span></span>                                                     | <span data-ttu-id="05504-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="05504-115">Description</span></span>                                                 |
|:-----------------------------------------------------------|:------------------------------------------------------------|
| [<span data-ttu-id="05504-116">**RescanDrives**</span><span class="sxs-lookup"><span data-stu-id="05504-116">**RescanDrives**</span></span>](imsrdpdrivecollection-rescandrives.md) | <span data-ttu-id="05504-117">Atualiza a lista de objetos na coleção.</span><span class="sxs-lookup"><span data-stu-id="05504-117">Refreshes the list of objects in the collection.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="05504-118">Propriedades</span><span class="sxs-lookup"><span data-stu-id="05504-118">Properties</span></span>

<span data-ttu-id="05504-119">A interface **IMsRdpDriveCollection** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="05504-119">The **IMsRdpDriveCollection** interface has these properties.</span></span>



| <span data-ttu-id="05504-120">Propriedade</span><span class="sxs-lookup"><span data-stu-id="05504-120">Property</span></span>                                                              | <span data-ttu-id="05504-121">Tipo de acesso</span><span class="sxs-lookup"><span data-stu-id="05504-121">Access type</span></span>          | <span data-ttu-id="05504-122">Description</span><span class="sxs-lookup"><span data-stu-id="05504-122">Description</span></span>                                                  |
|:----------------------------------------------------------------------|:---------------------|:-------------------------------------------------------------|
| [<span data-ttu-id="05504-123">**DriveByIndex**</span><span class="sxs-lookup"><span data-stu-id="05504-123">**DriveByIndex**</span></span>](imsrdpdrivecollection-drivebyindex.md)<br/> | <span data-ttu-id="05504-124">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="05504-124">Read-only</span></span><br/> | <span data-ttu-id="05504-125">Recupera a unidade no índice especificado.</span><span class="sxs-lookup"><span data-stu-id="05504-125">Retrieves the drive at the specified index.</span></span><br/>       |
| [<span data-ttu-id="05504-126">**DriveCount**</span><span class="sxs-lookup"><span data-stu-id="05504-126">**DriveCount**</span></span>](imsrdpdrivecollection-drivecount.md)<br/>     | <span data-ttu-id="05504-127">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="05504-127">Read-only</span></span><br/> | <span data-ttu-id="05504-128">Recupera a contagem de objetos na coleção.</span><span class="sxs-lookup"><span data-stu-id="05504-128">Retrieves the count of objects in the collection.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="05504-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="05504-129">Requirements</span></span>



| <span data-ttu-id="05504-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="05504-130">Requirement</span></span> | <span data-ttu-id="05504-131">Valor</span><span class="sxs-lookup"><span data-stu-id="05504-131">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="05504-132">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="05504-132">Minimum supported client</span></span><br/> | <span data-ttu-id="05504-133">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="05504-133">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="05504-134">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="05504-134">Minimum supported server</span></span><br/> | <span data-ttu-id="05504-135">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="05504-135">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="05504-136">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="05504-136">Type library</span></span><br/>             | <dl> <span data-ttu-id="05504-137"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="05504-137"><dt>MsTscAx.dll</dt></span></span> </dl>   |
| <span data-ttu-id="05504-138">DLL</span><span class="sxs-lookup"><span data-stu-id="05504-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="05504-139"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="05504-139"><dt>MsTscAx.dll</dt></span></span> </dl>   |
| <span data-ttu-id="05504-140">IID</span><span class="sxs-lookup"><span data-stu-id="05504-140">IID</span></span><br/>                      | <span data-ttu-id="05504-141">IID \_ IMsRdpDriveCollection é definido como 7ff17599-da2c-4677-ad35-f60c04fe1585</span><span class="sxs-lookup"><span data-stu-id="05504-141">IID\_IMsRdpDriveCollection is defined as 7ff17599-da2c-4677-ad35-f60c04fe1585</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="05504-142">Consulte também</span><span class="sxs-lookup"><span data-stu-id="05504-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="05504-143">Referência de Conexão Web de Área de Trabalho Remota</span><span class="sxs-lookup"><span data-stu-id="05504-143">Remote Desktop Web Connection Reference</span></span>](remote-desktop-web-connection-reference.md)
</dt> <dt>

[<span data-ttu-id="05504-144">**IMsRdpDrive**</span><span class="sxs-lookup"><span data-stu-id="05504-144">**IMsRdpDrive**</span></span>](imsrdpdrive.md)
</dt> </dl>

 

