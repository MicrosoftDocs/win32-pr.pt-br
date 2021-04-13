---
title: Interface do IMsRdpCameraRedirConfig
description: Representa as configurações de uma câmera que está disponível para redirecionamento.
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota de interface IMsRdpCameraRedirConfig
- Serviços de Área de Trabalho Remota da interface IMsRdpCameraRedirConfig, descrita
topic_type:
- apiref
api_name:
- IMsRdpCameraRedirConfig
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: fbb0f3344e0653ea4a87c876bb8ca7b8a67e7d21
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/19/2020
ms.locfileid: "104500114"
---
# <a name="imsrdpcameraredirconfig-interface"></a><span data-ttu-id="29846-105">Interface do IMsRdpCameraRedirConfig</span><span class="sxs-lookup"><span data-stu-id="29846-105">IMsRdpCameraRedirConfig interface</span></span>

<span data-ttu-id="29846-106">Representa as configurações de uma câmera que está disponível para redirecionamento.</span><span class="sxs-lookup"><span data-stu-id="29846-106">Represents the configurations for a camera that is available for redirection.</span></span>

## <a name="members"></a><span data-ttu-id="29846-107">Membros</span><span class="sxs-lookup"><span data-stu-id="29846-107">Members</span></span>

<span data-ttu-id="29846-108">A interface **IMsRdpCameraRedirConfig** herda de **IUnknown**.</span><span class="sxs-lookup"><span data-stu-id="29846-108">The **IMsRdpCameraRedirConfig** interface inherits from **IUnknown**.</span></span> <span data-ttu-id="29846-109">**IMsRdpCameraRedirConfig** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="29846-109">**IMsRdpCameraRedirConfig** also has these types of members:</span></span>

