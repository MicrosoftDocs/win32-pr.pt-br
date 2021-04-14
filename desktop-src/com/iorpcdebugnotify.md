---
title: Interface IOrpcDebugNotify
description: Fornece a funcionalidade de depuração remota.
ms.assetid: f91987c0-2e4b-4872-8ed6-e208a23baa49
keywords:
- COM interface IOrpcDebugNotify
- COM interface IOrpcDebugNotify, descrita
topic_type:
- apiref
api_name:
- IOrpcDebugNotify
api_location:
- N/A
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f4db08daf93997b2a7fa0ed383591cb5d111ac7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499800"
---
# <a name="iorpcdebugnotify-interface"></a><span data-ttu-id="e8c1f-105">Interface IOrpcDebugNotify</span><span class="sxs-lookup"><span data-stu-id="e8c1f-105">IOrpcDebugNotify interface</span></span>

<span data-ttu-id="e8c1f-106">Fornece a funcionalidade de depuração remota.</span><span class="sxs-lookup"><span data-stu-id="e8c1f-106">Provides remote debugging functionality.</span></span>

## <a name="when-to-implement"></a><span data-ttu-id="e8c1f-107">Quando implementar</span><span class="sxs-lookup"><span data-stu-id="e8c1f-107">When to implement</span></span>

<span data-ttu-id="e8c1f-108">Implemente essa interface para habilitar a depuração remota via RPC.</span><span class="sxs-lookup"><span data-stu-id="e8c1f-108">Implement this interface to enable remote debugging over RPC.</span></span>

## <a name="when-to-use"></a><span data-ttu-id="e8c1f-109">Quando usar</span><span class="sxs-lookup"><span data-stu-id="e8c1f-109">When to use</span></span>

<span data-ttu-id="e8c1f-110">Essa interface deve ser usada para depuração remota em processo quando exceções de software não devem ser usadas para as notificações do depurador COM.</span><span class="sxs-lookup"><span data-stu-id="e8c1f-110">This interface should be used for in-process remote debugging when software exceptions should not be used for the COM debugger notifications.</span></span> <span data-ttu-id="e8c1f-111">Ele permite que os depuradores em processo sejam notificados por chamadas diretas usando esses métodos.</span><span class="sxs-lookup"><span data-stu-id="e8c1f-111">It enables in-process debuggers to be notified by direct calls using these methods.</span></span>

## <a name="members"></a><span data-ttu-id="e8c1f-112">Membros</span><span class="sxs-lookup"><span data-stu-id="e8c1f-112">Members</span></span>

