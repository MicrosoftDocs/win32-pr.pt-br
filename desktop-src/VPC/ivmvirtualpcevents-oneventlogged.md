---
title: Método IVMVirtualPCEvents OnEventLogged (VPCCOMInterfaces. h)
description: Recebe uma notificação de que o Windows Virtual PC registra um evento.
ms.assetid: 89439e8e-e9bf-409e-a129-525b9feb8fdd
keywords:
- OnEventLogged do método virtual PC
- Método OnEventLogged Virtual PC, interface IVMVirtualPCEvents
- IVMVirtualPCEvents interface virtual PC, método OnEventLogged
topic_type:
- apiref
api_name:
- IVMVirtualPCEvents.OnEventLogged
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 196d480383f488c9c0885e95857c8d1a053d5887
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104499450"
---
# <a name="ivmvirtualpceventsoneventlogged-method"></a><span data-ttu-id="a9359-106">Método IVMVirtualPCEvents:: OnEventLogged</span><span class="sxs-lookup"><span data-stu-id="a9359-106">IVMVirtualPCEvents::OnEventLogged method</span></span>

<span data-ttu-id="a9359-107">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="a9359-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="a9359-108">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="a9359-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="a9359-109">Recebe uma notificação de que o Windows Virtual PC registra um evento.</span><span class="sxs-lookup"><span data-stu-id="a9359-109">Receives notification that Windows Virtual PC logs an event.</span></span>

## <a name="syntax"></a><span data-ttu-id="a9359-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a9359-110">Syntax</span></span>


```C++
HRESULT OnEventLogged(
  [in] long logMessageID
);
```



## <a name="parameters"></a><span data-ttu-id="a9359-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a9359-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a9359-112">*logMessageID* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="a9359-112">*logMessageID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a9359-113">O identificador de mensagem da mensagem de log de eventos que foi registrada.</span><span class="sxs-lookup"><span data-stu-id="a9359-113">The message identifier of the event log message that was logged.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a9359-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a9359-114">Return value</span></span>

<span data-ttu-id="a9359-115">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="a9359-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="a9359-116">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="a9359-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="a9359-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="a9359-117">Remarks</span></span>

<span data-ttu-id="a9359-118">Esse método é chamado quando o Windows Virtual PC registra uma mensagem no log de eventos do Windows.</span><span class="sxs-lookup"><span data-stu-id="a9359-118">This method is called when Windows Virtual PC logs a message to the Windows event log.</span></span> <span data-ttu-id="a9359-119">O programa cliente deve implementar esse método de interface para receber a notificação do evento **vmVirtualPCEvent \_ EventLogged** originado do [**IVMVirtualPC**](ivmvirtualpc.md).</span><span class="sxs-lookup"><span data-stu-id="a9359-119">The client program must implement this interface method to receive notification of the **vmVirtualPCEvent\_EventLogged** event originating from [**IVMVirtualPC**](ivmvirtualpc.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a9359-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a9359-120">Requirements</span></span>



| <span data-ttu-id="a9359-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="a9359-121">Requirement</span></span> | <span data-ttu-id="a9359-122">Valor</span><span class="sxs-lookup"><span data-stu-id="a9359-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="a9359-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a9359-123">Minimum supported client</span></span><br/> | <span data-ttu-id="a9359-124">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="a9359-124">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="a9359-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a9359-125">Minimum supported server</span></span><br/> | <span data-ttu-id="a9359-126">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="a9359-126">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="a9359-127">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="a9359-127">End of client support</span></span><br/>    | <span data-ttu-id="a9359-128">Windows 7</span><span class="sxs-lookup"><span data-stu-id="a9359-128">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="a9359-129">Produto</span><span class="sxs-lookup"><span data-stu-id="a9359-129">Product</span></span><br/>                  | <span data-ttu-id="a9359-130">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="a9359-130">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="a9359-131">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a9359-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="a9359-132"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="a9359-132"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="a9359-133">IID</span><span class="sxs-lookup"><span data-stu-id="a9359-133">IID</span></span><br/>                      | <span data-ttu-id="a9359-134">DIID \_ IVMVirtualPCEvents é definido como efed1ef1-3c09-41F7-a9c2-7e29fa286c9d</span><span class="sxs-lookup"><span data-stu-id="a9359-134">DIID\_IVMVirtualPCEvents is defined as efed1ef1-3c09-41f7-a9c2-7e29fa286c9d</span></span><br/>        |



## <a name="see-also"></a><span data-ttu-id="a9359-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="a9359-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a9359-136">**IVMVirtualPCEvents**</span><span class="sxs-lookup"><span data-stu-id="a9359-136">**IVMVirtualPCEvents**</span></span>](ivmvirtualpcevents.md)
</dt> </dl>

 