- [<span data-ttu-id="29846-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="29846-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="29846-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="29846-111">Properties</span></span>

<span data-ttu-id="29846-112">A interface **IMsRdpCameraRedirConfig** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="29846-112">The **IMsRdpCameraRedirConfig** interface has these properties.</span></span>

| <span data-ttu-id="29846-113">Propriedade</span><span class="sxs-lookup"><span data-stu-id="29846-113">Property</span></span>         | <span data-ttu-id="29846-114">Tipo de acesso</span><span class="sxs-lookup"><span data-stu-id="29846-114">Access type</span></span>           | <span data-ttu-id="29846-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="29846-115">Description</span></span>            |
|:-----------------|:----------------------|:-----------------------|
| [<span data-ttu-id="29846-116">**DeviceExists**</span><span class="sxs-lookup"><span data-stu-id="29846-116">**DeviceExists**</span></span>](imsrdpcameraredirconfig-deviceexists.md)      | <span data-ttu-id="29846-117">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="29846-117">Read-only</span></span> | <span data-ttu-id="29846-118">Especifica se o dispositivo de câmera existe ou não no momento (ou seja, a câmera está conectada).</span><span class="sxs-lookup"><span data-stu-id="29846-118">Specifies whether or not the camera device currently exists (that is, the camera is connected).</span></span>   |
| [<span data-ttu-id="29846-119">**FriendlyName**</span><span class="sxs-lookup"><span data-stu-id="29846-119">**FriendlyName**</span></span>](imsrdpcameraredirconfig-friendlyname.md)                       | <span data-ttu-id="29846-120">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="29846-120">Read-only</span></span> |    <span data-ttu-id="29846-121">Obtém o nome amigável da câmera.</span><span class="sxs-lookup"><span data-stu-id="29846-121">Gets the camera’s friendly name.</span></span>    |
| [<span data-ttu-id="29846-122">**InstanceId**</span><span class="sxs-lookup"><span data-stu-id="29846-122">**InstanceId**</span></span>](imsrdpcameraredirconfig-instanceid.md)      | <span data-ttu-id="29846-123">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="29846-123">Read-only</span></span> |  <span data-ttu-id="29846-124">Obtém a ID da instância da câmera.</span><span class="sxs-lookup"><span data-stu-id="29846-124">Gets the instance ID of the camera.</span></span>  |
| [<span data-ttu-id="29846-125">**ParentInstanceId**</span><span class="sxs-lookup"><span data-stu-id="29846-125">**ParentInstanceId**</span></span>](imsrdpcameraredirconfig-parentinstanceid.md)                       | <span data-ttu-id="29846-126">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="29846-126">Read-only</span></span> |    <span data-ttu-id="29846-127">Obtém a ID da instância do dispositivo pai da câmera.</span><span class="sxs-lookup"><span data-stu-id="29846-127">Gets the parent device instance ID of the camera.</span></span>   |
| [<span data-ttu-id="29846-128">**Redirected**</span><span class="sxs-lookup"><span data-stu-id="29846-128">**Redirected**</span></span>](imsrdpcameraredirconfig-redirected.md)      | <span data-ttu-id="29846-129">Leitura/Gravação</span><span class="sxs-lookup"><span data-stu-id="29846-129">Read/Write</span></span> |  <span data-ttu-id="29846-130">Especifica se a câmera é redirecionada ou não.</span><span class="sxs-lookup"><span data-stu-id="29846-130">Specifies whether or not the camera is redirected.</span></span>  |
| [<span data-ttu-id="29846-131">**SymbolicLink**</span><span class="sxs-lookup"><span data-stu-id="29846-131">**SymbolicLink**</span></span>](imsrdpcameraredirconfig-symboliclink.md)                       | <span data-ttu-id="29846-132">Somente leitura</span><span class="sxs-lookup"><span data-stu-id="29846-132">Read-only</span></span> |   <span data-ttu-id="29846-133">Obtém o link simbólico da interface de **KSCATEGORY_VIDEO_CAMERA** para a câmera.</span><span class="sxs-lookup"><span data-stu-id="29846-133">Gets the symbolic link of the **KSCATEGORY_VIDEO_CAMERA** interface for the camera.</span></span>   |

## <a name="requirements"></a><span data-ttu-id="29846-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="29846-134">Requirements</span></span>

| <span data-ttu-id="29846-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="29846-135">Requirement</span></span> | <span data-ttu-id="29846-136">Valor</span><span class="sxs-lookup"><span data-stu-id="29846-136">Value</span></span> |
|-------------------------------------|---------------------------------------|
| <span data-ttu-id="29846-137">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="29846-137">Minimum supported client</span></span>| <span data-ttu-id="29846-138">Windows 10, versão 1803 (build 17134)</span><span class="sxs-lookup"><span data-stu-id="29846-138">Windows 10, version 1803 (build 17134)</span></span>      |
| <span data-ttu-id="29846-139">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="29846-139">Type library</span></span>            | <span data-ttu-id="29846-140">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="29846-140">MsTscAx.dll</span></span>                        |
| <span data-ttu-id="29846-141">DLL</span><span class="sxs-lookup"><span data-stu-id="29846-141">DLL</span></span>                  | <span data-ttu-id="29846-142">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="29846-142">MsTscAx.dll</span></span>     |
| <span data-ttu-id="29846-143">IID</span><span class="sxs-lookup"><span data-stu-id="29846-143">IID</span></span>                      | <span data-ttu-id="29846-144">IID \_ IMsRdpCameraRedirConfig é definido como 09750604-D625-47C1-9FCD-F09F735705D7</span><span class="sxs-lookup"><span data-stu-id="29846-144">IID\_IMsRdpCameraRedirConfig is defined as 09750604-D625-47C1-9FCD-F09F735705D7</span></span>            |

## <a name="see-also"></a><span data-ttu-id="29846-145">Confira também</span><span class="sxs-lookup"><span data-stu-id="29846-145">See also</span></span>

- [<span data-ttu-id="29846-146">**IMsRdpCameraRedirConfigCollection**</span><span class="sxs-lookup"><span data-stu-id="29846-146">**IMsRdpCameraRedirConfigCollection**</span></span>](imsrdpcameraredirconfigcollection.md)
- [<span data-ttu-id="29846-147">**IMsRdpClientNonScriptable7::CameraRedirConfigCollection**</span><span class="sxs-lookup"><span data-stu-id="29846-147">**IMsRdpClientNonScriptable7::CameraRedirConfigCollection**</span></span>](imsrdpclientnonscriptable7-cameraredirconfigcollection.md)