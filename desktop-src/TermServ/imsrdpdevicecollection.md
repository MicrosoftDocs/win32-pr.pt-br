---
title: Interface IMsRdpDeviceCollection
description: Representa uma coleção de objetos de dispositivo.
ms.assetid: 9731b16b-12e0-457e-a4e5-a55d8a6db582
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota de interface IMsRdpDeviceCollection
- Serviços de Área de Trabalho Remota da interface IMsRdpDeviceCollection, descrita
topic_type:
- apiref
api_name:
- IMsRdpDeviceCollection
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cace1bc684be4e3e8cf20db84ec8923c9b35a8fa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104369228"
---
# <a name="imsrdpdevicecollection-interface"></a><span data-ttu-id="2d08b-105">Interface IMsRdpDeviceCollection</span><span class="sxs-lookup"><span data-stu-id="2d08b-105">IMsRdpDeviceCollection interface</span></span>

<span data-ttu-id="2d08b-106">Representa uma coleção de objetos de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="2d08b-106">Represents a collection of device objects.</span></span>

## <a name="members"></a><span data-ttu-id="2d08b-107">Membros</span><span class="sxs-lookup"><span data-stu-id="2d08b-107">Members</span></span>

<span data-ttu-id="2d08b-108">A interface **IMsRdpDeviceCollection** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="2d08b-108">The **IMsRdpDeviceCollection** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="2d08b-109">**IMsRdpDeviceCollection** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="2d08b-109">**IMsRdpDeviceCollection** also has these types of members:</span></span>

-   [<span data-ttu-id="2d08b-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="2d08b-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="2d08b-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="2d08b-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="2d08b-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="2d08b-112">Methods</span></span>

<span data-ttu-id="2d08b-113">A interface **IMsRdpDeviceCollection** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="2d08b-113">The **IMsRdpDeviceCollection** interface has these methods.</span></span>



| <span data-ttu-id="2d08b-114">Método</span><span class="sxs-lookup"><span data-stu-id="2d08b-114">Method</span></span>                                                        | <span data-ttu-id="2d08b-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="2d08b-115">Description</span></span>                                                 |
|:--------------------------------------------------------------|:------------------------------------------------------------|
| [<span data-ttu-id="2d08b-116">**RescanDevices**</span><span class="sxs-lookup"><span data-stu-id="2d08b-116">**RescanDevices**</span></span>](imsrdpdevicecollection-rescandevices.md) | <span data-ttu-id="2d08b-117">Atualiza a lista de objetos na coleção.</span><span class="sxs-lookup"><span data-stu-id="2d08b-117">Refreshes the list of objects in the collection.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="2d08b-118">Propriedades</span><span class="sxs-lookup"><span data-stu-id="2d08b-118">Properties</span></span>

<span data-ttu-id="2d08b-119">A interface **IMsRdpDeviceCollection** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="2d08b-119">The **IMsRdpDeviceCollection** interface has these properties.</span></span>



| <span data-ttu-id="2d08b-120">Propriedade</span><span class="sxs-lookup"><span data-stu-id="2d08b-120">Property</span></span>                                                                 | <span data-ttu-id="2d08b-121">Tipo de acesso</span><span class="sxs-lookup"><span data-stu-id="2d08b-121">Access type</span></span>          | <span data-ttu-id="2d08b-122">Descrição</span><span class="sxs-lookup"><span data-stu-id="2d08b-122">Description</span></span>                                                    |
|:-------------------------------------------------------------------------|:---------------------|:---------------------------------------------------------------|
| [<span data-ttu-id="2d08b-123">**DeviceById**</span><span class="sxs-lookup"><span data-stu-id="2d08b-123">**DeviceById**</span></span>](imsrdpdevicecollection-devicebyid.md)<br/>       | <span data-ttu-id="2d08b-124">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2d08b-124">Read-only</span></span><br/> | <span data-ttu-id="2d08b-125">Recupera o dispositivo com o identificador especificado.</span><span class="sxs-lookup"><span data-stu-id="2d08b-125">Retrieves the device with the specified identifier.</span></span><br/> |
| [<span data-ttu-id="2d08b-126">**DeviceByIndex**</span><span class="sxs-lookup"><span data-stu-id="2d08b-126">**DeviceByIndex**</span></span>](imsrdpdevicecollection-devicebyindex.md)<br/> | <span data-ttu-id="2d08b-127">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2d08b-127">Read-only</span></span><br/> | <span data-ttu-id="2d08b-128">Recupera o dispositivo no índice especificado.</span><span class="sxs-lookup"><span data-stu-id="2d08b-128">Retrieves the device at the specified index.</span></span><br/>        |
| [<span data-ttu-id="2d08b-129">**DeviceCount**</span><span class="sxs-lookup"><span data-stu-id="2d08b-129">**DeviceCount**</span></span>](imsrdpdevicecollection-devicecount.md)<br/>     | <span data-ttu-id="2d08b-130">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2d08b-130">Read-only</span></span><br/> | <span data-ttu-id="2d08b-131">Recupera a contagem de objetos na coleção.</span><span class="sxs-lookup"><span data-stu-id="2d08b-131">Retrieves the count of objects in the collection.</span></span><br/>   |



 

## <a name="requirements"></a><span data-ttu-id="2d08b-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2d08b-132">Requirements</span></span>



| <span data-ttu-id="2d08b-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="2d08b-133">Requirement</span></span> | <span data-ttu-id="2d08b-134">Valor</span><span class="sxs-lookup"><span data-stu-id="2d08b-134">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="2d08b-135">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2d08b-135">Minimum supported client</span></span><br/> | <span data-ttu-id="2d08b-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2d08b-136">Windows Vista</span></span><br/>                                                                  |
| <span data-ttu-id="2d08b-137">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2d08b-137">Minimum supported server</span></span><br/> | <span data-ttu-id="2d08b-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2d08b-138">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="2d08b-139">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="2d08b-139">Type library</span></span><br/>             | <dl> <span data-ttu-id="2d08b-140"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2d08b-140"><dt>MsTscAx.dll</dt></span></span> </dl>    |
| <span data-ttu-id="2d08b-141">DLL</span><span class="sxs-lookup"><span data-stu-id="2d08b-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2d08b-142"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2d08b-142"><dt>MsTscAx.dll</dt></span></span> </dl>    |
| <span data-ttu-id="2d08b-143">IID</span><span class="sxs-lookup"><span data-stu-id="2d08b-143">IID</span></span><br/>                      | <span data-ttu-id="2d08b-144">IID \_ IMsRdpDeviceCollection é definido como 56540617-D281-488c-8738-6a8fdf64a118</span><span class="sxs-lookup"><span data-stu-id="2d08b-144">IID\_IMsRdpDeviceCollection is defined as 56540617-d281-488c-8738-6a8fdf64a118</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="2d08b-145">Confira também</span><span class="sxs-lookup"><span data-stu-id="2d08b-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2d08b-146">Referência de Conexão Web de Área de Trabalho Remota</span><span class="sxs-lookup"><span data-stu-id="2d08b-146">Remote Desktop Web Connection Reference</span></span>](remote-desktop-web-connection-reference.md)
</dt> <dt>

[<span data-ttu-id="2d08b-147">**IMsRdpDevice**</span><span class="sxs-lookup"><span data-stu-id="2d08b-147">**IMsRdpDevice**</span></span>](imsrdpdevice.md)
</dt> </dl>

 

