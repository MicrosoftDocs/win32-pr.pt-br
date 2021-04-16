---
title: Interface IMsRdpDeviceV2
description: Contém informações sobre um objeto de dispositivo. Esse é um aprimoramento da interface IMsRdpDevice.
ms.assetid: 9a380a1a-d44f-4147-8917-bf1e07dbac15
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota de interface IMsRdpDeviceV2
- Serviços de Área de Trabalho Remota da interface IMsRdpDeviceV2, descrita
topic_type:
- apiref
api_name:
- IMsRdpDeviceV2
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c46e1e4df8f9cd521d67383960e9ccf5060bb2d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105757933"
---
# <a name="imsrdpdevicev2-interface"></a><span data-ttu-id="fcdc3-106">Interface IMsRdpDeviceV2</span><span class="sxs-lookup"><span data-stu-id="fcdc3-106">IMsRdpDeviceV2 interface</span></span>

<span data-ttu-id="fcdc3-107">Contém informações sobre um objeto de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="fcdc3-107">Contains information about a device object.</span></span> <span data-ttu-id="fcdc3-108">Esse é um aprimoramento da interface [**IMsRdpDevice**](imsrdpdevice.md) .</span><span class="sxs-lookup"><span data-stu-id="fcdc3-108">This is an enhancement of the [**IMsRdpDevice**](imsrdpdevice.md) interface.</span></span>

## <a name="members"></a><span data-ttu-id="fcdc3-109">Membros</span><span class="sxs-lookup"><span data-stu-id="fcdc3-109">Members</span></span>

<span data-ttu-id="fcdc3-110">A interface **IMsRdpDeviceV2** herda de [**IMsRdpDevice**](imsrdpdevice.md).</span><span class="sxs-lookup"><span data-stu-id="fcdc3-110">The **IMsRdpDeviceV2** interface inherits from [**IMsRdpDevice**](imsrdpdevice.md).</span></span> <span data-ttu-id="fcdc3-111">**IMsRdpDeviceV2** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="fcdc3-111">**IMsRdpDeviceV2** also has these types of members:</span></span>

