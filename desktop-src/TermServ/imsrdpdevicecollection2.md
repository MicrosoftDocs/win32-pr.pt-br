---
title: Interface IMsRdpDeviceCollection2
description: Representa uma coleção de objetos de dispositivo. Esse é um aprimoramento da interface IMsRdpDeviceCollection.
ms.assetid: df4d704c-e031-4df1-aed1-11aacf8a6992
ms.tgt_platform: multiple
keywords:
- Serviços de Área de Trabalho Remota de interface IMsRdpDeviceCollection2
- Serviços de Área de Trabalho Remota da interface IMsRdpDeviceCollection2, descrita
topic_type:
- apiref
api_name:
- IMsRdpDeviceCollection2
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ea35c0a66ad8bf5d291062eafb7be3ceae4ac58
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105759940"
---
# <a name="imsrdpdevicecollection2-interface"></a><span data-ttu-id="a0fe2-106">Interface IMsRdpDeviceCollection2</span><span class="sxs-lookup"><span data-stu-id="a0fe2-106">IMsRdpDeviceCollection2 interface</span></span>

<span data-ttu-id="a0fe2-107">Representa uma coleção de objetos de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a0fe2-107">Represents a collection of device objects.</span></span> <span data-ttu-id="a0fe2-108">Esse é um aprimoramento da interface [**IMsRdpDeviceCollection**](imsrdpdevicecollection.md) .</span><span class="sxs-lookup"><span data-stu-id="a0fe2-108">This is an enhancement to the [**IMsRdpDeviceCollection**](imsrdpdevicecollection.md) interface.</span></span>

## <a name="members"></a><span data-ttu-id="a0fe2-109">Membros</span><span class="sxs-lookup"><span data-stu-id="a0fe2-109">Members</span></span>

<span data-ttu-id="a0fe2-110">A interface **IMsRdpDeviceCollection2** herda de [**IMsRdpDeviceCollection**](imsrdpdevicecollection.md).</span><span class="sxs-lookup"><span data-stu-id="a0fe2-110">The **IMsRdpDeviceCollection2** interface inherits from [**IMsRdpDeviceCollection**](imsrdpdevicecollection.md).</span></span> <span data-ttu-id="a0fe2-111">**IMsRdpDeviceCollection2** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="a0fe2-111">**IMsRdpDeviceCollection2** also has these types of members:</span></span>

-   [<span data-ttu-id="a0fe2-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="a0fe2-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="a0fe2-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="a0fe2-113">Methods</span></span>

<span data-ttu-id="a0fe2-114">A interface **IMsRdpDeviceCollection2** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="a0fe2-114">The **IMsRdpDeviceCollection2** interface has these methods.</span></span>



| <span data-ttu-id="a0fe2-115">Método</span><span class="sxs-lookup"><span data-stu-id="a0fe2-115">Method</span></span>                                                                         | <span data-ttu-id="a0fe2-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="a0fe2-116">Description</span></span>                                                                                                 |
|:-------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a0fe2-117">**AddDeviceByInstanceId**</span><span class="sxs-lookup"><span data-stu-id="a0fe2-117">**AddDeviceByInstanceId**</span></span>](imsrdpdevicecollection2-adddevicebyinstanceid.md) | <span data-ttu-id="a0fe2-118">Adiciona um dispositivo não listado à coleção de dispositivos.</span><span class="sxs-lookup"><span data-stu-id="a0fe2-118">Adds an unlisted device to the device collection.</span></span><br/>                                                |
| [<span data-ttu-id="a0fe2-119">**RedirectNow**</span><span class="sxs-lookup"><span data-stu-id="a0fe2-119">**RedirectNow**</span></span>](imsrdpdevicecollection2-redirectnow.md)                     | <span data-ttu-id="a0fe2-120">Força os dispositivos que foram selecionados ou desmarcados da coleção a serem redirecionados ou removidos.</span><span class="sxs-lookup"><span data-stu-id="a0fe2-120">Forces devices that were selected or unselected from the collection to be redirected or removed.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="a0fe2-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a0fe2-121">Requirements</span></span>



| <span data-ttu-id="a0fe2-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="a0fe2-122">Requirement</span></span> | <span data-ttu-id="a0fe2-123">Valor</span><span class="sxs-lookup"><span data-stu-id="a0fe2-123">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="a0fe2-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a0fe2-124">Minimum supported client</span></span><br/> | <span data-ttu-id="a0fe2-125">Windows 8</span><span class="sxs-lookup"><span data-stu-id="a0fe2-125">Windows 8</span></span><br/>                                                                       |
| <span data-ttu-id="a0fe2-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a0fe2-126">Minimum supported server</span></span><br/> | <span data-ttu-id="a0fe2-127">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="a0fe2-127">Windows Server 2012</span></span><br/>                                                             |
| <span data-ttu-id="a0fe2-128">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="a0fe2-128">Type library</span></span><br/>             | <dl> <span data-ttu-id="a0fe2-129"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a0fe2-129"><dt>MsTscAx.dll</dt></span></span> </dl>     |
| <span data-ttu-id="a0fe2-130">DLL</span><span class="sxs-lookup"><span data-stu-id="a0fe2-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a0fe2-131"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a0fe2-131"><dt>MsTscAx.dll</dt></span></span> </dl>     |
| <span data-ttu-id="a0fe2-132">IID</span><span class="sxs-lookup"><span data-stu-id="a0fe2-132">IID</span></span><br/>                      | <span data-ttu-id="a0fe2-133">IID \_ IMsRdpDeviceCollection2 é definido como e0e5d68a-f2e7-4350-ADFE-ac0e08d74de0</span><span class="sxs-lookup"><span data-stu-id="a0fe2-133">IID\_IMsRdpDeviceCollection2 is defined as e0e5d68a-f2e7-4350-adfe-ac0e08d74de0</span></span><br/> |



 

 





