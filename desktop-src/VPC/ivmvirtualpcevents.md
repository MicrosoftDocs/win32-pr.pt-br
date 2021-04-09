---
title: Interface IVMVirtualPCEvents (VPCCOMInterfaces. h)
description: Define a interface de evento de saída para a interface IVMVirtualPC.
ms.assetid: 40ce14d8-43e4-4c72-9729-e5503d882be6
keywords:
- Virtual PC de interface IVMVirtualPCEvents
- Virtual PC de interface IVMVirtualPCEvents, descrito
topic_type:
- apiref
api_name:
- IVMVirtualPCEvents
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c3a6fd22f75027d1424b8605e8e36e373064069
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104009609"
---
# <a name="ivmvirtualpcevents-interface"></a><span data-ttu-id="ad79b-105">Interface IVMVirtualPCEvents</span><span class="sxs-lookup"><span data-stu-id="ad79b-105">IVMVirtualPCEvents interface</span></span>

<span data-ttu-id="ad79b-106">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="ad79b-106">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="ad79b-107">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="ad79b-107">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="ad79b-108">Define a interface de evento de saída para a interface [**IVMVirtualPC**](ivmvirtualpc.md) .</span><span class="sxs-lookup"><span data-stu-id="ad79b-108">Defines the outgoing event interface for the [**IVMVirtualPC**](ivmvirtualpc.md) interface.</span></span> <span data-ttu-id="ad79b-109">O cliente implementa esses métodos para receber eventos enviados do [**IVMVirtualPC**](ivmvirtualpc.md).</span><span class="sxs-lookup"><span data-stu-id="ad79b-109">The client implements these methods to receive events sent from [**IVMVirtualPC**](ivmvirtualpc.md).</span></span>

## <a name="members"></a><span data-ttu-id="ad79b-110">Membros</span><span class="sxs-lookup"><span data-stu-id="ad79b-110">Members</span></span>

<span data-ttu-id="ad79b-111">A interface **IVMVirtualPCEvents** herda da interface [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) .</span><span class="sxs-lookup"><span data-stu-id="ad79b-111">The **IVMVirtualPCEvents** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="ad79b-112">**IVMVirtualPCEvents** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="ad79b-112">**IVMVirtualPCEvents** also has these types of members:</span></span>

-   [<span data-ttu-id="ad79b-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="ad79b-113">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="ad79b-114">Métodos</span><span class="sxs-lookup"><span data-stu-id="ad79b-114">Methods</span></span>

<span data-ttu-id="ad79b-115">A interface **IVMVirtualPCEvents** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="ad79b-115">The **IVMVirtualPCEvents** interface has these methods.</span></span>



| <span data-ttu-id="ad79b-116">Método</span><span class="sxs-lookup"><span data-stu-id="ad79b-116">Method</span></span>                                                        | <span data-ttu-id="ad79b-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="ad79b-117">Description</span></span>                                                                  |
|:--------------------------------------------------------------|:-----------------------------------------------------------------------------|
| [<span data-ttu-id="ad79b-118">**OnEventLogged**</span><span class="sxs-lookup"><span data-stu-id="ad79b-118">**OnEventLogged**</span></span>](ivmvirtualpcevents-oneventlogged.md)     | <span data-ttu-id="ad79b-119">Recebe uma notificação de que o Windows Virtual PC registra um evento.</span><span class="sxs-lookup"><span data-stu-id="ad79b-119">Receives notification that Windows Virtual PC logs an event.</span></span><br/>      |
| [<span data-ttu-id="ad79b-120">**OnVMStateChange**</span><span class="sxs-lookup"><span data-stu-id="ad79b-120">**OnVMStateChange**</span></span>](ivmvirtualpcevents-onvmstatechange.md) | <span data-ttu-id="ad79b-121">Recebe a notificação de que o estado de uma máquina virtual foi alterado.</span><span class="sxs-lookup"><span data-stu-id="ad79b-121">Receives notification that a virtual machine's state has changed.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="ad79b-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ad79b-122">Requirements</span></span>



| <span data-ttu-id="ad79b-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="ad79b-123">Requirement</span></span> | <span data-ttu-id="ad79b-124">Valor</span><span class="sxs-lookup"><span data-stu-id="ad79b-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="ad79b-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ad79b-125">Minimum supported client</span></span><br/> | <span data-ttu-id="ad79b-126">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="ad79b-126">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="ad79b-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ad79b-127">Minimum supported server</span></span><br/> | <span data-ttu-id="ad79b-128">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="ad79b-128">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="ad79b-129">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="ad79b-129">End of client support</span></span><br/>    | <span data-ttu-id="ad79b-130">Windows 7</span><span class="sxs-lookup"><span data-stu-id="ad79b-130">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="ad79b-131">Produto</span><span class="sxs-lookup"><span data-stu-id="ad79b-131">Product</span></span><br/>                  | <span data-ttu-id="ad79b-132">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="ad79b-132">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="ad79b-133">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ad79b-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="ad79b-134"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="ad79b-134"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="ad79b-135">IID</span><span class="sxs-lookup"><span data-stu-id="ad79b-135">IID</span></span><br/>                      | <span data-ttu-id="ad79b-136">DIID \_ IVMVirtualPCEvents é definido como efed1ef1-3c09-41F7-a9c2-7e29fa286c9d</span><span class="sxs-lookup"><span data-stu-id="ad79b-136">DIID\_IVMVirtualPCEvents is defined as efed1ef1-3c09-41f7-a9c2-7e29fa286c9d</span></span><br/>        |



 

