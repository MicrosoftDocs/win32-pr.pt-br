---
title: Método IVMTask WaitForCompletion (VPCCOMInterfaces. h)
description: Aguarda a conclusão da tarefa ou o intervalo de tempo limite especificado para decorrer.
ms.assetid: 28718c54-4411-4c69-89de-35ea6a8d074c
keywords:
- WaitForCompletion do método virtual PC
- Método WaitForCompletion Virtual PC, interface IVMTask
- IVMTask interface virtual PC, método WaitForCompletion
topic_type:
- apiref
api_name:
- IVMTask.WaitForCompletion
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 950cc19bad2a0f5804f994fe9279cec649d7c2f9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/12/2020
ms.locfileid: "105763456"
---
# <a name="ivmtaskwaitforcompletion-method"></a><span data-ttu-id="ad977-106">Método IVMTask:: WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="ad977-106">IVMTask::WaitForCompletion method</span></span>

<span data-ttu-id="ad977-107">\[O Windows Virtual PC não está mais disponível para uso a partir do Windows 8.</span><span class="sxs-lookup"><span data-stu-id="ad977-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="ad977-108">Em vez disso, use o [provedor WMI do Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="ad977-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="ad977-109">Aguarda a conclusão da tarefa ou o intervalo de tempo limite especificado para decorrer.</span><span class="sxs-lookup"><span data-stu-id="ad977-109">Waits for the task to complete or for the specified time-out interval to elapse.</span></span>

## <a name="syntax"></a><span data-ttu-id="ad977-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ad977-110">Syntax</span></span>


```C++
HRESULT WaitForCompletion(
  [in] long timeout
);
```



## <a name="parameters"></a><span data-ttu-id="ad977-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ad977-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ad977-112">*tempo limite* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ad977-112">*timeout* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ad977-113">O tempo, em milissegundos, que esse método aguardará para a conclusão da tarefa antes de retornar o controle ao chamador.</span><span class="sxs-lookup"><span data-stu-id="ad977-113">The time, in milliseconds, that this method will wait for task completion before returning control to the caller.</span></span> <span data-ttu-id="ad977-114">Um valor de-1 especifica que o método aguardará até que a tarefa seja concluída sem atingir o tempo limite. Outros valores de tempo limite válidos variam de 0 a 4 milhões milissegundos.</span><span class="sxs-lookup"><span data-stu-id="ad977-114">A value of -1 specifies that method will wait until the task completes without timing out. Other valid timeout values range from 0 to 4,000,000 milliseconds.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ad977-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ad977-115">Return value</span></span>

<span data-ttu-id="ad977-116">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="ad977-116">This method can return one of these values.</span></span>



| <span data-ttu-id="ad977-117">Código/valor de retorno</span><span class="sxs-lookup"><span data-stu-id="ad977-117">Return code/value</span></span>                                                                                                                                                 | <span data-ttu-id="ad977-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="ad977-118">Description</span></span>                                      |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <span data-ttu-id="ad977-119"><dt>**S \_ OK**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="ad977-119"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="ad977-120">A operação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="ad977-120">The operation was successful.</span></span><br/>         |
| <dl> <span data-ttu-id="ad977-121"><dt>**E \_ INVALIDARG**</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="ad977-121"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>      | <span data-ttu-id="ad977-122">O parâmetro *Timeout* não é válido.</span><span class="sxs-lookup"><span data-stu-id="ad977-122">The *timeout* parameter is not valid.</span></span><br/> |
| <dl> <span data-ttu-id="ad977-123"><dt>**DISP \_ E \_**</dt> <dt>0x80020009</dt> de exceção</span><span class="sxs-lookup"><span data-stu-id="ad977-123"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="ad977-124">Ocorreu um erro inesperado.</span><span class="sxs-lookup"><span data-stu-id="ad977-124">An unexpected error has occurred.</span></span><br/>     |



 

## <a name="remarks"></a><span data-ttu-id="ad977-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="ad977-125">Remarks</span></span>

<span data-ttu-id="ad977-126">O método **WaitForCompletion** coloca o thread de execução atual em suspensão até que ele retorne.</span><span class="sxs-lookup"><span data-stu-id="ad977-126">The **WaitForCompletion** method puts the current execution thread to sleep until it returns.</span></span> <span data-ttu-id="ad977-127">A especificação de uma espera infinita (timeout =-1) não é recomendada, a menos que seja absolutamente crítica que a tarefa seja concluída em qualquer circunstância.</span><span class="sxs-lookup"><span data-stu-id="ad977-127">Specifying an infinite wait (timeout = -1) is not recommended unless it is absolutely critical that the task completes under any circumstance.</span></span>

## <a name="requirements"></a><span data-ttu-id="ad977-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ad977-128">Requirements</span></span>



| <span data-ttu-id="ad977-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="ad977-129">Requirement</span></span> | <span data-ttu-id="ad977-130">Valor</span><span class="sxs-lookup"><span data-stu-id="ad977-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="ad977-131">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ad977-131">Minimum supported client</span></span><br/> | <span data-ttu-id="ad977-132">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="ad977-132">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="ad977-133">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ad977-133">Minimum supported server</span></span><br/> | <span data-ttu-id="ad977-134">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="ad977-134">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="ad977-135">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="ad977-135">End of client support</span></span><br/>    | <span data-ttu-id="ad977-136">Windows 7</span><span class="sxs-lookup"><span data-stu-id="ad977-136">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="ad977-137">Produto</span><span class="sxs-lookup"><span data-stu-id="ad977-137">Product</span></span><br/>                  | <span data-ttu-id="ad977-138">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="ad977-138">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="ad977-139">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ad977-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="ad977-140"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="ad977-140"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="ad977-141">IID</span><span class="sxs-lookup"><span data-stu-id="ad977-141">IID</span></span><br/>                      | <span data-ttu-id="ad977-142">IID \_ IVMTask é definido como ab72b222-6e9c-48ae-aa54-85e3e635767c</span><span class="sxs-lookup"><span data-stu-id="ad977-142">IID\_IVMTask is defined as ab72b222-6e9c-48ae-aa54-85e3e635767c</span></span><br/>                    |



## <a name="see-also"></a><span data-ttu-id="ad977-143">Confira também</span><span class="sxs-lookup"><span data-stu-id="ad977-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ad977-144">**IVMTask**</span><span class="sxs-lookup"><span data-stu-id="ad977-144">**IVMTask**</span></span>](ivmtask.md)
</dt> </dl>

 

