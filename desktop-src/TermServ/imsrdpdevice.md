---
title: Interface IMsRdpDevice
description: Contém informações sobre um objeto de dispositivo.
ms.assetid: b486a591-870b-446c-8028-9e4406cdf0ce
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota de interface IMsRdpDevice
- Serviços de Área de Trabalho Remota da interface IMsRdpDevice, descrita
topic_type:
- apiref
api_name:
- IMsRdpDevice
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d7ddfbb739a8cf8e93ee2c2214e14095ac68bd77
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105754168"
---
# <a name="imsrdpdevice-interface"></a><span data-ttu-id="ab27e-105">Interface IMsRdpDevice</span><span class="sxs-lookup"><span data-stu-id="ab27e-105">IMsRdpDevice interface</span></span>

<span data-ttu-id="ab27e-106">Contém informações sobre um objeto de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ab27e-106">Contains information about a device object.</span></span>

## <a name="members"></a><span data-ttu-id="ab27e-107">Membros</span><span class="sxs-lookup"><span data-stu-id="ab27e-107">Members</span></span>

<span data-ttu-id="ab27e-108">A interface **IMsRdpDevice** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="ab27e-108">The **IMsRdpDevice** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="ab27e-109">**IMsRdpDevice** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="ab27e-109">**IMsRdpDevice** also has these types of members:</span></span>

-   [<span data-ttu-id="ab27e-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="ab27e-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="ab27e-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="ab27e-111">Properties</span></span>

<span data-ttu-id="ab27e-112">A interface **IMsRdpDevice** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="ab27e-112">The **IMsRdpDevice** interface has these properties.</span></span>



| <span data-ttu-id="ab27e-113">Propriedade</span><span class="sxs-lookup"><span data-stu-id="ab27e-113">Property</span></span>                                                               | <span data-ttu-id="ab27e-114">Tipo de acesso</span><span class="sxs-lookup"><span data-stu-id="ab27e-114">Access type</span></span>           | <span data-ttu-id="ab27e-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="ab27e-115">Description</span></span>                                                                                                   |
|:-----------------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ab27e-116">**DeviceDescription**</span><span class="sxs-lookup"><span data-stu-id="ab27e-116">**DeviceDescription**</span></span>](imsrdpdevice-devicedescription.md)<br/> | <span data-ttu-id="ab27e-117">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ab27e-117">Read-only</span></span><br/>  | <span data-ttu-id="ab27e-118">Recupera a descrição do dispositivo a ser exibida para o usuário se o nome para exibição não estiver disponível.</span><span class="sxs-lookup"><span data-stu-id="ab27e-118">Retrieves the device description to be displayed to the user if the display name is not available.</span></span><br/> |
| [<span data-ttu-id="ab27e-119">**DeviceInstanceId**</span><span class="sxs-lookup"><span data-stu-id="ab27e-119">**DeviceInstanceId**</span></span>](imsrdpdevice-deviceinstanceid.md)<br/>   | <span data-ttu-id="ab27e-120">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ab27e-120">Read-only</span></span><br/>  | <span data-ttu-id="ab27e-121">Recupera o identificador da instância de dispositivo do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ab27e-121">Retrieves the device instance identifier of the device.</span></span><br/>                                            |
| [<span data-ttu-id="ab27e-122">**FriendlyName**</span><span class="sxs-lookup"><span data-stu-id="ab27e-122">**FriendlyName**</span></span>](imsrdpdevice-friendlyname.md)<br/>           | <span data-ttu-id="ab27e-123">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="ab27e-123">Read-only</span></span><br/>  | <span data-ttu-id="ab27e-124">Recupera o nome de exibição do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ab27e-124">Retrieves the display name for the device.</span></span><br/>                                                         |
| [<span data-ttu-id="ab27e-125">**De redirecionamento**</span><span class="sxs-lookup"><span data-stu-id="ab27e-125">**RedirectionState**</span></span>](imsrdpdevice-redirectionstate.md)<br/>   | <span data-ttu-id="ab27e-126">Leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="ab27e-126">Read/write</span></span><br/> | <span data-ttu-id="ab27e-127">Indica o estado de redirecionamento do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ab27e-127">Indicates the redirection state of the device.</span></span><br/>                                                     |



 

## <a name="requirements"></a><span data-ttu-id="ab27e-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ab27e-128">Requirements</span></span>



| <span data-ttu-id="ab27e-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="ab27e-129">Requirement</span></span> | <span data-ttu-id="ab27e-130">Valor</span><span class="sxs-lookup"><span data-stu-id="ab27e-130">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ab27e-131">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ab27e-131">Minimum supported client</span></span><br/> | <span data-ttu-id="ab27e-132">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ab27e-132">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="ab27e-133">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ab27e-133">Minimum supported server</span></span><br/> | <span data-ttu-id="ab27e-134">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ab27e-134">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="ab27e-135">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="ab27e-135">Type library</span></span><br/>             | <dl> <span data-ttu-id="ab27e-136"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ab27e-136"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="ab27e-137">DLL</span><span class="sxs-lookup"><span data-stu-id="ab27e-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ab27e-138"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ab27e-138"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="ab27e-139">IID</span><span class="sxs-lookup"><span data-stu-id="ab27e-139">IID</span></span><br/>                      | <span data-ttu-id="ab27e-140">IID \_ IMsRdpDevice é definido como 60c3b9c8-9e92-4f5e-a3e7-604a912093ea</span><span class="sxs-lookup"><span data-stu-id="ab27e-140">IID\_IMsRdpDevice is defined as 60c3b9c8-9e92-4f5e-a3e7-604a912093ea</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="ab27e-141">Confira também</span><span class="sxs-lookup"><span data-stu-id="ab27e-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ab27e-142">Referência de Conexão Web de Área de Trabalho Remota</span><span class="sxs-lookup"><span data-stu-id="ab27e-142">Remote Desktop Web Connection Reference</span></span>](remote-desktop-web-connection-reference.md)
</dt> <dt>

[<span data-ttu-id="ab27e-143">**IMsRdpDeviceCollection**</span><span class="sxs-lookup"><span data-stu-id="ab27e-143">**IMsRdpDeviceCollection**</span></span>](imsrdpdevicecollection.md)
</dt> </dl>

 