-   [<span data-ttu-id="fcdc3-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="fcdc3-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="fcdc3-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="fcdc3-113">Properties</span></span>

<span data-ttu-id="fcdc3-114">A interface **IMsRdpDeviceV2** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="fcdc3-114">The **IMsRdpDeviceV2** interface has these properties.</span></span>



| <span data-ttu-id="fcdc3-115">Propriedade</span><span class="sxs-lookup"><span data-stu-id="fcdc3-115">Property</span></span>                                                                 | <span data-ttu-id="fcdc3-116">Tipo de acesso</span><span class="sxs-lookup"><span data-stu-id="fcdc3-116">Access type</span></span>          | <span data-ttu-id="fcdc3-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="fcdc3-117">Description</span></span>                                                                                        |
|:-------------------------------------------------------------------------|:---------------------|:---------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="fcdc3-118">**CmClassGuid**</span><span class="sxs-lookup"><span data-stu-id="fcdc3-118">**CmClassGuid**</span></span>](imsrdpdevicev2-cmclassguid.md)<br/>             | <span data-ttu-id="fcdc3-119">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fcdc3-119">Read-only</span></span><br/> | <span data-ttu-id="fcdc3-120">Contém o GUID da classe de instalação do Configuration Manager para o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="fcdc3-120">Contains the configuration manager setup class GUID for the device.</span></span><br/>                     |
| [<span data-ttu-id="fcdc3-121">**CmDeviceInstance**</span><span class="sxs-lookup"><span data-stu-id="fcdc3-121">**CmDeviceInstance**</span></span>](imsrdpdevicev2-cmdeviceinstance.md)<br/>   | <span data-ttu-id="fcdc3-122">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fcdc3-122">Read-only</span></span><br/> | <span data-ttu-id="fcdc3-123">Contém a instância de dispositivo do Configuration Manager do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="fcdc3-123">Contains the configuration manager device instance of the device.</span></span><br/>                       |
| [<span data-ttu-id="fcdc3-124">**DeviceText**</span><span class="sxs-lookup"><span data-stu-id="fcdc3-124">**DeviceText**</span></span>](imsrdpdevicev2-devicetext.md)<br/>               | <span data-ttu-id="fcdc3-125">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fcdc3-125">Read-only</span></span><br/> | <span data-ttu-id="fcdc3-126">Contém o texto do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="fcdc3-126">Contains the device text.</span></span><br/>                                                               |
| [<span data-ttu-id="fcdc3-127">**DriveLetterBitmap**</span><span class="sxs-lookup"><span data-stu-id="fcdc3-127">**DriveLetterBitmap**</span></span>](imsrdpdevicev2-driveletterbitmap.md)<br/> | <span data-ttu-id="fcdc3-128">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fcdc3-128">Read-only</span></span><br/> | <span data-ttu-id="fcdc3-129">Contém um campo de bits que representa um mapa de letras de unidade contidas no dispositivo.</span><span class="sxs-lookup"><span data-stu-id="fcdc3-129">Contains a bitfield that represents a map of drive letters contained within the device.</span></span><br/> |
| [<span data-ttu-id="fcdc3-130">**IsCompositeDevice**</span><span class="sxs-lookup"><span data-stu-id="fcdc3-130">**IsCompositeDevice**</span></span>](imsrdpdevicev2-iscompositedevice.md)<br/> | <span data-ttu-id="fcdc3-131">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fcdc3-131">Read-only</span></span><br/> | <span data-ttu-id="fcdc3-132">Especifica se o dispositivo é um dispositivo composto.</span><span class="sxs-lookup"><span data-stu-id="fcdc3-132">Specifies if the device is a composite device.</span></span><br/>                                          |
| [<span data-ttu-id="fcdc3-133">**IsOptionalDevice**</span><span class="sxs-lookup"><span data-stu-id="fcdc3-133">**IsOptionalDevice**</span></span>](imsrdpdevicev2-isoptionaldevice.md)<br/>   | <span data-ttu-id="fcdc3-134">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fcdc3-134">Read-only</span></span><br/> | <span data-ttu-id="fcdc3-135">Especifica se o dispositivo é opcional para o redirecionamento de USB.</span><span class="sxs-lookup"><span data-stu-id="fcdc3-135">Specifies if the device is optional for USB redirection.</span></span><br/>                                |
| [<span data-ttu-id="fcdc3-136">**IsUSBDevice**</span><span class="sxs-lookup"><span data-stu-id="fcdc3-136">**IsUSBDevice**</span></span>](imsrdpdevicev2-isusbdevice.md)<br/>             | <span data-ttu-id="fcdc3-137">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fcdc3-137">Read-only</span></span><br/> | <span data-ttu-id="fcdc3-138">Especifica se o dispositivo é para o redirecionamento de USB.</span><span class="sxs-lookup"><span data-stu-id="fcdc3-138">Specifies if the device is for USB redirection.</span></span><br/>                                         |



 

## <a name="requirements"></a><span data-ttu-id="fcdc3-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fcdc3-139">Requirements</span></span>



| <span data-ttu-id="fcdc3-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="fcdc3-140">Requirement</span></span> | <span data-ttu-id="fcdc3-141">Valor</span><span class="sxs-lookup"><span data-stu-id="fcdc3-141">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="fcdc3-142">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fcdc3-142">Minimum supported client</span></span><br/> | <span data-ttu-id="fcdc3-143">Windows 7 com SP1</span><span class="sxs-lookup"><span data-stu-id="fcdc3-143">Windows 7 with SP1</span></span><br/>                                                          |
| <span data-ttu-id="fcdc3-144">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fcdc3-144">Minimum supported server</span></span><br/> | <span data-ttu-id="fcdc3-145">Windows Server 2008 R2 com SP1</span><span class="sxs-lookup"><span data-stu-id="fcdc3-145">Windows Server 2008 R2 with SP1</span></span><br/>                                             |
| <span data-ttu-id="fcdc3-146">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="fcdc3-146">Type library</span></span><br/>             | <dl> <span data-ttu-id="fcdc3-147"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fcdc3-147"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="fcdc3-148">DLL</span><span class="sxs-lookup"><span data-stu-id="fcdc3-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fcdc3-149"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fcdc3-149"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="fcdc3-150">IID</span><span class="sxs-lookup"><span data-stu-id="fcdc3-150">IID</span></span><br/>                      | <span data-ttu-id="fcdc3-151">IID \_ IMsRdpDeviceV2 é definido como 5fb94466-7661-42a8-98b7-01904c11668f</span><span class="sxs-lookup"><span data-stu-id="fcdc3-151">IID\_IMsRdpDeviceV2 is defined as 5fb94466-7661-42a8-98b7-01904c11668f</span></span><br/>      |



 

 