<span data-ttu-id="e8c1f-113">A interface **IOrpcDebugNotify** herda da interface [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="e8c1f-113">The **IOrpcDebugNotify** interface inherits from the [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="e8c1f-114">**IOrpcDebugNotify** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="e8c1f-114">**IOrpcDebugNotify** also has these types of members:</span></span>

-   [<span data-ttu-id="e8c1f-115">Métodos</span><span class="sxs-lookup"><span data-stu-id="e8c1f-115">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="e8c1f-116">Métodos</span><span class="sxs-lookup"><span data-stu-id="e8c1f-116">Methods</span></span>

<span data-ttu-id="e8c1f-117">A interface **IOrpcDebugNotify** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="e8c1f-117">The **IOrpcDebugNotify** interface has these methods.</span></span>



| <span data-ttu-id="e8c1f-118">Método</span><span class="sxs-lookup"><span data-stu-id="e8c1f-118">Method</span></span>                                                              | <span data-ttu-id="e8c1f-119">Descrição</span><span class="sxs-lookup"><span data-stu-id="e8c1f-119">Description</span></span>                                                                    |
|:--------------------------------------------------------------------|:-------------------------------------------------------------------------------|
| [<span data-ttu-id="e8c1f-120">**ClientFillBuffer**</span><span class="sxs-lookup"><span data-stu-id="e8c1f-120">**ClientFillBuffer**</span></span>](iorpcdebugnotify-clientfillbuffer.md)       | <span data-ttu-id="e8c1f-121">Envia dados do depurador do cliente para o depurador do servidor.</span><span class="sxs-lookup"><span data-stu-id="e8c1f-121">Sends data from the client debugger to the server debugger.</span></span><br/>         |
| [<span data-ttu-id="e8c1f-122">**ClientGetBufferSize**</span><span class="sxs-lookup"><span data-stu-id="e8c1f-122">**ClientGetBufferSize**</span></span>](iorpcdebugnotify-clientgetbuffersize.md) | <span data-ttu-id="e8c1f-123">Recupera o tamanho do buffer RPC do depurador do lado do cliente.</span><span class="sxs-lookup"><span data-stu-id="e8c1f-123">Retrieves the RPC buffer size from the client-side debugger.</span></span><br/>        |
| [<span data-ttu-id="e8c1f-124">**ClientNotify**</span><span class="sxs-lookup"><span data-stu-id="e8c1f-124">**ClientNotify**</span></span>](iorpcdebugnotify-clientnotify.md)               | <span data-ttu-id="e8c1f-125">Informa ao cliente uma solicitação de depuração de saída para o servidor.</span><span class="sxs-lookup"><span data-stu-id="e8c1f-125">Informs the client of an outgoing debugger request to the server.</span></span><br/>   |
| [<span data-ttu-id="e8c1f-126">**ServerFillBuffer**</span><span class="sxs-lookup"><span data-stu-id="e8c1f-126">**ServerFillBuffer**</span></span>](iorpcdebugnotify-serverfillbuffer.md)       | <span data-ttu-id="e8c1f-127">Envia dados do depurador do servidor para o depurador do cliente.</span><span class="sxs-lookup"><span data-stu-id="e8c1f-127">Sends data from the server debugger to the client debugger.</span></span><br/>         |
| [<span data-ttu-id="e8c1f-128">**ServerGetBufferSize**</span><span class="sxs-lookup"><span data-stu-id="e8c1f-128">**ServerGetBufferSize**</span></span>](iorpcdebugnotify-servergetbuffersize.md) | <span data-ttu-id="e8c1f-129">Recupera o tamanho do buffer RPC do depurador do lado do servidor.</span><span class="sxs-lookup"><span data-stu-id="e8c1f-129">Retrieves the RPC buffer size from the server-side debugger.</span></span><br/>        |
| [<span data-ttu-id="e8c1f-130">**ServerNotify**</span><span class="sxs-lookup"><span data-stu-id="e8c1f-130">**ServerNotify**</span></span>](iorpcdebugnotify-servernotify.md)               | <span data-ttu-id="e8c1f-131">Informa ao servidor de uma solicitação de entrada do depurador do cliente.</span><span class="sxs-lookup"><span data-stu-id="e8c1f-131">Informs the server of an incoming debugger request from the client.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="e8c1f-132">Comentários</span><span class="sxs-lookup"><span data-stu-id="e8c1f-132">Remarks</span></span>

<span data-ttu-id="e8c1f-133">Uma biblioteca de importação que contém a interface **IOrpcDebugNotify** não está incluída no SDK (Software Development Kit) do Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="e8c1f-133">An import library containing the **IOrpcDebugNotify** interface is not included in the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="e8c1f-134">Um aplicativo pode usar as funções [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) e [**GetModuleHandle**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea) para recuperar um ponteiro de função para [**DllDebugObjectRPCHook**](dlldebugobjectrpchook.md) de oleaut.dll e fornecer esses métodos por meio da interface **IOrpcDebugNotify** .</span><span class="sxs-lookup"><span data-stu-id="e8c1f-134">An application can use the [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) and [**GetModuleHandle**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea) functions to retrieve a function pointer to [**DllDebugObjectRPCHook**](dlldebugobjectrpchook.md) from oleaut.dll and provide these methods via the **IOrpcDebugNotify** interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="e8c1f-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e8c1f-135">Requirements</span></span>



| <span data-ttu-id="e8c1f-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="e8c1f-136">Requirement</span></span> | <span data-ttu-id="e8c1f-137">Valor</span><span class="sxs-lookup"><span data-stu-id="e8c1f-137">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------|
| <span data-ttu-id="e8c1f-138">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e8c1f-138">Minimum supported client</span></span><br/> | <span data-ttu-id="e8c1f-139">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="e8c1f-139">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                     |
| <span data-ttu-id="e8c1f-140">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e8c1f-140">Minimum supported server</span></span><br/> | <span data-ttu-id="e8c1f-141">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="e8c1f-141">Windows 2000 Server \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="e8c1f-142">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="e8c1f-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="e8c1f-143"><dt>N/A</dt></span><span class="sxs-lookup"><span data-stu-id="e8c1f-143"><dt>N/A</dt></span></span> </dl> |
| <span data-ttu-id="e8c1f-144">INSERI</span><span class="sxs-lookup"><span data-stu-id="e8c1f-144">IDL</span></span><br/>                      | <dl> <span data-ttu-id="e8c1f-145"><dt>N/A</dt></span><span class="sxs-lookup"><span data-stu-id="e8c1f-145"><dt>N/A</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e8c1f-146">Confira também</span><span class="sxs-lookup"><span data-stu-id="e8c1f-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e8c1f-147">**IUnknown**</span><span class="sxs-lookup"><span data-stu-id="e8c1f-147">**IUnknown**</span></span>](/windows/desktop/api/Unknwn/nn-unknwn-iunknown)
</dt> <dt>

[<span data-ttu-id="e8c1f-148">**ORPC \_ DBG \_ All**</span><span class="sxs-lookup"><span data-stu-id="e8c1f-148">**ORPC\_DBG\_ALL**</span></span>](orpc-dbg-all.md)
</dt> <dt>

[<span data-ttu-id="e8c1f-149">**\_buffer de DBG ORPC \_**</span><span class="sxs-lookup"><span data-stu-id="e8c1f-149">**ORPC\_DBG\_BUFFER**</span></span>](orpc-dbg-buffer.md)
</dt> <dt>

[<span data-ttu-id="e8c1f-150">**\_argumentos de inicialização ORPC \_**</span><span class="sxs-lookup"><span data-stu-id="e8c1f-150">**ORPC\_INIT\_ARGS**</span></span>](orpc-init-args.md)
</dt> <dt>

[<span data-ttu-id="e8c1f-151">**DllDebugObjectRPCHook**</span><span class="sxs-lookup"><span data-stu-id="e8c1f-151">**DllDebugObjectRPCHook**</span></span>](dlldebugobjectrpchook.md)
</dt> </dl>

 

